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
<img width="740" height="162" alt="image" src="https://github.com/user-attachments/assets/189e5b5b-809f-4699-a822-df3e69355206" />






cat < file2
## OUTPUT
<img width="597" height="176" alt="image" src="https://github.com/user-attachments/assets/a7ca6bef-06b4-45bc-9294-5c4054189226" />




# Comparing Files
cmp file1 file2
## OUTPUT
<img width="732" height="77" alt="image" src="https://github.com/user-attachments/assets/cd73f251-b6d0-4ec1-af76-bfb300bfcb23" />

 
comm file1 file2
 ## OUTPUT
 <img width="546" height="352" alt="image" src="https://github.com/user-attachments/assets/3102d6ea-ae96-43bd-b716-d3fe8155c220" />


 
diff file1 file2
## OUTPUT
<img width="730" height="436" alt="image" src="https://github.com/user-attachments/assets/4c36183f-75de-4357-a4d9-58379f737d5b" />



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
<img width="682" height="295" alt="image" src="https://github.com/user-attachments/assets/12b10723-f30d-421b-907c-ade05a080072" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="692" height="125" alt="image" src="https://github.com/user-attachments/assets/f331822f-2aa0-43e6-a062-b40b524db113" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="667" height="122" alt="image" src="https://github.com/user-attachments/assets/4e267c33-fa66-4dd5-9cc6-c8f0ed5d8e32" />



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
<img width="502" height="67" alt="image" src="https://github.com/user-attachments/assets/7cc6a455-8c27-4c36-aef2-b579c0c3340b" />




grep hello newfile 
## OUTPUT
<img width="417" height="62" alt="image" src="https://github.com/user-attachments/assets/778c2c61-49c7-4174-8fc2-7ef6bd562056" />





grep -v hello newfile 
## OUTPUT
<img width="332" height="66" alt="image" src="https://github.com/user-attachments/assets/3af6bbc8-7184-423a-b362-28a0bcf0ff28" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="431" height="97" alt="image" src="https://github.com/user-attachments/assets/1112db69-7728-4d43-b560-b875485e66e4" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="437" height="75" alt="image" src="https://github.com/user-attachments/assets/ee38dcfe-86a6-4743-9710-f31c7f882ff5" />





grep -R ubuntu /etc
## OUTPUT
<img width="807" height="657" alt="image" src="https://github.com/user-attachments/assets/958d2c79-c387-4f5c-943d-616ef069290f" />




grep -w -n world newfile   
## OUTPUT
<img width="607" height="155" alt="image" src="https://github.com/user-attachments/assets/a6e6025d-64bb-4e6a-ba1c-998836617ab1" />



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
<img width="550" height="102" alt="image" src="https://github.com/user-attachments/assets/41014c7f-5f55-4268-8068-5c74ff84b20e" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="427" height="92" alt="image" src="https://github.com/user-attachments/assets/abd4d81d-52f7-4045-8f22-1fd4715f0047" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="710" height="160" alt="image" src="https://github.com/user-attachments/assets/1fa4f661-1cac-4180-ab9c-fdf89eb6302f" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="742" height="135" alt="image" src="https://github.com/user-attachments/assets/a56eb76b-aa41-4b0a-8674-5babcfe8e6a8" />




egrep '(world$)' newfile 
## OUTPUT
<img width="767" height="105" alt="image" src="https://github.com/user-attachments/assets/7c936ddd-7304-49be-9cd1-75ae89da35c7" />





egrep '(World$)' newfile 
## OUTPUT
<img width="767" height="132" alt="image" src="https://github.com/user-attachments/assets/f1d9f186-6742-4273-bfea-1187dbede987" />




egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="740" height="130" alt="image" src="https://github.com/user-attachments/assets/920a466e-dbe4-4431-8216-18084123f0af" />





egrep '[1-9]' newfile 
## OUTPUT
<img width="756" height="72" alt="image" src="https://github.com/user-attachments/assets/27cec293-7547-47a1-9380-cc9eb071e329" />





