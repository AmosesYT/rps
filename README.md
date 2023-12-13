# rps
#rockpaperscissors!

import random

def get_user_choice():
    print('Enter your choice 1-3: ')
    print('1. Rock ✊')
    print('2. Paper ✋')
    print('3. Scissors ✌')

    user_choice = (input('Your choice: '))
    return int(user_choice)

def get_computer_choice():
    return random.randint(1,3)

def determine_winner(player,computer):
    if player == computer:
        print('Tie!')
    elif (player == 1 and computer == 3) or (player == 2 and computer == 1) or (player == 3 and computer == 2):
        return 'You win!'
    else:
        return 'You lose!'
    
def print_choices(player,computer):
    choices = {1: "Rock ✊", 2: "Paper ✋", 3: "Scissors ✌"}
    print(f'You chose {choices[player]}')
    print(f'Computer chose{choices[computer]}')

def get_choice_string(choice):
    if choice == 1:
        return "Rock"
    elif choice == 2:
        return "Paper"
    elif choice == 3:
        return "Scissors"
    else:
        return "Invalid choice"
    
def main():
    player_choice = get_user_choice()
    computer_choice = get_computer_choice()

    print_choices(player_choice, computer_choice)

    result = determine_winner(player_choice, computer_choice)
    print(result)

if __name__ == "__main__":
    main()

       

