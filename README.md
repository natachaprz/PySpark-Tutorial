# Pyspark tutorial

Welcome to the Pyspark tutorial section.

The courses comprises of 4 folders containing notebooks. Folders and notebooks are sorted in order of difficulty given their name, so you should follow the numerotation. For example, you should finish all notebooks in `1-beginner` before starting `2-novice`. Likewise, when doing `2-novice` finish the `1-...` notebook before doing `2-...`.

Inside each notebook, we have documented a number of questions and unimplemented code cells answering the question, followed by a code cell which acts as test cases for the function called `Graded cell`. Your submission will be graded on how many test cases you pass given your implementation of the previous function. 

**PS**: The instructor has hidden test cases on his side so don't try to circumvent the system by just returning the expected value in your method.

## Prerequisites

- [Anaconda 2019+](https://www.anaconda.com/download/)
- Required Java 8/11. 
    - You can set the `JAVA_HOME` environment variable to point to the Java 8/11 folder you want to use for the project, from `Edit the system environment variables` window or `set JAVA_HOME=<path_to_java>` in command-line before running `jupyter notebook`. 
    - You may also install Java OpenJDK **inside** your Anaconda environment with `conda install openjdk`. The `JAVA_HOME` variable should be automatically updated for this environment only.

## Run

We provide you with a `requirements.txt` which is used to download dependencies in a conda environment we will name `pyspark-tutorial`.

#### Using Anaconda Navigator

Go to `Environments` tab then tap `Import` button. Name it `pyspark-tutorial`. In the dropdown type of file select `Pip requirement file .txt` and browse to the `requirements.txt` file and press enter to create the environment. You should now be able to select the environment.

Go to `Environments` tab, select the `pyspark-tutorial` environment. When your mouse is over the environment, you should see a green arrow, click on it and select `Open with Jupyter notebook`. Then browse to the folder with all the notebooks.

- you may need to define the `PYSPARK_PYTHON` environment variable so Spark workers can point to the correct Python command.

#### Using Anaconda prompt

```
conda create -n pyspark-tutorial python=3.8
conda activate pyspark-tutorial
conda install openjdk=8
pip install -r requirements.txt
pip install jupyter
set PYSPARK_PYTHON=python
jupyter notebook
```

Run a Jupyter Notebook session : `jupyter notebook` from the root of your project, when in your `pyspark-tutorial` conda environment.

Notes: 
- you may run into `java.io.FileNotFoundException: HADOOP_HOME and hadoop.home.dir are unset.` warnings on Windows. Do not worry about it, they are necessary for remote connections only.
- you may need to define the `PYSPARK_PYTHON` environment variable so Spark workers can point to the correct Python command.

When you are done with the environment, don't forget to deactivate your Anaconda environment : `conda deactivate`
