# Python-Challenge

I was unable to complete this challenge.  
After working on this myself, with my classmates, with a TA, and asking an IT friend, I was only able to write the below code.
Having multiple inputs from multiple people led to me getting lost in my own code and not knowing what anything meant.
I deleted a significant portion of what I had written in order to try and start from scratch, but by that time it was too late.

Written at midnight 3/31/2019
____________________________  
  
  #Import the operating system and import the CSV
import os
import csv

#Assign all the values
#Set them at zero and empty placeholder
totalmonths = 0
totalvalue = 0
averagechange = 0
highestvalue = 0
lowestvalue = 0
highestdate = ''
lowestdate = ''
net_change_list = 0

#total_net = 0

# define the file I'm working with
# Did not do it the same as in class because the .py file is in the same folder as the csv


with open("budget_data.csv", newline="") as csvfile:
    csvreader = csv.reader(csvfile, delimiter=",")
    next(csvfile)

    readCSV = csv.reader(csvfile, delimiter=',')
    
    for row in csvfile:
        #print(row)
        row = next(csvfile)
        totalmonths += 1
        totalvalue += 1
        prev_net = int(row[1])
        net_change = int(row[1]) - prev_net

    print(totalmonths)

    '''for row in csvfile:
        totalmonths += 1
        totalvalue = totalvalue + int(firstrow[1])
        net_change = int(firstrow[1]) - prev_net
        prev_net = int(firstrow[1])
        net_change_list = net_change_list + [net_change]'''


    if int(row[1]) > highestvalue:
           highestvalue = int(row[1]) 
           highestdate = str(row[0])
           #fix the math, or the part of this one
    elif int(row[1]) < lowestvalue:
           lowestvalue = int(row[1])
           lowestdate = str(row[0])

averagechange = (totalmonths/totalvalue)


print(totalmonths)
#print(f"$",totalvalue)
print(totalvalue)
print(lowestvalue)
print(lowestdate)
print(highestvalue)
print(highestdate)
print(averagechange)
print(net_change)


