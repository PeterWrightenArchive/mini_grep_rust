# Mini Grep
![](https://img.shields.io/badge/MIT-License-blue)

Mini Grep is a simple rust re-implementation of [GNU Grep](https://www.gnu.org/software/grep/manual/grep.html), which means it could just implement limited functions, such as searching specific string in ```.txt``` file (Actually I have supply a test example, ```peter.txt```).

# Setup

**Requirement**

Because this program is written by ```Rust```, and should be built by ```Cargo```, Please check your requirements first before setting up.

Type following command to check ```Cargo```:

```shell
$ cargo --version
```

## Build

Type following script in your Terminal to build Mini Grep.
```shell
$ git clone https://github.com/PeterWrighten/mini_grep_rust.git

$ cd mini_grep_rust

$ cargo build
```

## Mini Grep

Mini Grep has following features:

**1. Search string in file: Case insensitive or not.**

```shell
$ [CASE_INSENSITIVE=?] cargo run [query string] [filename]
```

You could test this by use my test file: ```peter.txt```.

> Example

Case insensitive search:

```shell
$ CASE_INSENSITIVE=1 cargo run am peter.txt
```

Case sensitive search:

```shell
$ cargo run am peter.txt
```
**2. Output results into ```.txt``` file in root directory without error.**

```shell
$ [CASE_INSENSITIVE=?] cargo run [query string] [filename] > [output filename]
```

>Example

Stdout:

```shell
$ CASE_INSENSITIVE=1 cargo run am peter.txt > container.txt
```

Error:

```shell
$ cargo run > container.txt
```


# Reference

1. [GNU Grep](https://www.gnu.org/software/grep/manual/grep.html)
2. [Rust Programming Languages](https://doc.rust-lang.org/book/title-page.html)
3. [A TDD Example in Rust](https://livebook.manning.com/book/a-rust-sampler/chapter-2/)
