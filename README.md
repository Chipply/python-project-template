# New Python Project Setup/Template

This covers how to setup a new Python project

## Setup Process


```bash
# 1. Use pyenv to install Python
#    1.1 Check if pyenv installed:
     pyenv versions
#    1.2 If error install with:
     curl https://pyenv.run | bash
     exec $SHELL
     pyenv update
#    1.3 If pyenv still not found execute the following 3 commands
     echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
     echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
     echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bashrc
#    1.4 Test with:
     pyenv update
     pyenv versions
# 2. Install Desired Python Version
pyenv install 3.10.2
# 3. Make new directory and naviate into directory
mkdir my_project && cd my_project
# 4. Set Python Version for the Folder
pyenv local 3.10.2
# 5. Create new virtual environment called "proj_env"
python -m venv proj_env
# 6. Activate virtual environment
source proj_env/bin/activate
# 7. Install packages needed for project (ie. below)
python -m pip install requests
# 8. Create requirements.txt file
python -m pip freeze > requirements.txt
```

## Usage

```python
import foobar

# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
