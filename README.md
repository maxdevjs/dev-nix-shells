# dev-nix-shells

> WIP

## Table of Contents

1. [What is this](#what-is-this)
1. [Dependencies](#dependencies)
1. [Why](#why)
1. [Nix Shells](#nix-shells)
1. [Available repositories](#available-repositories)
1. [Elixir, Phoenix, and OTP](#elixir-phoenix-and-otp)
1. [JS](#js)
1. [Lua](#lua)
1. [RoR](#ror)
1. [Rust](#rust)
3. [Usage](#usage)
4. [Resources](#resources)
5. [TODO](#todo)

## What is this

[nix-shell](https://nixos.org/manual/nix/stable/#description-13) (templates for several) development environments.

Basically, a [nix-shell](https://nixos.org/manual/nix/stable/#description-13) starts an interactive shell based on a [Nix](https://github.com/NixOS/nix) expression.

> 🧐 if not acquainted with the topic, it is better to do a quick research about it: [Resources](#resources)

### Dependencies

We need either:

- [NixOS](nixos.org/) (tested)
- [Nix](https://github.com/NixOS/nix) (package manager [installed](https://nixos.org/manual/nix/stable/#ch-installing-binary) in other OSs (`Linux` and `macOS`), untested)

## Why

[Nix](https://github.com/NixOS/nix) installs required dependencies and separates the environment from others on your system.

We can then check this Nix configuration into version control and share it with others to make sure we are all running the same software. Especially with many dependencies this is a great way to prevent configuration drift between different team members & contributors.

## Nix Shells

Every and each [nix-shell](https://nixos.org/manual/nix/stable/#description-13) is hosted in its own repository.

### Available repositories

#### Elixir, Phoenix, and OTP

- [nix-shell for elixir](https://github.com/maxdevjs/dev-nix-shells-elixir)
- [nix-shell for erlang](https://github.com/maxdevjs/dev-nix-shells-erlang)
- [nix-shell for phoenix](https://github.com/maxdevjs/dev-nix-shells-phoenix)

#### Node.js

- [nix-shell for Node.js](https://github.com/maxdevjs/dev-nix-shells-nodejs)

#### Lua

- [nix-shell for Lua](https://github.com/maxdevjs/dev-nix-shells-lua)

#### RoR

- [Nix-ifying Rust projects](https://github.com/maxdevjs/dev-nix-shells-rails)
- [nix-shell for ruby](https://github.com/srid/rust-nix-template)

#### Rust

##### Currently testing

- [Setting up a Rust environment in Nix](https://gutier.io/post/development-using-rust-with-nix/)
- [oxalica/rust-overlay](https://github.com/oxalica/rust-overlay)
  - experimenting with [rust-overlay#nix-flakes](https://github.com/oxalica/rust-overlay#nix-flakes)
    - `nix shell github:oxalica/rust-overlay` 
    - 
##### Next

- [nix-shell for ruby](https://srid.ca/rust-nix)
- [srid/rust-nix-template](https://github.com/maxdevjs/dev-nix-shells-ruby)

## Usage

- git clone the desired repo
  - example: `$ git clone https://github.com/maxdevjs/dev-nix-shells-nodejs my-awesome-nodejs-app`
- cd into the cloned folder
  - example: `cd my-awesome-nodejs-app`
- allow [direnv](https://direnv.net/) (if installed)
  - `$ direnv allow`
- otherwise
  - `$ nix-shell shell.nix` (default)
- wait for initialization
  - the first time all the tools will be installed
    - following times there can be updates
      - ...
- enjoy
  - eventually 🤔
- update the `README.md` and `LICENSE` files

## Resources

Every single [nix-shell](https://nixos.org/manual/nix/stable/#description-13) repository offers relevant resources.

Here there are a few commons ones.

### Direnv

- [direnv wiki page about Nix](https://github.com/direnv/direnv/wiki/Nix)
- [Automating development environment set-up with Direnv](http://www.futurile.net/2016/02/03/automating-environment-setup-with-direnv/)
- [More prac­ti­cal direnv](https://rnorth.org/more-practical-direnv/)

  - [rnorth/.direnvrc](https://gist.github.com/rnorth/0fd5048da85957da39c17bd49c4ca922)

### Miscellaneous

- [About using Nix in my development workflow - Jean-Philippe Cugnet - Medium](https://medium.com/@ejpcmac/about-using-nix-in-my-development-workflow-12422a1f2f4c)
- [nix-dot-dev/getting-started-nix-template: Based on nix.dev tutorials, repository template to get you started with Nix.](https://github.com/nix-dot-dev/getting-started-nix-template)
- [rajatsharma/snowstorm: ❄️ Hyper easy nix environments](https://github.com/rajatsharma/snowstorm)

### Nix

- [Nix Wiki](https://nixos.wiki/wiki/Nix)
- [Setup a development environment](https://nixos.org/guides/dev-environment.html)

## TODO

- [lorri](https://github.com/nix-community/lorri) integration
- [niv](https://github.com/joefiorini/niv)
- ...
