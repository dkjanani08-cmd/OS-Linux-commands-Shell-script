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
<img width="340" height="147" alt="Screenshot 2026-05-25 110421" src="https://github.com/user-attachments/assets/e6822d2f-5b5e-4ad4-a36e-a54d3b8c9ac0" />



cat < file2
## OUTPUT

<img width="319" height="205" alt="Screenshot 2026-05-25 111600" src="https://github.com/user-attachments/assets/933d3773-9f41-4468-ae8c-51a7f1ecec6d" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="382" height="77" alt="Screenshot 2026-05-25 111747" src="https://github.com/user-attachments/assets/106f3742-86d3-4ca7-ab17-f188f030c8a3" />

comm file1 file2
 ## OUTPUT
<img width="411" height="207" alt="Screenshot 2026-05-25 111912" src="https://github.com/user-attachments/assets/b0fae319-dac0-458a-9579-fc80e578690d" />

 
diff file1 file2
## OUTPUT
<img width="349" height="271" alt="Screenshot 2026-05-25 112039" src="https://github.com/user-attachments/assets/e5d9b745-9903-44aa-ac73-3f33ea92d981" />


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


<img width="305" height="125" alt="Screenshot 2026-05-25 112323" src="https://github.com/user-attachments/assets/808fc93a-ffaf-4957-bd49-8b7a067a4972" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="382" height="146" alt="Screenshot 2026-05-25 112937" src="https://github.com/user-attachments/assets/b356b272-0ac5-4ea3-bd25-894dea3e573d" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="357" height="156" alt="Screenshot 2026-05-25 112525" src="https://github.com/user-attachments/assets/2d5a5e39-cebb-443d-9704-0f1d2f957e64" />


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

<img width="249" height="98" alt="Screenshot 2026-05-25 230511" src="https://github.com/user-attachments/assets/00b8ea35-4bed-4a23-ac89-5fa81b8f4cdf" />


grep hello newfile 
## OUTPUT


<img width="298" height="69" alt="Screenshot 2026-05-25 230619" src="https://github.com/user-attachments/assets/721d8f2b-8870-48dd-8e3d-9957c701366a" />



grep -v hello newfile 
## OUTPUT


<img width="298" height="69" alt="Screenshot 2026-05-25 230619" src="https://github.com/user-attachments/assets/0704cfcf-e6b3-4510-9e89-ede21c341d34" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="625" height="96" alt="Screenshot 2026-05-25 230751" src="https://github.com/user-attachments/assets/de973cba-9af8-4dec-975a-3cfe47b13894" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="625" height="96" alt="Screenshot 2026-05-25 230751" src="https://github.com/user-attachments/assets/fd5fb292-9b6a-4488-aab7-f594be564dd3" />



grep -R ubuntu /etc
## OUTPUT


<img width="809" height="256" alt="Screenshot 2026-05-26 004444" src="https://github.com/user-attachments/assets/cc35d5b8-fbca-4016-8a11-ce5fcafc5568" />


grep -w -n world newfile   
## OUTPUT


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


<img width="418" height="98" alt="Screenshot 2026-05-26 004044" src="https://github.com/user-attachments/assets/fda2f4e5-bb75-4dae-9899-e73216851807" />




egrep -w '(H|h)ello' newfile 
## OUTPUT




<img width="386" height="100" alt="Screenshot 2026-05-26 004051" src="https://github.com/user-attachments/assets/f2886fba-ac73-4a9c-9641-a7b406118679" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="407" height="98" alt="Screenshot 2026-05-26 005517" src="https://github.com/user-attachments/assets/56fc75a4-dc5c-4210-8e3e-4d062ea32456" />




egrep '(^hello)' newfile 
## OUTPUT


<img width="317" height="75" alt="Screenshot 2026-05-26 005537" src="https://github.com/user-attachments/assets/61ee8c00-6956-4162-a422-9499977b0640" />



egrep '(world$)' newfile 
## OUTPUT


<img width="363" height="91" alt="Screenshot 2026-05-26 005551" src="https://github.com/user-attachments/assets/02118154-32fa-45b1-a2b2-3c63b443239f" />


egrep '(World$)' newfile 
## OUTPUT

<img width="396" height="76" alt="Screenshot 2026-05-26 005606" src="https://github.com/user-attachments/assets/15d14a22-978a-4426-9e6c-792a5961aa3e" />




egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="394" height="100" alt="Screenshot 2026-05-26 005621" src="https://github.com/user-attachments/assets/a605971f-62a2-4670-aa48-91e84f7033a1" />




egrep '[1-9]' newfile 
## OUTPUT

<img width="386" height="73" alt="Screenshot 2026-05-26 005652" src="https://github.com/user-attachments/assets/89d8680d-fc63-4ebd-afb8-8821e9588530" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="393" height="79" alt="Screenshot 2026-05-26 005710" src="https://github.com/user-attachments/assets/577e1034-07de-4afb-b5ee-0318757ce098" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="381" height="78" alt="Screenshot 2026-05-26 005727" src="https://github.com/user-attachments/assets/b5f366c5-844b-45ef-8186-8cfb51c1d69a" />


