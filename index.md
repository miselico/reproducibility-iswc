
**This is borrowed from the SIGMOD replroducibility effort. We are still working on adapting this for ISWC.**

### What is SIGMOD Reproducibility?

SIGMOD Reproducibility has three goals:

- Highlight the impact of database research papers.
- Enable easy dissemination of research results.
- Enable easy sharing of code and experimentation set-ups.

In short, the goal is to assist in building a culture where sharing *results*, *code*, and *scripts* of database research is the norm rather than an exception. The challenge is to do this efficiently, which means building technical expertise on how to better research via creating repeatable and shareable research. The [SIGMOD Reproducibility committee](http://db-reproducibility.seas.harvard.edu/#Committee) is here to help you with this.

---
<br/><br/>

### Why should I be part of this?

You will be making it easy for other researchers to compare with your work, to adopt and extend your research. This instantly means more recognition for your work and higher impact.

Taking part in the SIGMOD Reproducibility process enables your paper to take the **ACM Results Replicated** label. This is embedded in the PDF of your paper in the ACM digital library.

There is an option to also host your data, scripts and code in the ACM digital library as well to make them available to a broad audience, which will award the **ACM Artifacts Available** label.

##### <span style="color:#4952D8">ACM Results Replicated label</span>

*The experimental results of the paper were replicated by the committee and where found to support the central results reported in the paper*

##### <span style="color:#5EB773">ACM Results Replicated label</span>

*The experiments (data, code, scripts) are made available to the community*

> Both the "ACM Results Replicated label" and the "ACM Artifacts Available label" are visible in the **ACM digital library**.

Successful papers will be advertised at DBworld and the list of award winners will be maintained at [sigmod.org](https://sigmod.org). In addition, the official SIGMOD Reproducibility website [maintains and advertises your papers](http://db-reproducibility.seas.harvard.edu/papers), serving as a centralized location where researchers will be able to find all the experimentation material of shareable SIGMOD papers. We will continue to enhance the functionality and material on this website to make it attractive and useful for the community, so stop by often!

---
<br/><br/>

### ACM SIGMOD Most Reproducible Paper award
This is a new award that recognizes the best papers in terms of reproducibility. The [three most reproducible papers](http://db-reproducibility.seas.harvard.edu/awards/) are picked every year and the awards are presented during the awards session of the SIGMOD conference (next year). Each award comes with a 750$ honorarium sponsored IBM. The criteria are as follows:
- Replicability (ideal: all results can be verified)
- Ease of Replicability (ideal: just works)
- Portability (ideal: linux, mac, windows)
- Reproducibility (ideal: can change workloads, queries, data and get similar behavior with published results)

The awards are selected by the Reproducibility Awards Committee, chaired by Dennis Shasha. The committee is formed after all submissions are received so that there are no conflicts. Decisions are made based on scores that reviewers assign to each paper for all factors described above.

---
<br/><br/>

### How much overhead is it?
At first, making research shareable seems like an extra overhead for authors. You just had your paper accepted in a major conference; why should you spend more time on it? The answer is to have more impact!

If you ask any experienced researcher in academia or in industry, they will tell you that they in fact already follow the reproducibility principles on a daily basis! Not as an afterthought, but as a way of doing good research.

Maintaining easily reproducible experiments, simply makes working on hard problems much easier by being able to repeat your analysis for different data sets, different hardware, different parameters, etc. Like other leading systems designers, you will save significant amounts of time because you will minimize the set up and tuning effort for your experiments. In addition, such practices will help bring new students up to speed after a project has a lain dormant for a few months.

*Ideally reproducibility should be close to zero effort*

---
<br/><br/>

### Criteria and process

##### Availability
Each submitted experiment should contain: (1) A prototype system provided as a white box (source, configuration files, building environment) or a black-box system fully specified. (2) Input Data: Either the process to generate the input should be made available, or when the data is not generated, the actual data itself or a link to the data should be provided. (3) The set of experiments (system configuration and initialization, scripts, workload, measurement protocol) used to produce the raw experimental data. (4) The scripts needed to transform the raw data into the graphs included in the paper.

##### Replicability
The central results and claims of the paper should be supported by the submitted experiments, meaning we can recreate result data and graphs that demonstrate similar behavior with that shown in the paper. Typically when the results are about response times, the exact number will depend on the underlying hardware. We do not expect to get identical results with the paper unless it happens that we get access to identical hardware. Instead, what we expect to see is that the overall behavior matches the conclusions drown in the paper, e.g., that a given algorithm is significantly faster than another one, or that a given parameter affects negatively or positively the behavior of the system.

##### Reproducibility
One important characteristic of strong research results is how flexible and robust they are in terms of the parameters and the tested environment. For example, testing a new algorithm for several input data distributions, workload characteristics and even hardware with diverse properties provides a complete picture of the properties of the algorithm. Of course, a single paper cannot always cover the whole space of possible scenarios. Typically, the opposite is true. For this reason, we expect authors to provide a short description as part of their submission about different experiments that one could do to test their work on top of what already exists in the paper. Ideally, the scripts provided should enable such functionality so that reviewers can test these case. This would allow reviewers to argue about how “reproducible” the results of the paper are under different conditions. Reproducibility is not mandatory for getting the ACM Replicability and Availability labels. It is though the ultimate goal of this effort and is an essential criteria for the Most Reproducible Paper Award.

We do not expect the authors to perform any additional experiments on top of the ones in the paper. Any additional experiments submitted will be considered and tested but they are not required. As long as the flexibility report shows that there is a *reasonable* set of existing experiments, then a paper meets the flexibility criteria. What reasonable means will be judged on a case by case basis based on the topic of each paper and in practice all accepted papers in top database conferences meet this criteria. You should see the flexibility report mainly as a way to describe the design space covered by the paper and the design space which is interesting to cover in the future for further analysis that may inspire others to work on open problems triggered by your work.

##### Process
Each paper is reviewed by one database group. The process happens in communication with the reviewers so that authors and reviewers can iron out any technical issues that arise. The end result is a short report which describes the result of the process. For successful papers the report will be hosted in the ACM digital library along with the data and code.

The goal of the committee is to properly assess and promote database research! While we expect that authors try as best as possible to prepare a submission that works out of the box, we know that sometimes unexpected problems appear and that in certain cases experiments are very hard to fully automate. The committee will not dismiss submissions if something does not work out of the box; instead, they will contact the authors to get their input on how to properly evaluate their work.

---
<br/><br/>
### Packaging Guidelines
Every case is slightly different. Sometimes the reproducibility committee can simply rerun software (e.g., rerun some existing benchmark). At other times, obtaining raw data may require special hardware (e.g., sensors in the arctic). In the latter case, the committee will not be able to reproduce the acquisition of raw data, but then you can provide the committee with a protocol, including detailed procedures for system set-up, experiment set-up, and measurements.

Whenever raw data acquisition can be produced, the following information should be provided.

##### Environment
Authors should explicitly specify the OS and tools that should be installed as the environment. Such specification should include dependencies with specific hardware features (e.g., 25 GB of RAM are needed) or dependencies within the environment (e.g., the compiler that should be used must be run with a specific version of the OS).

##### System
System setup is one of the most challenging aspects when repeating experiments. System setup will be easier to conduct if it is automatic rather than manual. Authors should test that the system they distribute can actually be installed in a new environment. The documentation should detail every step in system setup:

- How to obtain the system?
- How to configure the environment if need be (e.g., environment variables, paths)?
- How to compile the system? (existing compilation options should be mentioned)
- How to use the system? (What are the configuration options and parameters to the system?)
- How to make sure that the system is installed correctly?

The above tasks should be achieved by executing a set o scripts provided by the authors that will download needed components (systems, libraries), initialize the environment, check that software and hardware is compatible, and deploy the system.

##### Tools
The committee strongly suggests using [ReproZip](http://vida-nyu.github.io/reprozip/) to streamline this process. ReproZip can be used to capture the environment, the input files, the expected output files, and the required libraries. A detailed how-to guide (installing, packing experiments, unpacking experiments) can be found in the [ReproZip Documentation](http://reprozip.readthedocs.org/en/). ReproZip will help both the authors and the evaluators to seamlessly rerun experiments. If using ReproZip to capture the experiments proves to be difficult for a particular paper, the committee will work with the authors to find the proper solution based on the specifics of the paper and the environment needed. More tools are available here: https://reproduciblescience.org/reproducibility-directory/

##### Experiments
Given a system, the authors should provide the complete set of experiments to reproduce the paper's results. Typically, each experiment will consist of the following parts.

1. A setup phase where parameters are configured and data is loaded.
2. A running phase where a workload is applied and measurements are taken.
3. A clean-up phase where the system is prepared to avoid interference with the next round of experiments.

The authors should document (i) **how to perform the setup**, running and clean-up phases, and (ii) **how to check** that these phases complete as they should. The authors should document the expected effect of the setup phase (e.g., a cold file cache is enforced) and the different steps of the running phase, e.g., by documenting the combination of command line options used to run a given experiment script.

Experiments should be automatic, e.g., via a script that takes a range of values for each experiment parameter as arguments, rather than manual, e.g., via a script that must be edited so that a constant takes the value of a given experiment parameter.

##### Graphs and Plots
For each graph in the paper, the authors should describe how the graph is obtained from the experimental measurements. The submission should contain the scripts (or spreadsheets) that are used to generate the graphs. We strongly encourage authors to provide scripts for all their graphs using a tool such as Gnuplot or Matplotlib. Here are two useful tutorials for Gnuplot: [a brief manual and tutorial](http://people.duke.edu/~hpgavin/gnuplot.html), [and a tutorial with details about creating eps figures and embed them using LaTeX](http://www.gnuplot.info/docs/tutorial.pdf) and another two for Matplotlib: [examples from SciPy](http://wiki.scipy.org/Cookbook/Matplotlib/), and [a step-by-step tutorial discussing many features](http://www.labri.fr/perso/nrougier/teaching/matplotlib/).

##### Ideal Reproducibility Submission
At a minimum the authors should provide a complete set of scripts to install the system, produce the data, run experiments and produce the resulting graphs along with a detailed Readme file that describes the process step by step so it can be easily reproduced by a reviewer.

The ideal reproducibility submission consists of a master script that:

1. installs all systems needed,
2. generates or fetches all needed input data,
3. reruns all experiments and generates all results,
4. generates all graphs and plots, and finally,
5. recompiles the sources of the paper

... to produce a new PDF for the paper that contains the new graphs. It is possible!

---
<br/><br/>
### How and When to Submit
All authors of research papers in SIGMOD 2018 are invited to submit an entry by **August 15**!

The material needed for the reproducibility will be submitted at [the CMT website](https://cmt3.research.microsoft.com/SIGMODRepro2019). The submission at the CMT should contain a PDF with at least the following information: (1) a link to download the code, data, and scripts; and (2) a step by step description on how to use the scripts for (a) code compilation, (b) data generation, and (c) repeating the paper experiments. In addition, please include a link to the the ACM digital library page for the paper and a detailed description of the hardware used. A readme template can be found [here](http://db-reproducibility.seas.harvard.edu/docs/readme.txt).

---
<br/><br/>
### Best Practices
A good source of dos and don’ts can be found in the [ICDE 2008 tutorial by Ioana Manolescu and Stefan Manegold](http://pages.saclay.inria.fr/ioana.manolescu/SLIDES/ManolescuManegoldICDE2008.pdf) (and a subsequent [EDBT 2009 tutorial](https://hal.archives-ouvertes.fr/file/index/docid/431423/filename/Tutorial.pdf)).

They include a road-map of tips and tricks on how to organize and present code that performs experiments, so that an outsider can repeat them. In addition, the ICDE 2008 tutorial discusses good practices on experiment design more generally, addressing, for example, how to chose which parameters to vary and in what domain.

A discussion about reproducibility in research including guidelines and a review of existing tools can be found in the [SIGMOD 2012 tutorial by Juliana Freire, Philippe Bonnet, and Dennis Shasha](http://dl.acm.org/citation.cfm?id=2213908).

---
<br/><br/>
### Reproducibility Committee


---
<br/>
<th align="center">[Copyright © 2015-2018 DASlab, Harvard SEAS. All Rights Reserved.](http://daslab.seas.harvard.edu/)</th>
