# limitation-recognizer

A program to recognize self-acknowledged limitation sentences in biomedical articles

The repository contains the source code for the system described in the article [Automatic recognition of self-acknowledged limitations in clinical research literature](https://academic.oup.com/jamia/article/25/7/855/4990607). The best performing rule-based system is presented (`gov.nih.nlm.limitations.RuleBasedLimitationSentenceRecognizer`), as well as the rule-based baseline (`gov.nih.nlm.limitations.RuleBasedLimitationSentenceRecognizerBaseline`).  

## Usage 

To replicate the results, run `gov.nih.nlm.limitations.RuleBasedLimitationSentenceRecognizer` with three arguments:
- DATA/XML: directory that contains the parsed XML of the test set
- DATA/limitation\_sentences\_final.txt: gold annotations
- Output file name (after the run, this file should match DATA/rule\_based\_test.out.txt)

The parsed XML is generated from PubMed Central XML using `gov.nih.nlm.limitations.CorpusParser`. 

### Processing plain text files

To process articles in plain text, run  `gov.nih.nlm.limitations.CombinedPreprintLimitationRecognizer` with two arguments:
- Input directory: a directory of plain text files
- Output file: the file for output (output is in JSON format)

## Note on Stanford CoreNLP package

Stanford CoreNLP model jar file that is needed for processing raw text for lexical and syntactic information (`stanford-corenlp-3.3.1-models.jar`) is  not included with the distribution due to its size. It can be downloaded from  <http://stanfordnlp.github.io/CoreNLP/> and copied to `lib` directory.

## Contact

- Halil Kilicoglu:      (`halil (at) illinois.edu`)

