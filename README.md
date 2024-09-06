# nlp_w_pytorch_zhongyu-pan

# The Main Project - a CNN for Text Classification

## The Course

This is my own work for the LinkedIn Course,
_Natural Language Processing with PyTorch_,
taugh by Zhongyou Pan. The URL for the course is

https://www.linkedin.com/learning/natural-language-processing-with-pytorch/

I had some nice motivation for this, which you can learn about in the
[Extra motivation](#Extra-motivation) section.

## The Project aka My Starting Point

A good, quick synopsis is the one that will follow - some notes I wrote
while watching the first lecture.

> We use PyTorch and a Convolutional Neural Network (using NLP features
> rather than the pixel position features we use with image processing) to 
> do our text classification.
>
> `Input -> Convolution -> Pooling -> ... -> Fully-connected layer -> Output`
>
> 
> We are also learning about RNNs. RNN doesn't only pass data forward, but also
> feeds the data back into itself. CNN only goes forward. RNN can remember
> context before and after words in a sequence. It's usually slower that a CNN.


(I guess I can use the chevron quotes to quote my notes. Well, I did.)

## Navigation - Get the Notebook from Different Places for Different Uses

### (Navigation for the main presentation notebook)

[Google CoLab on my Google Drive](https://colab.research.google.com/drive/1PKkdbNcqUfV0sHCosWZf3JdF6F3kGoj7?usp=sharing) - 
A place to see all inputs 
and outputs for the notebook, though you can't edit it without re-saving it.

<br/>

[GitHub Repo](#https://github.com/bballdave025/nlp_w_pytorch_zhongyu-pan) - 
Code repository: a place to see the latest changes as well as the Jupyter 
Notebooks completed on my way to the current version.

<br/>

[GitHub Notebook File (link to be put in, soon)](#) - I don't think this
is as useful as the repo, but you can see the IPYNB file placeholder. 
This file will only have input - I scrub the output before committing
any updates, because it's easier to do `diff`s (see changes in code)
on Jupyter Notebooks when you don't have the outputs.

<br/>

[On MyBinder (link to be put in, soon)](#) - A place to interact with 
the notebook, where you'll be led to the notebook without output and can
run the code and see the results yourself.<br/>
A note, [MyBinder](https://mybinder.org) is a great online project 
which allows you to interactively run a Jupyter notebook, completely 
online. It's nice to have when you'd like to play with code and better 
see the outputs that come from running that code. I've had some 
problems with images going down, but I'm going to work to keep 
this one up and running for access.

## Fun Extras

### AI Coding Help (LLM)

To make this course interesting, I'm using the AI Coding
Helper that Google CoLab provides. <strike>I think that means
it's CoPilot, but it might just be some version of
Gemini (which was BERT, before).</strike> All I found
was a 
[warning page](https://support.google.com/legal/answer/13505487) 
([archived](https://web.archive.org/web/20240824034012/https://support.google.com/legal/answer/13505487))
which had the words, "Generative Code Assistance".
Using it has taught me some 
prompt engineering. I have different notebooks for that. My plan
is to put them in Google CoLab notebooks to allow easy viewing,
though I might also put them in a folder with other/previous
versions. <strike>I'll attempt to show it (in cells
that you can minimize).</strike> I don't know hoe it will
be organized.

The main notebooks might show a few cells where things are
shown, but probably not too many.

### Network visualizations

<b>&lt;not-priority&gt;</b>

I want to visualize the network I'll build, as well as
some other networks I'll discuss

<b>&lt;/not-priority&gt;</b>

## NLP topics and their Jupyter Notebooks

<b>&lt;not-priority&gt;</b>

` --- information coming --- `

<b>&lt;/not-priority&gt;</b>


## Coding with an AI Helper and Prompt Engineering.

This is discussed in the AI Coding Help section, above.
But there's useful stuff here.
Here will be something like the way I show my attempts,
their output, and (when necessary) the things I had
to change to match what was in the Notebooks shared by
Zhongyou Pan in her lesson notebooks.
This will be in other notebooks, probably found
most conspicuously as CoLab notebooks in my
Google Drive.

` --- information coming --- `


## Extra motivation

I'm glad I found this course because of the project. I bungled
an interview question that was something like

> <i>You have a bunch of text strings, let's say they're a</i>
> <i>sentence long. Your goal is to output `Yes` or `No`</i>
> <i>depending on some criteria that doesn't matter for the</i>
> <i>question.</i>
>
> <i>How would you go about doing so, using machine learning?</i>

I had just finished doing a big review of Neural Networks.
My response was something like
I started by saying I'd use some kind of text vectorization
for words, and perhaps even n-grams and the complete
sentences.

When asked how I would classify the strings as `Yes` or `No`
after I got these numbers,
I went on about getting the vectorized numbers and putting
them into some kind of shallow neural network. When asked
for _more_ details, my first response was that I'd use a simple,
feedforward network with backpropagation (gradient descent).
I didn't mention any loss function or optimizer - Adam with 
binary cross entropy is always a good thing to say for that
subject. I said that the input should have the
size of the number of elements in each (e.g. `word2vec`)
vector, i.e. its dimension. I also noted that the size of the
output should be 1, and that could have a value of 0 or 1
(or maybe something in between, if we weren't using the 
perceptron activation. For hidden layers, I said that
perhaps 3 layers of size 8 each (or perhaps different numbers
close to 8) should be good, and I'd just fully connect them, 
creating dense layers.

I should have just said that I'd feed the numbers into a 
Support Vector Machine or even a decision tree (maybe dropping
the `XGBoost` implementation's name).

With this project, I will have an answer if that question
comes up on another interview. We'll have to wait and see
until after I finish the course to know exactly what it is.
