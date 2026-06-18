# Wolfram — Elementary Cellular Automaton

> Epitech project — B-FUN-400 (B4, *Functional Programming*)

A terminal program that computes and displays **Wolfram's elementary cellular automaton**, written in **Haskell**. Each generation is computed from the previous one according to a chosen rule, and rendered line by line in the terminal.

Rules 30, 90 and 110 are supported (the other 253 rules are an extension).

## Tech stack

- **Language:** Haskell
- **Build:** Stack (LTS 18), wrapped in a `Makefile`
- **Binary:** `wolfram`

## Build

```sh
make
```

## Usage

```sh
./wolfram --rule 30 --lines 20
```

| Option      | Description                                                        | Default |
|-------------|--------------------------------------------------------------------|---------|
| `--rule`    | The ruleset to use (mandatory)                                     | —       |
| `--start`   | Generation number at which to start the display                    | `0`     |
| `--lines`   | Number of lines to display (runs forever if omitted)               | ∞       |
| `--window`  | Number of cells per line (line width)                              | `80`    |
| `--move`    | Horizontal translation of the window (negative = left)             | `0`     |

Invalid arguments exit with code `84` and print a usage message.

## What I learned

- Functional programming idioms in Haskell: pure functions, pattern matching, guards, higher-order functions
- Separating pure logic from side effects (I/O)
- Manual argument parsing without `getopt`
