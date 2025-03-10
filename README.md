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

![Screenshot 2025-03-03 093057](https://github.com/user-attachments/assets/df07711e-5404-4e37-8f07-bd22d226b014)


cat < file2
## OUTPUT
![Screenshot 2025-03-03 093120](https://github.com/user-attachments/assets/99a58d3f-d579-4b5f-808c-d961eba5dae4)



# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-03-03 093144](https://github.com/user-attachments/assets/7a67c3e1-dbf5-4eca-ba2e-b76d55dafd51)

 
comm file1 file2
 ## OUTPUT
 ![Screenshot 2025-03-03 093202](https://github.com/user-attachments/assets/5b2f0bbb-b8a2-472c-968a-cd34128e0a98)


 
diff file1 file2
## OUTPUT
![Screenshot 2025-03-03 093329](https://github.com/user-attachments/assets/72010662-1efe-4676-8d58-71081dfd6cf3)



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
![Screenshot 2025-03-08 110308](https://github.com/user-attachments/assets/fd2dfbda-1336-4746-8eef-c0ee23562df6)





cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2025-03-08 110520](https://github.com/user-attachments/assets/cdb568d4-fe7c-407e-871d-5681611e09e2)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-03-08 110420](https://github.com/user-attachments/assets/5e62f6b9-8894-4520-8281-cfbcd9681b98)



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
![Screenshot 2025-03-08 111944](https://github.com/user-attachments/assets/af53b8c8-a4b2-49dd-abb3-08de8d51c1cc)



grep hello newfile 
## OUTPUT
![Screenshot 2025-03-08 112031](https://github.com/user-attachments/assets/3730dd1e-6e14-4e9b-8c7c-8fc8fb91c889)





grep -v hello newfile 
## OUTPUT
![Screenshot 2025-03-08 112518](https://github.com/user-attachments/assets/6e06e786-5d66-41c8-bf06-dec52bb1102b)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-03-08 112546](https://github.com/user-attachments/assets/95f17e3c-8975-4c9b-b691-662168f80bb2)





cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2025-03-08 112641](https://github.com/user-attachments/assets/e1889540-12bd-4b68-be41-686c131e16eb)





grep -R ubuntu /etc
## OUTPUT
![Screenshot 2025-03-08 112954](https://github.com/user-attachments/assets/c0171da0-7fc0-4420-80c6-dcf1d3b5a237)



grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-03-08 113426](https://github.com/user-attachments/assets/5353d34b-4e12-4bb9-9d9b-5127f6ce77a2)


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

![Screenshot 2025-03-08 133421](https://github.com/user-attachments/assets/99b5e71a-6ce0-4633-8d30-606c5f3afa9b)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2025-03-08 133839](https://github.com/user-attachments/assets/0f61c65b-64e1-479c-97cc-c2a69d64a98e)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![Screenshot 2025-03-08 133555](https://github.com/user-attachments/assets/75c100ba-c40b-4dc4-b6ef-2a704ee05055)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2025-03-08 134313](https://github.com/user-attachments/assets/9ac6ca3d-25e6-482b-a1a7-09b457fe6434)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2025-03-08 134328](https://github.com/user-attachments/assets/d98dc536-97a5-4fc3-8819-79a7cc1fb0a9)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2025-03-08 134353](https://github.com/user-attachments/assets/a6b91a56-23c5-4169-b4f0-a780f49a8894)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2025-03-08 134854](https://github.com/user-attachments/assets/ff223289-a7a0-45a4-b22e-2528471e56ec)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot 2025-03-08 134913](https://github.com/user-attachments/assets/4b2e776c-fd66-4c8b-a9f4-3cbb6854bb01)


egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot 2025-03-08 134928](https://github.com/user-attachments/assets/eb865d9b-ad56-425b-8d50-35172aa0717a)

egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2025-03-08 135133](https://github.com/user-attachments/assets/fe07f17e-7789-479a-aeeb-79ca16c971ec)


egrep l{2} newfile
## OUTPUT
![Screenshot 2025-03-08 135952](https://github.com/user-attachments/assets/1dcaa448-bce0-41d6-9262-19415f486027)




egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot 2025-03-08 140131](https://github.com/user-attachments/assets/8d9a2f08-5335-43bf-8461-9d2d4d20f16f)

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
![Screenshot 2025-03-08 142318](https://github.com/user-attachments/assets/757d8320-a2b8-41f0-920f-6fd14eefd063)



sed -n -e '$p' file23
## OUTPUT
![Screenshot 2025-03-08 142329](https://github.com/user-attachments/assets/320bfc21-a24f-4dfe-aa9b-1bd53beb20af)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-03-08 142346](https://github.com/user-attachments/assets/f7df3380-63aa-40e0-904c-1d9e6b7c0da1)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-03-08 142920](https://github.com/user-attachments/assets/b9ecb6c1-7920-4f46-917d-e891991307da)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2025-03-08 142933](https://github.com/user-attachments/assets/9248da84-72a5-4fed-9345-51186fbf0225)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2025-03-08 143054](https://github.com/user-attachments/assets/1f8643d9-b95c-4f7a-9aea-6af705fc3e66)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot 2025-03-08 143114](https://github.com/user-attachments/assets/0d08d240-72c9-4e63-b0f3-24152276750c)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot 2025-03-08 143130](https://github.com/user-attachments/assets/89af7d7d-a18d-4c24-9642-fd6ca9edaba2)


seq 10 
## OUTPUT

![Screenshot 2025-03-08 143554](https://github.com/user-attachments/assets/df5d3c6c-a7dd-4621-abd6-994d8bd171da)


seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2025-03-08 143426](https://github.com/user-attachments/assets/7f813181-af36-45c7-94b6-78da0d412803)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2025-03-08 143437](https://github.com/user-attachments/assets/d075dd0a-6a62-4b34-8e74-249270a1e79f)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2025-03-08 143450](https://github.com/user-attachments/assets/d6581653-d651-409a-a557-b7915df26916)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2025-03-08 143504](https://github.com/user-attachments/assets/f7f0962c-f738-40a6-9da3-ab691e617232)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2025-03-08 143830](https://github.com/user-attachments/assets/b8c39fa4-4a58-4515-8529-0efa7e5d8c7b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2025-03-08 143844](https://github.com/user-attachments/assets/23ce2349-0d42-4a32-9836-82d7bbe1c218)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot 2025-03-08 143857](https://github.com/user-attachments/assets/9d8cac58-f159-4a6d-af64-6fee052e7266)

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

![Screenshot 2025-03-08 204848](https://github.com/user-attachments/assets/86c93677-55ad-4aa3-be4a-2d918e6da73e)

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
![Screenshot 2025-03-08 185507](https://github.com/user-attachments/assets/221deb37-44fa-40fe-a5fd-d5fa76aac2dd)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2025-03-08 185530](https://github.com/user-attachments/assets/70590940-8aad-47e1-bbe8-05edaa21dcdb)

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
![Screenshot 2025-03-08 185840](https://github.com/user-attachments/assets/40125582-8a9c-475d-b4f9-b38eadcbf58d)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-03-08 185930](https://github.com/user-attachments/assets/591e368c-939c-4f90-b3a5-1ee2189de9aa)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2025-03-08 185953](https://github.com/user-attachments/assets/616eeb8d-c05a-4020-a75b-6e35090cfa20)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2025-03-08 205826](https://github.com/user-attachments/assets/70be2da6-53b2-41a6-b50a-136635d8d798)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2025-03-08 205837](https://github.com/user-attachments/assets/05d59a8c-5783-4ff3-a7e8-43f8eeba66bf)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot 2025-03-09 122921](https://github.com/user-attachments/assets/7a6b2d06-b626-4065-9628-a0989d1078e4)

gunzip backup.tar.gz
## OUTPUT
![Screenshot 2025-03-09 123344](https://github.com/user-attachments/assets/6b042a84-131c-4222-a272-3064a2d3e990)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUTchmod

 ![Screenshot 2025-03-09 123812](https://github.com/user-attachments/assets/4581e673-3f4d-43c1-92c7-0c7d4e85536f)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot 2025-03-09 105913](https://github.com/user-attachments/assets/5f79644b-26e0-4f1d-be42-8ad48706ad35)

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

 ![Screenshot 2025-03-09 111657](https://github.com/user-attachments/assets/4f7dab67-928f-4685-8903-b880def8d0bd)

ls file1
## OUTPUT
![Screenshot 2025-03-09 111900](https://github.com/user-attachments/assets/ee01f193-1f8b-4ac2-b33b-6ad5743fd2d8)

echo $?
## OUTPUT 
![Screenshot 2025-03-09 111937](https://github.com/user-attachments/assets/c87192c2-5a93-4290-8e0b-192871016e2b)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT echo
 ![Screenshot 2025-03-09 112143](https://github.com/user-attachments/assets/f1da64aa-e4d3-41ef-a772-b0e71eebbe31)

abcd
 
echo $?
 ## OUTPUT
![Screenshot 2025-03-09 112646](https://github.com/user-attachments/assets/f96fe94b-ff42-490c-bbb1-fee192530e6e)


 
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

![Screenshot 2025-03-09 113155](https://github.com/user-attachments/assets/8aae649f-90b4-497c-90d7-293cf3a411c4)

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
![Screenshot 2025-03-09 124605](https://github.com/user-attachments/assets/0f1c218e-50cc-4fb1-9a2e-f70e150bfcc0)

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

![Screenshot 2025-03-09 124958](https://github.com/user-attachments/assets/5607829b-e660-454b-877e-4d2ae824d73c)


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
![Screenshot 2025-03-09 125644](https://github.com/user-attachments/assets/83c2bd9e-fc69-40cd-b2e8-4ec1abb60f7c)

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
![Screenshot 2025-03-09 130101](https://github.com/user-attachments/assets/30c0903b-aaf6-49ba-a16d-dd6c6d2366c5)

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
![Screenshot 2025-03-09 130625](https://github.com/user-attachments/assets/6aabfdc4-d474-45d9-8991-97c44739712e)


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
![Screenshot 2025-03-09 131407](https://github.com/user-attachments/assets/b4888549-edc3-4e8d-880a-3709a3e0e59e)

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
![Screenshot 2025-03-09 132026](https://github.com/user-attachments/assets/5523b021-dc77-42bf-bcfd-8679c6573807)

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
![Screenshot 2025-03-09 132712](https://github.com/user-attachments/assets/75dafd01-5f21-4932-a8a9-c72368f2dc1b)



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
![Screenshot 2025-03-09 135319](https://github.com/user-attachments/assets/351710e2-59a4-4827-a080-0c5b7936eee1)

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
![Screenshot 2025-03-09 135840](https://github.com/user-attachments/assets/b2134ff0-3490-4052-9427-f6db035b2c6d)

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
![Screenshot 2025-03-09 140127](https://github.com/user-attachments/assets/fe257804-c075-4179-ba30-23564e5571e9)

 
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
![Screenshot 2025-03-09 143140](https://github.com/user-attachments/assets/9674ebb2-d405-40bd-983c-4078e99c76a1)

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
 ![Screenshot 2025-03-09 143254](https://github.com/user-attachments/assets/32277e5b-170d-44d0-86a9-69d5e21c489d)

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
![Screenshot 2025-03-09 143441](https://github.com/user-attachments/assets/ab0c3f08-05f2-4ad4-924a-9d65c0b15a1b)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2025-03-09 143958](https://github.com/user-attachments/assets/5933a38c-e7fe-4b0b-b582-66175f2cee79)


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

![Screenshot 2025-03-09 144437](https://github.com/user-attachments/assets/e0d79ffd-0b8e-4466-a38b-94ff0f1ac263)
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
![Screenshot 2025-03-09 144751](https://github.com/user-attachments/assets/e31ce0d6-da38-4599-bfb1-356c694ddbb2)

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
![Screenshot 2025-03-09 145135](https://github.com/user-attachments/assets/66afd19e-ecc8-4cd4-b1a7-1fd2feb82308)

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
 
 ![Screenshot 2025-03-09 145358](https://github.com/user-attachments/assets/9460b43d-7122-4fe7-a2fe-ab909e3b6f88)

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
 ![Screenshot 2025-03-09 145928](https://github.com/user-attachments/assets/d2bbf6c5-492c-4891-b277-c26961a8e87c)

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
![Screenshot 2025-03-10 095024](https://github.com/user-attachments/assets/e74a621e-3f0d-4f9b-88c3-4c32dca0f6a4)

# RESULT:
The Commands are executed successfully.
