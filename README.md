# Simple-grade-calc
print("EXAM GRADE CALCULATOR".center(50))
print()
print("--------")
def get_marks(subject):
  while True:
      try:
          marks = int(input(f"{subject} marks (0-100): "))
          if 0 <= marks <= 100:
              return marks
          else:
              print("Please enter a number between 0 and 100.")
      except ValueError:
          print("Invalid input. Please enter a valid integer.")

# Usage
mathsGrades = get_marks("Maths")
print()
physicsGrades = get_marks("Physics")
print()
chemsGrades = get_marks("Chemistry")
print()
engGrades = get_marks("English")
print()
frenchGrades = get_marks("French")
print()
print("-----------------".center(50))
print()
GRAND_TOTAL = mathsGrades + physicsGrades + chemsGrades + engGrades + frenchGrades
print(f"GRAND TOTAL:- {GRAND_TOTAL}".center(50))
print()
print("-----------------".center(50))
print("")
print("PERCENTAGE OBTAINED".center(50))
print()
percentage_1 = (GRAND_TOTAL / 500) * 100
print(f"Percentage:- {round(percentage_1, 2)} %".center(50))
print("------------------".center(50))
if  90 <= percentage_1 <= 100:
    print("GRADE:- A+".center(50))
elif 80 <= percentage_1 <= 90:
    print("GRADE:- A-".center(50))
elif 70 <= percentage_1<= 80:
    print("GRADE:- B".center(50))
elif 60 <= percentage_1<= 70:
    print("GRADE:- c".center(50))
elif 50 <= percentage_1<= 60:
    print("GRADE:- D".center(50))
else:
    print("GRADE:- F".center(50))
print("-----------------".center(50))
