# jEEBus

This repository contains all Open Source jEEBus libraries as Git submodules in one
composite Gradle build.
This enables quick and easy jEEBus development across all the different EEBus layers.

## Project Setup

The composit build overwrites the dependencies in the submodules. That means
`spine/` will build and use `ship/`. Also, `powerlimitation.controllablesystem/` will
build and use `ship/` as well as `spine/`.

### Git

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

### Gradle

This is a Gradle Project that comes with a packaged Gradle Wrapper (use `./gradlew`
on Linux and `gradlew.bat` on Windows systems). You can run the following command to
download all necessary dependencies and build the project:

```bash
./gradlew clean build
```

To run all jEEBus unit tests, run

```bash
./gradlew test
```

## Contributing

This repository is not intended for direct contributions. Please direct any code
changes to the concrete library repositories
for [ship](https://github.com/openmuc/jeebus.ship), [spine](https://github.com/openmuc/jeebus.spine)
or [powerlimitation.controllablesystem](https://github.com/openmuc/jeebus.usecase.powerlimitation.controllablesystem).

However, if you come across an issue concerning **multiple** layers, feel free to create
a new issue here.

## License

Copyright (c) 2026 Fraunhofer ISE

This program and the accompanying materials are made available under the
terms of the Eclipse Public License 2.0 which is available at
https://www.eclipse.org/legal/epl-2.0 or the provided `LICENSE` file.

SPDX-License-Identifier: `EPL-2.0`
