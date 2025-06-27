#  Text-Based Notes Manager (Java)

A simple console-based application built in Java that allows users to write and read notes using file handling.

##  Technologies Used

| Technology      | Purpose                         |
|-----------------|---------------------------------|
| Java            | Core programming language       |
| FileWriter      | Writing notes to a text file    |
| FileReader      | Reading notes from a file       |
| BufferedReader  | Efficient line-by-line reading  |
| Scanner         | Console input from user         |

## How the System Works ##

Step 1: Program Starts
The program begins with the main() method.
A Scanner object is created to take input from the user.
The program enters a do-while loop and displays a menu:
===== Notes Manager =====
1. Write a new note
2. View all notes
3. Exit
Enter your choice:

Step 2: User Enters Choice
The user enters a choice (e.g., 1 to write a note).
Based on the choice, the program uses a switch statement to call the respective method.
 
 ## If Choice = 1 (Write a Note) ##
The method writeNote(scanner) is called.

It asks:
Enter your note:
User types a note (e.g., Learn Java file handling).

The program opens the file notes.txt using:

FileWriter writer = new FileWriter(FILE_NAME, true);
true = append mode, so it doesn’t erase old notes.

The note is written to the file followed by a newline.

**Output:**
Note saved successfully!
The file is automatically closed.

## If Choice = 2 (View Notes) ##
The method readNotes() is called.
The program opens notes.txt using:
BufferedReader reader = new BufferedReader(new FileReader(FILE_NAME));
It reads the file line by line using readLine().

Each line is printed with a line number:
1. Learn Java file handling
2. Practice daily
If file is empty or not found:
No notes found yet.


 ## If Choice = 3 (Exit) ##
Program prints:
Exiting Notes Manager.
Loop stops and the program ends.

The Menu Repeats
After writing or viewing a note, the menu is shown again:

===== Notes Manager =====
1. Write a new note
2. View all notes
3. Exit
You can perform multiple operations until you choose option 3.



