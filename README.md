# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/user-attachments/assets/bb7356f3-bd6a-442a-a64a-a15ff1791e2b)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/13376d07-6ff1-43f0-8b31-187a872b989c)




# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/0c8bea4a-a4b9-4b2a-8913-01b44b61871c)

 
comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/84542127-e571-4fd3-9a40-6dd6759f2043)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/e300a3d6-0174-4a5b-9ef4-71d13bf1c4a7)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/user-attachments/assets/794b1739-97cb-49a0-b390-5b6b7612a679)




cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/090b0d22-3b51-4132-9c97-ed069c73a810)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/81695730-47da-423f-8aad-cf52ea01028d)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/c14cc333-4ebd-4e8e-a75e-39fbf0f3bdc5)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/2b32e4e4-fd88-4f1c-a4f0-11b42b7b4649)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/644d85a7-5f5c-4259-ab7f-6cc8fe2b6a29)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/273cf324-f63e-4ff8-84bd-8fe415861e31)



cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/69c334b4-155f-4e88-9b07-221342102c80)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/49b8fda8-1bc7-4156-bb2e-2d5d32ff4ac3)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/de00fc26-4e69-4d19-a3b6-ad2ef2cece18)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e38804c8-4597-4ec6-9280-d2f7ac16a30f)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/128d9e2d-7bc6-4442-9247-ef5e9b946113)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d17a63bb-c9dd-46f6-8d58-5d2c9114392c)




egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/56563020-ba45-4d8d-ad8f-70dd88417f23)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/640909a5-8377-4ee4-a2b7-005f03ac373b)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/42fd67b2-bbc2-43a8-aba6-88a70ab3709f)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2ec100bf-a536-4f84-88d7-1360b6a0f992)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b7ebfd63-2a36-4bb7-a25c-dfa3f459b07c)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/057bbed7-9a35-4d39-ada6-0e86e743a261)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/3c2b7720-fb9d-4721-8e9d-eff7a22856fd)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/10b04381-0bdd-4c21-91b5-0894117caf45)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/4c99a664-b2e4-440b-a2a1-322109bf6550)




cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR

1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8bb055cc-967f-4dad-acaf-10c21e2c5057)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/195d4cda-9d57-4981-8f4d-81d47618fc64)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1992d720-5944-4d46-b91b-c2a3195db819)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/06616f0a-05c8-4f2a-b969-4b35c439b66e)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/da8d44d3-3642-4b1c-bebf-98424bdd704e)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/7bfca80b-1ebf-4c64-9fa5-aab3e4c69976)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d4c52b6a-b897-41b9-9251-813206ab786d)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ea0ee694-a2af-4aa2-8509-634c2b4e7a43)



seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/b48bce00-30c5-4800-ac28-cc35faff0497)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/ac7040bc-0fcc-4bb3-aa4c-aa4be7bb8e20)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/5c48ec1c-12c7-4f67-8953-e8fcb04a93e2)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/d9f95832-1b37-45f2-bb60-865176b382a0)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/18274665-ada6-45bb-8883-c4c7326d288b)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/0500398f-1699-415b-9384-9e032a37cd58)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/d2ca4555-7427-4675-a61c-a4d9eb0da8f0)

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/user-attachments/assets/355f3f4f-d081-40e2-934b-38ce6b32ff3e)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![image](https://github.com/user-attachments/assets/60de2c32-1c68-43e5-9bf6-c914e670f6f2)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/e4707a21-c09a-4645-97c0-1ee1ff4561ed)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com


 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/user-attachments/assets/f64851b1-7f19-4147-b7ef-a56f7c4fe517)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/14b96b35-963a-4e7b-a199-02b698619cf7)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/497161d1-06d1-4845-9aaa-0a019599f53a)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/266a9a9f-2d41-4bde-943b-5538d34cccb9)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/fa53053f-1b46-4bc0-b934-7f8040f894df)


gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/68b178d0-20b6-4c8d-81d8-f649ae43cf7a)

 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
