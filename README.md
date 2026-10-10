# ROC Threshold Simulator

**▶ Try it live: https://jamag-md.github.io/roc-simulator/**

An interactive teaching tool for ROC curves and diagnostic test accuracy, built for medical students, residents and clinicians. It works in English and Spanish, runs in any browser (including phones), and needs no installation or login.

*Herramienta interactiva para enseñar curvas ROC y exactitud diagnóstica. Disponible en español: pulsa «Español» junto al título.*

## What it does

Healthy and diseased patients are shown as two overlapping score distributions, next to the matching ROC curve. Move the decision cutoff, reshape the groups or change the sample sizes, and everything updates at once:

- Sensitivity, specificity, PPV, NPV, accuracy, Youden's J, LR+ and AUC
- The confusion matrix (TP, FN, FP, TN)
- A plain-language summary of what the current numbers mean, with teaching points such as PPV collapsing at low prevalence

## Features

- Sliders for the mean, spread (SD) and sample size of each group (5 to 5,000 patients)
- Drag the cutoff on either chart, or jump to the cutoff with the highest Youden's J
- Smooth population curves alongside sample histograms and the stepped (empirical) ROC curve
- Metrics computed from the random sample or from the population curves; resample to see sampling variability
- Density or patient-count view, so prevalence is visible on the chart
- Seven ready-made scenarios: classic overlap, excellent test, weak test, no discrimination, unequal spread, rare disease, small study
- English / Spanish toggle covering the whole interface, including decimal commas in Spanish
- Light and dark mode

## Teaching ideas

- Why sensitivity and specificity always trade off, and what the ROC curve and AUC actually represent
- Rule-out versus rule-in: why low cutoffs (D-dimer, high-sensitivity troponin) catch nearly every case at the cost of false positives
- How prevalence drives PPV and NPV while sensitivity and specificity stay the same
- How small studies give jagged, unstable accuracy estimates
- Live demonstrations for journal clubs and teaching sessions

## Evidence from the literature

Each scenario is linked to a study from emergency or internal medicine, shown at the bottom of the page with a button that loads the matching scenario:

| Scenario | Study |
|---|---|
| Classic overlap | Maisel AS, et al. BNP in the emergency diagnosis of heart failure. *N Engl J Med*. 2002. [doi:10.1056/NEJMoa020233](https://doi.org/10.1056/NEJMoa020233) |
| Excellent test | Reichlin T, et al. Sensitive cardiac troponin assays for early diagnosis of MI. *N Engl J Med*. 2009. [doi:10.1056/NEJMoa0900428](https://doi.org/10.1056/NEJMoa0900428) |
| Weak test | Freund Y, et al. Prognostic accuracy of Sepsis-3 criteria in the emergency department. *JAMA*. 2017. [doi:10.1001/jama.2016.20329](https://doi.org/10.1001/jama.2016.20329) |
| No discrimination | Coburn B, et al. Does this adult patient with suspected bacteremia require blood cultures? *JAMA*. 2012. [doi:10.1001/jama.2012.8262](https://doi.org/10.1001/jama.2012.8262) |
| Unequal spread | Metz CE. Basic principles of ROC analysis. *Semin Nucl Med*. 1978. [doi:10.1016/s0001-2998(78)80014-2](https://doi.org/10.1016/s0001-2998(78)80014-2) |
| Rare disease | Freund Y, et al. The PROPER randomized clinical trial (PERC rule). *JAMA*. 2018. [doi:10.1001/jama.2017.21904](https://doi.org/10.1001/jama.2017.21904) |
| Small study | Bachmann LM, et al. Sample sizes of studies on diagnostic accuracy. *BMJ*. 2006. [doi:10.1136/bmj.38793.637789.2F](https://doi.org/10.1136/bmj.38793.637789.2F) |
| Small study | Lijmer JG, et al. Design-related bias in studies of diagnostic tests. *JAMA*. 1999. [doi:10.1001/jama.282.11.1061](https://doi.org/10.1001/jama.282.11.1061) |
| Choosing the cutoff | Righini M, et al. Age-adjusted D-dimer cutoff (ADJUST-PE). *JAMA*. 2014. [doi:10.1001/jama.2014.2135](https://doi.org/10.1001/jama.2014.2135) |

## How it works

Each group's scores follow a normal distribution. The population ROC curve and AUC come from the binormal model, AUC = Φ((μ<sub>D</sub> − μ<sub>H</sub>) / √(σ<sub>H</sub>² + σ<sub>D</sub>²)). The sample is drawn with a seeded random generator, so moving a mean or spread shifts the same simulated patients instead of drawing new ones. A test is positive when the score is at or above the cutoff.

## Running it locally

Download `index.html` and open it in a browser. It is a single self-contained file with no build step; only the web fonts load from Google Fonts.

## Disclaimer

This is a teaching aid. It is not intended for clinical decision-making.
