# 🐚✨ Shell-AI

Shell-AI or `sai` is a tiny Python script on top of [OpenAI's Python library](https://github.com/openai/openai-python) to write and run shell commands.

## 🛠️ Installation

Add the following for your shell rc:

```sh
export OPENAI_API_KEY=<your_key>
```

```sh
pip instal openai
```

Copy `sai` somewhere on your `PATH`.

## Usage

```sh
❯ sai create a folder for every day of the next week, including today named with the date formatted as 'yyyy-mm-dd'
mkdir $(date -v+0d +%Y-%m-%d) $(date -v+1d +%Y-%m-%d) $(date -v+2d +%Y-%m-%d) $(date -v+3d +%Y-%m-%d) $(date -v+4d +%Y-%m-%d) $(date -v+5d +%Y-%m-%d) $(date -v+6d +%Y-%m-%d)
run command? (y/N): y
```

```sh
❯ sai list folders in directory that start with 2023
ls -d 2023*
run command? (y/N): y
2023-04-16	2023-04-17	2023-04-18	2023-04-19	2023-04-20	2023-04-21	2023-04-22
```

**⚠️ Warning: do not try this ⚠️**

```sh
❯ sai remove root folder
sudo rm -rf /
run command? (y/N): ^C
canceled
```
