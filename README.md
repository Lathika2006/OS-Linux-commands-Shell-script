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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/645747f6-840a-4fb5-9bb8-3d37985808e1)


cat < file2
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/4680c410-0f1a-417d-9f0d-05e417dff105)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b72ea53a-f252-420f-b008-c1db50733c87)

comm file1 file2
 ## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/9d8206de-18fe-42e7-98c7-f58a03d1e027)

 
diff file1 file2
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/9db3fd92-ee1d-45f1-81b7-2421566f2f4a)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b05fb00f-680e-478f-bf30-40e73ed3f8fc)





cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/9b1db5ba-2294-4c27-93e3-04529c484132)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/ac5c3093-ce26-4a44-8342-2861d83fe00c)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c9dcc002-ec57-4d2a-ac12-b2118670b418)


grep hello newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1ba59f65-d89a-443c-b63e-658844690510)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/7898aa37-f171-4dd3-b9bf-4821a7c66366)


cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b34be529-da32-4875-ada4-5403c4b2b219)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b68bbe48-76d8-4261-aea9-5b3525862b73)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c7641628-681a-431e-a85d-f9606f4a5cf5)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/ab89cc80-61df-49c7-b155-4a5e5172bb58)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/3fb6eac9-fb4a-4396-9418-c277da0ac7af)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/15faa397-b760-4e38-88c5-46df8d1bdb60)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/cb5df577-6ca4-4fb2-a5b2-a1bbfc9342ff)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/84e6db99-923d-4dcb-9d2f-f759f1d23029)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/3e4a7354-30a8-4a78-9ba7-ef3d7b9205cc)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/73eb50dd-a4e7-4231-93fd-3043957f5bb6)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/10d9f5b0-41c6-4871-8acb-7c1bbfbefaaa)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/56fd1f75-45fe-46f6-8ed2-f25c8c712aec)



egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/7d6419cf-634f-4106-9a64-86fb2f8098c3)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1128e562-d671-4878-a83c-49a308d4f983)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/da8d070f-5f44-421c-b63e-b08b08021b2d)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c79a5769-68c8-4842-87e9-d9799398d1dc)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/d023edb3-6837-4065-98e9-08bb8b5d4360)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/4c0977d9-7438-4ace-a89a-e0536e3c96b0)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/03ea1332-8ae5-4e5b-9f27-5f150319a13b)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/54e0938a-b87e-4a52-a6d8-1d33b644ef58)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/f4539868-4ccb-480e-a828-de27371cc413)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/61c2937f-7b06-4bae-828a-7e00818b5287)

sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/07aa75ef-5b1e-4d5b-bfe5-7d36cb65c8d7)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b3664d94-dc31-448c-88b1-e74cd741c96b)


seq 10 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b51046e0-51df-4a04-97a3-9aff3b3929fd)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/4ed9f3b2-3d9a-4859-a477-9c4d47247f26)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/a910466b-be1c-4335-8842-201a475247b6)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/40491877-b232-4596-96a2-c3d9955510e8)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c0cd675e-bff0-4f16-a406-081556b997ad)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/0867c436-fe08-4955-b19f-d73264f8008b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/97a3d875-4b77-48e6-bba7-a65eedd77df3)


sed -n '2,4{s/$/*/;p}' file23


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.
