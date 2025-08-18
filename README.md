## OS-Linux-commands-Shell-scripting

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

<img width="372" height="155" alt="image" src="https://github.com/user-attachments/assets/cee2df91-66de-42a5-a3bb-7310c3bc453e" />



cat < file2
## OUTPUT

<img width="408" height="181" alt="image" src="https://github.com/user-attachments/assets/2f1260cb-d03c-4004-a378-a4148d6d8b84" />


# Comparing Files

cmp file1 file2
## OUTPUT
<img width="409" height="81" alt="image" src="https://github.com/user-attachments/assets/8fa31cb5-44f9-4e67-9325-9f2c59296b0d" />


comm file1 file2
 ## OUTPUT
<img width="380" height="232" alt="image" src="https://github.com/user-attachments/assets/d5012126-b538-464d-9a9a-21877fc5d467" />

 
diff file1 file2
## OUTPUT
<img width="377" height="281" alt="image" src="https://github.com/user-attachments/assets/f14e1794-e5ef-40f9-98b4-f2100e36b679" />


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
<img width="383" height="106" alt="image" src="https://github.com/user-attachments/assets/64b7e124-8550-406e-b582-198d2c1ecef5" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="364" height="127" alt="image" src="https://github.com/user-attachments/assets/369281a9-202a-4d83-b44a-f4c43b454986" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="387" height="127" alt="image" src="https://github.com/user-attachments/assets/a2b49573-8605-4905-b61e-047c70dea19f" />


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
<img width="383" height="79" alt="image" src="https://github.com/user-attachments/assets/1aac0066-cc53-4d2e-b7b0-4471c6951ace" />



grep hello newfile 
## OUTPUT
<img width="373" height="82" alt="image" src="https://github.com/user-attachments/assets/cebb2d2f-d208-4a8d-b54c-b79720088803" />




grep -v hello newfile 
## OUTPUT
<img width="406" height="82" alt="image" src="https://github.com/user-attachments/assets/fd5f8699-e8be-473e-944d-a2d60136bb50" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="447" height="108" alt="image" src="https://github.com/user-attachments/assets/e8a46144-3e7d-46c8-b861-a8bdbd949173" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="494" height="81" alt="image" src="https://github.com/user-attachments/assets/2afb45ea-820e-4e69-ae15-bc64513c17bf" />




grep -R ubuntu /etc
## OUTPUT
<img width="1557" height="908" alt="Screenshot 2025-08-11 135508" src="https://github.com/user-attachments/assets/e32bb85b-6a59-4766-8bcc-35545a8ef4ba" />





grep -w -n world newfile   
## OUTPUT
<img width="432" height="107" alt="image" src="https://github.com/user-attachments/assets/936567b3-2e9f-4634-83cb-be2b0f31ca18" />





cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
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

<img width="425" height="104" alt="image" src="https://github.com/user-attachments/assets/e04baae2-b1b2-4f6b-bdc2-7be6610eedcb" />




egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="485" height="105" alt="image" src="https://github.com/user-attachments/assets/2872a7a5-c986-41ad-a08d-674afd229143" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="492" height="99" alt="image" src="https://github.com/user-attachments/assets/4b602d3a-cc2e-4cd4-a98d-7d4c517a6c0d" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="478" height="81" alt="image" src="https://github.com/user-attachments/assets/0d754de6-7ae6-4803-9a8a-9a7505d9ce74" />



egrep '(world$)' newfile 
## OUTPUT
<img width="363" height="102" alt="image" src="https://github.com/user-attachments/assets/c6b2a84b-71d8-41b4-aa67-8f81115db72a" />



egrep '(World$)' newfile 
## OUTPUT
<img width="398" height="78" alt="image" src="https://github.com/user-attachments/assets/cacdb215-6f74-43f1-9660-0cc268072b03" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="511" height="132" alt="image" src="https://github.com/user-attachments/assets/4fd2b937-5bcd-4cee-beab-7c29b9244ff2" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="416" height="82" alt="image" src="https://github.com/user-attachments/assets/aefb811d-bb9d-4ce2-bc5d-ec0d9fab0e0f" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="395" height="79" alt="image" src="https://github.com/user-attachments/assets/fe296480-b627-4c0a-b4b7-dd54a22f8f43" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="448" height="79" alt="image" src="https://github.com/user-attachments/assets/67347925-d913-408e-898e-582df072a49c" />