```
hello in this world
i cant stop
for this non stop movement
```

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
```
./scriptest.sh: line 1: #!/bin/sh: No such file or directory
“File name is ./scriptest.sh ”
File name is  scriptest.sh
“First arg. is ” 1
“Second arg. is ” 2
“Third arg. is ” 3
“Fourth arg. is ”
The $@ is  1 2 3
The $\# is  1#
The $$ is  14337
    PID TTY          TIME CMD
  13614 pts/1    00:00:00 bash
  14337 pts/1    00:00:00 bash
  14340 pts/1    00:00:00 ps
```
 
ls file1
## OUTPUT
```
file1
```
echo $?
## OUTPUT 
```
0
```
echo $?
## OUTPUT 
```
1
```
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
```
0
```
 
abcd
 
echo $?
 ## OUTPUT
```
127
```

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
```
baseball is less than hockey
```


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

```
You are the owner of the /etc/passwd file

```
# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
```
"/root The object exists, is it a file?"
"No,/root it is not a file!"
```
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

```


“/home/sec The object exists, is it a file?”
“No,/home/sec it is not a file!”
“But /home/sec/.bash_history is a file!”

```

# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
```
“The test value 10 is greater than 5”
“The values are different”

```
# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
```
“/home/sec The object exists, is it a file?”
“No,/home/sec it is not a file!”
“But /home/sec/.bash_history is a file!”
```
# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
```
./elifcheck.sh: line 1: #!/bin/bash: No such file or directory
Sorry, you are not allowed here

```

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
```
./ifcompound.sh: line 1: #!/bin/bash: No such file or directory
The file exists and you can write to it
```
# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 

##Output
 ```
Sorry, you are not allowed here
```
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

##Output
```
10
9
8
7
6
5
4
3
2
1

```
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 $./untiltest.sh 
 ## Output 
 ```
./untiltest.sh: line 1: #using: command not found
100
75
50
25

```
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh

  $ ./forin1.sh

 ## Output
 ```
./forin1.sh: line 1: #!/bin/bash: No such file or directory
./forin1.sh: line 2: #basic: command not found
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado

```
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 ## Output 
 ```
“word:I”
“word:dont know if thisll”
“word:work”
```
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 ## Output 
```
word:I
word:don't
word:know
word:if
word:this'll
word:work

```
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
```
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

```
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities

```

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
```
The value is i is 1
The value is i is 2
The value is i is 3
The value is i is 4
The value is i is 5
```

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
```
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
```

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
  ## OUTPUT
```
Starting loop 1:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3
Starting Loop 2:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3
Starting Loop 3:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3


```

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
```
Iteration number: 1
Iteration number: 2
The for loop is completed

```

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 

## OUTPUT
```
Enter your name: Bhuvaneshwari
Hello Anuradha, welcome to my program. 

```
$ ./exread.sh 

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
./funcex.sh 
```
Usage: badtest1 a b
```
 
 ./funcex.sh 1 2

```
The result is 2
```


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 ```
1
2
3

```
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 ```
1
2
3

```
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
  ```
+ ((  3  ))
+ echo 1 
1
+ shift
+ ((  2  ))
+ echo 2
2
+ shift
+ ((  1  ))
+ echo 3
+ shift
+ ((  0  ))
+ set +x

```
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ```
7         bcdfghj
8	  abcdfghj
7	  bcdfghj
8  	  ebcdfghj
7	  bcdfghhj
8	  ibcdfghj
7	  bcdfghj
8	  obcdfghj
7	  bcdfghj
8 	  ubcdfghj
total characters 75
Number of Lines are 10
No of Words count: 10

```
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
```
locathost:~# chmod 755 palindrome.sh
locathost:~# ./palindrome.sh
Enter the number
21
Number is NOT palindrome
```
```
locathost:~# chmod 755 palindrome.sh
locathost:~# ./palindrome.sh
Enter the number
33
Number is palindrome
locathost:~#

```

# RESULT:
The Commands are executed successfully.
