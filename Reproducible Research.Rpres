Reproducible Research
========================================================
author: Vicki Hertzberg
date: 18 January, 2017
autosize: true
transition: fade
transition-speed: faster


========================================================

The keystones of science are replicability and reproducibility.

http://www.economist.com/node/21528593

========================================================

Direct replicability 

- Repetition of program with original data by re-execution
- Provides evidence that a finding can be obtained.

========================================================

Conceptual replication (reproducibility)

- Validate interpretation of original results by manipulation using different techniques 
- Provides evidence about the meaning of the finding.

=========================================================

Reproducibility

- Bridges gap between replication and letting the study stand alone
- Take data/code and replicate findings -> validate findings
- Why do we need reproducible research?
  - New technologies increase data throughput while adding complexities and dimensions to data 
  - Existing databases merged into bigger collection of data
  - Computational power increased


=========================================================

For computational science, reproducible research is often related to the concept of literate programming (Knuth, 1984).

Basic concept of literate programning: combine computer code and software documentation in the same document, with the code and documentation identified by special markers.

Tools for literate programming that we will use:

- R Markdown (Rmd)
- knitr (this will work under the hood, so to speak)
- Git
- GitHub

========================================================

Major journals (e.g., Science, Nature) are now requiring that the data and the code to run it are published in conjunction with the manuscript.

Reproducible experiment includes:

- Description of the input data
- Details about system where experiments were performed (hardware, software)
- Executable specification for the experiment

=======================================================

What do we mean by reproducible in computational science?

Same experimental procedure produces same results.

=======================================================

Same experimental procedure?

- Download the original software and data and run it
- Download the original software, compile on different machine, and run with original data
- Dowload software that does the same thing and apply to the original data
- Produce a new implementation of the algorithms described and run it on the original data
- Run any of the above on a refined or updated data set

========================================================

Same results?

- Identical output down to the bit level
- Exactly the same numbers
- Exactly the same numbers when run on similar machine
- Numbers that are within some bound of error
- Ensembles of outputs that share certain characteristics, within some bound of error



========================================================

Levels of Reproducibility

1. Depth - how much is made available
2. Level of portability - can experiment be reproduced on
  - Original environment
  - Similar environment
  - Entirely different environment
3. Coverage - how much can be reproduced

