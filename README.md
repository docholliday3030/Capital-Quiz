# Capital-Quiz
US States and capital quiz

import random

# List of States and their capitals


us_state_capitals = {
                        "Alabama": "Montgomery",
                        "Alaska": "Juneau",
                        "Arizona": "Phoenix",
                        "Arkansas": "Little Rock",
                        "California": "Sacramento",
                        "Colorado": "Denver",
                        "Connecticut": "Hartford",
                        "Delaware": "Dover",
                        "Florida": "Tallahassee",
                        "Georgia": "Atlanta",
                        "Hawaii": "Honolulu",
                        "Idaho": "Boise",
                        "Illinois": "Springfield",
                        "Indiana": "Indianapolis",
                        "Iowa": "Des Moines",
                        "Kansas": "Topeka",
                        "Kentucky": "Frankfort",
                        "Louisiana": "Baton Rouge",
                        "Maine": "Augusta",
                        "Maryland": "Annapolis",
                        "Massachusetts": "Boston",
                        "Michigan": "Lansing",
                        "Minnesota": "St Paul",
                        "Mississippi": "Jackson",
                        "Missouri": "Jefferson City",
                        "Montana": "Helena",
                        "Nebraska": "Lincoln",
                        "Nevada": "Carson City",
                        "New Hampshire": "Concord",
                        "New Jersey": "Trenton",
                        "New Mexico": "Santa Fe",
                        "New York": "Albany",
                        "North Carolina": "Raleigh",
                        "North Dakota": "Bismarck",
                        "Ohio": "Columbus",
                        "Oklahoma": "Oklahoma City",
                        "Oregon": "Salem",
                        "Pennsylvania": "Harrisburg",
                        "Rhode Island": "Providence",
                        "South Carolina": "Columbia",
                        "South Dakota": "Pierre",
                        "Tennessee": "Nashville",
                        "Texas": "Austin",
                        "Utah": "Salt Lake City",
                        "Vermont": "Montpelier",
                        "Virginia": "Richmond",
                        "Washington": "Olympia",
                        "West Virginia": "Charleston",
                        "Wisconsin": "Madison",
                        "Wyoming": "Cheyenne",
}

def state_capital_quiz():
    print("Welcome to the State Capital Quiz!")
    print("You will be asked to name the capitals of random U.S. states.")
    print("Type 'exit' anytime to quit.\n")

    states = list(us_state_capitals.keys())
    score = 0

    while True:
        # Randomly select a state
        state = random.choice(states)
        correct_answer = us_state_capitals[state]

        #Ask the user the question
        print(f"What is the capital of {state}?")
        user_answer = input("Your answer: ").strip()

        if user_answer.lower() == "exit":
            print(f"\nThanks for playing! Your final score is {score}.")
            break

        #Check if teh answer is correct
        if user_answer.lower() == correct_answer.lower():
            print("Correct!\n")
            score += 1
        else:
            print(f"Wrong! The capital of {state} is {correct_answer}.\n")

#Run the quiz
state_capital_quiz()
