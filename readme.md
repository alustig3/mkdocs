
# Mkdocs template
This is a template for creating documentation for hardware projects. It is built on top of the following projects:

- [MkDocs](https://github.com/mkdocs/mkdocs) static webiste generator
- [Material for MkDocs](https://github.com/squidfunk/mkdocs-material) theme
- [Mike](https://github.com/jimporter/mike) doc version management


## Setup
[Download](https://github.com/alustig3/mkdocs/releases/download/v1.0/mkdocs.zip) this template and place it in you project folder


### Install Python libraries
install [uv](https://github.com/astral-sh/uv?tab=readme-ov-file#getting-started) if you don't have it yet

create a python virtual environment for your project

```
uv venv
```

activate the virtual environment
```
# On macOS and Linux.
source .venv/bin/activate

# On Windows.
.venv\Scripts\activate
```


install the python libraries by running 

```
uv pip install -r mkdocs/mkdocs_requirements.txt
```

## Serve docs
```
cd mkdocs/
```
```
mkdocs serve
```

## Publish docs

### Setup GitHub Pages

go to `Settings -> Pages`
- Set the Buid and deployment source to `Deploy from a branch`
- Set the branch to `gh-pages` and `/(root)`

![pages setup](/pages_setup.png)

### Deploy using Mike

make sure you are in the `mkdocs` folder
```
cd mkdocs/
```

#### First time setup
```
mike delete --all
```

```
mike deploy v1.0 latest
```

```
mike set-default latest
```

#### Deploying a new version

```
mike deploy --update-aliases v1.1 latest
```