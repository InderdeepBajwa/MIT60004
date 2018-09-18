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
> I(x(i)) = log(2)(1/p(i))

## Information Conveyed by Data ##

Even when data doesn't resolve all the uncertainty, at least some information can be useful.

Equation template:
I(data) = log(2)(1/p(data))

Example:
> I(heart) = log(2)(1/(13/52)) = 2 bits

It is satisfying to the instructor that we got 2 bits as a result. This is satisfying to an MIT person since 2 is an integer.

In this case, even though information isn't resolving all of our uncertainties, we're still able to get the result 2 bits which help us to optimize the problem or at least know how to encode this information of 2 bits.

