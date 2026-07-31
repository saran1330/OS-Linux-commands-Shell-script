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
<img width="587" height="297" alt="os 5" src="https://github.com/user-attachments/assets/079f3991-d8ac-46db-a2ac-5bd79e959542" />
<img width="695" height="172" alt="os 3" src="https://github.com/user-attachments/assets/922710cb-203a-47c6-b3c3-fc4f71891037" />





cat < file2
## OUTPUT
<img width="697" height="272" alt="os 2" src="https://github.com/user-attachments/assets/57ab329c-af04-42cf-ade8-638737e6f104" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="587" height="297" alt="os 5" src="https://github.com/user-attachments/assets/c461a02e-9eca-4f6c-9a5b-24d3a52a633f" />

 
comm file1 file2
 ## OUTPUT
<img width="697" height="172" alt="os 4" src="https://github.com/user-attachments/assets/2e2ba079-0c40-42e7-b5f0-12d519a02a77" />

 
diff file1 file2
## OUTPUT
<img width="686" height="271" alt="os 6" src="https://github.com/user-attachments/assets/5444ebb1-92bb-440f-b61d-50d0bfdc11d4" />



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
<img width="657" height="181" alt="os 7" src="https://github.com/user-attachments/assets/5a81e9f8-8f4c-4a29-91a7-479889b53b57" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="676" height="120" alt="os 8" src="https://github.com/user-attachments/assets/79e9b204-5fb8-4253-936e-b06b861f77d7" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="632" height="127" alt="os 9" src="https://github.com/user-attachments/assets/88efa0c1-bc29-46c5-81de-f40ed0d3e073" />



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





grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT
<img width="712" height="537" alt="os 15" src="https://github.com/user-attachments/assets/2ed604bf-5819-4e65-991f-6b485684a0d8" />



grep -w -n world newfile   
## OUTPUT
<img width="442" height="95" alt="os 16" src="https://github.com/user-attachments/assets/278858e0-3de9-42fd-b427-533cc5a11090" />



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
<img width="641" height="105" alt="os 17" src="https://github.com/user-attachments/assets/e524ded3-d3be-4a6c-a0d1-6caffab7a52a" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="585" height="96" alt="os 18" src="https://github.com/user-attachments/assets/6d310c98-f27a-47c8-83fb-340d18ec4b47" />






egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="602" height="97" alt="os 19" src="https://github.com/user-attachments/assets/f433ca17-ecf2-4064-a39d-166cf9f4b832" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="602" height="97" alt="os 19" src="https://github.com/user-attachments/assets/5a590437-6a5b-4bb0-894c-7eb6da65aea2" />




egrep '(world$)' newfile 
## OUTPUT
<img width="602" height="102" alt="os 21" src="https://github.com/user-attachments/assets/89a6b7bf-768c-476a-acc7-0495b979c65e" />




egrep '(World$)' newfile 
## OUTPUT
<img width="602" height="102" alt="os 21" src="https://github.com/user-attachments/assets/ef6664d3-eff4-4fa1-919c-0cfe19285348" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="537" height="122" alt="os 22" src="https://github.com/user-attachments/assets/9489eb2b-827c-4f74-99c5-2cbfb8048a5c" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="456" height="77" alt="os 23" src="https://github.com/user-attachments/assets/d393df6a-e855-4310-b002-79b8e594d50e" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="547" height="72" alt="os 24" src="https://github.com/user-attachments/assets/cb46b38d-d883-413a-aa67-4d9c492d690d" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="572" height="77" alt="os 25" src="https://github.com/user-attachments/assets/ffbc2ae0-d6b9-47bc-b46d-893913b80736" />



