# dymsum

> DYnaMical Systems the Uncomplicated Manner, abbr. *dymsum*, is a free toolbox for solving symbolic equations involved in control engineering.

If you do STEM in college, it is likely that you use MATLAB with Symbolic Math Toolbox and Simulink with Simscape circuits, don't you? Despite being powerful tools, they often come with a costly license. In case you want an open-source alternative, give dymsum a try.

✔️ Dymsum is an interpreter that understands MATLAB scripts.

✔️ It can solve MATLAB equations written with Symbolic Math Toolbox.

❌ Dymsum is **NOT** a full-fledged computer algebra system (CAS). In fact, it depends on the C++ library *symengine* to find solutions.

❌ It does **NOT** guarantee solvability for all MATLAB code.

## Installation

We distribute `dymsum` as a standalone executable so that you can simply download and extract the ZIP package on your file system. Head over to our [release page](https://github.com/SymDynamics/dymsum/releases) to see supported platforms.

## Build from source

In this early development phase, Dymsum is just the frontend of [Racket](https://racket-lang.org/), which means all computation is made by the Racket interpreter. Building from source **for Linux** is as easy as these following steps. Windows and Mac users can find more instruction in [our document]().

1. Install Racket

```bash
wget https://download.racket-lang.org/releases/8.16/installers/racket-minimal-8.16-x86_64-linux-bc.sh

# Might require `sudo` to install in admin directories
sh racket-minimal-8.16-x86_64-linux-cs.sh

# Double-check successful installation
raco --version
```

2. Clone Dymsum repository and build (for Linux)

```bash
git clone https://github.com/SymDynamics/dymsum.git
cd dymsum
racket exe -o bin/dymsum
```

Now you have the `dymsum` CLI application in the `bin` folder. You can choose to add it to `PATH` so that `dymsum` can be invoked from anywhere.

3. *Optional:* add to PATH

```bash
export PATH=$PATH:$(pwd)/bin
```

## Usage

