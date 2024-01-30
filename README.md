
# RLC Circuit Simulator

-SPICE Circuit simulator is a well-known modern circuit simulator that uses direct methods to simulate analog circuits at the differential equation level.

-It takes an analog circuit schematic, simulates, calculates the voltage at each node, and the current produced by each voltage source.

-This simulation engine is responsible for performing all the numerical calculations
necessary to compute the various circuit parameters (i.e. nodal voltages and voltage source
currents).

-It using backward euler to make these computations and starts at time=0

## I/O Format

-The first line contains the time step

-The second line contains number of iterations

-The next lines contain the circuit components

-Each component starts with the type:
- R for resistor
- L for inductor
- C for capacitor
- V for voltage source
- I for current source

-The 2 strings contain the 2 nodes that the component is between (V0 is always ground)

-The next value is the value of the component (ohm for resistor, farad for capacitor, ...etc)

-The final string is the initial value


## Example

-Sample input file

```txt
0.1
20
R V1 V0 1 0
C V1 V0 1 0
R V1 V2 1 0
I V2 V0 1 0
Isrc V2 V0 1 0
-1
```

-Sample output file
```txt
V1
0.1 0.081967213115
0.2 0.147809728568
0.3 0.199355893225
0.4 0.238338718464
0.5 0.266384661801
0.6 0.285006178276
0.7 0.295597483941
0.8 0.299433021633
0.9 0.297668166929
1.0 0.291341758696
1.1 0.281380083773
1.2 0.268601988201
1.3 0.253724828089
1.4 0.237371011143
1.5 0.220074915103
1.6 0.202290001708
1.7 0.184395974307
1.8 0.166705853908
1.9 0.149472872369
2.0 0.132897102708

V2
0.1 0.983606557377
0.2 0.954044611664
0.3 0.914173433019
0.4 0.866505689326
0.5 0.813228756966
0.6 0.75622752131
0.7 0.697108024522
0.8 0.637221420196
0.9 0.57768778681
1.0 0.519419435071
1.1 0.463143418316
1.2 0.409423020676
1.3 0.358678055058
1.4 0.311203852829
1.5 0.267188869809
1.6 0.226730869467
1.7 0.189851674606
1.8 0.156510503824
1.9 0.12661592935
2.0 0.100036508808

I_L0
0.1 0.098360655738
0.2 0.193765116904
0.3 0.285182460206
0.4 0.371833029138
0.5 0.453155904835
0.6 0.528778656966
0.7 0.598489459418
0.8 0.662211601438
0.9 0.719980380119
1.0 0.771922323626
1.1 0.818236665457
1.2 0.859178967525
1.3 0.895046773031
1.4 0.926167158314
1.5 0.952886045295
1.6 0.975559132241
1.7 0.994544299702
1.8 1.010195350084
1.9 1.022856943019
2.0 1.0328605939


```
