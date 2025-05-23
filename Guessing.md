# Summary
This is a number-guessing game. The chart will tell you if your guess is too low, too high, or on point. 
# Chart
```mermaid
graph TD
  A[Choose Range: 1-10]--> B[Generate Random Number]
  B --> C[Enter your guess.]
  C --Guess is correct.--> D[Correct.]
  D --> G[End Game.]
  C --Guess is too low.--> E[Incorrect. Too low. Try again.]
  E --> C
  C --Guess is too high.--> F[Incorrect. Too high. Try again.]
  F --> C
