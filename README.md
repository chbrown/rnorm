# `rnorm`

`rnorm` is a command line tool to generate numbers from the [Normal distribution](https://en.wikipedia.org/wiki/Normal_distribution).

    npm install -g rnorm
    rnorm
    > -0.211

There are options to set the mean (`--mean`) and standard deviation (`--sd`), print out multiple numbers (`--number`), and set the printed precision (`--precision`), but otherwise, that's all it does.

For example, to print out 5 IQ scores drawn from a random sample of the population:

    rnorm --mean 100 --sd 10 --number 5 --precision 0
    > 116
    > 100
    > 101
    > 108
    > 92

It uses the [Box-Muller transform](https://en.wikipedia.org/wiki/Box-Muller_transform) to convert two (independent) random numbers from the Standard Uniform distribution (`Math.random()`) to two (independent) random numbers from the Standard Normal distribution (μ = 0, σ = 1). Thus, it is more efficient to draw an even number of random numbers at a time, but the default is to print just one.


## License

Copyright 2015 Christopher Brown. [MIT Licensed](http://chbrown.github.io/licenses/MIT/#2015).
