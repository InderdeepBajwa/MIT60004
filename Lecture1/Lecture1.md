# Introduction #
In this course lecture series 6.004, you will learn about computer structures from the core of the earth to the moon. As the instructor says in the first lecture, you'll learn (sort of) full stack development from atoms to the amazon. By this, he means you'll learn from the basic operators found in computers that calculate 0s and 1s, to the way today's cloud computing works (which in this case is referred to Amazon Web Services, AWS.)

## Atoms to Amazon - Preview ##

A rough outline the instructor shows in his lecture of going underneath the hood from the building blocks/components to engine and finally to the car is:

Insulators/Conductors/Semiconductors -->
    Lumped Component model -->
        Bits, Logic Gates -->
            Instruction set + memory -->
                Programming Languages -->
                    Virtual Machines -->
                        Cloud

## What is information? ##

Information, _n._ Data communicated or received that resolves uncertainty about a particular fact or circumstance.

According to the instructor, information is a way of measuring something, such as a unit of measurement. Information is expected to resolve an uncertainty. Another way of thinking this might be if you're not sure whether drinking a lot of water is healthy to your body or not. Here, an information could be a research published by a University that proves drinking a limited water but more frequently might be good for your body.

In the above discussion on water, the University's research should be enough to resolve the uncertainty in your mind on whether drinking more water will be beneficial.

An example that the instructor gives is:

> You have a deck of cards (52 total cards). If he asks you to locate a card with the given set of information, what would we analyze?
>> **A card contains a heart**: In this case, we've narrowed down to 13 cards since only **13** cards exists that have a heart symbol on them.

>> **A card is not Ace of spades**: In this case, we're left with **51** choices, removing 1 card (Ace of spades).

>> **A card is a face card (Jack, Queen, King)**: In this case, we're left with **12** cards

>> **A card is the "suicide king"**: This leaves **1** card. According to the instructor, suicide king is the King card with hearts.

> HERE, the least information is provided by 'A card is not Ace of spades' rendering us with 51 cards while most information is provided by 'A card is the suicide king' leaving us with just 1 card.


## Quantifying Information ##

Given discrete random variable X

1. N possible values: x1, x2, ...., xN.
2. Associated probabilities: p1, p2, ...., pN.

Information received when learning that choice was xi:
> _I_(x(i)) = log(2)(1/p(i))

## Information Conveyed by Data ##

Even when data doesn't resolve all the uncertainty, at least some information can be useful.

Equation template:
_I_(data) = log(2)(1/p(data))

Example:
> _I_(heart) = log(2)(1/(13/52)) = 2 bits

It is satisfying to the instructor that we got 2 bits as a result. This is satisfying to an MIT person since 2 is an integer.

In this case, even though information isn't resolving all of our uncertainties, we're still able to get the result 2 bits which help us to optimize the problem or at least know how to encode this information of 2 bits.

### Common case ###

Suppose you've faced with N equally probable choices, and you received data that narrows it down to M choices. The probability that data would be sent is M.(1/N) so the amount of information you have received is:
> _I_(data) = log(2)(1/(M.(1/N))) = log(2)(N/M)

## Example of Information Content ##

1. Informaiton in one coin flip:
     N = |   M =   |   Informaiton content =
      ----| ------- | -----------------------
      2   | 1   |       log(2)(2/1) = 1bit
2. Card drawn from a fresh deck is a heart:
     N = |   M =   |   Informaiton content =
      ----| ------- | -----------------------
      52   | 13   |       log(2)(52/3) = 2 bit

3. roll of 2 dice:
     N = |   M =   |   Informaiton content =
      ----| ------- | -----------------------
      36   | 1   |       log(2)36/1) = 5.17 bit

      Ooh! In the third case, it's not an integer. The .17 in the result here signifies: if we need to send thousands of messages (or more), we can find some more efficient coding that takes advantage of economies of scale.

## Entropy ##

In information theory, the _entropy_ H(X) is the average amount of informaiton contained in each piece of data received about the value of X:

>   _H(X) = E(I(X))_ = Sum(probability of occurance, p[i]).log(2)(1/(p[i]))

Example: X = {A, B, C, D}

_The following are some bogus values_

choice[i]   |   p[i]    |   log(2)(1/p[i])
----------- | --------- | ------------------
A   |   1/3 |   1.58 bits
B   |   1/2 |   1 bit
C   |   1/12 |   3.58 bits
D   |   1/12 |   3.58 bits

Entropy for the above case is:
> _H(X) = (1/3)(1.58) + (1/2)(1) + 2(1/12)(3.58) = **1.626 bits**


## Meaning of Entropy ##

If we're given a data sequence describing the values of some random variable X.

Let variable bitsTransmitted = Average Number of bits used to transmit an information

if (bitsTransmitted < H(X))
> then it isn't good

if (bitsTransmitted > H(X))
> then it's okay but inefficient

if (bitsTransmitted == H(X))
> then it's PERFECT!!!

## Encodings ##

An encoding is an unambigous mapping between bit strings and the set of possible data.

// Needs revisions

_Watch L01 Spring 2016 at 25:38 for examples_

### Encoding as Binary Trees ###

// Needs revision

It is helpful to represent an unambigous encoding as a binary tree with the symbols to be encoded as the leaves. The labels on the path from the root to the leaf gives the encoding for that leaf.

