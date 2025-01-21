# Maham_Butt_Continous_Game_Play
# Maham Butt- RPG Continous Game Play
# 20th January,2025
# A text-based adventure game with multiple events and decisions.

def display_menu():
    """Displays the game menu and returns the user's choice"""
    print("1. Explore the forest")
    print("2. Check inventory")
    print("3. Talk to a character")
    print("4. Look for treasure")
    print("5. Battle an enemy")
    print("6. Visit the village")
    print("7. Rest at camp")
    print("8. Encounter random event")
    print("9. Go fishing")
    print("10. Explore a hidden cave")
    print("11. Discover a waterfall")
    print("12. Encounter a merchant")
    print("13. Find a magical creature")
    print("14. Encounter a band of thieves")
    print("15.Solve a riddle")
    print("16. Find an ancient ruin")
    print("17. Meet a talking animal")
    print("18. Receive a mysterious letter")
    print("19. Discover a secret passage")
    print("20. Face a dragon")
    print("21. Find a healing herb")
    print("22. Encounter a giant spider")
    print("23. Visit the old library")
    print("24. Cross a dangerous bridge")
    print("25. Meet a wise old man")
    print("26. Find a buried treasure chest")
    print("27. Discover an old friend")
    print("28. Ride a mystical beast")
    print("29. Witness a meteor shower")
    print("30. Open a locked chest")
    print("31. Quit")
    
    #Loop for valid input
    while True:
        try:
            choice = int(input("Choose an action(1-31):"))
            if 1 <= choice <= 31:
                return choice
            else:
                print("Invalid choice.Please select a number between 1 and 31")
        except ValueError:
            print("Invalid input. Please enter a valid number.")
       
def explore_forest(inventory):
    """Simulates exploring the forest."""
    print("You venture into the forest and discover a hidden path!")
    print("You can either (1) follow the path, (2)pick berries, or (3) return the clearing.")
    
    #Loop for valid input
    while True:
        try:
            choice = int(input("Choose an action (1-3):"))
            if choice == 1:
                print("You follow the path and find a magical spring!")
                inventory.append("magical spring water")    #Event 1
                break
            elif choice == 2:
                print("You pick some delicious berries!")
                inventory.append("berries")    #Event 2
                break
            elif choice == 3:
                print("You return to the clearing safely")
                break
            else:
                print("Invalid choice.Please select a number between 1 and 3.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")
            
def check_inventory(inventory):
    """Displays the current inventory."""
    if inventory:
        print("Your inventory contains: "+",".join(inventory))   #Event 3
    else:
        print("Your inventory is empty.")
        
def talk_to_character():
    """Simulates talking to a character."""
    print("You approach a mysterious figure")
    print("They offer you a quest. Do you(1) accept or (2) decline?")
    
    #Loop for valid input
    while True:
        try:
            choice = int(input("Choose an action (1-2):"))
            if choice == 1:
                print("You accepted the quest! Good luck!")   #Event 4
                break
            elif choice == 2:
                print("You declined the quest and walked away.")     #Event 5
                break
            else:
                print("Invalid choice.Please select a number between 1 and 2.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")
            
def look_for_treasure(inventory):
    """Simulates looking for treasure."""
    print("You search the area and find a shiny gold coin!")
    inventory.append("gold coin")     #Event 6
    
def battle_enemy():
    """Simulates a battle with an enemy."""
    print("A wild goblin appears! Prepare for battle!")
    
       # Loop for valid input
    while True:
        try:
            action = int(input("Do you want to (1) Fight or (2) Run away? "))
            if action == 1:
                print("You bravely fight the goblin and win!")  # Event 7
                break
            elif action == 2:
                print("You successfully escape the goblin!")  # Event 8
                break
            else:
                print("Invalid action. Please select 1 or 2.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")
                                          
def visit_village(inventory):
    """Simulates visiting the village"""
    print("You arrive at a bustling village.")
    print("You can (1) buy supplies, (2) talk to the villagers, or (3) leave.")
    
     # Loop for valid input
    while True:
        try:
            choice = int(input("Choose an action (1-3): "))
            if choice == 1:
                print("You buy a health potion.")  # Event 10
                inventory.append("health potion")
                break
            elif choice == 2:
                print("The villagers tell you about a dragon in the mountains!")  # Event 11
                break
            elif choice == 3:
                print("You leave the village and head back to the forest.")  # Event 12
                break
            else:
                print("Invalid choice. Please select 1, 2, or 3.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")