egrep l{2} newfile
## OUTPUT
<img width="438" height="106" alt="image" src="https://github.com/user-attachments/assets/84db0f18-bfba-4176-9829-753d7fc27724" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="417" height="131" alt="image" src="https://github.com/user-attachments/assets/a0b2a5f0-4619-48dc-bef0-1fb613e31a3d" />


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
<img width="348" height="74" alt="image" src="https://github.com/user-attachments/assets/5e108670-a68b-4f79-b9d9-1aaa5e217f7b" />



sed -n -e '$p' file23
## OUTPUT
<img width="467" height="259" alt="image" src="https://github.com/user-attachments/assets/f0a3772a-a924-46d4-8016-803a3ae482e5" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="418" height="257" alt="image" src="https://github.com/user-attachments/assets/2a4c7dd9-6ece-41c3-8075-8a4b9282ec60" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="421" height="259" alt="image" src="https://github.com/user-attachments/assets/ba8183eb-28a3-443c-a6d9-0f93ae584be3" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="458" height="257" alt="image" src="https://github.com/user-attachments/assets/ba2ada2f-8c70-4e36-b326-218a0937b560" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="382" height="185" alt="image" src="https://github.com/user-attachments/assets/cfa38af5-fc99-4e5a-ba7d-70205920761d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="429" height="131" alt="image" src="https://github.com/user-attachments/assets/f643b6b7-ef42-426c-af44-a77a8427dc8c" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="420" height="112" alt="image" src="https://github.com/user-attachments/assets/fd933018-0fa0-4fe3-af35-76cf82ba5b34" />



seq 10 
## OUTPUT
<img width="353" height="305" alt="image" src="https://github.com/user-attachments/assets/d0383342-2cd8-49fc-a845-351b56cf4ecd" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="399" height="134" alt="image" src="https://github.com/user-attachments/assets/f5296643-1545-479e-be6a-f285b8723238" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="402" height="125" alt="image" src="https://github.com/user-attachments/assets/3b5757d5-a4e5-4cec-b3f9-c75e9a76259b" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="409" height="159" alt="image" src="https://github.com/user-attachments/assets/35d0d867-2d4b-4ce7-bb88-65cf722ff759" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="395" height="127" alt="image" src="https://github.com/user-attachments/assets/eee8df6e-9032-4e34-86c4-eb4a07543f5d" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="431" height="126" alt="image" src="https://github.com/user-attachments/assets/456fea46-5b9f-4181-98f6-bf11cae4c87b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="546" height="131" alt="image" src="https://github.com/user-attachments/assets/f34950a0-ad13-47d6-83e1-9143be81edfc" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="424" height="137" alt="image" src="https://github.com/user-attachments/assets/ecd407fa-aa2c-41ca-9b6d-27d225dae6bf" />




## Sorting File content

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
<img width="411" height="182" alt="image" src="https://github.com/user-attachments/assets/2edab8d2-797d-494b-8d68-79f26f998a7b" />


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
<img width="331" height="179" alt="image" src="https://github.com/user-attachments/assets/8c2a5bb5-0ab4-4ade-94f0-f726c99e7990" />



## Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="496" height="250" alt="image" src="https://github.com/user-attachments/assets/628a7c8b-7691-4445-b330-70aeaf8540d8" />




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
<img width="360" height="123" alt="image" src="https://github.com/user-attachments/assets/567c9f64-d5d2-444a-b0ca-0041a936618f" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="497" height="125" alt="image" src="https://github.com/user-attachments/assets/5b6ac1e6-61e2-44a5-8016-383c6ef5dc53" />



## Backup commands

tar -cvf backup.tar *
## OUTPUT
<img width="415" height="277" alt="image" src="https://github.com/user-attachments/assets/7547684b-cd10-45a3-837e-c5746d88f57e" />





mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="682" height="284" alt="image" src="https://github.com/user-attachments/assets/736afd7b-5a8a-462c-866d-b95e34904caf" />


