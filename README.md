# Sched

`chrt` like tool in rust
- show sched info of a task
- change sched info of a task

```shell
Usage: sched --pid <PID> <COMMAND>

Commands:
  read   [aliases: r]
  write  [aliases: w]
  help   Print this message or the help of the given subcommand(s)

Options:
  -p, --pid <PID>  
  -h, --help       Print help
  -V, --version    Print version
```

support rich sched policy, as well as "SCHED_EXT"

```shell
Usage: sched --pid <PID> write <SCHED> <PRIO>

Arguments:
  <SCHED>  [possible values: normal, fifo, rr, batch, idle, deadline, ext]
  <PRIO>   

Options:
  -h, --help     Print help
  -V, --version  Print version
```

support for glibc or musl

```shell
$ cargo build --release

$ cargo build --target x86_64-unknown-linux-musl --release
```