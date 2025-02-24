# TigerFetch

## Installation

#### Command line tool
Install the command line tool (you need a julia installation for this)
```bash
mkdir -p /.local/share/julia # or some other directory 
git clone git@github.com:eloualiche/TigerFetch.jl.git  ~/.local/share/julia
cd ~/.local/share/julia  && julia --project deps/build.jl install
```

The binary will available at `~/.julia/bin/tigerfetch` but also depends on the downloaded packages.
An easier way is to install the package directly from julia. 

#### Julia package

TigerFetch.jl is not yet a registered package. 
You can install it from github via
```julia
import Pkg
Pkg.add(url="https://github.com/eloualiche/TigerFetch.jl")
```

Then install the cli tool with
```julia
using TigerFetch; TigerFetch.comonicon_install()
````



## Usage

#### Command line tool

You can use it 
```bash
~/.julia/bin/tigerfetch --help
~/.julia/bin/tigerfetch state --output tmp
~/.julia/bin/tigerfetch cousub --state IL --output tmp 
~/.julia/bin/tigerfetch areawater --state "Minnesota" --output tmp # does not work # 10,000 lakes
~/.julia/bin/tigerfetch areawater --state "Minnesota" --county "Hennepin" --output tmp # works
```


#### Julia package

Look at the test suite (specifically `UnitTests/downloads.jl`) for now
