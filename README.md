# Use Googles Syntaxnet pretrained with English model

## How to use:
    echo "Hello , how are you ?" | docker run -i --rm malakhov/syntaxnet-english > out.txt
    cat out.txt

Result:

    Input: Jag vill byta abonnemang till mer data imorgon
    Parse:
    vill NN ROOT
    +-- Jag NNP nsubj
    +-- abonnemang NNP dobj
    |   +-- byta NNP nn
    +-- till IN prep
        +-- imorgon NN pobj
            +-- mer NN amod
            +-- fron NN nn
            |   +-- data NNS nn
            +-- och NN amod
            +-- med VBN amod

## To switch language
Just look at the dockerfile and replace English to any of the supported languages. 
