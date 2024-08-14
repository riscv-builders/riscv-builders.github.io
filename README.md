# RISC-V builders

Runs Github Action on **REAL RISC-V board/machine/box**!

## Core feature

## Installation
Install [RISC-V builders Github App](https://github.com/apps/riscv-builders) (admin permission is required since we need to install runners for you.)

## Usage

Change your Github workflow with:

```diff
- runs-on: ubuntu-latest
+ runs-on: riscv-builders
```
and you are good to Go!!

You can also requires extensions like Bit/Vector, etc.

For example:

```yaml
runs-on:
  - riscv-builders
  - rve-zbb
  - rve-v
```

Or specify the RISCV SOC name that you wish to runs on.

```yaml
runs-on:
  - riscv-builders
  - soc-spacemit-k1
```

### Available labels:

#### SOC
* `soc-spacemit-k1`
* `soc-thead-1520` *NOT Available for now*
* `soc-starfive-jh7100`

#### RISC-V extenstions

* `rve-zba`
* `rve-zbb`
* `rve-zbc`
* `rve-zbs`
* `rve-v`

Note: *If no builder statisfied the combination of labels, action run will hanged FOREVER*


## Contribute builder

TODO


## Roadmap
* [ ] Pretty statistic website and homepage
* [ ] More robust service scheduler

## License
- Free to use if you are a non-profit or for personal use.
- Not available for commercial organizations *for now*.

## SLA
This project is very early *alpha stage* and *NO WARRENTY*.

