
## Homework #1: Fortune

### Due: Sept 13 at the start of class.

The GitHub Classroom link for this assignment can be found here: https://classroom.github.com/a/XlkuZ7hY

To turn in: commit all of your code to your github repo by the deadline.

In this homework, you'll get some experience writing a Java program that can handle user input, read and write to a file,
and use loops, conditionals and static methods.

This homework will be graded using specifications grading. There are a sequence of tasks to complete. Grades will be assigned as follows:
All code should be well-formatted, with no extraneous or commented-out code. Please include your name in a comment at the top of Fortune.java.

- To receive a C, you should complete tasks 1,2,3,4,5,10
- To receive a B, complete all the C-level tasks, plus 6,7,8,9
- To receive an A, complete the B-level tasks, plus task 11.

Fortune is a classic unix utility. It uses a text file full of fortunes and selects one at random to display to the user, like so:

    (base) ML-ITS-801953: cbrooks$ fortune fortune.db 
    Either one of us, by himself, is expendable.  Both of us are not.
    -- Kirk, "The Devil in the Dark", stardate 3196.1

In this homework, I've provided you with a set of fortunes (titled fortune.db), which are all quotes from the classic Star Trek TV show, as well
as a template class, Fortune.java. You should modify this file to complete your work.

The fortune file is formatted as a series of multi-line fortunes, each separated by a line containing only a '%' character.

------

Task 1: Implement the getFileHandle method. It takes as input a String representing the filename, and returns a Scanner connected to the file.
If there is an error, print an error message and return null.

Task 2. Implement the getFirstFortune method. It should take as input a filename, call getFileHandle (from task 1), and return a String containing the first fortune.

Task 3. Implement fortuneCount. It should take as input a filename call getFileHandle, and return an int indicating how many fortunes are in the file.

Task 4. Implement getRandomFortune. It should take as input a filename (from task 1), generate a random number between 1 and the number of fortunes,
and then find and print that fortune.

Task 5. Implement the userInterface method. It should:
- prompt the user for the name of a fortune db, then call getFileHandle.
- Print the total number of fortunes in the file.
- Ask the user whether they want the first fortune, or a random fortune.
- prompt the user to see if they want additional fortunes, or if they'd like to exit. (use a while loop for this.)

Task 6. Extend userInterface to give the user the option to get a number of fortunes all at once, and print each of them out.

Task 7. Implement the search method. It should take as input a filename and a word to search for, and return the first fortune containing that word. (exact matches only.) Extend the userInterface method to support this.

Task 8. Implement the shortFortunes method. It should take as input a filename and an int indicating the length, and print out all fortunes less than that length. Extend the userInterface method to support this.

Task 9. Implement the writeFortune method. It should take as input a String representing a filename and a String containing a fortune, and write the fortune to the *end* of that file.

Task 10. Implement the test method. It should call each of your other methods with sample input. Print out the name of the method being tested, as well as the result. Extend the userInterface method to support this.

Task 11. Extend your search method to add at least two of the following options.  Extend the userInterface method to support this.

- Add an option for case-insensitive search. Call this caseInsensitiveSearch (e.g. "Cat" and "cat" would match)
- Return all fortunes that contain the search term, in a single string. Call this allSearch.
- Allow the user to provide an array of Strings containing keywords, and return all fortunes that contain *all* the keywords in a single string. Call this andSearch.
- Allow the user to provide an array of Strings containing keywords, and return all fortunes that contain *any* the keywords in a single string. Call this orSearch.
