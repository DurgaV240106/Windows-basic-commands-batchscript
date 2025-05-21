# Windows-basic-commands-batchscript
# Ex08-Windows-basic-commands-batchscript

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
![image](https://github.com/user-attachments/assets/65fec388-b77d-4bf7-bf9e-898e103e7f41)

Remove the directory "my-folder"

## COMMAND AND OUTPUT
![image](https://github.com/user-attachments/assets/ae70d29b-787f-4eff-a5ce-660f86b31ed6)


Create the file Rose.txt

## COMMAND AND OUTPUT
![image](https://github.com/user-attachments/assets/51b6d7f3-951c-42cd-b176-163fa42fa9f9)


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

![image](https://github.com/user-attachments/assets/aba41aa9-af5c-48cb-924c-981850791d54)

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

![image](https://github.com/user-attachments/assets/8bfff234-65ca-4a96-8f7e-d8a73a519104)

Remove the file hello1.txt

## COMMAND AND OUTPUT
![image](https://github.com/user-attachments/assets/63136c8b-de2d-44f1-b58c-d6987c578b78)

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

![image](https://github.com/user-attachments/assets/29a25692-25e5-4386-8b48-0e289a2c8011)

List out all the associated file extensions 

## COMMAND AND OUTPUT
![image](https://github.com/user-attachments/assets/2c3604e1-a72a-4af8-adbe-318d4c831daa)

![image](https://github.com/user-attachments/assets/597de78d-c38e-4616-900d-db70f47cf663)

![image](https://github.com/user-attachments/assets/f532f488-fa95-4315-8125-a4b7f054d6ec)

![image](https://github.com/user-attachments/assets/32ff9d37-8185-4a1e-92d7-b705e39f158c)

![image](https://github.com/user-attachments/assets/9375eee0-2309-437f-a631-c14b61d38445)

![image](https://github.com/user-attachments/assets/dace4de7-b841-462f-8aee-84b4168bc518)

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

## batch program
```
@echo off
set name=John
echo Hello, %name%
pause
```




## OUTPUT
![Screenshot 2025-05-21 160928](https://github.com/user-attachments/assets/1ba8e4c3-a516-4a41-b1d5-4927270421db)



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.


## batch program:
```
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```
## OUTPUT

![image](https://github.com/user-attachments/assets/29959a98-88cd-4785-a8bb-98ac65f90b7a)



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.


## batch program:
```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/9ba219e0-7a6f-4b69-8b19-b3ea06a4d31e)



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
## batch program:
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
![image](https://github.com/user-attachments/assets/bfe1ac15-30b2-4bad-81d9-66b171064074)


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

## batch program:
```
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```
## OUTPUT
![image](https://github.com/user-attachments/assets/753e8fdb-6253-4237-9324-be310c11f801)

![image](https://github.com/user-attachments/assets/50ae70c9-807b-4f4d-b476-f36f02ed58fb)

![image](https://github.com/user-attachments/assets/c51251fc-5f26-47a7-bb74-9cde29fce004)


# RESULT:
The commands/batch files are executed successfully.

