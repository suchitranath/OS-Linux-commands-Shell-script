# OS-Linux-commands-Shell-scripting
-Suchitra Nath Btech IT
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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/055495b1-e4cf-4a5b-adbc-654f904e94be)



cat < file2
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/105e6b55-feaa-4562-aec2-3654b92e59ee)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/7263c35c-a9dc-4e0e-81d3-2427d243253d)

comm file1 file2
 ## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/97f180d1-e063-4973-ae0c-d86cf8bc1288)

 
diff file1 file2
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/dc96700e-2a1a-449b-9b9d-9cac80777895)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/c471fb98-5ffd-480d-881f-ab61aae4bbac)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/378a8d80-a2b4-48fc-ba29-4a32ef25d421)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/c591089e-e0de-4205-9810-32553563ac09)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/47141119-f85d-4361-a4d9-375b5d21b600)



grep hello newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/dcf8fd62-e386-413e-bf38-af508c7d5833)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/31739b7f-f886-493a-b180-c37f01873e9b)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/aa033696-ad93-4b25-8b98-69ff4a28dd79)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/73605880-1dc5-4217-8323-8d02dc9f9670)




grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/473ab04f-d5c5-451c-87bc-ad79feee086f)

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/164b15e7-07fc-4e98-8623-0e8385594cb0)

grep -w -n world newfile   
## OUTPUT

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/fcb22aeb-f6a9-401a-a503-e76d34e6b088)

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

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/f104920a-bc3a-4935-893a-205e5c20cd88)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/3dbda5a9-05a3-429c-b4a7-cd21c6c5ad0e)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/af2c89a8-8a2e-4abd-977d-9d8919e22eab)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/f32d4ac0-83ab-486f-a8d7-70c319b8c63c)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/1db9523b-4c23-4911-99f4-344b5902c50e)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/971ee8a4-61fe-4e97-9707-7004e7340fcb)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/0cb279ef-04f2-44db-8a6e-e880f3113dbd)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/30bed9f3-7f37-4db6-bc20-66596b655c34)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/2a67ff3f-2e28-448d-aeb8-3136a1cf5026)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/f6979794-e520-4318-b655-97518b39b1d2)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/84eceeaf-5a07-4691-9d52-453fe8035f37)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/f5e5c820-1d24-4b30-86c7-492dbd3d922c)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/27ea85b1-c681-44b1-9acd-ef9e4e16f251)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/2f6d90e9-6e2e-4538-9cc9-d8bed738be05)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/7f35e682-b292-4a37-ad92-1e15fc6da9db)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/db8183ef-e656-4e63-9ad5-9ca7b2396ad6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/2d681d5a-399d-45d2-b45f-31809ab5cca7)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/60e5238a-911d-4b2a-ab07-4a90cfb324f0)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a89f5db7-cf03-4142-baa2-0b0fddaa6495)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/2f3194e0-717d-405c-a104-689ae6143d1b)


seq 10 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/44de3a6c-fbb0-4661-9cfd-d9e10f15ebf1)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/29227095-8c91-4cff-bafa-568088b3dfd9)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/8c14e36b-ec98-4cd0-8ce6-dfdcce43267f)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/ad7560ae-4cdf-4058-a926-3a8a9aea2517)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a6683c65-dca9-4f0c-974e-0cc9cfc2e7c1)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/d1014af3-7dc7-4b8c-9a4c-cd1d61ca8541)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/dc29f7db-0791-4567-8597-de3f4c52add3)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/d1ef217a-b53e-4853-a9af-ff7a5f266bc9)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/8e13e027-ab72-4d5e-b333-b70880a7a99f)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a54b382b-81b0-45f1-921b-469f3efc0bf4)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/19832dd1-cd7c-4d47-ac5b-d5b97549170b)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/1b669bbc-9136-44ed-9017-185864b72e83)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/b23f6e8b-f805-4600-94e5-22fe7d933e3e)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/95efb6ed-5489-4be2-82da-12953c7058f7)
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/c064f95a-ef02-4ab5-aac0-1ef8a38443d4)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/2cc8b147-523d-4c0f-9c43-c3e499dae71a)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/5b5e0260-8c83-46db-b46a-8fbff2dceb92)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a9b35836-99e0-4f3b-8a81-0556ac57f570)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/bd23747e-c254-48d0-88be-ef2ad6345666)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/742253cf-4671-4fcc-b625-b700d95f5112)

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

![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a9bfcb05-ebfc-4c19-b2ce-aedf89b651dd)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/affaee5f-3f37-4a8e-bc5a-eec46df8b6e8)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/c2fe6fd4-180c-428d-b4f6-d4c3a4c95360)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/3ba4f3fa-bbdd-49b9-b62d-ea3cadaddd6f)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/f4f2036a-86c5-4109-b38d-4180317b58f7)

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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a3d7799f-1f7e-4857-84e5-ead31f51cf7f)

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
 
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/7aefe80b-3c06-4b3b-9265-612130207b5d)

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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/3dd66eb3-98e1-4cae-998a-d4af12e1371e)

 
 
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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/8f0cf911-95be-4ff2-aa68-53208b1bce83)

 
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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/4d2e6896-c7fe-41f6-bdd7-3652f1aa1234)

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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a005690d-3f70-4981-bebc-458b7ca05862)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/bfcae572-2a41-47dc-8de0-21e3a342a2a9)


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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/a55cbcc7-545b-4f52-91a7-73a4224edd7b)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/0f4f3887-7d24-47c9-90a1-a83376fc5dc2)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/ef1833a2-01ce-476b-8a6a-552071f87996)

 
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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/dc6f5edb-c5ad-45a4-a228-58435e16d5e5)

 
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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/83724ece-69b5-4f4c-8833-9273044b30ca)


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

 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/b8e69617-a43e-487a-928c-bbd62ccb32db)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/bf37278d-6eba-4fcc-8200-6b65f245d9e4)

 
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

 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/36d46125-6adf-4133-b0bb-067f5ed75be0)

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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/af6ec02b-51b9-4158-936e-1f65c1ef7747)

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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/28d2bc9f-5d69-4c0e-8b79-117b385e5f46)

 
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
 ![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/987d3465-7d87-4cd9-8456-a662d78e97bd)

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
![image](https://github.com/suchitranath/OS-Linux-commands-Shell-script/assets/145742631/48dba329-2cd2-4e4f-a118-d06070c5b744)

# RESULT:
The Commands are executed successfully.
