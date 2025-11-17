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
<img width="501" height="170" alt="Screenshot from 2025-11-17 17-06-11" src="https://github.com/user-attachments/assets/9584bf75-e714-4513-b065-9c9e27195516" />



cat < file2
## OUTPUT
<img width="501" height="170" alt="Screenshot from 2025-11-17 17-06-39" src="https://github.com/user-attachments/assets/7c8c44bb-cf8a-419a-ae85-5e7642c715df" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="555" height="165" alt="Screenshot from 2025-11-17 17-07-33" src="https://github.com/user-attachments/assets/c933a029-f8d1-469d-a934-7875cb633f87" />

comm file1 file2
 ## OUTPUT
<img width="622" height="329" alt="Screenshot from 2025-11-17 17-07-57" src="https://github.com/user-attachments/assets/2db66a57-8e5a-4844-af99-10e3835b4815" />

 
diff file1 file2
## OUTPUT
<img width="622" height="317" alt="Screenshot from 2025-11-17 17-08-35" src="https://github.com/user-attachments/assets/03925d40-fdf9-4105-b141-1be533bc2938" />


## Filters

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
<img width="616" height="114" alt="Screenshot from 2025-11-17 17-15-17" src="https://github.com/user-attachments/assets/951b71f3-0fb2-4af7-9f37-fad9428c4051" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="654" height="125" alt="Screenshot from 2025-11-17 17-17-56" src="https://github.com/user-attachments/assets/8ec7ca04-2e17-47e4-963d-65393afe10eb" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="654" height="125" alt="Screenshot from 2025-11-17 17-18-41" src="https://github.com/user-attachments/assets/c93b9c01-5f0d-4da0-af30-ef07975a664d" />


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

<img width="640" height="119" alt="Screenshot from 2025-11-17 17-48-07" src="https://github.com/user-attachments/assets/e74cb12a-1d4e-4827-b9a8-bdf23a11a7aa" />


grep hello newfile 
## OUTPUT

<img width="576" height="119" alt="Screenshot from 2025-11-17 17-48-40" src="https://github.com/user-attachments/assets/04bb3c63-9cec-4058-99d6-58a90ff9e4f2" />



grep -v hello newfile 
## OUTPUT
<img width="619" height="119" alt="Screenshot from 2025-11-17 17-49-36" src="https://github.com/user-attachments/assets/1a35cfac-ff2f-433d-80d1-1c577e2c4efb" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="700" height="119" alt="Screenshot from 2025-11-17 17-51-57" src="https://github.com/user-attachments/assets/8c1faff2-e793-4f98-a847-778021993d56" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="712" height="100" alt="Screenshot from 2025-11-17 17-54-07" src="https://github.com/user-attachments/assets/e7ebc797-f7f0-4adb-bc1c-29764a0537a8" />




grep -R ubuntu /etc
## OUTPUT
<img width="1222" height="731" alt="Screenshot from 2025-11-17 17-55-29" src="https://github.com/user-attachments/assets/007ef3dc-fbe6-4b04-9519-7176d6fe2277" />



grep -w -n world newfile   
## OUTPUT
<img width="632" height="113" alt="Screenshot from 2025-11-17 17-56-56" src="https://github.com/user-attachments/assets/0eeb46f0-3fcd-4364-ac64-a674e89cbc29" />


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
<img width="716" height="101" alt="Screenshot from 2025-11-17 18-08-09" src="https://github.com/user-attachments/assets/2e35769b-98fd-4b64-80ad-5f36b796f37b" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="716" height="101" alt="Screenshot from 2025-11-17 18-08-29" src="https://github.com/user-attachments/assets/51928ab8-59ea-4786-9850-74a9cd9f7395" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="716" height="101" alt="Screenshot from 2025-11-17 18-10-03" src="https://github.com/user-attachments/assets/def2af7c-f4f0-4be6-ba55-03ce026cbbc6" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="716" height="101" alt="Screenshot from 2025-11-17 18-10-45" src="https://github.com/user-attachments/assets/8565de99-1ec9-4599-813c-abfcce7596b6" />



egrep '(world$)' newfile 
## OUTPUT
<img width="716" height="101" alt="Screenshot from 2025-11-17 18-11-49" src="https://github.com/user-attachments/assets/0d697428-1782-4ab5-882e-ee87df348379" />