egrep l{2} newfile
## OUTPUT
<img width="412" height="101" alt="os 26" src="https://github.com/user-attachments/assets/352d3747-be8c-4c7a-8a08-3f1406f79e5a" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="537" height="117" alt="os 27" src="https://github.com/user-attachments/assets/da0f57b8-0cba-4f30-bbc4-e7b151ffed72" />



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
<img width="490" height="107" alt="os 28" src="https://github.com/user-attachments/assets/0fc1cd6e-6f3e-412e-8149-4ede79459cdc" />



sed -n -e '$p' file23
## OUTPUT
<img width="542" height="80" alt="os 29" src="https://github.com/user-attachments/assets/d903dd73-6a0f-4598-af8d-e38b6650d1d1" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="477" height="252" alt="os 30" src="https://github.com/user-attachments/assets/60e6eec6-db5b-4d23-8743-64b6d06046e4" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT<img width="655" height="251" alt="os 31" src="https://github.com/user-attachments/assets/92ece56f-7c9e-457c-ad82-3f55b4e39414" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="630" height="252" alt="os 32" src="https://github.com/user-attachments/assets/6f06e1e3-fe7f-4665-b425-f65e70e7bd01" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="532" height="125" alt="os 34" src="https://github.com/user-attachments/assets/f97228d3-b382-4a18-8f21-c736c0a9c32a" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="532" height="125" alt="os 34" src="https://github.com/user-attachments/assets/2d30953d-0e83-4088-b2ba-03ce162e1bfa" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="532" height="125" alt="os 34" src="https://github.com/user-attachments/assets/bed52cf8-689c-4e90-8d1a-b45f82f28aeb" />




seq 10 
## OUTPUT
<img width="452" height="302" alt="os 35" src="https://github.com/user-attachments/assets/e97d4c12-c17f-43bd-8f5d-414fa06c1c6a" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="432" height="122" alt="os 36" src="https://github.com/user-attachments/assets/7d98e1c6-c6f3-4241-afd7-ef744b8257a6" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="505" height="130" alt="os 37" src="https://github.com/user-attachments/assets/e2c7c6c1-09b9-4320-98ee-784579b97004" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="587" height="151" alt="os 38" src="https://github.com/user-attachments/assets/7ac35f02-5177-4658-9f56-81fa3cfd5816" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="602" height="117" alt="os 39" src="https://github.com/user-attachments/assets/092d6112-5c26-42e4-8c73-f6de6b2d1d28" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="537" height="127" alt="os 40" src="https://github.com/user-attachments/assets/38cba446-7732-4001-b4aa-4c4ca4942b1f" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="471" height="222" alt="OS 43" src="https://github.com/user-attachments/assets/7c6a9f54-5797-490a-b289-8cba839980f9" />



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

<img width="471" height="222" alt="OS 43" src="https://github.com/user-attachments/assets/d4026b0f-0e2d-48f6-8b07-1c3ded5c31c2" />



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
<img width="502" height="181" alt="OS 44" src="https://github.com/user-attachments/assets/d3165b1e-ee34-4a55-9a00-4e6625a9f5c3" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="512" height="276" alt="OS 45" src="https://github.com/user-attachments/assets/2b781da6-5a38-4b6d-ae18-c5982ec92e63" />


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
 <img width="532" height="131" alt="OS 46" src="https://github.com/user-attachments/assets/a8d242e9-f276-42bd-aed0-80d94d3821af" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="552" height="126" alt="OS 47" src="https://github.com/user-attachments/assets/20673a22-4f4c-41e1-8a7d-382612a1e13d" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="652" height="356" alt="OS 48" src="https://github.com/user-attachments/assets/efad4190-0dcd-476d-adca-e9c5585d1929" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="705" height="592" alt="OS 49" src="https://github.com/user-attachments/assets/6b0d5462-7656-4f5b-a079-4baf78814dfb" />



tar -xvf backup.tar
## OUTPUT

