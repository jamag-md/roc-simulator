# ROC Threshold Simulator

An interactive teaching tool for ROC curves and diagnostic test accuracy.

Change the healthy and diseased score distributions (mean, spread, sample size), move the decision cutoff, and see the distributions, the ROC curve, the confusion matrix and the metrics (sensitivity, specificity, PPV, NPV, accuracy, Youden's J, LR+, AUC) update together.

## Features

- Sliders for the mean, SD and sample size of each group
- Drag the cutoff on either chart, or jump to the cutoff with the highest Youden's J
- Smooth population curves alongside sample histograms and the empirical (stepped) ROC curve
- Metrics computed from the sample or from the population curves
- Ready-made scenarios: classic overlap, excellent test, weak test, no discrimination, unequal spread, rare disease, small study
- Plain-language summary of what the current numbers mean
- Light and dark mode, works on phones

## Usage

Open `index.html` in a browser. It is a single self-contained file with no build step.