egrep '(World$)' newfile 
## OUTPUT
<img width="716" height="101" alt="Screenshot from 2025-11-17 18-15-37" src="https://github.com/user-attachments/assets/b29bca44-b4b8-4214-9bc4-b125be8da0a6" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="743" height="135" alt="Screenshot from 2025-11-17 18-17-50" src="https://github.com/user-attachments/assets/1ba2d805-0eb7-421b-a77e-50d07d4e54a2" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="598" height="81" alt="Screenshot from 2025-11-17 18-19-12" src="https://github.com/user-attachments/assets/08baae40-3e29-4b8f-bbbd-b3ec1047e679" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="684" height="88" alt="Screenshot from 2025-11-17 18-19-50" src="https://github.com/user-attachments/assets/79e425b2-8695-4775-b2f2-b73109f6bba1" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="699" height="96" alt="Screenshot from 2025-11-17 18-20-31" src="https://github.com/user-attachments/assets/9de2603e-5441-473c-be49-0a85614587b1" />


egrep l{2} newfile
## OUTPUT
<img width="699" height="96" alt="Screenshot from 2025-11-17 18-21-02" src="https://github.com/user-attachments/assets/1b041a30-6c5d-418c-af75-0d2380fcebfe" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="704" height="128" alt="Screenshot from 2025-11-17 18-22-56" src="https://github.com/user-attachments/assets/d6b2c9e4-d555-4531-bef7-4d5cd38e772b" />


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

<img width="704" height="128" alt="Screenshot from 2025-11-17 18-24-27" src="https://github.com/user-attachments/assets/1c074823-f8b1-4bec-84fe-d91c94991c66" />


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="691" height="238" alt="Screenshot from 2025-11-17 18-26-18" src="https://github.com/user-attachments/assets/8b741f50-3981-4330-9669-7c69f82b6bef" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="691" height="238" alt="Screenshot from 2025-11-17 18-27-11" src="https://github.com/user-attachments/assets/2acf5e8f-dfbf-4f8d-b933-8db071c678ba" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="693" height="221" alt="Screenshot from 2025-11-17 18-28-06" src="https://github.com/user-attachments/assets/066aebfd-aa26-4752-b583-57dddb699159" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="621" height="188" alt="Screenshot from 2025-11-17 18-28-56" src="https://github.com/user-attachments/assets/644a6b45-b303-47bd-8d31-5b96394aedb7" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="670" height="188" alt="Screenshot from 2025-11-17 18-29-31" src="https://github.com/user-attachments/assets/835220b0-2799-4e0c-a899-29b41f00c322" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="708" height="130" alt="Screenshot from 2025-11-17 18-30-59" src="https://github.com/user-attachments/assets/9708d695-56c9-465c-9123-edeb38773696" />


seq 10 
## OUTPUT
<img width="718" height="266" alt="Screenshot from 2025-11-17 18-31-44" src="https://github.com/user-attachments/assets/ac01cbd1-bada-4e9f-89a3-fa2c022ab0e1" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="703" height="152" alt="Screenshot from 2025-11-17 18-32-27" src="https://github.com/user-attachments/assets/e8ea5668-7639-48a9-ae3c-a5c28cbb674d" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="703" height="152" alt="Screenshot from 2025-11-17 18-34-02" src="https://github.com/user-attachments/assets/59b08547-1340-4da4-a253-e91f9f03bb6f" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="703" height="152" alt="Screenshot from 2025-11-17 18-34-29" src="https://github.com/user-attachments/assets/66c0c68e-90d0-4e41-8227-c7010799b612" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="703" height="152" alt="Screenshot from 2025-11-17 18-35-30" src="https://github.com/user-attachments/assets/09123d27-a907-4fde-9130-ed9cfb7fd07b" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="703" height="152" alt="Screenshot from 2025-11-17 18-36-32" src="https://github.com/user-attachments/assets/22c7ec5c-f673-4e2b-923f-963aea6b35e6" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="709" height="164" alt="Screenshot from 2025-11-17 18-41-45" src="https://github.com/user-attachments/assets/fe1bdb27-aa5c-4654-9070-d13ad9e8d9c1" />



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
<img width="624" height="188" alt="Screenshot from 2025-11-17 23-13-44" src="https://github.com/user-attachments/assets/0aa439a3-07c2-4000-a105-bab34c6e7468" />


# RESULT:
The Commands are executed successfully.
