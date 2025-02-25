# Analog integer arithmetic

## Addition and subtraction

TODO

## Comparisons

### Basic analog equality

A circuit to check for equality between two analog signals:

![image](eq2.png)

The pink OR gate is in max value mode. The other OR gates are in add mode. The AND gate is in add mode. This will work for positive and negative analog values. It will output an analog value of 100% if the values are equal, 0% otherwise.

### Inf direction combiner equality

A more efficient equality checker can be built with a direction combiner and an input of `-inf`:

![image](eq1.png)

The pink direction combiner is in angleify mode, the others in combine mode. It will output a digitally on signal with an analog value of 100% if the values are equal, 0% and digitally off otherwise.

## Multiplication

TODO

## Division

16-bit analog divider:

![image](div1.png)

The top output is the quotient. The bottom output is the remainder. This design can be adapted for any word size up to 24 bits. Ensure the AND gate with the battery at the bottom is outputting a value of 1 for the word size you're using. In this example, the word size is 16 bits so a value of 2<sup>-16</sup> is needed, which is equal to 0.25<sup>8</sup> hence the 8 inputs into the AND gate.

A more efficiency design could be built using direction combiners.

## Arbitrary bitshifting

TODO
