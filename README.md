# Portfolio 5: Strings
## Title: Heart Rate Monitoring System (For UHS)

### Description
#### This Python program demonstrates the use of strings,
#### loops, conditions, slicing, concatenation, and string methods
#### through a simple heart rate monitoring system.

#### The program accepts patient information and determines
#### whether the heart rate is:
#### - Low
#### - Normal
#### - High

#### It also performs several string operations to analyze
#### the patient's name and course/program.

### Concepts Applied
#### - String Data Type
#### - String Concatenation
#### - String Slicing
#### - Looping Through Strings
#### - String Methods
#### - Conditional Statements
#### - len() Function
#### - in Operator
#### - Counting Technique

#### User Input
```python
patient_name = input("Enter patient name: ")
course = input("Enter course/program: ")
heart_rate = input("Enter heart rate (BPM): ")
```

#### Remove extra spaces
```python
patient_name = patient_name.strip()
course = course.strip()
heart_rate = heart_rate.strip()
```

#### Convert heart rate string into integer
```python
bpm = int(heart_rate)
```


### DISPLAY PATIENT INFORMATION
```python
print("PATIENT INFORMATION")

print("Patient Name :", patient_name.title())
print("Course       :", course.upper())
print("Heart Rate   :", bpm, "BPM")
```

### HEART RATE ANALYSIS
```python
print("HEART RATE STATUS")
```

#### Determine heart rate condition
```python
if bpm < 60:
    print("Status: Low Heart Rate")

elif bpm >= 60 and bpm <= 100:
    print("Status: Normal Heart Rate")

else:
    print("Status: High Heart Rate")
```

### STRING LENGTH OPERATIONS
```python
print("STRING ANALYSIS")

print("Length of patient name:", len(patient_name))

print("Length of course name :", len(course))
```

### STRING SLICING
```python
print("STRING SLICING")

print("First 4 letters of patient name:",
      patient_name[0:4])

print("Last 3 letters of course:",
      course[-3:])
```

### USING 'in' AS A LOGICAL OPERATOR
```python
print("WORD CHECKER")

if "med" in course.lower():
    print("The course contains 'med'.")

else:
    print("The course does not contain 'med'.")
```

### LOOPING THROUGH STRINGS
```python
print("LETTERS IN PATIENT NAME")

for letter in patient_name:
    print(letter)
```

### COUNTING VOWELS
```python
vowel_count = 0

for letter in patient_name.lower():

    if letter == "a":
        vowel_count = vowel_count + 1

    elif letter == "e":
        vowel_count = vowel_count + 1

    elif letter == "i":
        vowel_count = vowel_count + 1

    elif letter == "o":
        vowel_count = vowel_count + 1

    elif letter == "u":
        vowel_count = vowel_count + 1

print("Total vowels in patient name:", vowel_count)
```
### DISPLAY INITIALS
```python
print("PATIENT INITIALS")

words = patient_name.split()

if len(words) >= 2:

    print("Initials:",
          words[0][0].upper() + "." +
          words[1][0].upper() + ".")
```
### STRING CONCATENATION
```python
message = "Patient " + patient_name + \
          " has completed the heart rate check."

print(message)
```