# 章节 1-2 Hello, Cargo!


## 初始化
```bash
$ cargo new hello_cargo
$ cd hello_cargo
```

第一个命令创建一个名为 hello_cargo 的新目录和项目。 我们已将项目命名为 hello_cargo，Cargo 在 同名目录。

进入hello_cargo目录并列出文件。你会看到货物 为我们生成了两个文件和一个目录：一个 Cargo.toml 文件和一个包含 main.rs 文件的 src 目录。

<!-- 备注 -->
---
它还初始化了一个新的 Git 存储库以及一个 .gitignore 文件。 如果在现有 Git 中运行，则不会生成 Git 文件 存储 库;可以使用 覆盖此行为。cargo newcargo new --vcs=git


## Cargo.toml

此文件使用 TOML （Tom's Obvious， Minimal 语言）格式。


第一行 是节标题，指示 以下语句正在配置包。随着我们添加更多信息 此文件，我们将添加其他部分。[package]

接下来三行设置 需要编译的配置信息 
你的程序：名称、版本和要使用的 Rust 版本


## 构建和运行项目

```bash
$ cargo build
   Compiling hello_cargo v0.1.0 (/workspaces/study_rust/1.2/hello_cargo)
    Finished dev [unoptimized + debuginfo] target(s) in 0.56s
```

此命令在 target/debug/hello_cargo 中创建可执行文件，而不是在当前 目录。由于默认版本是调试版本，因此 Cargo 将二进制文件放入 名为 "debug" 的目录。您可以使用以下命令运行可执行文件

```bash
$ ./target/debug/hello_cargo
```

我们刚刚构建了一个项目并运行它，但我们也可以用它来编译代码，然后在一个命令中运行生成的可执行文件

```bash
$ cargo run
```

使用比必须记住运行然后使用二进制文件的整个路径更方便  


Cargo 还提供了一个名为 的命令。此命令快速检查 您的代码，以确保它可以编译但不生成可执行文件：

```bash
$ cargo check
```