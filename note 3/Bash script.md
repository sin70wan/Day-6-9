*INTRODUCTION*
 ● Bash = Bourne Again Shell
  ● It is a shell, that used to interact with your kernel.
   ●  Script : Script is a file that contains shell commands in a simple and clear algorithm. 
   ● The original is sh - Bourne shell.
        Starting with Bash
 ● Bash files can have “.sh” extension but you can have it without ‘.sh’ too
  ● The file have to have executable Permissions. 
  ● You can use any text editors u need: VIM,nano,VScode,gedit,cherrytree…
       Displaying output
   ● To start Every bash scripts use shebang. 
     ○ #! /bin/bash 
    ○ #! /bin/sh 
● To display outputs on bash you just do
    ○ echo “YOUR TEXT HERE” 
    ● To run your project you can do: 
    ○ /bin/bash filename
      Variables
        ○ VARIABLE_NAME=value 
     ○ NO Space between the equal sign ( = )
        ■ NAME=”lina” => Correct. 
        ■ Never Start with Numbers
        ■ USE double quotes only.
● To use the variable we will use dollar sign( $ ) before the Variable name 
● If you want to display the variable sticked with other text use ${VARIABLE_NAME} 
● Bash Variables are string by default.
 example :
 NAME="Lina"
 AGE="20"
 echo "your Name is $NAME your age is $AGE"
      System Variables 
● Are variables those are declared by the system.
  like : echo $BASH , echo $BASH_VERSION ,echo $PWD ...
        ● Arrays 
           a) Arrays are lists or tuples on python. 
           b) Syntax:
            i) var=(“list1” “list2” “list3” “list4) 
            ii) TO display echo 
                 (1) ${var[0]}
             iii) To get all the elements 
                 (1) ${var[@]} cont…
              i) To get the indexes (1) 
                 ${!var[@]} 
              ii) To get the length (1) 
                 ${#var[@]}
               iii) To add element to the array 
                   (1) var[4]=”list5”
               iv) To remove from the array 
                (1) unset var[3]
              Bash Input 
    ● On bash we have 2 methods to accept input
     1. Read function
     2. Arguments 
        1) Bash read
        ● Read used to accept inputs while the script is running. 
        ● Syntax: 
            ○ read -p “Text To Display” var 
            ○ read -sp “Password: ” var => used to accept hidden texts like password. 
             ○ read -a var => for accepting arrays(lists)
         1) Arguments
        ● These helps to get input before the script starts 
        ● Syntax: 
            ○ Just use $0-$9 while you want to work with the input
    Comments: <<COMMENTS.......COMMENTS
                 Bash sleep 
        ● Sleep used to make a good waiting on our script. 
          ● Syntax: 
             ○ sleep <num>
IF ELSE CONDITIONS   
    example:
           if [ 2 -gt 1 ]
           then
           echo "he"
          else 
          echo "bye"
          fi
          
            Further on Bash
    Regular Expressions! /regex/ 
● Most filter Validation on any platform done by Regular expression/regex/.
● They are patterns that helps to filter so texts,space,tabs & symbols.
● Like telegram or other platforms filtering links inside group, filtering some bad words.. All are regex. 
● Regex is PATTERN!
● Regex are used on Linux tools called grep,awk and sed
●use vscode to demonstrate and don't forget to turn regex button

Metacharacters 
● Those are regex pattern symbols for filter.
● They are :  . ,^ ,$ ,* ,+ ,? ,{ } ,[ ] ,( ) , | ,\
        Dot ( . ) 
     ● Used to get All the line except new lines 
     ● Syntax: . 
     ○ This means give me all lines except the new lines
          Caret ( ^ ) - Assertion 
    ● Used to get line that start with pattern
           Dollar sign( $ ) - Assertion 
    ● Used to get line that ends with some pattern.
            Plus ( + ) - Quantity 
    ● Used to get line that have pattern that occurs 1 and more times
             Asteriks ( * ) - Quantity
    ● Used to get line that have pattern that occurs 0 and more times.
           Question mark ( ? ) - Quantity
     ● Used to get line that have pattern that occurs 0 and 1 times
            Curly Bracket ( { min , max} ) - Quantity
    ● Used to get line that have pattern that occurs min and max times.it is custom
     ● Syntax: hellos{1,3}
               \w 
    ● Used to get Alphanumeric 
    ● Syntax: \w 
    ○ All texts except newlines and symbol
             \W 
    ● Used to get All except Alphanumeric 
    ● Syntax: \W
             \s 
    ● Used to get whitespace.
    ● Syntax: \s
            \S 
    ● Used to get all except whitespace.
	● Syntax: \S
	         \d 
	● Used to get Digits/numbers/
	 ● Syntax: \d
	         \D 
	● Used to get all except Digits/numbers/ 
	● Syntax: \D
	         Pipe ( | ) - OR
	 ● Used to search 2 different things. 
	 ● Syntax: a|b
	         Escape ( \ )
	● Used to search symbols that are metacharacters.
	 ● Syntax: \
	          Square Brackets ( [ ] ) - Custom pattern 
    ● Used to Create your own patterns 
    ● Syntax: [pattern]
              Bash else if 
    ● To do more than 1 comparing. 
    ● It is same with python is is “elif”
        example :
             if condition 
             then 
             elif  condition
             then
                  body
              else 
                 body 
              fi 
    Loops
     ● On Bash, there are 3 types of loops 
     a. For loop 
     b. While loop 
     c. Until loop
      For loops
      ● The iteration may be different here. We can use arrays like list on python but we dont have range in bash but we can do {a..b} this iterates from a to b           for condition
          do 
             body
          done  
      While loop 
          while [experssion]
          do 
             body
          done
BASH and Linux :We can run linux commands inside our bash.