###### KvF API Reference
[Home](/docs/api/README.md) | [Project](/README.md) | [Module](/docs/api/modules/kvf/__init__/README.md) | [Source](/src/kvf/__init__.py)

# Functions within module
> Module: [kvf.\_\_init\_\_](/docs/api/modules/kvf/__init__/README.md)

Here are functions exposed in the module:
- [\_iterate](#_iterate)
- [dump](#dump)
- [get\_config](#get_config)
- [load](#load)
- [parse](#parse)
- [put\_config](#put_config)
- [render](#render)

## \_iterate
No docstring

```python
def _iterate(sections):
    ...
```

<p align="right"><a href="#kvf-api-reference">Back to top</a></p>

## dump
No docstring

```python
def dump(sections, file, *, spacing=1, mode='c', type_ref=None, bin_to_text=False, root_dir=None, attachments_dir='attachments'):
    ...
```

<p align="right"><a href="#kvf-api-reference">Back to top</a></p>

## get\_config
No docstring

```python
def get_config(filename, *, type_ref=None, obj_builder=None, end_of_stream=None):
    ...
```

<p align="right"><a href="#kvf-api-reference">Back to top</a></p>

## load
No docstring

```python
def load(file, *, type_ref=None, obj_builder=None, end_of_stream=None, root_dir=None):
    ...
```

<p align="right"><a href="#kvf-api-reference">Back to top</a></p>

## parse
No docstring

```python
def parse(s, *, type_ref=None, root_dir=None, obj_builder=None, end_of_stream=None):
    ...
```

<p align="right"><a href="#kvf-api-reference">Back to top</a></p>

## put\_config
No docstring

```python
def put_config(sections, filename, *, spacing=1, type_ref=None, bin_to_text=False, attachments_dir='attachments'):
    ...
```

<p align="right"><a href="#kvf-api-reference">Back to top</a></p>

## render
No docstring

```python
def render(sections, *, spacing=1, mode='c', type_ref=None, bin_to_text=True, root_dir=None, attachments_dir='attachments'):
    ...
```

<p align="right"><a href="#kvf-api-reference">Back to top</a></p>
