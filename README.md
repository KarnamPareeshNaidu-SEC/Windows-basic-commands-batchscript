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
<img width="606" height="167" alt="Screenshot 2026-05-26 112224" src="https://github.com/user-attachments/assets/10a37512-b2fe-4c95-8f2a-8a53513f7538" />


## COMMAND AND OUTPUT

Remove the directory "my-folder"
<img width="573" height="157" alt="Screenshot 2026-05-26 112251" src="https://github.com/user-attachments/assets/fa96dec2-c97d-41e0-9991-86a3253f7db8" />

## COMMAND AND OUTPUT


Create the file Rose.txt

<img width="684" height="391" alt="Screenshot 2026-05-26 112805" src="https://github.com/user-attachments/assets/0e190216-8ff8-4408-9499-92b0fadf36be" />

## COMMAND AND OUTPUT


Create the file hello.txt using echo and redirection

<img width="429" height="160" alt="Screenshot 2026-05-26 112456" src="https://github.com/user-attachments/assets/02660bca-4b76-4e37-90cb-fea84f22adc3" />

## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt
<img width="514" height="210" alt="Screenshot 2026-05-26 112528" src="https://github.com/user-attachments/assets/efc819f8-de79-42bb-a16c-afc654218e41" />

## COMMAND AND OUTPUT

Remove the file hello1.txt

<img width="499" height="305" alt="Screenshot 2026-05-26 112603" src="https://github.com/user-attachments/assets/cbdbf90d-877a-4d53-89f8-f1f7b1f380d0" />

## COMMAND AND OUTPUT

List out all the associated file extensions 

<img width="507" height="898" alt="Screenshot 2026-05-26 112715" src="https://github.com/user-attachments/assets/3df11a29-ce96-4087-81ef-d426671d5e5e" />


## COMMAND AND OUTPUT


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
~~~
BATCH SCRIPT
Open Notepad with filename 1.bat and type the following batch script
@echo off
set name=John
echo Hello, %name%!
pause
~~~

<img width="651" height="265" alt="Screenshot 2026-05-26 113317" src="https://github.com/user-attachments/assets/a1098185-f9f9-45b9-ae3e-33508e2ae73d" />



## OUTPUT



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

~~~
Open Notepad with filename 2.bat and type the following and execute 2.bat
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
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
~~~


<img width="604" height="281" alt="Screenshot 2026-05-26 113418" src="https://github.com/user-attachments/assets/63b38dce-493a-4b7f-b5e3-89a5dfb7f4e5" />

## OUTPUT




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.


~~~
Open Notepad with filename 3.bat and type the following and execute 3.bat
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

~~~
<img width="524" height="326" alt="Screenshot 2026-05-26 113601" src="https://github.com/user-attachments/assets/e5ea535c-9827-4562-aaf6-4b869c05b583" />

## OUTPUT




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
~~~
Open Notepad with filename 4.bat and type the following and execute 4.bat
Then create the file sample.txt and execute 4.bat

@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
~~~
<img width="565" height="241" alt="Screenshot 2026-05-26 113758" src="https://github.com/user-attachments/assets/08b566ec-6fff-46a5-beb9-bca91370dfda" />
## OUTPUT


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
~~~
Open Notepad with filename 5.bat and type the following and execute 5.bat

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


~~~

<img width="447" height="336" alt="Screenshot 2026-05-26 113854" src="https://github.com/user-attachments/assets/ef4961da-31d9-48a1-9466-6f98ee5e9766" />

## OUTPUT:

Thus, the basic Windows commands and batch script operations were executed successfully using Command Prompt, and the desired output was obtained.




# RESULT:
The commands/batch files are executed successfully.

