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

```
mkdir my-folder
```


## COMMAND AND OUTPUT
<img width="876" height="73" alt="image" src="https://github.com/user-attachments/assets/f227c6b9-5bac-416e-aac2-0d4a3916fcbe" />


Remove the directory "my-folder"


## COMMAND AND OUTPUT

```
rmdir my-folder
```
<img width="872" height="73" alt="image" src="https://github.com/user-attachments/assets/10430bc8-5f19-4d36-ace5-217e70dcd337" />


Create the file Rose.txt

## COMMAND AND OUTPUT


```
COPY CON Rose.txt
A clock in a office can never get stolen
Too many employees watch it all the time


```
<img width="884" height="328" alt="image" src="https://github.com/user-attachments/assets/2f7f142c-f160-4679-8b2b-6e7e53c8519d" />



Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

```
echo “hello world” > hello.txt
type hello.txt

```

<img width="1046" height="142" alt="image" src="https://github.com/user-attachments/assets/cf5f24e6-dd99-4d01-ad9d-712566c7fd32" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT


```
copy hello.txt hello1.txt

```

<img width="1022" height="125" alt="image" src="https://github.com/user-attachments/assets/c05d8c23-07e6-4a17-819a-03eebb9457da" />



Remove the file hello1.txt

## COMMAND AND OUTPUT


```
del hello1.txt



```
<img width="868" height="113" alt="image" src="https://github.com/user-attachments/assets/307063e4-06e3-45e6-a0bb-783f0a02d054" />



List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

```
dir hello1.txt
```





List out all the associated file extensions 

## COMMAND AND OUTPUT

```
assoc | more

```
<img width="848" height="719" alt="image" src="https://github.com/user-attachments/assets/070122c3-c4e6-421c-9d6a-e3bf5e283251" />


Compare the file hello.txt and rose.txt

## COMMAND AND  OUTPUT


```
fc hello.txt Rose.txt


```
<img width="942" height="185" alt="image" src="https://github.com/user-attachments/assets/c1954320-072f-487c-ac67-b41eaa18a7b3" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".





## COMMAND AND OUTPUT

```

@echo off
set name=John
echo Hello, %name%!
pause


```

<img width="752" height="82" alt="image" src="https://github.com/user-attachments/assets/611a2e9f-8a61-4b6a-bfdb-934245c5846a" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.



## COMMAND AND OUTPUT


```

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

```

<img width="847" height="236" alt="image" src="https://github.com/user-attachments/assets/82075cec-6156-4a62-9037-62454198f4f2" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.




## COMMAND AND OUTPUT

```

@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```
<img width="842" height="208" alt="image" src="https://github.com/user-attachments/assets/3c1be5f1-5a9f-4ab9-99ef-ecccaaa9d27a" />


Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## COMMAND AND OUTPUT

```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause

```
<img width="852" height="117" alt="image" src="https://github.com/user-attachments/assets/2b517761-8e62-4fd9-aba0-d34307169e4a" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## COMMAND AND OUTPUT

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


<img width="755" height="263" alt="image" src="https://github.com/user-attachments/assets/33ccfc8f-4665-470c-8759-7aef80289be6" />


# RESULT:
The commands/batch files are executed successfully.

