# nlp_w_pytorch_zhongyu-pan

This is my own work for the LinkedIn Course,
_Natural Language Processing with PyTorch_,
taugh by Zhongyou Pan. The URL for the course is

https://www.linkedin.com/learning/natural-language-processing-with-pytorch/ 
`#popular-topics-in-nlp`

## Fun Extras (Most for Later)

### AI Coding Helped (LLM)

To make this course interesting, I'm using the AI Coding
Helper that Google CoLab provides. I think that means
it's CoPilot, but it might just be some version of
Gemini (which was BERT, before). That teaches me some
prompt engineering, which I'll attempt to show (in cells
that you can minimize).

### Network visualizations

I want to visualize the network I'll build, as well as
some other networks I'll discuss


## NLP topics and their Jupyter Notebooks

` --- information coming --- `

## Coding with an AI Helper and Prompt Engineering.

Here will be something like the way I show my attempts,
their output, and (when necessary) the things I had
to change to match what was in the Notebooks shared by
Zhongyou Pan in her lesson notebooks.

` --- information coming --- `


# The Main Project - a CNN for Text Classification


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
