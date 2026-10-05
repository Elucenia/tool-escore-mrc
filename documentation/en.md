<!-- ELUCENIA technical documentation · escore-mrc · en · no clinical/professional/rights approval -->

# MRC muscle strength sum score

[conditions, sources and permissions](https://elucenia.org/en/tools/escore-mrc)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Shoulder abduction – right

`ombro_d`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Shoulder abduction – left

`ombro_e`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Elbow flexion – right

`cotovelo_d`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Elbow flexion – left

`cotovelo_e`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Wrist extension – right

`punho_d`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Wrist extension – left

`punho_e`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Hip flexion – right

`quadril_d`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Hip flexion – left

`quadril_e`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Knee extension – right

`joelho_d`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Knee extension – left

`joelho_e`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Ankle dorsiflexion – right

`tornozelo_d`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

### Ankle dorsiflexion – left

`tornozelo_e`

- `0` — 0 – No contraction
- `1` — 1 – Visible contraction without movement
- `2` — 2 – Active movement with gravity eliminated
- `3` — 3 – Movement against gravity, without resistance
- `4` — 4 – Movement against gravity and some resistance
- `5` — 5 – Normal strength

## Method edition

MRC sum score/Kleyweg 1991: 6 bilateral groups 0–5, total 0–60

## Documented formula

MRC per group: 0 no contraction · 1 visible contraction without movement · 2 active movement with gravity eliminated · 3 overcomes gravity · 4 overcomes gravity and some resistance · 5 normal strength.

Sum 6 bilateral groups: shoulder abduction, elbow flexion, wrist extension, hip flexion, knee extension, ankle dorsiflexion. Total 0 to 60.

## Limits and population

A sum of manual strength assessments in a patient who can be examined. ICU studies involved specific recruitment conditions, which are not universal restrictions on MRC. The strength sum must not be confused with an etiological diagnosis or a global disability scale.

## References

- [Kleyweg RP, van der Meché FG, Schmitz PI. Interobserver agreement in the assessment of muscle strength and functional abilities in Guillain-Barré syndrome. Muscle Nerve, 1991.](https://doi.org/10.1002/mus.880141111)

- [De Jonghe B et al. Paresis acquired in the intensive care unit: a prospective multicenter study. JAMA, 2002.](https://doi.org/10.1001/jama.288.22.2859)

- [Hermans G et al. Acute outcomes and 1-year mortality of intensive care unit-acquired weakness: a cohort study and propensity-matched analysis. Am J Respir Crit Care Med, 2014.](https://doi.org/10.1164/rccm.201312-2257OC)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
