# STM32 Memory Loaders

## Overview

This repository contains STM32 flashloader source code for both external and internal memories used on STM32 hardware boards.
The **master** branch provides the flashloader projects and source files integrated with STM32CubeProgrammer.

## External memories

External memories are available on many STM32 hardware boards such as evaluation and discovery kits. They can be Flash or SRAM and provide higher storage capabilities. STM32 boards support many types of external memories from vendors such as Micron and Winbond, connected through interfaces like FMC and SPI.

## Internal memories

Internal memories are embedded inside STM32 MCUs (such as on-chip Flash and SRAM).

## External memory loaders

External memory loaders are located in `external_memory_loaders/` and are organized by STM32 series and board.

Each external flashloader project is built with EWARM or MDK-ARM IDE and comes with the corresponding source, header, and linker files:

* Library: source/header files providing required drivers to manage read, write, and erase functionalities of the supported memory, needed to implement initialization, erase, and write functions.
* Loader: source/header files containing specific information related to the supported memory (name, size, and related functions).
* Project: a preconfigured project with the associated linker file.

### How to adapt an external flashloader project for a customized board

The required steps to build a customized external loader for STM32CubeProgrammer are available at this [link](https://www.st.com/content/ccc/resource/technical/document/user_manual/e6/10/d8/80/d6/1d/4a/f2/CD00262073.pdf/files/CD00262073.pdf/jcr:content/translations/en.CD00262073.pdf) (Section 3.9).

## Internal memory loaders

Internal memory loaders are located in `internal_memory_loaders/`.

## Feedback and contributions

Please refer to the [CONTRIBUTING.md](CONTRIBUTING.md) guide.
