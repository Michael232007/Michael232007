flowchart TD
    Start([Start]) --> Generate[Generate Random Number]
    Generate --> Prompt[Prompt User for a Guess]
    Prompt --> UserInput{Is Input Numeric?}
    UserInput -- Yes --> CheckRange{Is Guess Within Range?}
    UserInput -- No --> InvalidInput[Display "Invalid Input"]
    InvalidInput --> Prompt

    CheckRange -- Yes --> Compare{Is Guess Correct?}
    CheckRange -- No --> OutOfRange[Display "Guess Out of Range"]
    OutOfRange --> Prompt

    Compare -- Yes --> Correct[Display "Correct! You Win!"]
    Compare -- No --> HighLow{Is Guess Too High?}
    
    HighLow -- Yes --> DisplayHigh[Display "Too High!"]
    HighLow -- No --> DisplayLow[Display "Too Low!"]
    
    DisplayHigh --> Prompt
    DisplayLow --> Prompt
    Correct --> End([End])
# Random Guessing Game Flowchart

This flowchart illustrates the sequence of events for a random guessing game. The game allows the user to guess a number selected randomly by the computer. The following steps outline the process:

1. **Start**: The game begins.
2. **Generate Random Number**: The computer generates a random number within a specified range (e.g., 1 to 100).
3. **Prompt User for a Guess**: The user is prompted to enter their guess.
4. **Is Input Numeric?**: The game checks if the input is a numeric value:
   - **Yes**: Proceed to the next step.
   - **No**: Display an "Invalid Input" message and prompt the user to guess again.
5. **Is Guess Within Range?**: The game checks if the guess falls within the valid range:
   - **Yes**: Proceed to check if the guess is correct.
   - **No**: Display "Guess Out of Range" and prompt for a new guess.
6. **Is Guess Correct?**: The game checks if the user's guess matches the random number:
   - **Yes**: Display "Correct! You Win!" and end the game.
   - **No**: Check if the guess is too high or too low.
7. **Is Guess Too High?**: Determine if the guess is too high:
   - **Yes**: Display "Too High!" and prompt for another guess.
   - **No**: Display "Too Low!" and prompt for another guess.
8. **End**: The game concludes once the user guesses the correct number.

This flowchart ensures that all possible scenarios are covered, including input validation and feedback for the user.
