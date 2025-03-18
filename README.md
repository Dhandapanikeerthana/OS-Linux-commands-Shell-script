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
![Screenshot 2025-03-10 101012](https://github.com/user-attachments/assets/b8c925a2-f555-4913-97e5-c298bdaf323f)

gunzip backup.tar.gz
## OUTPUT
![Screenshot 2025-03-10 101114](https://github.com/user-attachments/assets/8680c16c-f6ce-4ddc-83d7-69ecf7dd3c81)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUTchmod

![Screenshot 2025-03-10 104717](https://github.com/user-attachments/assets/e77008a6-9920-4dc4-a6d2-0b16eb6523ee)


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot 2025-03-10 104849](https://github.com/user-attachments/assets/2aa9c76c-128f-44be-a19d-dc3ec540f01f)

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

![Screenshot 2025-03-10 105134](https://github.com/user-attachments/assets/573092a8-44d1-4203-bb13-2aa5680004ce)


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
![Screenshot 2025-03-10 105304](https://github.com/user-attachments/assets/0d0993f5-805f-4a12-8d49-67cd7329e561)


abcd
 
echo $?
 ## OUTPUT
![Screenshot 2025-03-10 105350](https://github.com/user-attachments/assets/865be10a-6140-4ef2-8cf0-5797f21d6565)



 
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

![Screenshot 2025-03-10 110230](https://github.com/user-attachments/assets/6d17ee4f-2d18-4f23-8eb8-613cd609359a)


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
![Screenshot 2025-03-10 110301](https://github.com/user-attachments/assets/a5549694-067a-4ff5-b6ee-71e332fcd386)


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

![Screenshot 2025-03-10 121248](https://github.com/user-attachments/assets/01ce8bd4-5980-4c79-8c79-8a657c8e920d)



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
![Screenshot 2025-03-10 121525](https://github.com/user-attachments/assets/00a002cb-4110-4a66-8fd2-bc2b225cead3)

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

![Screenshot 2025-03-13 093859](https://github.com/user-attachments/assets/8ac760b8-1302-432d-8d73-bd5c0427cada)

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
![Screenshot 2025-03-13 094159](https://github.com/user-attachments/assets/579d065b-7c0a-4f63-8a0a-3bf1fb20992c)


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


![Screenshot 2025-03-13 094510](https://github.com/user-attachments/assets/5e89208d-ccfa-44e9-9f40-63b46453bf9d)

cat > whiletest
![Screenshot 2025-03-13 095310](https://github.com/user-attachments/assets/1b7585a3-cdf6-4378-adeb-1612e2341976)


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
 ![Screenshot 2025-03-13 095505](https://github.com/user-attachments/assets/c9d58922-181a-4462-a62e-5463c7eb2451)

 
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
 
 ![Screenshot 2025-03-13 095735](https://github.com/user-attachments/assets/b2cf3c3a-3599-4a76-9d28-508b5a2cb824)

 
cat forin1.sh 
![Screenshot 2025-03-13 095955](https://github.com/user-attachments/assets/47096e29-5a9b-470a-849e-642b25e1ecc3)


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
![Screenshot 2025-03-13 100428](https://github.com/user-attachments/assets/8e38f8ce-0ee6-4e1b-a88d-f2ba618ec729)


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
 ![Screenshot 2025-03-13 100428](https://github.com/user-attachments/assets/998a0147-7c33-4164-addb-c9d1ce3c4dc4)

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
![Screenshot 2025-03-13 100428](https://github.com/user-attachments/assets/f65d2989-de0b-42dd-adfe-20ac594bfc04)
 
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
![Screenshot 2025-03-13 101238](https://github.com/user-attachments/assets/db507746-35e7-45eb-bfa8-85dc9f9e86f6)

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
![Screenshot 2025-03-13 101745](https://github.com/user-attachments/assets/c2003ed7-90bf-48b4-a1cb-6eb2e71c072c)

 
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
![Screenshot 2025-03-13 102028](https://github.com/user-attachments/assets/463cddb3-cf49-43fb-9412-4949a6ef8a9d)


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
![Screenshot 2025-03-13 102303](https://github.com/user-attachments/assets/838c94bf-bebc-44c7-821d-31f1e07cd6d8)

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
![Screenshot 2025-03-13 102515](https://github.com/user-attachments/assets/c73036a9-0e4a-4c91-8b4b-f2db8b5c2eed)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![Screenshot 2025-03-13 102840](https://github.com/user-attachments/assets/5ba65b8b-5bee-4b6b-ae96-ca7ccbd624a0)


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

![Screenshot 2025-03-13 103339](https://github.com/user-attachments/assets/f73079d0-afb4-42f7-90c8-0e277c115e9e)

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
![Screenshot 2025-03-13 103533](https://github.com/user-attachments/assets/4b84e122-efb9-412e-b1f1-b9e51b00fb9c)


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
![Screenshot 2025-03-13 103731](https://github.com/user-attachments/assets/bb0dca4d-9e96-4d29-bc66-127080a61558)

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
 
 ![Screenshot 2025-03-13 103951](https://github.com/user-attachments/assets/bf66ea70-3d30-42ac-b27e-9da4a55fba49)

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
