## libuv sample

参考[Build Instructions](https://github.com/libuv/libuv#build-instructions)编译libuv，生成静态库`libuv.a`。

拷贝`libuv.a`到`lib`目录，拷贝libuv头文件到`include`目录。

vscode直接使用快捷键`Command+Shift+B`进行构建。

### 注意事项

#### 链接静态库时，需要先`-L`指定目录，再-l指定名称

例如`libuv.a`，静态库名称为`uv`：

```bash
clang src/main.c -o out/main -I`pwd`/include -L`pwd`/lib -luv
```