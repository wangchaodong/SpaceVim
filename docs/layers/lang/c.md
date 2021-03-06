---
title: "SpaceVim lang#c layer"
description: "This layer is for c/c++/object-c development"
---

# [Layers](https://spacevim.org/layers) > lang#c


<!-- vim-markdown-toc GFM -->

- [Description](#description)
- [Layer Installation](#layer-installation)
- [Configuration](#configuration)

<!-- vim-markdown-toc -->

## Description

This layer is for c/c++/object-c development.

## Layer Installation

To use this configuration layer, add `SPLayer 'lang#c'` to your custom configuration file or load layer with custom options.

```vim
call SpaceVim#layers#load('lang#c',
        \ {
        \ 'enable_libclang' : 1,
        \ }
        \ )
```

## Configuration

- `clang_executable` (string)

set the path to the clang executable

- `enable_libclang` (boolean)

use libclang instead of `clang -cc1`, by default it is 0.

- `libclang_path` (string)

The libclang shared object (dynamic library) file path. by default it is empty.

- `clang_std` (dict)

```json
{
    "c": "c11",
    "cpp": "c++1z",
    "objc": "c11",
    "objcpp": "c++1z",
}
```

- `clang_flag`

Create a `.clang` file at your project root. You should be able to just paste most of your compile flags in there. You can also use a list ['-Iwhatever', ...] when loadding this layer.
