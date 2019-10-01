
**The Software Heritage Acquisition Process (SWHAP)** is the process of acquisition of software source code from a request (*push* acquisition) or from a discover (*pull* acquisition).

To acquire software, we consider *source code* - rather than executables, for its value in terms of readability and understanding of the operation of the system - possibly with its *version history* - as an analogous of the strata of an archeological site, providing insights on the development process of the software.

The process is build of the following steps:

* **Collect**:
  the activities in which the material is recognized, digitally acquired when needed and cataloged. This process may be particularly hard and costly when the original software is not already accessible in digital form: it may involve the discovery of the coding scheme of the stored information and the recovery, may be even the building anew of the reading device, when the source code is stored on obsolete data supports.
* **Curate**:
  the activities of restoring, refining, correcting, integrating and reshaping into standard forms of materials, in such a way that they can be easily accessed and consulted. In particular, a work of identifying the different versions of a software, with their authors, is required.
* **Present**:
  the activities of organizing the collected and refined data for their presentation to the large public. 
  
  In particular, apart from the submission to the Software Heritage Archive (that is the primary goal of the project, that is, to preserve the software base), many different supports may be needed for different purposes.
  For instance, Wikidata/Wikipedia, to preserve the related historical information in a machine-accessible way, for further generic dissemination of the knowledge embedded in the software.
  Open Access repositories can be used for articles, books, technical reports. Presentation tools/mechanisms, to provide the relevant information available in the previous archives in a way tailored to specific situations, like public events, lectures, etc. A good example is the work that has been done for [Science Stories](http://sciencestories.io).

Each part of the process can be done by different people with different technical and cultural knowledge.
The artifacts resulting at the end of each step are somehow milestones and represents a goal.
When someone reaches a milestone, the administrator of the project and other users should be able to know that.

To realize the process go through three phases; each phase correspond to a virtual place and it is equipped with:

* a **Catalogue**, similar to a library catalogue, is a complete list of items, typically one in alphabetical or other systematic order;
* a **Journal**, that is a registry where all the done operations are written. For the depository and the warehouse, the journal contains records for acquisitions, their date, notes about the origin of the artifacts, information about where they are archived. For the workbench the journal is more detailed: is a sort of lab notebook where every activity is tracked.

In particular, the stages of the process are supported by the following resources:
 
* **Warehouse**
when the acquisition concerns physical items they are immediately stored in this physical storage place, where they are maintained thereafter

* **Depository**:
  it is a collection of raw (digital) material: there may be cases where it is needed to recover the digital representation from printouts of a software system, blueprints of a system architecture, punched cards, floppy disks, etc.
   
* **Workbench**: is is the digital place where the work is done; it may contains temporary files
* **Vault**: is the final result of the software acquisition process, that is, a curated version of source code with metadata.

The final product of the process is the **curated source code (CuratedSC)** that will be stored into the Vault, that is the Software Heritage Archive ([HAL](https://hal.archives-ouvertes.fr/)).
Both the depository and the workbench are introduced to be able to trace the origin and the evolution of the artifacts leading to the CuratedSC.
In the end, we must be able to answer the questions *"What we have ?"*, *"Where and when we found it ?"*, *"In which way an item has been archived and transformed?"*.  
After being either pulled or pushed, the software is Collected from an *Origin*, and stored in its digital copy into the Depository.
The origin, in the case of physical repositories, can be a physical place, we speak of a warehouse. From the warehouse, a digital "as is" copy is made into the depository.

## Process instantiation: SWHAP@PISA

To acquire the legacy software of the Department of Computer Science at the University of Pisa, we instantiated SWHAP using GitHub as support.

Nowadays, major technology companies (Google, Facebook, Twitter etc) and many Open Source software foundations (Apache Foundation, Linux Kernel etc) host their open source project to GitHub, and actually GitHub has become by far the most popular place to host open source code on the web.
A CVS is suited for multiple users operation like tha acquisition process we describe as anyone can develop, curate, perform correction and integrations and then use the pull-request feature to submit those changes to the project's maintainers.
<!--; otherwise these steps need to be done with sorts of submission by email and integrate changes manually.-->
Moreover, GitHub offers extensive free disk space for open source projects, it is already integrated with the SoftwareHeritage crawler. thus realizing reliable preservation and convergence to on-line SC process.
<!--Finally GitHub offers facilities to compile the journal (in the form of commit history, where each change is tracked), the catalogue, some usefull collaboration and presentation and analisys tools.-->

In particular, we choose GitHub as main implementation support, both for the depository and the workbench as

* it is a well-established platform to store open source projects with multi-partners collaboration. It offers an extensive and reachable disk space at a convenient price - free for open source projects;
* at the moment, Software Heritage has already a crawler that feeds the Vault from GitHub - we have an instantaneous realization of redundancy for persistence and convergence to the on-line software code acquisition process.;
* it offers facilities to compile the journal (in the form of commit history, where each change is tracked) and the catalogue;
* it offers collaboration tools (via team, issues, etc) and it is integrated with presentation tools.

The implementation has involved the skeletal definition of several GitHub repositories. Most are introduced as templates, and are instantiated for the operations (storage included) of each acquisition.

1.  **SWHAP-PISA**
     This is the front-page of the project. It presents the SWHAP@PISA project, the SWHAP software acquisition process, collects the documentation, contains the catalogue of acquired softwares and the journal of acquisitions. It also links the template repository that has to be instantiated to support each acquisition process.
    It is curated by one or more maintainers in charge of accepting records for the catalogue.
2.  **SWHAP-TEMPLATE**
    This repository defines the skeleton of directories and files that has to be used for each software acquisition.
    In particular it is structured as

    * DEPOSITORY: 
        * CATALOGUE.<span></span>md 
            Contains references on where the physical source material is stored, possibly with some instructional references to contact.
            When the depository is done, the file content will be copied inside the SWHAP@PISA CATALOGUE.<span></span>md .
        * JOURNAL.<span></span>md 
            Contains a log of what has ben done, by whom and in what way is been done.
        * ACTORS.<span></span>md 
            Contains references and details about the people cited in the JOURNAL.<span></span>md. 
            For Authors it may contains current and historical data.
            It may contains many different roles: Authors, Collectors, Curators. 
        * README.<span></span>md 
            Contains a brief presentation of the $SW_NAME and on their authors.
            Contains a link to other files and section of the repository itself.
        * codemeta.<span></span>json
            Contains a list of pair value=data, using [CodeMeta](https://codemeta.github.io/crosswalk/) anthology, of all the raw - subject of further correction and integration - collected metadata.
            These metadata should be possibly filled by the author of the software himself, or the person in charge of the software in the moment of acquisition.
        If the software is already digitally acquired on other platforms (eg [HAL](https://hal.archives-ouvertes.fr/)) it can be omitted (the link to the other platform should be annotated into SWHAP@PISA catalogue).

    * WORKBENCH:
      * SRC
         Sinthetic git of source code versions (int the style of [@Spi16g]).
      * CATALOGUE.<span></span>md 
      * JOURNAL.<span></span>md 
      * README.<span></span>md 
      * LICENCE.<span></span>md 
      * METADATA.json
            Contains the [CodeMeta](https://codemeta.github.io/crosswalk/) sheet with all the structured completed and refined metadata - in the style of other platforms (eg [HAL](https://hal.archives-ouvertes.fr/)). 
      * Pointer to actively developed branch
      * DATA
            Additional data
    
    README.<span></span>md  and LICENCE.<span></span>md  as written by the original author for historic memory.

![DIUNIPI SWHAP](./IMAGES/SH_UNIPI_PROCESS.png)

The process here is as follows (see Fig. 1):

1.  For every new software acquisition, the DIUNIPI SWH TEMPLATE, which contains the depository skeleton template, is forked into a LAB repository.
   The forked repository is named according to the pattern $SW_NAME LAB, <!-- where $SW_NAME is in the form of Software_name+Main author surname+Year !-->.
2.  The acquisition process begins by filling the DEPOSITORY directory with all the digital version of original materials and the traces are written into the specific Depository Journal. Once the acquisition process is terminated the specific Depository catalog is compiled the DEPOSITORY directory is cloned into a $SW_NAME DEPOSITORY repository. This repository will be set as read-only (that is, writable only by the owner - the repositoy [is archived](https://github.blog/2017-11-08-archiving-repositories/)).
3.  The curation process begins filling the  directory from the material of the DEPOSITORY directory. In particular, the SRC folder will contain a synthetic git build following what done by Spinellis [@Spi16g]. The DATA directory will contain all additional information. As for depository, once the curation process is completed, the WORKBENCH directory is cloned into a $SW_NAME repository and will be set as read-only. This is the curated software, the result of the acquisition process.
When (both the collect and) the curation process is terminated the LAB depository is deleted and the link to $SW_NAME DEPOSITORY and to $SW_NAME are added to the SWHAP@PISA CATALOGUE.
1.  Once the curated software repository is done, the curator proposes a record into the catalog of [SWHAP@PISA](https://github.com/Unipisa/SWHAP@PISA) repository. The owner of [SWHAP@PISA](https://github.com/Unipisa/SWHAP@PISA) repository will accept the record and will submit the curated software to the Software Heritage Archive ([HAL](https://hal.archives-ouvertes.fr/)).

The whole process requires some administrators and moderators of SWHAP@PISA process, while each step can be done by different people.
For this reason, HOWTO<span></span>.md contains distinct guidelines for the many different roles involved.

The final picture, with curation process ended, is as in see Fig. 2.

![DIUNIPI SWHAP final result](./IMAGES/SH_UNIPI_PROCESS_RESULT.png)