# Escore de força muscular MRC (soma)

Identificador: `escore-mrc`. Pacote independente da interface ELUCENIA, para navegador e Node.js.

## Situação

- Revisão: **needs-review**. Revisão documental e clínica independente pendente.
- Execução: **disponível para reprodução técnica da fórmula**.
- Validação clínica independente: **não realizada**. Os testes abaixo verificam aritmética e transporte dos campos.
- Fonte importada: Panorama Médico; arquivo `app/content/ferramentas/neuro-mente.php`.
- 5/5 casos de referência conferidos na importação. 0 casos independentes desta ferramenta.
- Dados: o exemplo funciona localmente, sem rede, armazenamento ou identificação de pacientes.

## Uso no Node.js

```js
const { calculate } = require('./calculator.js');
const example = require('./examples.json')[0];
console.log(calculate(example.input));
```

Execute `node test.cjs` (ou `npm test`) para conferir os exemplos. Abra `index.html` para usar a versão local do navegador. Não há dependências npm.

## Contrato

`calculate(input)` recebe um objeto, devolve `{id, main, label, raw, clinicalValidation}` ou `{error, code, field?}`. Consulte `tool.json` e `metadata.fields` para nomes, unidades, opções e intervalos. Números aceitam valores finitos ou strings numéricas; opções precisam corresponder às chaves documentadas. Campos obrigatórios vazios, booleanos inválidos, valores fora de intervalo e resultados não finitos são rejeitados. Somente checkbox omitido representa falso; um campo numérico ou uma opção obrigatória nunca é preenchido automaticamente.

Interpretações, ordens terapêuticas e tabelas herdadas não são retornadas pelo adaptador. Classificações e valores ainda dependem da população e das limitações da fonte.

## Fórmula / versão

Graduação MRC em cada grupo: 0 nenhuma contração · 1 contração visível sem movimento · 2 movimento ativo sem a gravidade · 3 vence a gravidade · 4 vence a gravidade e alguma resistência · 5 força normal.Soma de 6 grupos bilaterais (abdução do ombro, flexão do cotovelo, extensão do punho, flexão do quadril, extensão do joelho, dorsiflexão do tornozelo). Total: 0 a 60.

A transcrição acima documenta o acervo de origem e pode requerer atualização. 

## Condições e limites

Soma a força de 6 grupos musculares de cada lado (0 a 5 cada). Usado no diagnóstico de fraqueza adquirida na UTI e no acompanhamento de Guillain-Barré.

Confirme população, exclusões, unidades, versão e diretriz aplicável ao país e serviço. O resultado não deve ser utilizado isoladamente para diagnóstico, alta ou prescrição. O pacote não representa certificação clínica, aprovação regulatória ou indicação para toda população. Veja a revisão completa em `tool.json`.

## Fontes originais

- [Kleyweg RP, van der Meché FG, Schmitz PI. Interobserver agreement in the assessment of muscle strength and functional abilities in Guillain-Barré syndrome. Muscle Nerve, 1991.](https://doi.org/10.1002/mus.880141111)
- [De Jonghe B et al. Paresis acquired in the intensive care unit: a prospective multicenter study. JAMA, 2002.](https://doi.org/10.1001/jama.288.22.2859)
- [Hermans G et al. Acute outcomes and 1-year mortality of intensive care unit-acquired weakness: a cohort study and propensity-matched analysis. Am J Respir Crit Care Med, 2014.](https://doi.org/10.1164/rccm.201312-2257OC)

## Exemplos e rastreabilidade

`examples.json` preserva `originalInput`, expectativa e entrada explícita do exemplo. Não foi necessário expandir opções zero nos exemplos.

## Direitos e repositório

Este pacote integra o acervo privado de desenvolvimento da ELUCENIA. A publicação externa depende de liberação expressa. A licença MIT (arquivo LICENSE) cobre o código de integração, preservando o aviso de autoria e a licença; não transfere direitos sobre instrumentos, traduções, questionários, artigos, marcas ou outros materiais de terceiros. Consulte NOTICE.md e as condições de cada titular. O acesso a este adaptador não publica nem licencia automaticamente o restante da plataforma ELUCENIA.

## Acesso ao repositório

Repositório privado da organização ELUCENIA. A abertura pública depende de liberação expressa.
