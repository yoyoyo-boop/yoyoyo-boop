
import random

# List of hiding locations
hiding_spots = ["under the bed", "behind the door", "in the closet", "in the attic", "in the basement"]

def play_hide_and_seek():
    print("Welcome to Hide and Seek!")
    print("Let's take turns being the hider and the seeker.")

    while True:
        seeker_name = input("\nEnter the name of the seeker: ")
        hider_name = input("Enter the name of the hider: ")

        # Randomly select a hiding spot
        hiding_spot = random.choice(hiding_spots)

        print(f"\n{hider_name} is hiding...")
        print(f"{seeker_name}, it's your turn to seek!")

        while True:
            guess = input("\nMake a guess or enter 'quit' to give up: ")

            if guess.lower() == "quit":
                print("You gave up! The hider wins!")
                break

            if guess.lower() == hiding_spot:
                print("Congratulations! You found the hider!")
                break
            else:
                print("That's not the correct hiding spot. Keep searching!")

        play_again = input("\nDo you want to play again? (yes/no): ")
        if play_again.lower() != "yes":
            break

    print("\nThank you for playing Hide and Seek!")

# Start the game
play_hide_and_seek()
