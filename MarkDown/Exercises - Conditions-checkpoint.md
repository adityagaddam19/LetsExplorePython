
# Exercises - Conditions

Write a program to 
- perform a quiz of 10 questions and once its completed provide the results to the user

- create a guess the number program. Program should ask for user's name in the beginning and then generate a number number between 10 and 100. It should then request user to guess the number, and check if the number guessed is same generated number, if yes then it should print "Congratulation" else should provide an indication is guessed number was higher or lower then the generated number 

- What would be printed from the following Python program section if "Java" was input by the user?
```python
  language=raw_input('Enter your favorite language:')
  app=language.contains('thon')
  if  app:
      print 'Good, ' + str(language) + ' is a good languge'
  else:
      print 'Nice Choice'
```
- calculate if the user provided year is a leap year. 

- assign grades to students at the end of the year. The program must do the following:
        Ask for a student number.
        Ask for the student’s tutorial mark.
        Ask for the student’s test mark.
Calculate whether the student’s average so far is high enough for the student to be permitted to write the examination. If the average (mean) of the tutorial and test marks is lower than 40%, the student should automatically get an F grade, and the program should print the grade and exit without performing the following steps.

    -- Ask for the student’s examination mark.
    
    -- Calculate the student’s final mark. The tutorial and test marks should count for 25% of the final mark each, and the final examination should count for the remaining 50%.
    
    -- Calculate and print the student’s grade, according to the following table:

Weighted final score|Final grade 
:-------------------:|-----
80 <= mark <= 100|A 
70 <= mark < 80|B
60 <= mark < 70 | C
50 <= mark < 60 | D
mark < 50 | E
        
        
- Rewrite the following fragment as an if-ladder (using elif statements):
```python
if temperature < 0:
    print("Below freezing")
else:
    if temperature < 10:
        print("Very cold")
    else:
        if temperature < 20:
            print(Chilly)
        else:
            if temperature < 30:
                print("Warm")
            else:
                if temperature < 40:
                    print("Hot")
                else:
                    print("Too hot")
```