<img width="592" height="417" alt="OS 50" src="https://github.com/user-attachments/assets/b71fd3cc-a5f3-452c-8b53-b9482d987874" />


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
<img width="422" height="120" alt="OS 51" src="https://github.com/user-attachments/assets/41e944fd-2594-489c-bf01-66fe065c27e8" />



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
<img width="812" height="437" alt="OS 52" src="https://github.com/user-attachments/assets/7011dcfe-76f3-484c-8120-5c4e46e4773c" />



 
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
<img width="511" height="97" alt="OS 53" src="https://github.com/user-attachments/assets/b6d9c886-81fd-429a-b681-ba7183cac654" />


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
<img width="640" height="512" alt="OS 54" src="https://github.com/user-attachments/assets/55f0542e-9942-46e5-8ffc-6d05208eea05" />




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

<img width="527" height="411" alt="OS 55" src="https://github.com/user-attachments/assets/3d293dda-2b94-412d-bb7d-1afd1fd7b807" />



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

<img width="546" height="512" alt="OS 56" src="https://github.com/user-attachments/assets/7d2f9988-fbf5-462d-b5c9-911bbc086fad" />


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

<img width="647" height="237" alt="OS 57" src="https://github.com/user-attachments/assets/58013877-b60f-4b1e-93af-deda3160ec80" />



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

<img width="551" height="191" alt="OS 58" src="https://github.com/user-attachments/assets/9e2ac327-3d41-4440-a930-6c4dc75979d6" />


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
<img width="481" height="236" alt="OS 65" src="https://github.com/user-attachments/assets/ce0e88f6-4cff-40a4-b7fc-b84acef468bd" />



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

<img width="357" height="232" alt="OS 66" src="https://github.com/user-attachments/assets/cae45d9b-65f7-4307-af96-5d444182e544" />


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

<img width="502" height="240" alt="OS 67" src="https://github.com/user-attachments/assets/82075882-177d-417a-b4f3-8883273aa258" />


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

 <img width="436" height="500" alt="OS 68" src="https://github.com/user-attachments/assets/4b5fc8fe-f4b8-40bf-9f29-c6a8dba9a3cb" />


 
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
<img width="382" height="107" alt="OS 69" src="https://github.com/user-attachments/assets/2734e440-00b2-44e6-a479-4face8a6b664" />


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
<img width="465" height="231" alt="OS 70" src="https://github.com/user-attachments/assets/88aebb07-0e34-4304-95aa-26ffa8abdafb" />

 
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

<img width="551" height="112" alt="OS 71" src="https://github.com/user-attachments/assets/c21e97fd-44e9-4753-9b2c-3f9609d49dd3" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="581" height="121" alt="OS 72" src="https://github.com/user-attachments/assets/002f8468-084d-4c25-9e3f-316e0d11fe1d" />




$ ./exread1.sh 

<img width="581" height="121" alt="OS 72" src="https://github.com/user-attachments/assets/7f9f7c6c-8b08-432e-8a23-391948807b29" />

 
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
<img width="482" height="87" alt="OS 73" src="https://github.com/user-attachments/assets/c8ef4d56-2c93-40ac-973b-a75ac3f6bb16" />


 
 ./funcex.sh 1 2
 <img width="382" height="87" alt="OS 74" src="https://github.com/user-attachments/assets/9c3a573a-716b-42e1-94b7-e9408486253b" />


 
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

<img width="421" height="155" alt="OS 76" src="https://github.com/user-attachments/assets/8b50818c-3459-40e3-b381-4a1f07588f0c" />

 
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

 <img width="732" height="605" alt="OS 77" src="https://github.com/user-attachments/assets/b37b9ccc-1c19-4800-a5fd-9df7ac30471e" />

 
 
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

<img width="527" height="562" alt="OS 78" src="https://github.com/user-attachments/assets/f06444b9-595a-47af-9a10-edef1cb7f2b3" />

 
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

<img width="462" height="662" alt="OS 80" src="https://github.com/user-attachments/assets/f574be6f-bc58-41b4-a952-fdb25c0a1fa9" />



# RESULT:
The Commands are executed successfully.
