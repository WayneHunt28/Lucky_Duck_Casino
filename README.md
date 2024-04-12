Module 3 Challenge
UWA Cybersecurity Bootcamp 2024


A High-Stakes Investigation

You have just been hired by Lucky Duck Casino as a security analyst.

Lucky Duck has lost a significant amount of money on the roulette tables over the last month.

The largest losses occurred on March 10, 12, and 15.

Your manager believes there is a player working with a Lucky Duck dealer to steal money at the roulette tables.

The casino has a large database containing data on wins and losses, player analysis, and dealer schedules.

You are tasked with navigating, modifying, and analyzing these data files to gather evidence on the rogue player and dealer.

You will prepare several evidence files to assist the prosecution.

You must work quickly, as Lucky Duck can't afford any more losses.

Lucky Duck Casino has provided you with the following files:

Roulette Player Data: Week of March 10Links to an external site.
Employee Dealer Schedule: Week of March 10Links to an external site.
NOTE
The instructions ask you to set up the files using a wget command, but the files are also provided in compressed zip format if the command does not work.

Lab Environment
You will use your web lab virtual machine for today's activities.
Instructions
Use your command-line skills to uncover the identities of the rogue casino player and dealer colluding to scam Lucky Duck out of thousands of dollars.

After your investigation, you will provide a summary of your findings to the casino.

Step 1: Investigation Preparation
Your first task is to set up directories to prepare for your investigation.

From your HOME Directory, make a single directory titled Lucky_Duck_Investigations.

In this directory, create a directory for this specific investigation titled Roulette_Loss_Investigation.

In Roulette_Loss_Investigation, create the following directories:

Player_Analysis to investigate the casino player.
Dealer_Analysis to investigate the dealers.
Player_Dealer_Correlation to summarize your findings about the collusion.
Create empty files called Notes_<Directory Name>.txt under each subdirectory to store investigation notes.

For example: Notes_Player_Analysis.txt
Step 2: Gathering Evidence
Your next task is to move evidence from the specific days on which Lucky Duck experienced heavy losses at the roulette tables.

Navigate to your HOME directory where you created the Lucky_Duck_Investigations directory and run the following command to set up the evidence files:

wget "https://drive.google.com/uc?id=1ZLY_fuFu3wz7tOlxf-GUrnvp3htuGKSa" -O 3-HW-setup-evidence && chmod +x ./3-HW-setup-evidence && ./3-HW-setup-evidence
After running this command, your current directory should have the following subdirectories:

Dealer_Schedules_0310: Contains the dealer schedules.
Lucky_Duck_Investigations: Contains the investigation directories and notes files you created.
Roulette_Player_WinLoss_0310: Contains the data for player wins and losses.
The Dealer_Schedules_0310 and Roulette_Player_WinLoss_0310 directories contain the dealer schedules and win/loss player data from the roulette tables during the week of March 10.

Since the losses occurred on March 10, 12, and 15, move the schedules for those days into the directory Dealer_Analysis.

Move the files for those days into the directory Player_Analysis.

Step 3: Correlating the Evidence
Your next task is to correlate the large losses from the roulette tables with the dealer schedule. This will help you determine which dealer and player are colluding to steal money from Lucky Duck.

NOTE
Winnings for Lucky Duck Casino are indicated with a positive number and losses are indicated with a negative number.

Complete the player analysis with the following steps:

Navigate to the Player_Analysis directory.

Use grep to isolate all of the losses that occurred on March 10, 12, and 15.

Place those results in a file called Roulette_Losses.txt.

Preview the file Roulette_Losses.txt and analyze the data.

Record the following in the Notes_Player_Analysis.txt file:

The times the losses occurred on each day.
Whether there is a certain player who was playing during each of those times.
The total count of times this player was playing. > Hint: Use the wc command to find this value.
Complete the dealer analysis with the following steps:

Navigate to the Dealer_Analysis directory.

This file contains the dealer schedules for the various Lucky Duck casino games: Blackjack, Roulette, and Texas Hold 'Em.

Preview the schedule to view the format and to understand how the data is separated.
Using your findings from the player analysis, create a separate script to look at each day and time that you determined losses occurred. Use awk, pipes, and grep to isolate out the following four fields:

Time

a.m./p.m.

First name of roulette dealer

Last name of roulette dealer

For example, if a loss occurred on March 10 at 2 p.m., you would write one script to find the roulette dealer who was working at that specific day and time.

HINT
Run all of the scripts and append those results to a file called Dealers_working_during_losses.txt.

Preview your file Dealers_working_during_losses.txt, and analyze the data.

Record the following in the Notes_Dealer_Analysis.txt file:

The primary dealer working at the times where losses occurred.

How many times the dealer worked when major losses occurred.

Complete the player/employee correlation.
In the notes file of the Player_Dealer_Correlation directory, add a summary of your findings noting the player and dealer you believe are colluding to scam Lucky Duck.

Make sure to document your specific reasons for this finding.

Step 4: Scripting Your Tasks
You manager is impressed with the work you have done so far on the investigation.

They've now tasked you with building a shell script that can easily analyze future employee schedules. They will use this script to determine which employee was working at a given time in the case of future losses.

Complete the following tasks:

Remain in the Dealer_Analysis directory. Develop a shell script called roulette_dealer_finder_by_time.sh that can analyze the employee schedule to easily find the roulette dealer at a specific time.

HINT
Design the shell script to accept the following two arguments:
Date (four digits)
Time
NOTE
The argument should be able to accept a.m. or p.m.

Test your script on the schedules to confirm that it outputs the correct dealer at the time specified.

Optional Additional Challenge
In case there is future fraud on other Lucky Duck games, create a shell script called roulette_dealer_finder_by_time_and_game.sh that has the following three arguments:

Specific time
Specific date
Casino game being played
HINT
Submission Guidelines
Move the following to the Player_Dealer_Correlation directory:

All note files
The following evidence files:
Roulette_Losses.txt
Dealers_working_during_losses.txt
Your shell script(s)
Compress the Player_Dealer_Correlation folder to a zip file, and submit it through Canvas.

Use the following documentLinks to an external site. for assistance with zipping and submitting homework from your weblab.
