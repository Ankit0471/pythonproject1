# pythonproject1
questions = ("Who conceptualized python?  : ",
                       "How many types of operators are there in python?: ",
                       "Reserved words in python are known as?: ",
                       "How many keywords are there in python?: ",
                       " What type of programming language does python support: ")

options = (("A. Dennis Ritchie ", "B. Bjarne Stroustrup", "C. Guido Van Rossum", "D. James Gosling"),
                   ("A. 8", "B. 5", "C. 9", "D. 7"),
                   ("A. Keywords", "B. Data Types", "C. Variables", "D. Operators"),
                   ("A. 33", "B. 34", "C. 35", "D. 36"),
                   ("A. procedural programming", "B. object oriented programming", "C. functional programmig", "D. structured programming"))

answers = ("C", "D", "A", "A", "B")
guesses = []
score = 0
question_num = 0

for question in questions:
    print("----------------------")
    print(question)
    for option in options[question_num]:
        print(option)

    guess = input("Enter (A, B, C, D): ").upper()
    guesses.append(guess)
    if guess == answers[question_num]:
        score += 1
        print("CORRECT!")
    else:
        print("INCORRECT!")
        print(f"{answers[question_num]} is the correct answer")
    question_num += 1

print("----------------------")
print("       RESULTS        ")
print("----------------------")

print("answers: ", end="")
for answer in answers:
    print(answer, end=" ")
print()

print("guesses: ", end="")
for guess in guesses:
    print(guess, end=" ")
print()

score = int(score / len(questions) * 100)
print(f"Your score is: {score}%")
