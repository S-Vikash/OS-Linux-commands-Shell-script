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
<img width="264" height="194" alt="image" src="https://github.com/user-attachments/assets/ad569e85-d419-45ca-a30b-41eac551949d" />


cat < file2
## OUTPUT
<img width="252" height="197" alt="image" src="https://github.com/user-attachments/assets/86df2a91-f073-48b2-bedb-8bf06d04104e" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="356" height="73" alt="image" src="https://github.com/user-attachments/assets/1da2e740-0e0d-411d-8fa0-3158654e8a51" />

 
comm file1 file2
 ## OUTPUT
<img width="358" height="292" alt="image" src="https://github.com/user-attachments/assets/76aea9ce-bf98-4fd4-85c0-0d3c7bb91dcb" />

 
diff file1 file2
## OUTPUT
<img width="256" height="300" alt="image" src="https://github.com/user-attachments/assets/80b19b2e-25c7-4f4e-940f-4d9c48337f04" />


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
<img width="335" height="149" alt="image" src="https://github.com/user-attachments/assets/3c403807-f521-4d69-a217-fb9f209986a7" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="300" height="129" alt="image" src="https://github.com/user-attachments/assets/5082b544-fe8b-45c2-89cd-8105138e1d8d" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="295" height="125" alt="image" src="https://github.com/user-attachments/assets/7c21df29-23cb-43a5-9348-df404cd9e352" />


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
<img width="351" height="176" alt="image" src="https://github.com/user-attachments/assets/45344b2c-1d6e-4609-9efd-6c8a3129ac27" />



grep hello newfile 
## OUTPUT
<img width="308" height="76" alt="image" src="https://github.com/user-attachments/assets/81425cd4-eb6f-4c7e-ad65-8d399c79235c" />


grep -v hello newfile 
## OUTPUT
<img width="302" height="72" alt="image" src="https://github.com/user-attachments/assets/0548157a-e7a0-4b29-b0a6-83011f39997f" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="357" height="102" alt="image" src="https://github.com/user-attachments/assets/008f2f48-1e03-4b40-9c5c-9ea08f4f1351" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="387" height="75" alt="image" src="https://github.com/user-attachments/assets/0e15aca6-738b-4075-bddb-bbdcb282cb48" />



grep -R ubuntu /etc
## OUTPUT



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
<img width="373" height="98" alt="image" src="https://github.com/user-attachments/assets/04c5fb3e-499d-4060-8169-810791738ca1" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="348" height="106" alt="image" src="https://github.com/user-attachments/assets/7d075613-d489-4c3e-b14e-ebb5f992f4e9" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="384" height="102" alt="image" src="https://github.com/user-attachments/assets/aa1fc003-d9db-4d96-bc69-59d496640a27" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="325" height="79" alt="image" src="https://github.com/user-attachments/assets/b2d3b01e-b85f-4904-8ee7-09042ac299b6" />


egrep '(world$)' newfile 
## OUTPUT
<img width="311" height="100" alt="image" src="https://github.com/user-attachments/assets/26b79052-9b0d-440e-9ba4-ed55c6ffb038" />


egrep '(World$)' newfile 
## OUTPUT
<img width="318" height="74" alt="image" src="https://github.com/user-attachments/assets/15c6cf47-c00c-44f5-b913-039bb662efab" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="343" height="130" alt="image" src="https://github.com/user-attachments/assets/420af861-3d76-4dc5-a300-377e47778de4" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="295" height="80" alt="image" src="https://github.com/user-attachments/assets/7ebee029-c33f-4d02-a964-2efd849b507f" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="351" height="73" alt="image" src="https://github.com/user-attachments/assets/1188da30-9a4d-496e-aeda-3be864f9a07a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="346" height="75" alt="image" src="https://github.com/user-attachments/assets/ced69f78-e18a-46c5-bcd5-6ff39c25d9c5" />


egrep l{2} newfile
## OUTPUT
<img width="290" height="99" alt="image" src="https://github.com/user-attachments/assets/88f516d8-4e2f-465e-b1c7-52a786628a5b" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="294" height="131" alt="image" src="https://github.com/user-attachments/assets/538d7779-75ac-4626-9e72-1dee1545bee5" />


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
<img width="442" height="373" alt="image" src="https://github.com/user-attachments/assets/3bc48591-9e37-40f0-8207-9375ee695732" />



sed -n -e '$p' file23
## OUTPUT
<img width="304" height="74" alt="image" src="https://github.com/user-attachments/assets/6da10369-891f-4590-8fae-97fbb2231e59" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="356" height="253" alt="image" src="https://github.com/user-attachments/assets/04bf4fab-a38f-4877-91dc-9bc36087e58e" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="357" height="245" alt="image" src="https://github.com/user-attachments/assets/b26d5ac1-0154-44de-b4d7-176ccba72565" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="385" height="258" alt="image" src="https://github.com/user-attachments/assets/cea2af70-f846-4242-a1b7-86f043ecc0a5" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="316" height="176" alt="image" src="https://github.com/user-attachments/assets/09a1e02a-b0a1-48d6-be86-fdcb80ea26e5" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="350" height="132" alt="image" src="https://github.com/user-attachments/assets/48c1c82c-7052-40d2-b1da-1d3ff87de154" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="383" height="103" alt="image" src="https://github.com/user-attachments/assets/96bd90c7-f9b5-4f52-9ba8-ef8e3a630c5b" />


