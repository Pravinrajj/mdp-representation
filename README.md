# MDP REPRESENTATION

## AIM:
The aim of this MDP is to model the decision-making process of a person while coding, considering two levels of concentration - full concentration and half concentration, and to maximize productivity

## PROBLEM STATEMENT:

### Problem Description

#### In this scenario ,The team wants to win the football tournament,they has two choice,one is move right and reach the final win the cupand another one is move left ,get knocked from tournament.

### State Space

Knocked out ,Semi's ,Final.

### Sample State
Semi's.

### Action Space

Right , Left

### Sample Action

Right(1) and Left(0).

### Reward Function

Right= 1,Left= 0

### Graphical Representation
![image](https://github.com/Pravinrajj/mdp-representation/assets/117917674/079130a7-5224-43c2-ac43-d4097ec4abf5)

## PYTHON REPRESENTATION:
```
mdp = {
    "Final": {
         0 : [(0.7, "Semi's", 0, False),(0.3, "Final", 1, True)],
        1 : [(0.8, "Final", 1, True),(0.2, "Semi's", 0, False)]
    },
    "Semi's": {
        0 : [(0.8, "Knocked out", 0, False),(0.2, "Semi's", 0, False)],
        1 : [(0.9, "Final", 1, True),(0.1, "Semi's", 0, False)]
    },
    "Knocked out": {
        0 : [(0.8, "Knocked out", 0, False),(0.2, "Semi's", 0, False)],
        1 : [(0.7, "Semi's`", 0, False),(0.3, "Knocked out", 0.0, False)]
    }
}
```

## OUTPUT:
![image](https://github.com/Pravinrajj/mdp-representation/assets/117917674/3ac01c43-884f-4983-930b-3dd61915729d)


## RESULT:
The result of solving this MDP would be an optimal policy that tells the person which action to take in each state to maximize their productivity while coding.

