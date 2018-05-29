# HID-IO layouts Python API

This is the Python API for the HID-IO [layouts](https://github.com/hid-io/layouts) repository.

The purpose of this API is to acquire and merge the JSON HID layouts.
With some additional helpers to deal with string composition.

[layouts](https://pypi.org/project/layouts/) is also available on PyPi.
```bash
pip install layouts
```

[![Travis Status](https://travis-ci.org/hid-io/layouts-python.svg?branch=master)](https://travis-ci.org/hid-io/layouts-python)

[![Visit our IRC channel](https://kiwiirc.com/buttons/irc.freenode.net/hid-io.png)](https://kiwiirc.com/client/irc.freenode.net/#hid-io)


## Usage

Some basic usage examples.


### List Layouts

```python
import layouts

mgr = layouts.Layouts()
print(mgr.list_layouts()
```


### Retrieve Layout

```python
import layouts

mgr = layouts.Layouts()
layout = mgr.get_layout('default')

print(layout.name()) # Name of merged layout
print(layout.json()) # Fully merged JSON dict
```


### Composition Example

```python
import layouts

mgr = layouts.Layouts()
layout = mgr.get_layout('default')

input_str = "Hello World!"
print(layout.compose(input_str))
```

