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
#    If pyenv still not found execute the following 3 commands
     echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
     echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
     echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bashrc
#    Test with:
     pyenv update
     pyenv versions
# 2. Install Desired Python Version
pyenv install 3.10.2
# 3. Make new directory and naviate into directory
mkdir my_project && cd my_project
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
