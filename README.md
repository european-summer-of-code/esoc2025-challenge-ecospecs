# ESoC 2025 challenge - ecoSPECS

This repository contains trial datasets for the ecoSPECS challenge at European Summer of Code 2025, and suggested trial tasks.


### Trial datasets

#### Description of data

##### Data origin

The data were created by ecoSPECS as artificial, stylized cases for the purpose of the ESoC 2025 challenge. This means, while they correspond to no real use cases, they were created in a stylized way inspired by a larger number of real use cases, and meant to be representative for a small cross-section of cases.

The files were shared by ecoSPECS in early April 2025.

##### Files

The trial dataset can be found [here](https://github.com/european-summer-of-code/esoc2025-challenge-ecospecs/tree/main/data).

The trial dataset consists of nine `docx` (MS Word 2025) files corresponding to 3 stylized cases of clean room design, and 3 documents for each case, corresponding to the first three steps of the documentation and specification process and initial contracting.

The three steps corresponding to documents are:

* 0: coarse user requirement specification, sent by user/requestor
* 1: detail user requirement specification, typically created by an expert from 0
* 2: functional specification, typically created by an expert from 1.

The three stylized cases are called "A", "B", and "C".

The document for case X and step Y has the file name `X_Y.docx`.

##### Challenge

In a simplified version of the more complex real application, an AI should be able to:

* create document 1 from document 0
* create document 2 from document 1 (and, possibly but not necessarily, document 0)

both using potentially initial and iterative expert user prompts for refinement, example documents in internal repositories, and direct training feedback by experts to the AI.

The AI should account for documents 0 varying considerably, whereas documents 1 and 2 are meant to follow a highly standardized structure.


### Trial tasks

#### 1. parsing tables

Write python code to parse all tables in a Word or `pdf` document, producing a list-of-2D-array-like structure (one 2D array per table).

Include tests.

#### 2. filling tables using GenAI

write some python code which, using any commonly used GenAI model, does the following:

given a general prompt that the user can specify, and prescribed headers (rows, columns, or both), fills in the table in a plausible way.

Showcase your code on some use cases, and include tests.

Examples of tables you could try fill in:

[[1]](https://xkcd.com/394/) [[2]](https://xkcd.com/808/) [[3]](https://xkcd.com/1497/) [[4]](https://xkcd.com/2877/)

Bonus 1: solve this using open source GenAI models only.

Bonus 2: include the ability to generate tables from scratch, including rows and columns.

Bonus 3: add a feature to write to `doc` or `pdf` file format with a short introduction paragraph.

#### Bonus: towards a pre-prototype

Using the example documents, and possibly code from the above tasks, prepare a showcase how you would approach the problem.

This should be an indicative pre-prototype only for the purpose of explaining your general approach. Please do not spend too much time on this - especially on graphical user interfaces or productionization.

(you can publish your code under a permissive license if you want)


### License

The contents of this repository, including but not restricted to the challenge datasets, are released under the [CC BY-NC-ND 4.0 license](https://creativecommons.org/licenses/by-nc-nd/4.0/).
