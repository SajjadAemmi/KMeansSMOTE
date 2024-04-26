# Oversampling for Imbalanced Learning based on K-Means and SMOTE

K-Means SMOTE is an oversampling method for class-imbalanced data. It
aids classification by generating minority class samples in safe and
crucial areas of the input space. The method avoids the generation of
noise and effectively overcomes imbalances between and within classes.

This repo is the official implementation of [Oversampling for Imbalanced Learning Based on K-Means and SMOTE](https://arxiv.org/abs/1711.00837) paper.

K-means SMOTE works in three steps:

1. Cluster the entire input space using k-means [1].
2. Distribute the number of samples to generate across clusters:

   1. Filter out clusters which have a high number of majority class
      samples.
   2. Assign more synthetic samples to clusters where minority class
      samples are sparsely distributed.

3. Oversample each filtered cluster using SMOTE [2].

This project is a python implementation of k-means SMOTE. It is
compatible with the scikit-learn-contrib project [imbalanced-learn](https://github.com/scikit-learn-contrib/imbalanced-learn).

## Installation

```bash
pip install -r requirements.txt
```

## Usage
You can try [demo notebook](./demo.ipynb)

## Contributing

Please feel free to submit an issue if things work differently than
expected. Pull requests are also welcome - just make sure that tests are
green by running ``pytest`` before submitting.

## Citation

If you use k-means SMOTE in a scientific publication, we would
appreciate citations to the following:

```
    @article{kmeans_smote,
        title = {Oversampling for Imbalanced Learning Based on K-Means and SMOTE},
        author = {Last, Felix and Douzas, Georgios and Bacao, Fernando},
        year = {2017},
        archivePrefix = "arXiv",
        eprint = "1711.00837",
        primaryClass = "cs.LG"
    }
```

## References

[1] MacQueen, J. “Some Methods for Classification and Analysis of
Multivariate Observations.” Proceedings of the Fifth Berkeley Symposium
on Mathematical Statistics and Probability, 1967, p. 281-297.

[2] Chawla, Nitesh V., et al. “SMOTE: Synthetic Minority over-Sampling
Technique.” Journal of Artificial Intelligence Research, vol. 16, Jan.
2002, p. 321357, doi:10.1613/jair.953.