egrep 'Linux.*world' newfile 
## OUTPUT
<img width="762" height="76" alt="image" src="https://github.com/user-attachments/assets/1f7e4a20-c478-4883-9ee3-e80c391390bf" />




egrep 'Linux.*World' newfile 
## OUTPUT
<img width="752" height="72" alt="image" src="https://github.com/user-attachments/assets/52b73b1a-6dce-4d36-a2ba-54b52715364d" />



egrep l{2} newfile
## OUTPUT
<img width="677" height="95" alt="image" src="https://github.com/user-attachments/assets/c413570c-190a-4c99-bea7-373cad392f18" />




egrep 's{1,2}' newfile
## OUTPUT
<img width="712" height="130" alt="image" src="https://github.com/user-attachments/assets/92f8bd25-1c32-4a32-90a2-77906e13ddfe" />




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
<img width="812" height="81" alt="image" src="https://github.com/user-attachments/assets/938b4eb6-9bb8-44db-b227-7277575d0f31" />




sed -n -e '$p' file23
## OUTPUT
<img width="730" height="77" alt="image" src="https://github.com/user-attachments/assets/5d9317dc-2606-450e-aeb5-e92b93aac46d" />





sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="752" height="247" alt="image" src="https://github.com/user-attachments/assets/311c8a75-b81b-44b1-b8e0-093c6565bb06" />





sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="707" height="252" alt="image" src="https://github.com/user-attachments/assets/709a73d6-2cd1-4d4f-9dfc-d4a52e05086e" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="766" height="252" alt="image" src="https://github.com/user-attachments/assets/2012365d-89a4-4887-a6f5-4b4afd8e7c27" />





sed -n -e '1,5p' file23
## OUTPUT
<img width="677" height="171" alt="image" src="https://github.com/user-attachments/assets/7247d0fc-85d9-4a41-946c-8ad1b9a54c88" />





sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="777" height="126" alt="image" src="https://github.com/user-attachments/assets/e3039b6d-351f-456a-bcb2-0a66004ffec7" />






sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="687" height="102" alt="image" src="https://github.com/user-attachments/assets/b5615b2f-29dc-4305-8fe8-2773f71eb79b" />





seq 10 
## OUTPUT
<img width="586" height="300" alt="image" src="https://github.com/user-attachments/assets/a97da11b-9438-47f6-8105-35204e1d29ba" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="592" height="127" alt="image" src="https://github.com/user-attachments/assets/e613a276-2356-441c-b58a-fcc1f2b289e6" />





seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="602" height="122" alt="image" src="https://github.com/user-attachments/assets/c709b36b-ee97-4d6d-9d19-a13ced64c19a" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="597" height="151" alt="image" src="https://github.com/user-attachments/assets/96b4e547-3c83-4349-a770-be77728fa4dc" />





seq 2 | sed '2i hello'
## OUTPUT
<img width="601" height="127" alt="image" src="https://github.com/user-attachments/assets/4617a3cf-32bd-4c4f-80f8-3d7e02801666" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="656" height="127" alt="image" src="https://github.com/user-attachments/assets/4df1bfe0-694e-40c3-a7b9-5134af2be9a3" />




sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="695" height="122" alt="image" src="https://github.com/user-attachments/assets/32570c1a-f359-4f4e-be4e-90b65fd83bf9" />





sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="701" height="125" alt="image" src="https://github.com/user-attachments/assets/fca6f754-e4d0-487a-8a9f-4aaeacd9831d" />



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
<img width="712" height="175" alt="image" src="https://github.com/user-attachments/assets/7278f907-0acb-4551-946c-79e9056ce0ae" />



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
<img width="656" height="175" alt="image" src="https://github.com/user-attachments/assets/fdcbc7b6-c2ef-47fc-bfea-02f51857e8e0" />





#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="712" height="250" alt="image" src="https://github.com/user-attachments/assets/45f23a34-7d51-4f96-abba-d896d5742e9e" />


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

cd backupdir
 
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
