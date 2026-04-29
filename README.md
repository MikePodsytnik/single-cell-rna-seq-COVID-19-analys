# Анализ single-cell RNA-seq данных PBMC при COVID-19

## Введение

В этом ноутбуке вы проведёте полный базовый анализ scRNA-seq данных: загрузка матрицы, QC, нормализация, выбор вариабельных генов, PCA, кластеризация, UMAP, аннотация клеточных типов, differential expression и интерпретация.

> **Важное уточнение про датасет**  
> Для single-cell части здесь используется датасет [**GSE149689**](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE149689).  
В нём можно найти PBMC scRNA-seq здоровых доноров, пациентов с COVID-19 и пациентов с influenza. Там же есть ссылки на две статьи, в которых используются эти данные для анализа.

## Описание задачи

В этом задании мы будем пытаться частично повторить результаты из этих статей, поэтому желательно с ними ознакомиться.

Кратко:
- объект исследования: **PBMC**;
- организмы: **human**;
- тип данных: **single-cell RNA-seq**;
- группы: **healthy donors**, **COVID-19 patients**, **influenza patients**;
- в этом задании можно сравнивать:
  - **COVID-19** vs **healthy**;
  - мsevere/mild COVID**, если вы добавите более подробную метаинформацию;
  - **COVID-19** vs **influenza** как дополнительное задание.

## Используемые инструменты
- [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide)
- [Pandas](https://pandas.pydata.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [NumPy](https://numpy.org/)
- [SciPy](https://scipy.org/)
- [Matplotlib](https://matplotlib.org/)
- [Scikit-learn](https://scikit-learn.org/)
- [Scanpy](https://github.com/scverse/scanpy)
- [Anndata](https://anndata.readthedocs.io/en/latest/)
- [GSEApy](https://github.com/zqfang/gseapy)
