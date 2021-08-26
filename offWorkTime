#!/bin/bash

# @auther: Leon

echo 请输入您的上班时间。
read time
hour=${time%%.*}
min=${time##*.}
echo 想要误餐补吗？（18块）1要0不要。
read flag
case "$flag" in
	1)
		if [ $min -gt 30 ]
		then

			hour=`expr $hour + 11`
			if [ `expr $min - 30` -lt 10 ]
			then
				min=0`expr $min - 30`
			else
				min=`expr $min - 30`
			fi
		elif [ $min -eq 30 ]
		then
			hour=`expr $hour + 11`
			min=00
		else
			hour=`expr $hour + 10`
			min=`expr $min + 30`
		fi
		echo 您需要$hour:$min下班。
		;;
	0)
		hour=`expr $hour + 8`
		echo 您需要$hour:$min下班。
		;;
	*)
		echo 输入有误！请规范输入，如"8.3"代表“8:03”。
		exit;
		esac

