# quiz-game-py
import time

# Displaying current time in a correct format
current_time = time.strftime('%H:%M:%d')
print(f"Current time: {current_time}")

# Questions and answers
questions = [
    ["What is the capital of Pakistan?", "Islamabad", "Karachi", 1],
    ["What is 2 + 2?", "4", "2", 1],
    ["Who wrote 'The Origin of Species'?", "Harry Brook", "Charles Darwin", 2],
    ["What is the boiling point of water in Celsius?", "122", "100", 2],
    ["Which programming language is known as the 'language of AI'?", "C-", "Python", 2]
]

levels = [1, 2, 3, 4, 5]

print(".......Welcome to our game.......\n")

# Main game loop
for i in range(len(questions)):
    question = questions[i]
    print(f"Question for Rs {levels[i]} is:")
    print(f"a. {question[1]}         b. {question[2]}")

    # Getting user input
    reply = int(input("Enter your answer (1 for 'a', 2 for 'b'): "))

    # Check the answer
    if reply == question[-1]:
        print(f"Congratulations! You have won Rs {levels[i]}.\n")
    else:
        print("Wrong answer. Game over!\n")
        break
else:
    print("Congratulations! You've answered all the questions correctly!")
