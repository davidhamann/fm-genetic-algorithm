# Genetic Algorithm implementation in FileMaker
This file demonstrates an easy implementation of a genetic algorithm in FileMaker and should serve as an introduction. Play around with it and see how the different settings change the evolutionary process.

##Terminology

**Genes** represent the solution data. They can be represented in a binary sequence, ascii characters or other encodings. In this file we take a list of ascii chracters.

**Individuals** (chromosomes) contain genes and make up a **population** of candidate solutions.

The fitness function is used to evaluate the "fitness" of an individual. In this example the maximum fitness (best) is zero. The fitness function is an essential part (and usually the hardest part) of any genetic algorithm since it tells you how close the given solution is to achieving the set aims or near-optimal answer.

In the evolutionary process we evolve from one generation to the next. Every new population is created by randomly selecting (**selection**) individuals from the current population, taking the ones with the best fitness and performing a **crossover** function to create an offspring (reproduction). In this demo file tournament selection is used; of course you could also implement roulette wheel selection, rank selection or other forms of selection. The **tournament selection** can be controlled by the pool size setting (larger pool size means, that weak individuals have a smaller chance to be selected).

To maintain a certain diversity **mutation** is applied to the new population. In this demo file you can control both crossover and mutation with the uniform rate and mutation rate setting.

Sometimes it can be useful to take the best individual of a population and carry it on to the next generation without undertaking the process of crossover and mutation. This setting is called **elitism** and makes sure that you don't lose the best chromosome. It also means that a good answer always remains in the population until a better one is found.

##This demo file

The code in this sample is vastly commented and should be very easy to read and also to adjust to different problems (you will always have selection, crossover, mutation). I tried to focus on the basics without adding too much complexity to make it easier to understand. Feel free to explore, tweak or destroy the algorithm :-)

For more information see the presentation slides from the dotfmp unconference, June 2015.
