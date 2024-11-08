# DITA Topic Model - ENTER TITLE OF PROJECT HERE

This repo contains a DITA topic model (TM) related to [enter main goal and topic of your model here].

## Authors

- Elijah Reddick
- Madison Young

## Folders &amp; Files

- `.github`: Contains configuration files for "Github Actions".
- `assets`: Contains all assets used within the TM.
- `concepts`: Contains all concept topics.
- `references`: Contains all reference topics.
- `tasks`: Contains all task topics.
- `shared`: Contains all topic files that are shared across multiple maps.
- `out`: Contains all output folders.
- `themes`: Contains `.yaml` style configuration files.
- **Skeleton files**: All topic folders contain a single "skeleton" topic file for you to copy, whenever you need to quickly create a new file.
- `.keep` **files**: Ignore these files. They ensure that any empty folders are tracked by git. 
- `.gitignore`: This file tells git which files to ignore in the repo. You can leave this one be.

## Filenaming Conventions

- Task Topics: `t_verb_verbobject.dita`
- Concept Topics: `c_nounphrase.dita`
- Reference Topics: It varies, but something akin to `r_types_of_nounphrase.dita`
- Dita Maps: `_modelname.ditamap`

## Building Outputs with Github Actions

This repo uses Github Actions to create outputs. Refer to the following for details: 

- [.github/workflows/dita-ot-build-actions.yaml](.github/workflows/dita-ot-build-actions.yaml)
- [DITA User Docs - Using Github Actions](https://www.dita-ot.org/dev/topics/using-github-actions)
- [DITA Example YAML files](https://github.com/dita-ot/docs/blob/develop/samples/github-actions/build-using-a-project-file.yaml)

## Building Outputs Manually with the Command Line

See the DITA-OT user guide about how to generate output: [https://www.dita-ot.org/dev/topics/build-using-dita-command](https://www.dita-ot.org/dev/topics/build-using-dita-command)

### Sample DITA Commands

#### Help

To see all of the commands and parameters, use the following command:

```
dita --help
```

#### DITA options and arguments

```
-f == dita output format
-i == dita input map file
-o == dita output directory
-D&lt;property&gt;=&lt;value&gt; == add custom args
    with particular values to dita transformation
-filter &lt;file&gt; == filter and flagging file
```

#### Create an HTML5 site

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```

#### Create an HTML5 site with a custom CSS file

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
  -Dargs.cssroot='url/to/your/assets/folder' \
  -Dargs.css='${cssroot}/your-custom-css-file.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
```

#### Create a PDF

```
dita -f pdf -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```
## Project Maps

### LCA Data Collection
user scenario 1: 

A legal assistant who has been working at an immigration law firm for six months has been primarily
helping compile information for employment-based petitions. Recently, they have also been
trusted with a crucial part of the process that helps establish a living wage the employer must pay to the
sponsoring client so that they are being compensated appropriately for their employment. This document is known
as a LCA (Labor Condition Application) and is submitted by a head attorney but can be drafted by a junior
assistant. This step is not very complex but the form is located on a new website that requires a login and a new
fillable form interface using hyperlinks to other websites that help the user understand what wage is appropriate
for the worker based on degree, years of experience, and special skills.

map 1: 

topic reference idea 1: LCA Data Collection 
  standard wage ranges (concept)
  wage levels (concept)
    determining correct wage ranges (task)
    determining correct wage level (task)
  types of petitions that need a LCA (reference)
  types of documents needed LCA (reference)

map 2: 

topic reference idea 2: LCA Application Completion 
  standard wage ranges (concept)
  wage levels (concept)
  the labor condition application (concept)
    completing the labor condition application (task)
  types of search functions in o-net (reference)

user scenario 2: A legal assistant who has been working at an immigration law firm for three months has been helping create employment-based immigration petitions like the H-1B visa. A H-1B visa is part of the I-129 employment-based petition and requires different documents, forms, and clients that the legal assistant must interact with now. They are familiar with the USCIS website, the workflow of compiling a petition and contacting clients for required information. They are confident in their ability to manage this case but still need advice on specific tasks like how to craft a company support letter since that is not a requirement in family-based petitions. In addition to creating a H-1B visa, they have also been trusted to collect data for the LCA application but not fill out the form. 

map 1: 

topic reference idea 1: H-1B and LCA Petition Process for New Users

  contents of a H-1B petition (concept)
  what is a USCIS cover letter (concept)
    organizing a H-1B petition (task)
    creating a USCIS cover letter (task)
  standard wage ranges (concept)
  wage levels (concept)
    determining the correct wage range (task)
    determining the correct wage level (task)
    types of petitions that need LCA (reference)

map 2: 

topic reference idea 2: H-1B and LCA Petition Process for Advanced Users

  contents of a H-1B petition (concept)
  standard wage ranges (concept)
  wage levels (concept) 
    determining the correct wage range (task)
    determining the correct wage level (task)
    types of search functions in o-net (reference)

### H-1B Petition Creation
user scenario 3: A new legal assistant has just been hired by an immigration law firm. They have an undergraduate education in the humanities and have undertaken positions that require great amounts of reading and writing in the past. They do not have experience in legal studies but have experience in following complex processes at their previous company. They have been tasked with drafting their first H-1B petition packet for a client coming from Norway who has been sponsored by an international automotive company wishing to have an employee work at one of their U.S. automotive factories. They have been told what a H-1B petition does and why it exists but have not been clearly told why an H-1B petition is the required petition in this specific scenario context. Additionally, they have been told what types of documents are needed but have been instructed to look at the firm's past petitions of this type to see what specific documents are required, but they are unsure of whether they should use the document types they find in other petitions due to the dated nature of the last petition. They also have been instructed to look at the USCIS website to find current form editions and physical addresses for USCIS field offices to send the petition to after the petition draft has been approved, but the website is vast in content. They are not required to manage the entire case from start to finish but, there is an expectation that they will produce a good first draft and compile the correct documents needed so that a more senior employee can file it themselves. 

map 1: 

topic reference idea 1: 

What is a H-1B Petition? (concept)
  Contents of a H-1B Petition (concept)
  What is a USCIS Cover Letter? (concept)
    Creating A USCIS Cover Letter (task)
  Labor condition application information (concept)
    completing the labor condition application form (task)
    required documents for the labor condition application (reference)
  Organizing the H-1B Petition (task)
  search functions offered within o*net (reference)

map 2: 

topic reference idea 2: 

Search functions offered within o*net (reference)
What is a H-1B Petition? (concept)
Contents of a H-1B Petition (concept)
What is a USCIS Cover Letter? (concept)
  Creating A USCIS Cover Letter (task)
Labor condition application information (concept)
    completing the labor condition application form (task)
    required documents for the labor condition application (reference)
    types of petitions that require lca (reference)
Organizing the H-1B Petition (task)