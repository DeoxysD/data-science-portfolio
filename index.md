---
layout: default
title: FAN ZIQIAN
---

# FAN ZIQIAN

I study data analysis and build classification models on tabular data. This page collects one finished project and the chart I would use to explain it.

## Technical skills

Python, pandas, scikit-learn, matplotlib, and Jupyter. On a Kaggle playground competition I stacked out-of-fold predictions with L2 logistic regression and compared that stack with the public leaderboard.

## Project showcase

**Predicting Smartphone Addiction** — completed

Research question: can phone-use features predict the binary label `addicted_label`, and is a public-leaderboard gap of 0.00006 enough to choose the final model?

Screen time already carries most of the signal. On rows where the feature is observed, `daily_screen_time_hours` alone reaches about 0.890 ROC-AUC. A stacked model (`mask_student`) reaches 0.970158 on five-fold out-of-fold predictions, just above an earlier stack at 0.970023.

![Single-feature ROC-AUC compared with the stacked model]({{ site.baseurl }}/figures/03_single_feature_auc.png)

The public leaderboard, which covers about 20% of the test set, ranks the two stacks in the opposite order. The private result later matched the out-of-fold order. The left panel makes the swap easy to see. The right panel keeps the axis from 0.5 to 1.0, so the same swap is visibly a very small gap. These are two evaluations of the same submissions, not a change over time.

![Out-of-fold AUC and public leaderboard, zoomed and at full scale]({{ site.baseurl }}/figures/02_oof_vs_public_rank.png)

Project repository: [DeoxysD/data-science-project](https://github.com/DeoxysD/data-science-project)

Status: completed
