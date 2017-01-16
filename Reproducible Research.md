Reproducible Research
========================================================
author: Vicki Hertzberg
date: 18 January, 2017
autosize: true

========================================================

The keystones of science are replicability and reproducibility.

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
- take data/code and replicate findings -> validate findings
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

- Idential output down to the bit level
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

With the exception of LaTeX,
- poor integration with VCSs
- ill-suited for workflow automation (i.e., lots of cutting and pasting, with potentil for errors)

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

Process of ensuring data analysis is cear and transparent in terms of describing programs used to generate results.

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