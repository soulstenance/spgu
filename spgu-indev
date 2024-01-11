#!/bin/bash
echo "Welcome to Soul's Pretty Good Updater v0.0.3 Alpha for Debian based systems."
echo "This script is licensed under GPL v3 and is provided as-is with no guarantee of suitability for a particular purpose. Use at your own risk."
echo ""

#VARIABLES
#Modules
	APTMOD="true"
	FLATMOD="true"
#Colors
	GREEN=`echo -en "\e[32m"`
	RED=`echo -en "\e[31m"`
	NORMAL=`echo -en "\e[0m"`

#INDEV
#This section warns the user they are using a development version of the application - it can be commented out for stable versions
read -p "${RED}WARNING:${NORMAL} This is an indev version - code may be unstable or break! Proceed anyways y/N? " ANSWERx
case "$ANSWERx" in
	[yY])
		echo "Proceeding..."
		echo "Thank you for testing this software! Please report any bugs you find."
		echo ""
		;;
	*)
		echo "Aborted."
		exit
		;;
esac

#MODULE CHECKS
if [ "$APTMOD" == "true" ]
then
	echo "Base module is ${GREEN}ACTIVE${NORMAL}"
else
	echo "Base module is ${RED}INACTIVE${NORMAL}"
fi
if [ "$FLATMOD" == "true" ]
then
	echo "Flatpak module is ${GREEN}ACTIVE${NORMAL}"
else
	echo "Flatpak module is ${RED}INACTIVE${NORMAL}"
fi
echo "No custom modules found."
echo ""

#PROMPT
#Apt update
read -p "Would you like to update apt now Y/n? " ANSWER0
case "$ANSWER0" in
	[yY])
		sudo apt update && sudo apt upgrade -y
		echo "Apt update complete!"
		;;
	[nN])
		echo "Thank you for your time! Goodbye!"
		;;
#	[aA])
#	    sudo apt update && sudo apt upgrade -y
#		echo "Apt update complete!"
#		ANSWER1=ANSWER0
#		;;
	*)
		sudo apt update && sudo apt upgrade -y
		echo "Apt update complete!"
		;;
esac

#Flatpak update
read -p "Would you like to update flatpak now Y/n? " ANSWER1
case "$ANSWER1" in
	[yY])
		echo "Updating flatpak..."
		flatpak update -y
		echo "Flatpak update complete!"
		;;
	[nN])
		echo "Thank you for your time! Goodbye!"
		;;
#	[aA])
#	    echo "Updating flatpak..."
#		flatpak update -y
#		echo "Flatpak update complete!"
	*)
		echo "Updating flatpak..."
		flatpak update -y
		echo "Flatpak update complete!"
		;;
esac
