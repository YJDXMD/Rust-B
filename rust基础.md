# Rust 学习笔记 


## BUG集

cargo build 提示 Blocking waiting for file lock on package cache

解决方案：
.cargo下新建文件config（改用国内镜像）

```
[source.crates-io]
registry = "https://github.com/rust-lang/crates.io-index"
replace-with = 'ustc'
[source.ustc]

registry = "git://mirrors.ustc.edu.cn/crates.io-index"
```
## 
单线程网页无法正常显示

```
let mut buffer = [0; 1024];
//let mut buffer = [0; 512];
```

