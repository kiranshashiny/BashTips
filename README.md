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
