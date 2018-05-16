# BashTips


Tips that can be used in Bash Scripting Language


To change trump.1.1.jpeg to User.1.1.jpeg

	files=`ls trump*jpeg`
	for file in $files
	do
		# echo ${file#*.}, 
		echo User.${file#*.}
		cp $file User.${file#*.}
	done



Another example :

	#! /bin/bash

	filename="bash.string.txt"

	echo ${filename#*.}
	echo ${filename%.*}


To change spaces to an underscore 
(This can happen if you trying to read file names that have spaces in them, and you need to modify it)
Let's say the line contains "Screen Shot 2018-05-15 at 9.32.27 PM.png"


    list=`ls  *.png|head -n 1`
    count=0
    for file in $list
    do
        #echo "-> $file"
        echo ${file// /_}
        echo $file
        count=$((count+1))

        #echo "new name", leftroadsign.3.$count.png

        #mv $file User.3.$count.jpeg

    done
