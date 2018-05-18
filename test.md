# Table of Contents
1. [Example](#example)
2. [Example2](#example2)
3. [Third Example](#third-example)
4. [4](#how-to)

# Example
blablabla

How to

a*b

a**b

a'*'b



## Example2
## Third Example

sdsd


sddsa


d


dsds
# How to

The NAXOS AKE protocol uses a mathematical group G and two hash functions, H1: {0,1}\* -> Zq
and H2: {0,1}\* -> {0,1}<sup>λ</sup> (for some constant λ). A long-term secret key of a party A is an exponent

All numbers in the key exchange functions are represented in arrays of chars.

* selectCurve: selects the NIST curve and the length of the key
* privateKey: calculates the private key pk from the secret key sk: pkA=g\*skA and pkB=g\*skB
* randomGen: generates random numbers based on unix-like /dev/urandom device (used in calculateXY)
* calculateXY: calculates X=g`*`H(eskA,skA) and Y=g`*`H(eskB,skB)
* calculateKa: calculates the key for user A Ka=H(Y`*`skA, pkB`*`H(eskA,skA), Y`*`H(eskA,skA), A, B)
* calculateKb: calculates the key for user B Kb=H(pkA`*`H(eskB,skB), X`*`skB, X`*`H(eskB,skB), A, B)
