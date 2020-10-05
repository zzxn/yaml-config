# YAML Config

A config lib using yaml.

## Requirements

* `python 3.6+`
* `pyyaml`

## Usage Example

Write a .yaml config file:

```yaml
user:
  username: zzxn
  password: mypassword
database:
  path: localhost:1234
  password: dbpass
```

Read like this:

```python
from yaml_config import Config

# init config
config = Config('/path/to/config.yaml')

# read config (way 1)
print(config['user.username'])

# read config (way 2)
print(config('user.password'))

# read config (way 3, specify default value for absent case)
print(config('user.authorities', None))

```