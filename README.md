# Dueces-Wild-Poker
A simulator of the Deuces Wild Poker casino game and odds predictor 

/Users/michaelbinger/Downloads/IMG_6154.heic

## Summary
This code recreates the Video Poker game, Deuces Wild Poker, with the ability to project the odds of finishing with a winning hand based on your opening hand and all possible discard options. 

## Overview
The primary component of this project is the Deuces_Wild.ipynb file. This file holds the complete, functioning game.

### How the program works
The code begins with creating a "card deck." The deck is actually a list of lists. Each individual list within the deck list represents a card, and holds three items to identify the card. The first item is the card number, the second item is the card suit, and the third item is a Y/N string indicator representing whether or not the card is a wildcard (all #2 cards are wildcards). 

Note: For the sake of calculating certain winning hands, "face" cards (Jack, Queen, King) and Aces were coded in as numbers. Jack is #11, Queen is #12, King is #13, and Ace is #14. 

![Example First Dealt Hand](/Users/michaelbinger/Documents/Projects/Dueces-Wild-Poker/images/First_hand.png)

After the deck is created, the program will randomly select 5 cards from the deck list, remove them from the deck list, and add the cards to a new list which will be the first dealt hand (shown in image above). Once your hand is created, the program will run all possible options you have to create a winning hand based on your first dealt hand and all possible final hands depending on which cards you choose to discard. It will display the best discard options in order to produce a winning hand in a pandas dataframe (shown below). 

[insert photo of odds dataframe]

You will then be prompted to choose which cards from your first dealt hand you would like to discard. You can choose no cards, or any combination of the cards in your first hand. Discarded cards are identified by their position in the hand. In order to discard a card, you enter in the position number associated with the card. The program will display the cards next to their associated position number. 

[insert photo of hand with position numbers]

After choosing your discard options, the program will pull the appropriate number of cards at random from the remaining cards in the deck to ensure your final hand has 5 cards. Once your final hand is assigned, the program will determine if your final hand is a winning hand. The final output will display your original hand, the cards you discarded, your final hand, and the result of your final hand. 

[insert photo of final output]

To play a new hand, simply restart the program.

### Additional components
The winning odds are displayed by filtering an imported CSV which has been converted into a dataframe. This CSV contains all possible hands from a standard 52 card deck, as well as what the result of that hand would be if it were your final hand. The code used to create this CSV and the CSV itself are saved in a separate folder, as the files were too large to upload to Github in the standard fashion. 





