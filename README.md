##### Return to [About Me](https://pacman715.github.io/pcabano-portfolio/)

For our final project we were tasked with building a program that allowed the user to interact with it.  My partner and I chose to build a blackjack program.

While I was able to find a good skeleton of code online, I made several modifications to make the program more true to the game.

Originally the code for the player's hand was:

```python
	while choice != "q":
		print "The dealer is showing a " + str(dealer_hand[0])
		print "You have a " + str(player_hand) + " for a total of " + str(total(player_hand))
		blackjack(dealer_hand, player_hand)
		choice = raw_input("Do you want to [H]it, [S]tand, or [Q]uit: ").lower()
		clear()
		if choice == "h":
			hit(player_hand)
			while total(dealer_hand) < 17:
				hit(dealer_hand)
			score(dealer_hand, player_hand)
			play_again()
		elif choice == "s":
			while total(dealer_hand) < 17:
				hit(dealer_hand)
			score(dealer_hand, player_hand)
			play_again()
		elif choice == "q":
			print "Bye!"
			exit()
```

In order to allow the player to hit more than one time, I modified the code as follows:

```python
#Player hand
	while total(player_hand) < 21:
		print ("The dealer is showing a " + str(dealer_hand[0]))
		print ("You have a " + str(player_hand) + " for a total of " + str(total(player_hand)))
#Hit or stand?
        choice = input("Do you want to [H]it or [S]tand: ").lower()
		if choice == 'h':
			hit(player_hand)
			clear()
		elif choice == "s":
			break
```
Please enjoy our [Python Hackathon Presentation](https://youtu.be/ddibLfuTo10)