(Freire, et al. SIGMOD'12)

======================================================

Computational Research Life Cycle

- Individual exploration
- Collaboraton
- Production-scale execution
- Publication
- Education

=======================================================

Tools used at the Individual Level:

Excel, MATLAB, Mathematica, Prism, R, SPSS, SAS, STATA, programming language

Issues:

- Some are proprietary and/or expensive
- Most are relatively slow
- Most do not have a rich document format

=======================================================

Tools used at the Collaboration Level:

email, VCSs, shared folders (e.g., network drive or Dropbox)

Issues
- Most common is email with ad hoc naming conventions
- email does not scale for large projects

========================================================

Tools used at the Production Level:

Move from interactive computing environment to compiled code and libraries.
Results from compiled code are imported to interactive computing environment for production of graphics, etc.

- Maintenance of two versions of code
- Back and forth is difficult for VCS

========================================================

Tools used at the Publication and Education Levels:

LaTeX, Google Docs, MS Word, MS Powerpoint

With the exception of LaTeX, these have
- poor integration with VCSs
- ill-suited for workflow automation (i.e., lots of cutting and pasting, with potential for errors)

=========================================================

Summary

- Common approaches and tools today produce discontinuities at each stage of research, increasing error potential.
- Key gap: discontinuity between "final outcomes" (i.e., papers and presentations containing figures, tables) and the pipeline that feeds these outcomes
- Problem: both technical AND social; need buy-in from all team members for improved work habits at the beginning of the project. 

======================================================

Workflow in Data Science

- Question
- Raw data
- Cleaned data 
- How the data fit together
- Data analysis
- Publication

Need to establish provenance at each step along the way.

======================================================

http://www.biostat.jhsph.edu/~rpeng/research.html

======================================================
Literate Statistical Analysis (Rossini)

Process of ensuring data analysis is clear and transparent in terms of describing programs used to generate results.

Extends beyond the Literate Programming paradigm to 

1. Scientific question and origins of the data
2. Statistical methods used, their caveats and assumptions
3. Code and programs used
4. Results and interpretation

In addition to mixing of code and documentation, tables / figures generated are to be imported back into the document, concentrating more on data analysis as a whole instead of just data and programs.

========================================================
RESOURCES

- Managing a statistical analysis project guidelines and best practices

    http://www.r-statistics.com/2010/09/managing-a-statistical-analysis-project-guidelines-and-best-practices/

- Project template - a pre-organized set of files for data analysis 

    http://projecttemplate.net/

========================================================
Reluctance to Share Code and Data (Borgman, 2007)

1. Lack of incentives (citations, promotion)
2. Effort required to clean data and code
3. Creation of a competitive disadvantage among peers
4. Intellectual property issues

One way around reasons 1 and 2: http://www.runmycode.org/home

========================================================

Reproducible Research Checklist

- Are we doing good science?
- Was any part of this done by hand?
  - If so, are those parts precisely documented?
  - Does the documentation match reality?
- Have we taught a computer to do as much as possible?
- Are we using a version control system?
- Have we documented our software environment?
- Have we saved any output that we cannot reconstruct from original data + code?
- How far back in the analysis pipeline can we go before our results are no longer (automatically) reproducible?

=======================================================

Do's and Don't's for Reproducible Research

=======================================================

Do's

- Start with good science
- Teach a computer
- Use version control
- Keep track of software environment
- Set random number generator seed
- Think about the entire pipeline

========================================================

Start with Good Science

- work on interesting problem (to you and your team)
- form coherent / focused question to simplify your problem
- collaborate with others to reinforce good practices and habits

==========================================================

Teach a Computer

- automate all tasks through scripting or programming
- code = precise instructions to process /  analyze the data
- teach the computer almost guarantees reproducibility
- download.file("url", "filename") is convenient way to download the file
  - full URL specified instead of a series of links and clicks
  - name of file specified
  - directory specified
  - code can be executed in R as long as link works
  
==========================================================

Use Version Control

- GitHub, BitBucket, Google Code, CodePlex, SourceForge
- the use helps to slow you down
  - forces you to think about changes made, commit those changes, and keep track of analyses performed 
- helps to keep track of history / snapshots
- allows reverting to old versions

===========================================================


Keep Track of Software Environment

- Some tools / datasets only work on certain software or in certain environments
  - software and computing environment are critical to reproducing analysis
  - everything should be documented
- Computer architecture: CPU (Intel, AMD, ARM), GPUs, 32 v 64 bit
- Operating system: Windows, Mac, Linux/Unix
- Software toolchain: compilers, interpreters, command shell, programming languages (C, Perl, Python, etc.), database backends, data analysis software
- Supporting software / infrastructure: Libraries, R packages, dependencies
- External dependencies: web sites, data repositories (data source), remote databases, software repositories
- Version numbers: ideally, for everything (if possible)
- Use sessionInfo() - this prints R version, OS, local and base/attached/utilized packages

=============================================================

Set Random Number Generator Seed

- random number generators produce pseudo-random numbers based on an initial seed
  set.seed() can be used to specify the seed for random generator in R
- setting seed allows for the stream of random numbers to be reproduced
- whenever you need to generate a stream for random numbers for non-trivial purposes, always set the seed

=============================================================

Think about the Entire Pipeline

- Data analysis is a lengthy process, important to ensure each piece is reproducible
  - Final product is important, but the process is just as important
- Raw data -> processed data -> analysis -> report
- The more of the pipeline is made reproducible, the more cridible the results are

=============================================================

Don't's

- Don't do things by hand
- Don't point and click
- Don't save output for convenience

=============================================================

Don't Do Things by Hand

- may lead to unreproducible results (or errors)
  - edit spreadsheets in Excel
  - remove outliers without noting criteria
  - edit tables / figures
  - validate / quality control for data
- downloading data from website (clickin on link)
  - need lengthy set of instructions to obtain the same dataset
- moving / splitting / reformatting data without record of what was done
- if necessary, document manual tasks precisely, accounting for end users with different backgrounds or from different context

===============================================================

Don't Point and Click

- GUIs make it easier to do this
  - GUIs are intuitive to use by actions are difficult to track and for others to reproduce
  - some GUIs include log files that can be used for review
- any interactive software should be carefully used to ensure all results can be reproduced
- text editors are usually ok
- when in doubt, document

================================================================

Don't Save Output for Convenience

- Avoid saving data analysis output
  - Tables, summaries, figures, processed data
- Output that is saved as stand-alone without code is not reproducible
- When data changes or error detected in parts of the analysis the output that is dependent on the original output will not be updated
- Intermediate files (processed data) are ok to save but clear and precise documentation must be created
- You should save the data + code instead of the output

================================================================
