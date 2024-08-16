# RISC-V builders

Runs Github Action on **REAL RISC-V** !

## Core features
* Native *RISC-V (riscv64)* architecture
* *Faster* than official runner
* *Free* for Github opensource project
* Multiple *SoCs* and *RISC-V extensions* available

## Installation
Install [RISC-V builders Github App](https://github.com/apps/riscv-builders) 

> Note: admin permission is required since we need to install runners for you.

## Usage

Change Github workflow with:

```diff
- runs-on: ubuntu-latest
+ runs-on: riscv-builders
```

You can also requires extensions like Bit/Vector, etc.

For example:
```yaml
runs-on:
  - riscv-builders
  - rve-zbb
  - rve-v
```

Or specify the RISCV SoC/CPU name that you wish to runs on.

For example:
```yaml
runs-on:
  - riscv-builders
  - soc-spacemit-k1
```

Real workflow example: [mengzhuo/GhostWrite](https://github.com/mengzhuo/GhostWrite/blob/main/.github/workflows/test.yml)

> NOTE "riscv-builders" MUST be the first label of runs-on

### Available labels:

#### SOC/CPU
* `soc-spacemit-k1`
* `soc-thead-1520` *NOT Available for now*
* `soc-starfive-jh7100`

#### RISC-V extenstions

* `rve-zba`
* `rve-zbb`
* `rve-zbc`
* `rve-zbs`
* `rve-v`

> Note: If no builder statisfied the combination of labels, action run will *hanged FOREVER* (Github limitation is 35 days).


## Contribute builder

For remote podman builders, please open a new issue on [Contribute Builder](https://github.com/riscv-builders/riscv-builders.github.io/discussions/new?category=contribute-builder)

For real builder send to us, please contact `tech<at>riscv.builders`, (change `<at>` to @) 


## Roadmap
* [ ] Pretty statistic website and homepage
* [ ] More robust service scheduler

## License
- Free to use if you are a non-profit or for personal use.
- Not available for commercial organizations *for now*.

## WIKI

Visit [WIKI page](https://github.com/riscv-builders/riscv-builders.github.io/wiki), for further information

## SLA
This project is very early *alpha stage* and *NO WARRENTY*.

## Author
* [mengzhuo](https://github.com/mengzhuo)

