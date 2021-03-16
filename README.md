
---
<p align="center">
  <img src="./additional_materials/SWHAP-PISA-LOGO-HEAD.png" alt="SWHAP@PISA"/>
</p>

---

# SWHAP@Pisa

The SWHAP@Pisa project is a joint venture of the [Department of Computer Science](https://di.unipi.it) of the [University of Pisa](https://unipi.it) and [Software Heritage](https://www.softwareheritage.org) (SWH). It aims at defining and supporting a process to acquire sorce code to be saved in the SWH [archive](https://archive.softwareheritage.org/browse/search/?q=https%3A%2F%2Fgithub.com%2FUnipisa%2F).

This repository brings together the documentation, the catalogue and other information about this process, dubbed SWH Acquisition Process (SWHAP) and its Github based support SWHAPPE (SWHAP Pisa Enactor).


---


- [SWHAP@Pisa](#swhappisa)
  - [The Process](#the-process)
  - [Process support](#process-support)
  - [Current state](#current-state)
  - [How To Contribute](#how-to-contribute)


---

## The Process

SWHAP organizes the activities involved in the acquisition process in four phases:

- *collect*, aiming at finding the source code and related materials and gathering each piece *as is* in physical or logical places where they can be properly archived for later processing;
- *curate*, aiming at analyzing, cleaning up and structuring the raw materials that have been collected;
- *archive*, aiming at contributing the curated materials to specialized public archives, Software Heritage in primis;
- *present*, aiming at creating dedicated presentations of the curated materials.

The process must be seen as iterative, in the sense that, when new materials are available, the pertinent phase can be re-entered and the process enacted once more from there to update all the relevant information.

For more details, please see [the process documentation](https://github.com/SoftwareHeritage/swhapguide/blob/master/SWHAP%40Pisa.pdf).

## Process support

The SWHAP@Pisa project designed and implemented the SWHAP Pisa Enactor (SWHAPPE), an environment to support SWHAP based on the platform you are accessing, that is, [GitHub](https://github.com/).

SWHAPPE provides a [*template repository*](https://github.com/Unipisa/SWHAP-TEMPLATE) to be instantiated and then filled for each acquisition. According to the supported naming rules, acquiring the source code XYZ will result in the following repositories:

- the *XYZ Workbench*, a working area where one can temporarily *collect* the materials and then proceed to *curate* the code;
- the *XYZ Depository*, to archive the raw materials;
- the *XYZ*, where the version history of the code is rebuilt by the *curation team*, as it is *archived* in SWH.

For a detailed description of SWHAPPE, please see section 3 of the [SWHAP guide](https://github.com/SoftwareHeritage/swhapguide/blob/master/SWHAP@Pisa.md).

For a detailed guide on how to use SWHAPPE, please refer to the *walk through an example* in section 4 of the [same guide](https://github.com/SoftwareHeritage/swhapguide/blob/master/SWHAP@Pisa.md) and to the [scripted acquisition example](https://github.com/Unipisa/SWHAP-EXAMPLE).

## Current state

The list of the currently available acquisitions is in the [Catalogue](./catalogue.md).

Notable acquisitions include: [CMM](https://github.com/Unipisa/CMM), [OrbFit](https://github.com/Unipisa/OrbFit), [TAUmus](https://github.com/Unipisa/TAUmus), [Softi](https://github.com/Unipisa/Softi).


## How To Contribute<!--_Here a brief description of how an acquisition can be done_ -->

[This is a mailing list](https://sympa.inria.fr/sympa/info/swhap) dedicated to the Software Heritage Acquisition Process.
Feel free to register and exchange informations and best practices.

For a detailed description of SWHAPPE, please see section 3 of the [SWHAP guide](https://github.com/SoftwareHeritage/swhapguide/blob/master/SWHAP%40Pisa.pdf); for an overview, see the [presentation](https://annex.softwareheritage.org/public/talks/2019/2019-10-28-Hapoc_CarloMontangero.pdf) at [HaPoC 2019](https://hapoc2019.sciencesconf.org)



----------------------------

:construction: :construction_worker: **Warning** _this repository is still under contruction_  :construction_worker: :construction:
