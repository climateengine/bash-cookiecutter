# Bash Cookiecutter
A bunch of boilerplate code to create good bash scripts.

## Usage
Copy `bash_cookiecutter` to `your_script` or whatever you want to name your script.


### Argbash
[Argbash.io](https://argbash.readthedocs.io/en/latest/index.html) is used to generate the argument parsing code.
In order to modify the argument parsing code (i.e. modify arguments) you modify the Argbash
template (lines 3-10) and then run:
```shell
argbash your_script -o your_script
```

If you do not have `argbash` installed, you can copy/paste your code into [online argbash](https://argbash.io/generate)
which will do the same as running argbash locally (but installing argbash is recommended).

Read more about Argbash in the [online docs](https://argbash.readthedocs.io/en/latest/index.html) but
honestly, it's something that makes more sense once you start using it.

### Logging
`bash_cookiecutter` creates a bunch of logging functions:
```shell
notify "notify message - always notifies regardless of log level"
fatal "fatal message"
error "error message"
warn "warning message"
info "info message"
debug "debug message"
```

Use these instead of `echo` for logging. They do a lot of neat things like printing the time,
the line number (for debug messages), and allowing output to a file.


## tl;dr:
  - `cp bash_cookiecutter your_script`
  - Edit *only* lines 3-10 and 180-190
  - Argbash template is lines 3-10
    - If you modify this, run `argbash your_script -o your_script`
  - Write your code in lines 180-190
  - Use `notify`, `debug`, etc. for logging messages.

