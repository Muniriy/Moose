# Moose Tournament

## Problem Statement
Moose are large quadrupedal herbivores which range in Northern longitudes from the Northern United States, Canada, Scandinavia, and Russia. They are territorial in nature and they are known for fighting when encountering each other. In this simulation, we will create a model of the environment in order to understand the nature of these creatures.

## Problem Definition
The environment in which they live is three territorial regions which we will helpfully entitle as _A_, _B_, and _C_ fields. In these fields, various vegetation grows in a sigmoid fashion given by equation

_f(X)=(10*e^x)/(1+e^x)_

You may assume that these fields start with _X=1_, i.e. _f(1)_. If a Moose is not present in the square, then the field increases _X_ by 1. If a Moose is in the field, or if two Moose are in the field, then the field’s _X_ is decreased by 1, to a minimum of 0.

Moose receive the following payouts. If there is only a single Moose in the field _k_, then he eats the vegetation based on the amount available and gains _f_k(X_k)-f(0)_. If both of the Moose are in the same field, then they will fight. Fighting is exhausting and prevents eating and damages the local area, and causes of a score of 0 to be given to both Moose.

## Task
You need to create an agent for the Moose (public class with public default constructor) implementing the interface as seen below. The interface contains:
1. a void method _reset()_ which will be called in order to ‘reset’ the agent before the match with each player containing several rounds
2. an integer method _move()_ returning the move which is given based on the last opponent move (0 – if this is the first move), and the current _X_ values for the three fields. The _move()_ method returns 1 for _A_, 2 for _B_ and 3 for _C_ fields
3. a double default _eatVegetation()_ calculating the energy gained by the Moose (should not be overridden).
      
Your agent will be tested via a tournament method. The code of this interface should not be submitted. You are NOT allowed to make any changes in the given interface. You should assume that your code should be in the package _cibcb22.moose.players_. If you require more than 1 class, use nested classes.

## Tools
Language: _Java 11_

Build automation tool: _Maven_

## Submission
1. Agent code _*.java_
2. If you need any dependencies to be used for your code, attach _dependencies.txt_ file containing all dependencies for _pom.xml_