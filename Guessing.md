# Summary
This is a number-guessing game. The chart will tell you if your guess is too low, too high, or on point. 

# Chart
```mermaid
graph TD
  A[Set Range: 1-10]--> B[Generate Random Whole Number]
  B --> C[Enter your guess as a whole number.]
  C--Guess is a decimal.-->J[Please only enter a whole number.]
  J-->C
  C --Guess is non-numeric.-->H[Please only enter a number.]
  H --> C
  C --Guess is outside of boundary values-->I[Please enter a number in the specified range.]
  I-->C
  C --Guess is correct.--> D[Correct.]
  D --> G[End Game.]
  C --Guess is too low.--> E[Incorrect. Too low. Try again.]
  E --> C
  C --Guess is too high.--> F[Incorrect. Too high. Try again.]
  F --> C
  ```
# Documentation
1. Set the range as being 1-10. This means that those are the only numbers the user can guess. 
2. Randomly generate a whole number in the range 1-10. 
3. Prompt the user for a guess.
4. If the guess is a decimal, prompt them to enter a whole number and return to the original 'guess' prompt.
5. If the guess contains non-numeric characters, prompt them to enter a number and return to the original 'guess' prompt.
6. If the guess is less than 1 or greater than 10, prompt the user to enter a number in the correct range and return to the original 'guess' prompt.
7. If the guess is too high, prompt the user to enter a lower number and return to the original 'guess' prompt.
8. If the guess is too low, prompt the user to enter a higher number and return to the original 'guess' prompt.
9. If the guess matches with the randomly generated number, tell the user they got it right and end the program. 
