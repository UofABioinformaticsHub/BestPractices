# <img src="UoA_logo_col_vert.png" alt="UofALogo" style="width: 100px;"/> University of Adelaide - Bioinformatics Hub

## Best Practices for Bioinformatics Research

Last Revised 22-Jan-2017

# Reproducible Research

- **All research should be reproducible from a technical standpoint:**
  - If two runs of the same code produce different results, these are not valid results.
- **Never edit files using a GUI:**
  - If provided with Excel or csv files which require editing or transforming, write code to do this.
    1. You will know exactly what you have done, and so will other researchers
    2. The chances of you having to repeat the editing with revised data are high, so write the code once
- **Reproducible doesn't mean correct**
  - Reproducible code with errors will simply reproduce the errors. Make sure your code is analytically sound.

# Coding Practices

## Write code for people, not computers

- **Variable names must be easy to interpret:**
  - e.g. a list of genomes should be called `genomeList` not `g`
  - Don't call objects `results` and `results2`. Include information in the name.
  - Typing extra characters is easy using auto-complete
- **Comment your code extensively:**
  - You will have to revisit most analyses in the future.
    Write comments to remind yourself of what you've done.
  - Collaborators with less coding experience than you will often need to read your code. Communication is much easier if they can understand what you've actually done.
- **Write intelligent comments**
  - Comments such as `# Load all data` could be better written as `# The data is spread across 183 csv files in the directory /myData. Load all into a single object`
  - Too much information in a comment never broke a program
- **Be stylistically consistent**
  - This just makes your code easier to follow for everyone


## Always Use Version Control

- **Version control is not just for package or software development.**
  - Use version control for _every analysis_!
  - Where appropriate use private repositories
- **Be consistent across an organisation**
  - _Git_ is the version control methodology used by the Bioinformatics Hub
- **Make incremental changes**
  - Recompile or rerun regularly to minimise coding errors.
  - _Stage after a successful run_
- **Write informative commit messages**
  - This makes it easier to find old code
- **Use a remote code repository**
  - Push your code daily. This provides an up-to-date copy in the case of disk failure
  - This also enables collaborators to contribute

## Error Handling

- **Include Checks:**
  - These can include simple things like the presence of a file with the correct name, to verification of the output of a function.
- **Error Handling:**
  - You will make mistakes! Often.
  - Write code to fail quickly and loudly on errors
  - Write clear error messages

# Data Management

## Data Integrity

- **Keep a copy of all source data**
  - Utilise storage which is backed up by the storage provider.
  - For UofA research, use the `phoenix` HPC system

- **Make the source data read-only**
  - This prevent accidental deletion or editing as a result of poorly written, or copied scripts can easily do this
  - This setting can easily be temporarily changed was required

## Metadata and Study Design are important

- **Always begin an analysis by decribing the data, motivation and the intended path to the results.**
- **Where possible, make raw data available**
  - At the least, collaborators should know where to find it.

# Research Collaborations

- **Always confirm with the principal researcher before collaborating** (or adding new collaborators)
  - If you've made a contribution which has not been approved by the PI, don't be surprised if it is not treated with the respect you hope for
- **Agree on the key positions of authors in advance**
  - Any significant contributon should be rewarded with co-authorship

# Record Keeping

- **Never use a GUI**
  - Ever
- **Analytic code must be version controlled**
  - This provides digitally verified copies of the analysis with dates recorded
  - Old approaches which need to be reinstated can be accessed
- **Keep a lab book**
  - Despite working mainly _in silico_, records of new approaches should be written and signed off in a lab book
  - Keep full details of thought processes and ideas for new analytic approaches
  - These are essential to legal proceedings (e.g. prosecuting a patent)
- **See previous section about source data**

# Hub Preferred Approaches

## Operating Systems
- Ubuntu >14.04 is the preferred OS
- Mac OSX > 10.9 is also acceptable
- Windows 10 is not desired, but can be used to provide access to Ubuntu running on this OS. Windows < 10 is not acceptable

## Statistical Analysis
- This is to be perfomed using `R` or `Python`
  - R-Markdown or Sweave are preferred for analysis
- Excel, SPSS etc are not acceptable

## Version Control
- Git is the only acceptable version control system
- GitHub is the preferred repository, although bitbucket can be used for code with privacy requirements
- Analysis stored in a private repository must have a minimum of two users with read access

## Theses and Journal Articles
- LaTeX is the recommended language for formal documents
