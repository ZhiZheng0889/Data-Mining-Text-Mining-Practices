# Data Mining and Text Mining Practices

Course materials and hands-on Python exercises for **CAP 5771: Data Mining and Text Mining**. This repository includes programming notebooks, data manipulation and visualization examples, lecture slides, and datasets. The included syllabus is for Fall 2023, taught by Dr. Parisa Hajibabaee.

## Practice notebooks

Work through the numbered notebooks in order:

| Notebook | Topics |
| --- | --- |
| [01_Basics_DataTypes_Operators.ipynb](01_Basics_DataTypes_Operators.ipynb) | Syntax, variables, input, data types, strings, collections, and operators. |
| [02_Functions_Controlflow.ipynb](02_Functions_Controlflow.ipynb) | Conditionals, loops, functions, scope, arguments, recursion, and built-in functions. |
| [03_Modules_Class.ipynb](03_Modules_Class.ipynb) | Standard library modules, classes, methods, and inheritance. |
| [04_Numpy.ipynb](04_Numpy.ipynb) | Array creation, attributes, reshaping, calculations, indexing, slicing, and random sampling. |
| [05_Matplotlib.ipynb](05_Matplotlib.ipynb) | Plotting and customization, bar charts, pie and donut charts, scatter plots, and histograms. |
| [06_Pandas.ipynb](06_Pandas.ipynb) | Series, indexing, descriptive statistics, CSV input/output, aggregation, and slicing. |
| [07_TransformingData.ipynb](07_TransformingData.ipynb) | Concatenation, adding and deleting rows, merging, sorting, tidy data, melting, and pivot tables. |

An additional version of the basics notebook is included as [01_Basics_DataTypes_Operators (1).ipynb](01_Basics_DataTypes_Operators%20%281%29.ipynb).

## Lecture slides and syllabus

| File | Contents |
| --- | --- |
| [Week1_Session1.pptx](Week1_Session1.pptx) | Introduction to data mining and the motivation for analyzing large datasets. |
| [Week1_Session2.pptx](Week1_Session2.pptx) | Data objects, attributes, and foundational data concepts. |
| [Session1.pptx](Session1.pptx) | Data mining material including distance measures and standardization. |
| [Session1_DR.pptx](Session1_DR.pptx) | Dimensionality reduction: linear algebra review, eigenvalues and eigenvectors, covariance, PCA, LDA, and t-SNE. |
| [Session2_DR.pptx](Session2_DR.pptx) | PCA examples in Python, explained variation, visualization, and loading scores. |
| [Session3_DR.pptx](Session3_DR.pptx) | Further dimensionality reduction material, including PCA extensions such as kernel PCA. |
| [Course syllabus](CAP_5771-01-Data_Text_Mining-PHajibabaee_rev_08-17.docx) | Fall 2023 course information, instructor details, and course requirements. |

## Datasets and archived exercises

| File | Contents |
| --- | --- |
| [census2010.csv](census2010.csv) | 53 records with `Geography` and `Census 2010` columns; used in the data transformation notebook. |
| [Column_database.csv](Column_database.csv) | 316 records describing column specimens, references, failure labels, and numerical engineering features. |
| [Column_database.xlsx](Column_database.xlsx) | Excel workbook for the column database. |
| [Shear_Wall_Database.csv](Shear_Wall_Database.csv) | 393 records describing shear wall specimens, failure modes, section types, and numerical engineering features. |
| [Column_database.zip](Column_database.zip) | Additional notebooks (`column.ipynb`, `shear.ipynb`) and Excel datasets (`Column_database.xls`, `Shear_Wall_Database.xls`). |

The archived notebooks use scikit-learn for scaling, PCA, linear discriminant analysis (LDA), and t-SNE. The engineering CSV files contain unnamed columns, so inspect their headers before selecting features for analysis.

## Getting started

Install Python 3 and run the following commands from the repository directory to install the main notebook dependencies and open JupyterLab:

```sh
python -m pip install jupyterlab numpy pandas matplotlib
python -m jupyterlab
```

Open a notebook and execute its cells in order. Keep the working directory at the repository root so relative dataset paths resolve correctly. Open the slides and syllabus with applications that support PowerPoint and Word files.

### Execution notes

- `06_Pandas.ipynb` reads `catalog.csv`, which is not included in this repository.
- `07_TransformingData.ipynb` reads `estimate2018.csv`, which is not included. Its other input, `census2010.csv`, is provided.
- Supply the missing files with the columns expected by the examples, or adapt those cells to your own data.
- Some examples use older library APIs, including `DataFrame.append` in `07_TransformingData.ipynb`. These cells may need adaptation to your installed pandas version, using `pd.concat` where appropriate. Dependency versions are not pinned.
- Extract `Column_database.zip` to explore the additional exercises. Their input paths are `data/Column_database.xlsx` and `data/Shear_Wall_Database.xlsx`, while the archive contains `.xls` files. Adjust the paths and Excel formats before running them.
- The archived exercises also require `scikit-learn` and an Excel reader appropriate to the chosen format (`openpyxl` for `.xlsx` or `xlrd` for `.xls`).
