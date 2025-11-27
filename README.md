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

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d

cat > file2

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d

### Display the content of the files
cat < file1
## OUTPUT
<img width="397" height="148" alt="image" src="https://github.com/user-attachments/assets/2dd73263-f176-4169-a98e-845df2526455" />




cat < file2
## OUTPUT
<img width="298" height="173" alt="image" src="https://github.com/user-attachments/assets/566ff3d1-dd72-4570-aa20-6ba27628d8d5" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="462" height="93" alt="image" src="https://github.com/user-attachments/assets/bb63b90c-6353-4e28-88fe-a0d62de5322e" />


comm file1 file2
 ## OUTPUT
![WhatsApp Image 2025-11-18 at 9 24 20 PM](https://github.com/user-attachments/assets/90ddd296-05a6-4fb7-a6bd-f26121bb54f9)


 
diff file1 file2
## OUTPUT
<img width="538" height="322" alt="image" src="https://github.com/user-attachments/assets/5236e97b-efff-48a8-a73b-fb6fee3f1d3a" />



#Filters

### Create the following files file11, file22 as follows:

cat > file11

Hello world
This is my world
^d

cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d



cut -c1-3 file11
## OUTPUT
<img width="417" height="130" alt="image" src="https://github.com/user-attachments/assets/b6edec53-0af6-466c-869e-2cf1f22a6b92" />






cut -d "|" -f 1 file22
## OUTPUT
<img width="423" height="118" alt="image" src="https://github.com/user-attachments/assets/08410f29-74bc-4f8a-9674-bbf513504c7f" />





cut -d "|" -f 2 file22
## OUTPUT
<img width="440" height="130" alt="image" src="https://github.com/user-attachments/assets/81c96812-d582-42b1-9531-23c7a6123f2d" />




cat < newfile 

Hello world
hello world
^d
`
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="397" height="78" alt="image" src="https://github.com/user-attachments/assets/acb774b1-46b1-4dd1-827f-e008d2f3e3c4" />




grep hello newfile 
## OUTPUT

<img width="370" height="73" alt="image" src="https://github.com/user-attachments/assets/748ff340-f785-400f-a0b3-0cc216e5385e" />




grep -v hello newfile 
## OUTPUT

<img width="345" height="76" alt="image" src="https://github.com/user-attachments/assets/6ffc3d30-2f0b-4e14-8b6a-a4cb6e87ad3a" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="391" height="107" alt="image" src="https://github.com/user-attachments/assets/67ae1bb1-1ad7-460b-bee4-557365a6725d" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="427" height="77" alt="image" src="https://github.com/user-attachments/assets/f7d9b49c-8120-4efb-99c0-5e236e82b969" />





grep -R ubuntu /etc
## OUTPUT
<img width="1427" height="426" alt="image" src="https://github.com/user-attachments/assets/0aa1f5a6-8118-471a-97f4-ea4c208a07c8" />




grep -w -n world newfile   
## OUTPUT
<img width="362" height="95" alt="image" src="https://github.com/user-attachments/assets/4b79768a-b43c-4473-9f0d-166e38b68703" />



cat < newfile 

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d


cat > newfile

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="457" height="103" alt="image" src="https://github.com/user-attachments/assets/de82dbf5-a205-44dc-a032-dec7d99209ad" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="410" height="102" alt="image" src="https://github.com/user-attachments/assets/d1d8f2e1-e096-416c-9175-e20d2562e136" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="528" height="146" alt="image" src="https://github.com/user-attachments/assets/9cd6ad22-a932-4402-9818-37d3b09ec605" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="418" height="78" alt="image" src="https://github.com/user-attachments/assets/df8fe341-227d-4c46-8663-4cc53a7ad0f2" />



egrep '(world$)' newfile 
## OUTPUT
<img width="436" height="100" alt="image" src="https://github.com/user-attachments/assets/59f89b38-5ef0-40e3-8f81-5ef8e70d5a70" />



egrep '(World$)' newfile 
## OUTPUT
<img width="475" height="66" alt="image" src="https://github.com/user-attachments/assets/7de35b75-b725-448a-b0c3-2b3c551b8733" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="453" height="122" alt="image" src="https://github.com/user-attachments/assets/8ee1a380-c1b6-40d1-a2f3-f5971dc55473" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="422" height="80" alt="image" src="https://github.com/user-attachments/assets/4f13c884-8b48-4994-bdd9-472927c63fbb" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="437" height="76" alt="image" src="https://github.com/user-attachments/assets/ec918ada-7dc6-4a1f-93f1-603ad0f872af" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="468" height="77" alt="image" src="https://github.com/user-attachments/assets/9bb2eb1b-c53b-435b-b947-faeaf5a092bb" />



egrep l{2} newfile
## OUTPUT
<img width="412" height="102" alt="image" src="https://github.com/user-attachments/assets/30ae2c45-83f7-4903-81e7-a24b9928ad92" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="417" height="112" alt="image" src="https://github.com/user-attachments/assets/5faedf46-2dbc-4a7e-8d98-a02011f30002" />



cat > file23

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d



sed -n -e '3p' file23
## OUTPUT
<img width="373" height="78" alt="image" src="https://github.com/user-attachments/assets/84e9d5ad-76cc-4d74-ba23-55063d5d0c8b" />




sed -n -e '$p' file23
## OUTPUT
<img width="402" height="80" alt="image" src="https://github.com/user-attachments/assets/107bc8b4-ced8-46fc-92ae-9f2e028bb2d3" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="535" height="260" alt="image" src="https://github.com/user-attachments/assets/b5595c1b-d31d-4476-86f8-92c3a2b09c0a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="520" height="257" alt="image" src="https://github.com/user-attachments/assets/0caaadc6-4175-4d53-ae16-5bc654700f17" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="532" height="247" alt="image" src="https://github.com/user-attachments/assets/ca9073b4-3cfb-46a4-9868-4e16b7f5be21" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="462" height="173" alt="image" src="https://github.com/user-attachments/assets/7911bbd5-8cdb-4a03-8d7a-2324a366806f" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="442" height="126" alt="image" src="https://github.com/user-attachments/assets/65a00950-4e5a-4432-b560-b3644b2aa0cb" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="445" height="97" alt="image" src="https://github.com/user-attachments/assets/67bbac26-1ad1-4f70-827b-0694d5ae3f3d" />




seq 10 
## OUTPUT
<img width="437" height="311" alt="image" src="https://github.com/user-attachments/assets/971579c5-d4f2-4380-a777-2c3caf8cf56e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="357" height="127" alt="image" src="https://github.com/user-attachments/assets/f5f370b8-6e18-4c0c-a1e3-3bc8f953d6d3" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="410" height="127" alt="image" src="https://github.com/user-attachments/assets/7ca7190d-b720-4017-a6b9-ce0bb7f51267" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="381" height="156" alt="image" src="https://github.com/user-attachments/assets/43f0ac2d-507d-4929-a372-1a055bb8e26a" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="350" height="122" alt="image" src="https://github.com/user-attachments/assets/d00c9350-a3f7-415d-998e-999d2b643644" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="411" height="122" alt="image" src="https://github.com/user-attachments/assets/8fe1facf-99ae-4e35-a249-f2619c971908" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="588" height="130" alt="image" src="https://github.com/user-attachments/assets/ed41434c-d797-45f2-b1fb-ae0d6556d801" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="456" height="121" alt="image" src="https://github.com/user-attachments/assets/78eb314b-6c2f-4560-8981-98398d644404" />



#Sorting File content
cat > file21

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
sort file21
## OUTPUT
![367115582-1a364d26-c72f-4a7f-ae2d-8452f208b154](https://github.com/user-attachments/assets/1b9cd914-a522-4416-b1bc-53f16445ded7)


cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
uniq file22
## OUTPUT
![367115602-9bf8b097-c08e-414f-8624-64d9a2e51b52](https://github.com/user-attachments/assets/f8232178-e836-4b6c-91ee-ad71d7576d49)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![367115643-be369833-db07-4973-96fa-a0fdeebd677b](https://github.com/user-attachments/assets/ada97cf2-b333-4361-b059-7b72a42934e6)

cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
^d
 
cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
 
cat urllist.txt | tr -d ' '
 ## OUTPUT
![367115669-e55aac5f-fcb4-4740-89f1-d94a08c36b69](https://github.com/user-attachments/assets/3efafe75-3107-4244-b1fc-b88a680ff68d)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![367115680-946166cd-c8fa-4611-ac47-a167a89d2916](https://github.com/user-attachments/assets/e7f1cfe3-a6e9-4a96-a7ea-b84c15bc70db)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![367115736-0f92925f-66b9-4c2b-903b-4cc5e17fc2ad](https://github.com/user-attachments/assets/3128ac3e-29dd-4ffb-afe5-d702c8457a54)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![367115769-9224664e-3cd4-4b1d-8554-64e228822cd3](https://github.com/user-attachments/assets/b7d10414-d99f-4d64-9544-fc044a9f6232)


tar -xvf backup.tar
## OUTPUT
![367115793-6b360647-9ea5-4243-a009-b231733331c1](https://github.com/user-attachments/assets/19150a72-2ff0-42b6-9cf1-19ce0cee6ae8)

gzip backup.tar
## OUTPUT
![367115819-be2e1435-c098-4eb8-9d48-14553f1d938b](https://github.com/user-attachments/assets/5d80a72b-bde8-41b1-8fc7-1bc0eef7528d)

ls .gz
## OUTPUT
 ![367115819-be2e1435-c098-4eb8-9d48-14553f1d938b](https://github.com/user-attachments/assets/4e60d86b-db41-41e4-a2bd-ffa7d8065574)

gunzip backup.tar.gz
## OUTPUT
![367115836-bdc8d7f5-38d4-4418-9205-e48fcbd7ce2c](https://github.com/user-attachments/assets/39001746-a8ac-446b-9ef8-a6363af484b0)

 
# Shell Script

echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![367115864-e717c948-9945-4667-8824-062d77a5bb09](https://github.com/user-attachments/assets/0322b809-aedc-434f-87ed-8a7e0038ca56)
![367115892-31f1f1b3-7cba-4c89-a3fe-82566950bc00](https://github.com/user-attachments/assets/a55c0d2c-89ee-4a54-8018-d2f04422ff03)

 
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop


cat herecheck.txt
## OUTPUT
![367115908-71951ce4-e1cf-4201-b9f6-971da6f7c17b](https://github.com/user-attachments/assets/f9bb98a2-241e-4a6c-bbef-45af5bde6882)


cat < scriptest.sh 
bash
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
 

cat scriptest.sh 
bash
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

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![367115950-fe608d01-2ae6-48f6-a23b-7ded10204b69](https://github.com/user-attachments/assets/7b57a072-05df-4077-8545-d2d3ff6adb42)

 
ls file1
## OUTPUT
![367115990-0793dc3d-d87c-4b57-94cd-fb8140cb04e6](https://github.com/user-attachments/assets/c441de58-ca42-499d-82e9-28bec1fe82da)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![367116046-e01719a8-0b37-44a1-b7f6-42842d42ab06](https://github.com/user-attachments/assets/c3114c7e-af18-4ce0-8349-dab9a0fb5436)

 
# mis-using string comparisons

cat < strcomp.sh 
bash
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


cat strcomp.sh 
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi

## OUTPUT
![367116139-9c8d3a8d-f3b0-4399-94c2-28a300e18d27](https://github.com/user-attachments/assets/3469b2e8-3c68-402e-bb0e-dc1c5e467891)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![367116160-bacab6ce-81c0-4758-9efb-7529713e24ed](https://github.com/user-attachments/assets/ecd9e8a0-003b-49de-8e0b-21afc33722d4)


# check file ownership
cat < psswdperm.sh 
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d


cat psswdperm.sh 
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 
./psswdperm.sh
## OUTPUT
![367116184-314caf81-7a05-4f49-83e3-225c59bf17ab](https://github.com/user-attachments/assets/db6d9268-e10e-46fb-b24a-c57d5d03bbdd)

# check if with file location
cat>ifnested.sh 
bash
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

cat ifnested.sh 

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


./ifnested.sh 
## OUTPUT
![367116214-24197447-471b-4918-bc8b-30241cd269b6](https://github.com/user-attachments/assets/5aee7d6e-970c-4236-ba6b-180a717ff917)



# using numeric test comparisons
cat > iftest.sh 
bash
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



cat iftest.sh 
bash
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


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![367116258-5db659ac-38be-4fb2-a347-6ede773c9a2a](https://github.com/user-attachments/assets/0d0f4252-20b0-4254-9670-2132f4525ee0)

# check if a file
cat > ifnested.sh 
bash
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


cat ifnested.sh 
bash
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


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
![367116328-52d7af81-3b4e-41c5-9626-64f82185d935](https://github.com/user-attachments/assets/fab0300b-2022-4ad0-a3bd-9b3ac9eeee2c)

# looking for a possible value using elif
cat elifcheck.sh 
bash
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


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![367116353-e259d406-0edd-4f51-8f06-63169bb5827b](https://github.com/user-attachments/assets/33d8ce98-fcea-421b-96ad-f7510a391eaa)


# testing compound comparisons
cat> ifcompound.sh 
bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![367116385-7acc02b1-2a20-48a5-ad93-b3ef2e4dc116](https://github.com/user-attachments/assets/9449f425-72b7-4c9c-bf39-bb3b36ee4a6e)

# using the case command
cat >casecheck.sh 
bash
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

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done

$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done

$ ./forin3.sh 
 
cat forin1.sh 
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

$ chmod 755 forin1.sh
## OUTPUT
![367117237-3e29dd0b-9511-4548-a980-4ed3fcd14ab8](https://github.com/user-attachments/assets/c1696d99-ba95-4fbd-87d2-68caa6a9fe1f)

cat forinfile.sh 
bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done

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
![367117195-8d1a115e-950e-48dc-8364-5d0649ffc055](https://github.com/user-attachments/assets/c2274e30-fd57-49f3-a66d-3854567d23c7)


cat forctype.sh 
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
`
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![367117170-cb913922-82db-4cde-8a55-0c595a856b5c](https://github.com/user-attachments/assets/27312fa1-741f-4968-8443-80393b19f7d7)

cat forctype1.sh 
bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![367117143-692188b8-4f08-4a56-b5d8-3b5619277470](https://github.com/user-attachments/assets/a134c06d-bc2f-47d6-8079-55a8d1099bd0)

cat fornested1.sh 
bash
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

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![367117110-97137899-28a4-4f38-b4c8-f447e4c72e38](https://github.com/user-attachments/assets/d473c5f2-88f2-47ad-bf72-36db4122db46)

 
cat forbreak.sh 
bash
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

## OUTPUT
![367117063-a5501dea-e2f0-40dc-a328-5d846c03c91a](https://github.com/user-attachments/assets/80125046-a293-4f6d-a045-41e24a09659b)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
bash
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


 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![367117014-9377cb17-0ee9-41c4-af0b-5d329daa76ba](https://github.com/user-attachments/assets/a71f37e6-a7b7-4936-b6ac-d4d1df7c52cd)

cat exread.sh 
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![367116983-f6050b6b-46a5-4f33-86a4-03c0a8ae723d](https://github.com/user-attachments/assets/88f36639-b54b-4c80-8d6f-35126e84e673)


 cat exread1.sh
bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
 
$ chmod 755 exread1.sh 

## OUTPUT
![367116945-014589f7-78cd-4662-a17c-acfcc364063e](https://github.com/user-attachments/assets/ac5a4a45-d04b-4748-ab7f-c6b5e1d6d381)



$ ./exread1.sh 
 
cat funcex.sh
bash
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

## OUTPUT
![367116910-8f2a4f1d-c2e8-4574-bc4d-741f549ebed1](https://github.com/user-attachments/assets/ad721d8a-b4ae-4eab-81fa-8cef958b6421)

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done

$ chmod 777 argshift.sh
## OUTPUT
![367116862-d075ae2f-7ceb-48c6-b57e-4384c28f3b9e](https://github.com/user-attachments/assets/cdc9d420-ac46-4688-a926-b017c1eb8106)

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
bash
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

$ chmod 777 argshift.sh
## OUTPUT
![367116813-83a88364-1614-4625-9038-794dbdc25b82](https://github.com/user-attachments/assets/24b06404-63f9-4358-8f23-ba80165d2f22)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x

## OUTPUT
![367116765-8cfd0582-a07b-49df-97c2-9163576b0c07](https://github.com/user-attachments/assets/4d226e69-fd6b-4322-8e04-359eccb5b146)

 ./argshift.sh 1 2 3
 
 
cat > nc.awk
bash
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
 
cat>data.dat
bash
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

awk -f nc.awk data.dat
## OUTPUT 
 ![367116723-7746ed8b-5940-47c4-8d18-76c2628c4fdf](https://github.com/user-attachments/assets/0913aaaf-815c-43e5-8a68-67d378785123)

cat > palindrome.sh
bash
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

## OUTPUT 
![367116660-ffca7dcb-3c61-45d9-97b1-02996d5fefde](https://github.com/user-attachments/assets/892623f1-936a-4c9a-8fb0-6bdfcf70f9ab)
![367116686-57b1dc37-f7bd-49e8-a770-6f9cc79f8b46](https://github.com/user-attachments/assets/1acacb37-ab32-4a18-85f8-90048c3b8bcd)


# RESULT:
The Commands are executed successfully.