tar -xvf backup.tar
## OUTPUT
<img width="538" height="273" alt="image" src="https://github.com/user-attachments/assets/b429c517-cca1-4417-9d91-fc252baf6632" />




gzip backup.tar
ls *.gz
## OUTPUT
<img width="587" height="83" alt="image" src="https://github.com/user-attachments/assets/a4a24102-f183-4fa1-84c7-9ec49247014f" />



gunzip backup.tar.gz
ls
## OUTPUT
<img width="592" height="160" alt="image" src="https://github.com/user-attachments/assets/5b277354-8b3c-4d4a-b46f-a29d4f954e26" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="762" height="177" alt="image" src="https://github.com/user-attachments/assets/98a7bcc4-ac88-4fe0-8bc1-09ec506ffa14" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="405" height="130" alt="image" src="https://github.com/user-attachments/assets/55826235-c70e-4cbd-bbff-92a49b1ca634" />


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
<img width="678" height="454" alt="image" src="https://github.com/user-attachments/assets/4f697554-19cb-477a-b853-c5694061a146" />

 
ls file1
## OUTPUT
<img width="534" height="79" alt="image" src="https://github.com/user-attachments/assets/b95bd1ca-84d9-42ce-b12c-16f783757ddf" />


echo $?
## OUTPUT 
<img width="461" height="79" alt="image" src="https://github.com/user-attachments/assets/e8fd3130-72ee-4886-8f73-42f0536232c4" />


./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="422" height="74" alt="image" src="https://github.com/user-attachments/assets/3a14b10d-8c61-46eb-9319-0301af217a57" />

abcd
 
echo $?
 ## OUTPUT
<img width="478" height="80" alt="image" src="https://github.com/user-attachments/assets/3898e6a7-5f7a-4635-91aa-8411cb290052" />


 
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
<img width="436" height="278" alt="image" src="https://github.com/user-attachments/assets/81facce6-0afd-4642-9407-19283ab80e14" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="695" height="150" alt="image" src="https://github.com/user-attachments/assets/23d9f3d8-1e78-4353-9926-45e816230d14" />


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
<img width="464" height="74" alt="image" src="https://github.com/user-attachments/assets/2da04220-bdc4-4dd7-b96c-44c52a64405a" />



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
<img width="445" height="83" alt="image" src="https://github.com/user-attachments/assets/748145ff-c25e-4a7e-bcde-7d440f710c2c" />



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


## OUTPUT
<img width="435" height="151" alt="image" src="https://github.com/user-attachments/assets/7f1ed304-e617-4376-a592-ea2cd45c31d1" />




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
<img width="513" height="180" alt="image" src="https://github.com/user-attachments/assets/c079bb29-4343-4b16-b429-87b563adfa65" />




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
<img width="410" height="132" alt="image" src="https://github.com/user-attachments/assets/0bfb6a60-7b29-47dc-b4ab-24cf8c25d2f1" />


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
<img width="488" height="129" alt="image" src="https://github.com/user-attachments/assets/5ed041ca-1532-4b05-a1bc-bdfec4cfd6d1" />




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
 
cat > whiletest.sh
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

 ## OUTPUT 
<img width="376" height="349" alt="image" src="https://github.com/user-attachments/assets/f715ebd7-5bda-4306-9d38-9746b0eed76b" />

 
 
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
$ ./untiltest.sh 

## OUTPUT 
<img width="423" height="202" alt="image" src="https://github.com/user-attachments/assets/56a1305b-f543-4eaf-abc1-89eee1ca1550" />


 
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

## OUTPUT 
<img width="368" height="256" alt="image" src="https://github.com/user-attachments/assets/268e8967-9936-4dca-a396-6228c5e5bd36" />

 
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

## OUTPUT
<img width="420" height="181" alt="image" src="https://github.com/user-attachments/assets/67ef03ca-69d9-46a7-945a-e6c7aff03e29" />

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

## OUTPUT 
<img width="382" height="182" alt="image" src="https://github.com/user-attachments/assets/daeb12c9-8065-442c-9226-0f4038523b31" />



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
