# Essh sshrc library

This library provides `hooks_after_connect` hook for using [sshrc](https://github.com/Russell91/sshrc) in Essh.

## Installation

Put `sshrc.lua` in your `~/.essh/lib`.

## Usage

```lua
local sshrc = require "sshrc"

host "your-server" {
    HostName = "192.168.56.12",
    Port = "22",
    hooks_after_connect = {
        sshrc,
    },
}
```

You can modify `SSHHOME`.

```lua
host "your-server" {
    HostName = "192.168.56.12",
    Port = "22",
    hooks_after_connect = {
        -- sshhome default is `~`.
        sshrc({sshhome = "path/to/sshhome"}),
    },
}
```

see also: [Russell91/sshrc](https://github.com/Russell91/sshrc)

## About sshrc

[Russell91/sshrc](https://github.com/Russell91/sshrc)

```
Copyright (c) 2014 Russell Stewart

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
