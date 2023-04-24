 # python-settings

 This is a python module I've created to manage settings in python programs. I don't have any plans to put this on pypi though.

 ## Usage

 import the `Settings` class
 ```python
from settings import Settings
 ```
 
 Create settings object

 ```python
settings = Settings(filename = 'settings.json')
 ```
 See `Settings.__init__.__doc__` for arguments.

 Load settings
 ```python
settings.load()
 ```

 Save settings

 ```python
settings.save()
 ```
 Output is in json format.

 Example
 ```json
{
  "version": 1
}
 ```

 Set a value
 ```python
settings.set('option', 'value')
 ```

 To save a setting within a setting, e.g. sub-dictionary, use `.`.
 ```python
settings.set('options.value', 'foo')
# output
# {'options': {'value': 'foo'}}
 ```

 Get a value
 ```python
settings.get('option')
 ```

 Remove an option
 ```python
settings.remove('option')
 ```

 Reset all settings
 ```python
settings.initialize()
 ```

 
