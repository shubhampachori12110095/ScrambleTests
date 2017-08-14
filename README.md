# ScrambleTests
Codebase to 
1. Train classifiers on pairs of InferSent embedded sentences to predict NLI labels
2. Test its performance on a new Scrambled dataset

## Instructions ##
### Getting data ###
In the Downloads folder, run:
`./get_data.bash`

### Run-through with toy ###
Run: `python main.py`, with `toy = True`.
This should run through training the classifier and test code on toy data sets (provided).

Setting it False will run the true classifier and take a long time, and very high memory for embeddings.

### Analysing tests ###
The logistic regression models (in ./models/) as well as their outputs on the true scramble-test results (in ./regout/) are provided.
So you can run the tests directly.

Running AnalyseTests.ipynb will produce the plots (inline as well as in ./figures/), as well as display high-margin BOW misclassifications (inline).
In AnalyseTest, setting `Scram = True` runs tests for Scramble test data, `Scram = False` runs it for te SNLI test and/or dev sets.
