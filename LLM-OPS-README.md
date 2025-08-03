# LLM OPS

## Software Installation

```
### creates the virtual env in anaconda3 folder
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
# Delete the folder venv_ur_name
conda env list
```

## Steps

1. Create a folder (llmops-app)
2. Create the setup.py
3. create requirements.txt
4. create conda envvironment
5. create the below folders in the llmops-app. execute the following  command in vscode to create the below folders md "config", "data", "exception", "faiss_index", "logger", "model", "notebook", "prompt", "src", "static", "templates", "utils"
   - config
   - data
   - exception
   - faiss_index
   - logger
   - model
   - notebook
   - prompt
   - src
   - static
   - templates
   - utils



