go to the top level of you project

`git submodule add <repository-url> mkdocs`

`git submodule init`

`git submodule update`


install uv if you don't have it yet

```
# On macOS and Linux.
curl -LsSf https://astral.sh/uv/install.sh | sh

# On Windows.
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

create a python virtual environment for your project

`uv venv`

activate the virtual environment
```
# On macOS and Linux.
source .venv/bin/activate

# On Windows.
.venv\Scripts\activate
```


install the python libraries by running 

`uv pip install -r mkdocs/mkdocs_requirements.txt`
