
# PIC-1-



#!/bin/bash

read -p "enter the name of the destination file" dest

read -p "enter the name of the source file 1" src1
read -p "enter the name of the source file 2" src2

cat "$src1" "$src2" > "$dest"

echo "files copied succesfully"


#!/bin/bash

hour=$(date +%H)

if [ $hour -lt 12 ]; then
    echo "Good Morning!"
elif [ $hour -lt 17 ]; then
    echo "Good Afternoon!"
elif [ $hour -lt 20 ]; then
    echo "Good Evening!"
else
    echo "Good Night!"
fi


#!/bin/bash

read -p "Enter password: " password

if [[ $password == *[A-Z]* && $password == *[a-z]* && $password == *[0-9]* && $password == *['!@#$%^&*']* ]]
then
    echo "Strong Password"
else
    echo "Weak Password"
fi
