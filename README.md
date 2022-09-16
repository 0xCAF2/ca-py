# calcium-py

Calcium interpreted language on Python

## Create a runtime

```python
from converter import convert
import json
from calciumlang import Runtime

# converter can read the subset of Python code and
# generate Calcium code.
json_text = convert('''
# write Python source code here
message = 'Hello, World.'
print(message)
''')

code = json.loads(json_text)

# A Runtime executes Calcium code given as JSON array.
runtime = Runtime(code)
runtime.run() # outputs 'Hello, World.'
```

## Applications

With Blockly, [you can generate Calcium code in visual environment.](https://calcium-editor.web.app/en/),
