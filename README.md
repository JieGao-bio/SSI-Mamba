# SSI-Mamba

## Data Preparation

First, download the required histone modification files for your target cell line from the [ENCODE database](https://www.encodeproject.org/).

For example, for the **GM12878** cell line, you may download:

```text
GM12878_H3K27me3.bigWig
```

In addition, download the corresponding reference genome sequence file in `.fa` format, such as:

```text
hg38.fa
```

## Configure File Paths

After downloading the required files, modify the corresponding file paths in `Train.py`, including:

* The histone modification `.bigWig` file (e.g., `GM12878_H3K27me3.bigWig`)
* The DNA sequence `.fa` file corresponding to the target species (e.g., `hg38.fa`)
* The silencer-silencer interaction dataset for the target cell line

Example:

```python
histone_file = "/path/to/GM12878_H3K27me3.bigWig"
genome_file = "/path/to/hg38.fa"
interaction_file = "/path/to/silencer_interaction_dataset"
```

Please replace the example paths with the actual locations of your downloaded files.

## Model Training

After configuring all file paths, run the following command to train the model:

```bash
python Train.py
```

## Prediction

You can also use `test.py` to perform predictions with the trained model weights:

```bash
python test.py
```