def rest_at_camp():
    """Simulates resting at a camp."""
    print("You set up camp and rest for a while.")
    print("You regain some health and feel refreshed!")   #Event 13
    
    def enounter_random_event():
        """Simulates a random event."""
        print("A mysterious event occurs!")
        events = [
            "You find an ancient artifact",   #Event 14
            "A storm approaches, forcing you to seek shelter",   #Event 15
            "You encounter a friendly traveler who shares their story",     #Event 16
            "You discover a hidden cave",    #Event 17
            "A wild animal crosses your path",    #Event 18
            "You feel a magical presence nearby"     #Event 19
        ]
    event = random.choice(events)
    print(f"Event: {event}")
    
def go_fishing(inventory):
    """Simulates fishing in a nearby stream"""
    print("You cast your line into the stream.")
    if random.random() <0.5:
        print("You catch a fish!")    #Event 20 
        inventory.append("fish")
    else:
        print("You wait for a while but don't catch anything.")     #Event 21
        
def explore_cave(inventory):
    """Explores a hidden cave"""
    print("You find a hidden cave and venture inside.")
    print("You can (1) explore deeper or (2) leave.")
    
       # Loop for valid input
    while True:
        try:
            choice = int(input("Choose an action (1-2): "))
            if choice == 1:
                print("You explore deeper and find a treasure chest!")  # Event 22
                inventory.append("treasure chest")
                break
            elif choice == 2:
                print("You leave the cave safely.")  # Event 23
                break
            else:
                print("Invalid choice. Please select 1 or 2.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")

def discover_waterfall():
    """Discover a waterfall in the forest."""
    print("You find a beautiful waterfall.")
    print("You can(1) take a swim or (2) rest by the waterfall.")
    
      # Loop for valid input
    while True:
        try:
            choice = int(input("Choose an action (1-2): "))
            if choice == 1:
                print("You take a refreshing swim and feel invigorated!")  # Event 24
                break
            elif choice == 2:
                print("You rest by the waterfall and enjoy the peaceful surroundings.")  # Event 25
                break
            else:
                print("Invalid choice. Please select 1 or 2.")
        except ValueError:
              print("Invalid input. Please enter a valid number.")
              
def encounter_merchant(inventory):
    """Encounter a traveling merchant."""
    print("A traveling merchant approaches. They offer to trade.")
    print("They have (1) potions, (2) weapons, or (3) food.")
    
    # Loop for valid input
    while True:
        try:
            choice = int(input("Choose an option (1-3): "))
            if choice == 1:
                print("You buy a health potion from the merchant.")  # Event 26
                inventory.append("health potion")
                break
            elif choice == 2:
                print("You buy a sword!")  # Event 27
                inventory.append("sword")
                break
            elif choice == 3:
                print("You buy some dried meat.")  # Event 28
                inventory.append("dried meat")
                break
            else:
                print("Invalid choice. Please select 1, 2, or 3.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")

def find_magical_creature(inventory):
    """Find a magical creature in the forest."""
    print("You stumble upon a mystical creature in the forest")
    print("Do you (1) approach it or (2) run away?")
    
    # Loop for valid input
    while True:
        try:
            choice = int(input("Choose an action (1-2): "))
            if choice == 1:
                print("The creature grants you a blessing of good fortune!")  # Event 29
                inventory.append("blessing of good fortune")
                break
            elif choice == 2:
                print("You run away, but feel the creature's eyes on you.")  # Event 30
                break
            else:
                print("Invalid choice. Please select 1 or 2.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")
            
# Function definitions for other actions like fishing, cave exploration, waterfall discovery, etc.
# Each function simulates an action and modifies the player's inventory or provides an outcome.

def main():
    """Main function to run the game."""
    inventory =[]    #Initialize an empty inventory
    while True:
        user_choice = display_menu()
        
        if user_choice == 1:
            explore_forest(inventory)
        elif user_choice == 2:
            check_inventory(inventory)
        elif user_choice == 3:
            talk_to_character()
        elif user_choice == 4:
            look_for_treasure(inventory)
        elif user_choice == 5:
            battle_enemy()
        elif user_choice == 6:
            visit_village(inventory)
        elif user_choice == 7:
            rest_at_camp()
        elif user_choice == 8:
            encounter_random_event()
        elif user_choice == 9:
            go_fishing(inventory)
        elif user_choice == 10:
            explore_cave(inventory)
        elif user_choice == 11:
            discover_waterfall()
        elif user_choice == 12:
            encounter_merchant(inventory)
        elif user_choice == 13:
            find_magical_creature(inventory)
        elif user_choice == 31:
            print("Thank you for playing! Goodbye!")
            break  # Exit the loop and quit the game
        else:
            print("Invalid choice. Please select a valid action.")

if __name__ == "__main__":
    main()








        


         
        
