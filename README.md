# sdhayes.assignment4
student_name = "Silas Hayes"
current_gpa = 3.4
study_hours = 25
social_points = 35
stress_level = 50

print(f"Welcome {student_name}")
print("Your starting stats are:")
print(f"Current GPA: {current_gpa}")
print(f"Study hours: {study_hours}")
print(f"Social points: {social_points}")
print(f"Stress level: {stress_level}")

print("Choose your course load:")
print("A) Light (12 credits)")
print("B) Standard (15 credits)")
print("C) Heavy (18 credits)")

choice = input("Your choice: ")

if choice == "A":
    if current_gpa <= 2.1:
        study_hours += 5
        stress_level -= 10
    else:
        study_hours += 3
        stress_level -= 5
    print("You chose the light work load.")

elif choice == "B":
    if current_gpa < 3.0:
        study_hours += 12
        stress_level += 25
    else:
        study_hours += 10
        stress_level += 15
    print("You chose the standard work load.")

elif choice == "C":
    if current_gpa >= 3.8:
        study_hours += 15
        stress_level += 20
    else:
        study_hours += 20
        stress_level += 30
    print("You chose the heavy work load.")

else:
    print("Invalid input.")

study = ["Programming", "Math", "English", "History"]
print("Choose a class to study: ")
print(study)
choice = input("Class selected: ")

if choice == "Programming":
    current_gpa += 0.3
    social_points -= 5
    print("You chose a challenging class, more studying, less free time.")
elif choice == "Math":
    current_gpa += 0.3
    social_points -= 7
    print("You chose a very challenging class, even more studying and even less free time")
elif choice == "English":
    current_gpa += 0.2
    social_points += 3
    print("You chose a fairly easy class, less studying and more free time.")
elif choice == "History":
    current_gpa += 0.1
    social_points += 3
    print("You chose an easy class, less studying and more free time.")
elif choice not in study:
    print("Invalid choice.")

print("Final Statistics:")

if (current_gpa) is not float and (study_hours) is not int:
    print("One or more variables are not correct. Final Statistics will not show.")
else:
    print("All data is correct, show Final Statistics.")

if current_gpa >= 3.5:
    if stress_level < 60:
        print("Ending 1: You had a balanced and successful semester, ending with good grades and a good social life.")
    else:
        print("Ending 2: You kept a high GPA and had good grades, but became burned out from stress.")
elif current_gpa >= 2.5:
    if social_points >= 40:
        print("Ending 3: You passed the semester with decent grades and a decent social life.")
    else:
        if stress_level > 80:
            print("Ending 4: You ended the semester very stressed out and with terrible grades.")

print("Final Statistics:")
print(f"Name: {student_name}")
print(f"GPA: {current_gpa}")
print(f"Study Hours: {study_hours}")
print(f"Social Points: {social_points}")
print(f"Stress Level: {stress_level}")
