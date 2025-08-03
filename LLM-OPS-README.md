
# LLM OPS 

## July-19th

### Create Project Folder and Environment Setup

|#| Step Info | Command   | Notes   |
|:---:| :---   | :--- | :--- |
|1| Create a folder  | mkdir llmops-app |    |
|2| Create  folders ||Refer 'create folders' section below
|3| Create the __init__.py file || Refer ' __init__.py' section below for details
|4| Create the setup.py|| Refer 'setup.py' section below for details
|5| Create conda environment| | refer 'create conda environment' section below
|6| Minimum Requirements for the Project|| Refer 'Minimum Requirements for the Project' section below
|7| 

#### create folders

```
md "config", "data", "exception", "faiss_index", "logger", "model", "notebook", "prompt", "src", "static", "templates", "utils"

#### __init__.py
- below command will create the __init__.py in all project folders

```
Get-ChildItem -Recurse -Directory | ForEach-Object {
    $initPath = Join-Path $_.FullName '__init__.py'
    if (-not (Test-Path $initPath)) {
        New-Item -Path $initPath -ItemType File | Out-Null
    }
}
```

#### setup.py
- python will look for __init__.py and will include as a package

```
from setup import setup, find_packages

setup(
    name = "<project-name>",
    version = "0.1",
    packages = find_packages()
)
```

#### create conda environment

```
# creates the virtual env in anaconda3 folder
conda create -n venv_ur_name python==3.12 -y
conda activate venv_ur_name
conda deactivate
conda remove -n venv_ur_name --all
conda env list

OR

# creates the virtual env in current folder
conda create -p venv_ur_name python==3.12 -y
conda activate
conda deactivate
conda env list
```


```

#### Minimum Requirements for the Project
We need the below to create the RAG Pipeline

##### LLM Model 
   -groq (free)
   - openai
   - gemini
   - claude
   - huggingface
   - ollama (local setup - need good configurations)
##### embedding model
   - openai
   - gemini 
   - huggingface
##### vector database
   - 3 variant 
     - 1st- in memory (fiass)
     - 2nd -disk
     - 3rd - cloud (aws bedrock)



## July-19th
