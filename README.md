# Introduction

This repository contains our Java implementations of SHIP, SPINE and our Use Cases
as submodules. It is set up to ignore the dependencies in the submodules. That means
`spine/` will build and use `ship/`. Also, `use-cases/` will build and use `ship/`
and `spine/`.

## Important!

- After cloning, run
  ```bash
  git submodule init
  git submodule update
  ```
  to initiate all submodules.

- To switch to the develop branch in all submodules, run
  ```bash
  git submodule foreach 'git switch develop'
  ```

- To pull the newest changes in all submodules, run
  ```bash
  git submodule foreach 'git pull'
  ```
