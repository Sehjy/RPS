# RPS

    Started with the computerPlay function which was just using the random function to get a number        between 1 and 3 in order to determine what the computer will play in a game of RPS.

    Next made rpsResults function that takes in two inputs, one from the user and the other from the random computer function. Based on the input parameters, the function determines a win, loss, or tie for the user.
        for this function I was unsure for what to return initially or how I would track wins and losses for multiple games. I decided on using 1 for win, 0 for loss, and leaving a tie as undefined and returning these values to be used later

    Made a playGame() function that would just take user input through a prompt question and then input it into the rpsResults function. And then output a console log of the results. Has no return value

    Lastly made the game() function that will play 5 games of rps and determine a overall outcome of the games.
        Each game, regarless of individual wins or losses, was being output as a tie. My gameResult was not being updated properly because I was assigning it to playGame() in order to try to catch the result value but playGame() only outputs a console log and so each comparison in the game() function was assuming a tie because in rpsResults, I was using undefined return to indicate ties.
            Simple change was to return rpsResults in playGame() instead of returning a console.log which is an undefined type return
