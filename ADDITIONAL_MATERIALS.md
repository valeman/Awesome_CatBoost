# Additional CatBoost materials

This is a deliberately curated companion to [Awesome CatBoost](README.md) and
[Mastering CatBoost](https://github.com/valeman/mastering-catboost). It follows
the book's workflow, then points to primary documentation, source repositories,
and research that are useful for going further. Links were checked on
2026-08-22; version-specific behavior should still be verified against the
CatBoost version used in an experiment.

## Use the book code first

The public companion repository contains the book's 119 canonical Python
listings and matching notebooks:

- [Listing index](https://github.com/valeman/mastering-catboost/blob/main/book_code/INDEX.md)
- [How to run the examples](https://github.com/valeman/mastering-catboost/blob/main/book_code/README.md)
- [Base dependencies](https://github.com/valeman/mastering-catboost/blob/main/requirements.txt)
- [Optional integrations](https://github.com/valeman/mastering-catboost/blob/main/requirements-optional.txt)

The Pro companion is separately licensed and is not mirrored in this public
repository.

## Follow the book by topic

| Book area | Companion code | Recommended next stop |
| --- | --- | --- |
| Foundations, ordered statistics, and symmetric trees | [Chapter 3](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter03) and [Appendix A](https://github.com/valeman/mastering-catboost/tree/main/book_code/appendixA) | [CatBoost: Unbiased Boosting with Categorical Features](https://proceedings.neurips.cc/paper_files/paper/2018/file/14491b756b3a51daac41c24863285549-Paper.pdf) |
| Tuning, sampling, quantization, and validation | [Chapter 4](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter04) | [CatBoost parameter tuning](https://catboost.ai/docs/en/concepts/parameter-tuning) and [cross-validation](https://catboost.ai/docs/en/concepts/python-reference_cv) |
| Uncertainty and conformal prediction | [Chapter 5](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter05) | [CatBoost uncertainty](https://catboost.ai/docs/en/references/uncertainty), [Conformal Prediction: A Gentle Introduction](https://arxiv.org/abs/2107.07511), and [MAPIE](https://mapie.readthedocs.io/en/latest/) |
| Learning to rank and click feedback | [Chapter 6](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter06) | [Official ranking tutorial](https://github.com/catboost/tutorials/tree/master/ranking) and [RankNet to LambdaMART](https://www.microsoft.com/en-us/research/publication/from-ranknet-to-lambdarank-to-lambdamart-an-overview/) |
| Categorical, text, embedding, and time features | [Chapter 7](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter07) | [Categorical features](https://catboost.ai/docs/en/features/categorical-features), [text features](https://catboost.ai/docs/en/features/text-features), and [embedding features](https://catboost.ai/docs/en/features/embeddings-features) |
| Classification, calibration, and production thresholds | [Chapter 8](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter08) | [Classification tutorial](https://github.com/catboost/tutorials/tree/master/classification) and [probability calibration](https://scikit-learn.org/stable/modules/calibration.html) |
| Regression, quantiles, and forecasting | [Chapter 9](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter09) | [Regression tutorial](https://github.com/catboost/tutorials/tree/master/regression) and [time-series conformal prediction](https://proceedings.mlr.press/v139/xu21h.html) |
| Importance, SHAP, interactions, and fairness | [Chapter 10](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter10) | [CatBoost SHAP values](https://catboost.ai/docs/en/concepts/shap-values), [SHAP TreeExplainer](https://shap.readthedocs.io/en/latest/generated/shap.TreeExplainer.html), and [SHAP source examples](https://github.com/shap/shap) |
| MLOps, export, monitoring, and serving | [Chapter 11](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter11) | [CatBoost model API](https://catboost.ai/docs/en/concepts/python-reference_catboost), [Python/C++ export](https://catboost.ai/docs/en/features/export-model-to-python), [MLflow CatBoost](https://mlflow.org/docs/latest/api_reference/python_api/mlflow.catboost.html), [DVC](https://dvc.org/doc/command-reference/), and [FastAPI deployment](https://fastapi.tiangolo.com/deployment/) |
| Embedding hybrids and causal/propensity ideas | [Chapter 12](https://github.com/valeman/mastering-catboost/tree/main/book_code/chapter12) | [Generalized Random Forests](https://projecteuclid.org/journals/annals-of-statistics/volume-47/issue-2/Generalized-Random-Forests/10.1214/18-AOS1709.full) and [Double/Debiased Machine Learning](https://doi.org/10.1111/ectj.12097) |

## Official CatBoost learning path

1. [Python tutorial](https://github.com/catboost/tutorials/blob/master/python_tutorial.ipynb) for training, validation, early stopping, snapshots, and feature importance.
2. [Python tutorial with tasks](https://github.com/catboost/tutorials/blob/master/python_tutorial_with_tasks.ipynb) for deliberate practice.
3. [Official tutorials repository](https://github.com/catboost/tutorials) for classification, ranking, text, model analysis, custom losses, export, and GPU examples.
4. [CatBoost documentation](https://catboost.ai/docs/en/) for the pinned API, metrics, training modes, model application, export formats, and recovery.
5. [CatBoost source repository](https://github.com/catboost/catboost) for implementation details, issues, discussions, and release notes.

## Research foundations

These are the primary papers behind the ideas used throughout the book:

- [Greedy Function Approximation: A Gradient Boosting Machine](https://projecteuclid.org/journals/annals-of-statistics/volume-29/issue-5/Greedy-Function-Approximation-A-Gradient-Boosting-Machine/10.1214/aos/1013203451.full) — Friedman (2001).
- [CatBoost: Unbiased Boosting with Categorical Features](https://proceedings.neurips.cc/paper_files/paper/2018/file/14491b756b3a51daac41c24863285549-Paper.pdf) — Prokhorenkova et al. (NeurIPS 2018).
- [CatBoost: Gradient Boosting with Categorical Features Support](https://arxiv.org/abs/1810.11363) — Dorogush, Ershov, and Gulin.
- [XGBoost: A Scalable Tree Boosting System](https://dl.acm.org/doi/10.1145/2939672.2939785) — Chen and Guestrin (2016).
- [LightGBM: A Highly Efficient Gradient Boosting Decision Tree](https://proceedings.neurips.cc/paper/2017/hash/6449f44a102fde848669bdd9eb6b76fa-Abstract.html) — Ke et al. (NeurIPS 2017).
- [A Unified Approach to Interpreting Model Predictions](https://papers.neurips.cc/paper_files/paper/2017/hash/8a20a8621978632d76c43dfd28b67767-Abstract.html) — Lundberg and Lee (NeurIPS 2017).
- [Conformalized Quantile Regression](https://arxiv.org/abs/1905.03222) — Romano, Patterson, and Candès.
- [Adaptive Conformal Inference Under Distribution Shift](https://proceedings.neurips.cc/paper/2021/hash/0d441de75945e5acbc865406fc9a2559-Abstract.html) — Gibbs and Candès (NeurIPS 2021).
- [Learning to Rank: From Pairwise Approach to Listwise Approach](https://dl.acm.org/doi/10.1145/1273496.1273513) — Cao et al. (ICML 2007).
- [Challenges in Deploying Machine Learning: A Survey of Case Studies](https://doi.org/10.1145/3533378) — Paleyes, Urma, and Lawrence.

## Benchmarks and alternatives

Use these as comparison points, not as universal rankings:

- [TabArena](https://arxiv.org/abs/2506.16791) and its [living leaderboard](https://huggingface.co/spaces/TabArena/leaderboard).
- [A Closer Look at Deep Learning on Tabular Data](https://arxiv.org/abs/2407.00956) with [LAMDA-TALENT code](https://github.com/qile2000/LAMDA-TALENT).
- [Why Do Tree-Based Models Still Outperform Deep Learning on Typical Tabular Data?](https://proceedings.neurips.cc/paper_files/paper/2022/hash/0378c7692da36807bdec87ab043cdadc-Abstract-Datasets_and_Benchmarks.html).
- [When Do Neural Nets Outperform Boosted Trees on Tabular Data?](https://arxiv.org/abs/2305.02997).
- [TabPFN v2](https://www.nature.com/articles/s41586-024-08328-6) and the [TabPFN repository](https://github.com/PriorLabs/TabPFN).
- [TabR: Tabular Deep Learning Meets Nearest Neighbors](https://openreview.net/forum?id=rhgIgTSSxW).

## Dataset and experiment hygiene

The book's examples use public or synthetic data, but the correct split and
estimand matter more than a leaderboard number. For reproducible extensions:

- [scikit-learn dataset loading utilities](https://scikit-learn.org/stable/datasets/loading_other_datasets.html)
- [OpenML](https://www.openml.org/)
- [DVC data versioning workflow](https://dvc.org/doc/command-reference/)
- [MLflow model tracking and packaging](https://mlflow.org/docs/latest/ml/model/)
- [Feast feature store documentation](https://docs.feast.dev/)
- [FastAPI deployment concepts](https://fastapi.tiangolo.com/deployment/concepts/)

When adapting a listing, keep a development/validation/test boundary, record
the dataset version and feature schema, and report the metric with its split,
seed, and horizon. A result from one synthetic fixture is an illustration,
not a general theorem.

## Contributing

Prefer primary sources, stable URLs, and a short note explaining why a link is
useful. Please avoid duplicate entries, unsourced performance claims, and
links that require a paid account to read the underlying research.
