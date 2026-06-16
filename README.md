# SSI-Mamba
## 数据准备与使用说明

首先，需要前往 [ENCODE 数据库](https://www.encodeproject.org/) 下载所需细胞系的组蛋白修饰文件。

例如：

* 细胞系：`GM12878`
* 组蛋白修饰类型：`H3K27me3`
* 文件格式：`.bigWig`

示例文件：

```text
GM12878_H3K27me3.bigWig
```

同时，还需要准备对应物种的基因组碱基序列文件，例如：

```text
hg38.fa
```

## 文件路径配置

下载完成后，请将以下文件路径修改到 `Train.py` 文件中：

1. 组蛋白修饰文件路径，例如：

```text
/path/to/GM12878_H3K27me3.bigWig
```

2. 对应细胞系或物种的 DNA 序列文件路径，例如：

```text
/path/to/hg38.fa
```

3. 对应细胞系的沉默子-沉默子互作数据集路径，例如：

```text
/path/to/silencer_silencer_interaction_dataset
```

请根据实际文件存放位置，在 `Train.py` 中修改相应参数。

## 模型训练

完成路径配置后，可以运行 `Train.py` 进行模型训练：

```bash
python Train.py
```

## 权重预测

训练完成后，也可以通过 `test.py` 文件对权重进行预测：

```bash
python test.py
```