egrep l{2} newfile
## OUTPUT


<img width="348" height="91" alt="Screenshot 2026-05-26 005735" src="https://github.com/user-attachments/assets/1365be8d-76af-410f-a30f-cc2eb2509f05" />


egrep 's{1,2}' newfile
## OUTPUT 


<img width="369" height="120" alt="Screenshot 2026-05-26 005744" src="https://github.com/user-attachments/assets/2cdfb1aa-e45d-46e0-b7e1-827343395483" />

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


<img width="366" height="266" alt="Screenshot 2026-05-26 005752" src="https://github.com/user-attachments/assets/4d938386-8c52-467c-a576-adf42771850f" />


sed -n -e '3p' file23
## OUTPUT

<img width="396" height="69" alt="Screenshot 2026-05-26 005804" src="https://github.com/user-attachments/assets/3ee7eddb-1c0b-474f-99c6-25571ba3d6be" />



sed -n -e '$p' file23
## OUTPUT

<img width="347" height="72" alt="Screenshot 2026-05-26 005811" src="https://github.com/user-attachments/assets/9a6d1410-c799-498f-81d7-40de4d95b804" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="464" height="280" alt="Screenshot 2026-05-26 005819" src="https://github.com/user-attachments/assets/abede824-2da3-4e4e-bfc7-f07ccdc50a6d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="432" height="273" alt="Screenshot 2026-05-26 005831" src="https://github.com/user-attachments/assets/af183d46-0449-47ef-8bae-d1191c5af51e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="414" height="80" alt="Screenshot 2026-05-26 005846" src="https://github.com/user-attachments/assets/610f2b89-fa6c-4146-bdff-f245459cc3a8" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="456" height="177" alt="Screenshot 2026-05-26 005856" src="https://github.com/user-attachments/assets/ddee6fea-4dad-4809-ac7b-73f9d36b0037" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="489" height="124" alt="Screenshot 2026-05-26 005903" src="https://github.com/user-attachments/assets/87d3936a-e22e-489e-8132-26e257bde052" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="475" height="95" alt="Screenshot 2026-05-26 005911" src="https://github.com/user-attachments/assets/689cfeeb-493a-45ca-8b02-cee15cd20080" />


seq 10 
## OUTPUT


<img width="429" height="300" alt="Screenshot 2026-05-26 005920" src="https://github.com/user-attachments/assets/1afe4fcc-0393-4f6c-a983-a62e164aaaa6" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="365" height="129" alt="Screenshot 2026-05-26 005928" src="https://github.com/user-attachments/assets/ce352d81-f5f2-4c4d-85d6-5ddb47889eba" />



seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="322" height="129" alt="Screenshot 2026-05-26 005944" src="https://github.com/user-attachments/assets/450bd4f4-05da-41a8-a34b-0da6858963d8" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="346" height="155" alt="Screenshot 2026-05-26 005952" src="https://github.com/user-attachments/assets/53a82c25-c345-4f14-9091-5577dccf4cdd" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="286" height="129" alt="Screenshot 2026-05-26 010003" src="https://github.com/user-attachments/assets/8590d152-67e1-4d0b-a143-d1117aa767e0" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="368" height="124" alt="Screenshot 2026-05-26 010015" src="https://github.com/user-attachments/assets/62afb49b-309a-4556-b3ee-e30b5d0b45b7" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="460" height="123" alt="Screenshot 2026-05-26 010034" src="https://github.com/user-attachments/assets/fb909ff6-faef-4831-ba3d-88799852bb5e" />


sed -n '2,4{s/$/*/;p}' file23

<img width="402" height="118" alt="Screenshot 2026-05-26 010047" src="https://github.com/user-attachments/assets/c0a5f45f-a881-4dda-9aaf-b832e36e7d3c" />


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

<img width="382" height="175" alt="Screenshot 2026-05-26 011341" src="https://github.com/user-attachments/assets/e0da2841-a979-44cd-9816-2b0befb5eb34" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="557" height="275" alt="Screenshot 2026-05-26 011348" src="https://github.com/user-attachments/assets/25338f55-172f-4f74-98a5-049020918c50" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="373" height="153" alt="Screenshot 2026-05-26 011405" src="https://github.com/user-attachments/assets/017e5ecd-a278-4b8d-a39f-d97c020f3f4b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="408" height="156" alt="Screenshot 2026-05-26 011419" src="https://github.com/user-attachments/assets/2a29bf2d-9802-4879-9738-84d16a7a080c" />


tar -xvf backup.tar
## OUTPUT

<img width="553" height="165" alt="Screenshot 2026-05-26 011426" src="https://github.com/user-attachments/assets/185d4cad-3f3e-46e7-8aac-1ae310281f46" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="559" height="49" alt="Screenshot 2026-05-26 011441" src="https://github.com/user-attachments/assets/84cf511e-8abd-4c0b-ad85-5ecef73e55ec" />

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
