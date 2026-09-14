# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT

mkdir my-folder

Directory created successfully.


Remove the directory "my-folder"

## COMMAND AND OUTPUT

rmdir my-folder

Directory removed successfully.

Create the file Rose.txt

## COMMAND AND OUTPUT

COPY CON Rose.txt

<img width="498" height="137" alt="image" src="https://github.com/user-attachments/assets/ec712bfc-1026-4392-8806-0494451d126b" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

echo hello world > hello.txt

<img width="690" height="225" alt="image" src="https://github.com/user-attachments/assets/ab617041-148b-427a-b7dc-eb30cbb26fdd" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

copy hello.txt hello1.txt

1 file(s) copied.


Remove the file hello1.txt

## COMMAND AND OUTPUT

del hello1.txt

File deleted successfully.


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

dir hello1.txt

File Not Found


List out all the associated file extensions 

## COMMAND AND OUTPUT

assoc | more

<img width="531" height="407" alt="image" src="https://github.com/user-attachments/assets/7c932418-486f-49e9-9149-f05b0270c7e4" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

fc hello.txt Rose.txt

<img width="527" height="235" alt="image" src="https://github.com/user-attachments/assets/16970f4b-e2aa-488f-87b6-70798cbaa642" />



## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause
```



## OUTPUT

<img width="622" height="162" alt="image" src="https://github.com/user-attachments/assets/c3693596-8fe1-455e-be4c-a93750b972f0" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:main
set /p number=Enter a number: 
set /a remainder=%number% %% 2

if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)

:choice
set /p continue=Do you want to check another number? (Y/N): 

if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end

echo Invalid choice, please enter Y or N.
goto choice

:end
echo Thank you for using the odd number checker!
pause
```

## OUTPUT

<img width="500" height="192" alt="image" src="https://github.com/user-attachments/assets/541c0b4c-475a-4043-af4f-6b3bd7b7f424" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```



## OUTPUT

<img width="500" height="192" alt="image" src="https://github.com/user-attachments/assets/d189a951-d945-46e7-9260-c1ca3b898827" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT

<img width="411" height="92" alt="image" src="https://github.com/user-attachments/assets/15bf9a4b-552d-4663-bd6f-2fa30d09d4f4" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu

:end
echo Goodbye!
pause
```

## OUTPUT

<img width="433" height="396" alt="image" src="https://github.com/user-attachments/assets/3d9c7d52-55db-4d62-b165-f5f2a1009c67" />


# RESULT:
The commands/batch files are executed successfully.