seq 10 
## OUTPUT
<img width="293" height="293" alt="image" src="https://github.com/user-attachments/assets/f5f5afe6-c2dc-46c9-8d79-8e7e8b4dac3c" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="288" height="125" alt="image" src="https://github.com/user-attachments/assets/53b899a8-31b7-4271-b69e-7eb1ac363a7e" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="307" height="127" alt="image" src="https://github.com/user-attachments/assets/fc849304-18d1-4993-a254-9eef7c797e68" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="287" height="150" alt="image" src="https://github.com/user-attachments/assets/1eb95fe1-7b39-4ba8-8bb2-c664300a0e10" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="296" height="121" alt="image" src="https://github.com/user-attachments/assets/de98e07d-5dae-46f1-bda3-0f73ecc2e484" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="318" height="125" alt="image" src="https://github.com/user-attachments/assets/8dd35164-0955-4ccf-aa8e-2148f280b241" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="358" height="130" alt="image" src="https://github.com/user-attachments/assets/2161cb54-a878-4e71-a974-ceba1e1b3bd9" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="352" height="136" alt="image" src="https://github.com/user-attachments/assets/b34cdb62-b3c3-4c7d-a20e-426ca76ea427" />


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
<img width="333" height="148" alt="image" src="https://github.com/user-attachments/assets/e7c57469-89d1-4f52-9739-c1314a08ceb1" />


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
<img width="340" height="151" alt="image" src="https://github.com/user-attachments/assets/75f3b789-6082-4f2a-8154-6879f4be5379" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="415" height="254" alt="image" src="https://github.com/user-attachments/assets/bca6f9b2-9dc1-4185-9e4b-62156295cc9c" />


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
<img width="341" height="98" alt="image" src="https://github.com/user-attachments/assets/30b89f26-d465-46a4-b20a-5664f8182996" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="457" height="101" alt="image" src="https://github.com/user-attachments/assets/4f6c192c-dc59-4342-8142-52a78ce019e2" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="296" height="206" alt="image" src="https://github.com/user-attachments/assets/06008157-f2ae-40cf-9359-c023c4dfb0e6" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="609" height="200" alt="image" src="https://github.com/user-attachments/assets/f7106b33-37f3-4dcd-aa2e-8493e9849de1" />


tar -xvf backup.tar
## OUTPUT
<img width="400" height="205" alt="image" src="https://github.com/user-attachments/assets/6eadd279-7c29-4948-8237-fead1a6e04a2" />


gzip backup.tar

ls .gz
 
gunzip backup.tar.gz

 
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
<img width="397" height="130" alt="image" src="https://github.com/user-attachments/assets/de16a8cd-63a7-48cc-b5cf-61f5ac7a39e4" />


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
<img width="308" height="553" alt="image" src="https://github.com/user-attachments/assets/9a98beae-4540-4832-883c-45415f6eeeaa" />

 
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
<img width="396" height="301" alt="image" src="https://github.com/user-attachments/assets/55dc5664-b62c-4f39-99ed-e77d36acf6a5" />


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
<img width="595" height="231" alt="image" src="https://github.com/user-attachments/assets/ebd3d836-053f-4ea2-b08d-99cc3fada1d4" />


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
<img width="453" height="474" alt="image" src="https://github.com/user-attachments/assets/fe3393a3-85fe-4ce6-8794-91d897324248" />



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
<img width="449" height="379" alt="image" src="https://github.com/user-attachments/assets/d47a982a-5885-4ec4-9666-944d442bb82e" />


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
<img width="457" height="471" alt="image" src="https://github.com/user-attachments/assets/cabcada1-21aa-48aa-8669-68d38a37d2b5" />


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
<img width="479" height="229" alt="image" src="https://github.com/user-attachments/assets/34d868e6-3ce9-4b8a-bcb8-36cd1d613316" />



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
<img width="640" height="169" alt="image" src="https://github.com/user-attachments/assets/515e09f6-5241-4f57-b192-252428997cc8" />


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
<img width="503" height="132" alt="image" src="https://github.com/user-attachments/assets/6b1a7fc7-9c94-405b-89b5-a792d3e13935" />


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
 <img width="536" height="268" alt="image" src="https://github.com/user-attachments/assets/e663fceb-49b0-4ef3-b389-4b16c8be74ff" />


 
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
<img width="475" height="101" alt="image" src="https://github.com/user-attachments/assets/56d979b4-6a12-426d-bc11-6e1f51a91c2b" />

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
<img width="491" height="136" alt="image" src="https://github.com/user-attachments/assets/468e2fcf-9fab-4a43-9183-70bb84955fd1" />

 
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
<img width="462" height="99" alt="image" src="https://github.com/user-attachments/assets/ce2e49ea-1cda-44ee-b2fc-191de31b01fd" />

 
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
<img width="507" height="100" alt="image" src="https://github.com/user-attachments/assets/adb5b1fc-76a6-4fdc-b9f4-5c5099fa976e" />

 
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
 <img width="509" height="311" alt="image" src="https://github.com/user-attachments/assets/78e49b43-deb8-409d-a176-da75fb13dcb3" />

 
 
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
<img width="473" height="275" alt="image" src="https://github.com/user-attachments/assets/da12355b-0fe1-4c27-8b47-91cad26b68f2" />

 
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
<img width="523" height="290" alt="image" src="https://github.com/user-attachments/assets/a12056b0-e2cc-4141-9be7-59c40a58d7d7" />


# RESULT:
The Commands are executed successfully.
