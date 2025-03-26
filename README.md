# Dream-premier-League
# <u>Dream Premier League (DPL)</u>

### A match of DPL is going on. Team Aravali has a made score of **195** for **7** in **20** overs and the opponent Team Shivalik is doing some analytics to find out what they need to do to win. You are the Data Scientist of the Team Shivalik and you have been asked to help them.

## <u>Problem 1</u>

###Team Shivalik has stored the runs made by Team Aravali players in the following dictionary.



aravali ={ "Dhoni":25, "Virat":31, "Pollard":11, "Rohit": 0, "Maxwell":12, "Sachin":59, "Sehwag":12 }

### Get the list of all players in Team Aravali

# Get the list of players in Team Aravali
list_players= list(aravali.keys())
print(list_players)

## <u>Problem 2</u>

### By mistake, the runs made by Rohit was recorded as <code>0</code>. Your next task is to figure out how many runs were made by Rohit and update the dictionary

# We know the total runs
total_run= 195
total_recorded_run= sum(aravali.values())
rohit_run= total_run-total_recorded_run
print(rohit_run)





# Print runs scored by Rohit
rohit_run= total_run-total_recorded_run
print(rohit_run)

# Update the dictionary with correct value of runs
aravali['Rohit']= rohit_run
print(aravali)

## <u>Problem 4</u>

#### Your next task is to find out who scored the second highest runs in Team Aravali

# Your code below
aravali_copy=aravali.copy()
list_of_runs=list(aravali_copy.values())
print(list_of_runs)
list_of_runs.sort()
print(list_of_runs)
second_highest_run= list_of_runs[-2]
print(second_highest_run)
for key,value in aravali_copy.items():
  if value==second_highest_run:
    print(key)

## <u>Problem 4</u>

#### Just out of curiosity, you want to find out the unique runs made by Team Aravali players.

# Your code below
run_set = set(list(aravali_copy.values()))

# Print the unique runs
run_set

## <u>Problem 5</u>
#### Team Shivalik has 6 fixed players and 5 slots for players who are playing good currently. Create two collections using appropriate data structure to write this 6 fixed and 5 mutable players. You can choose any player you want.

#### Available Players in the squad :
<code>['Vijay', 'Lasith', 'Dravid', 'Smith', 'Ambati', 'Hardik', 'Sushant', 'Mandeep', 'Harbhajan', 'Yuvraj', 'Jadeja','Rajeev','Amrit']


# Your code below
fixed = ['Dravid', 'Hardik', 'Harbhajan', 'Yuvraj', 'Jadeja','Rajeev']
mutable =['Vijay', 'Lasith', 'Smith', 'Ambati', 'Mandeep']

# Print them on same line using comma to seperate them
print(fixed)
print(mutable)

## <u>Problem 6</u>
Try changing fixed player and mutable player

# Change fixed player
fixed[0]= 'Smith'
fixed

# Change mutable player
mutable[2]= 'Dravid'
mutable

## <u> Problem 7</u>

#### Find out the runrate required for Team Shivalik to win (for 20 overs)<br>
#### Hint: Runrate is runs required per over to win the match

# Your code here
total_run=195
required_run =total_run+1
runrate= required_run/20
runrate


# Print the run rate
print(runrate)

## <u> Problem 8</u>
#### You have just received a secret message form your informant stating that some players of the other team are into match fixing. You have to decode a message and inform authorities about it.<br>

#### You received a string **"skdlfjnvuerhw qefnnaosfu qrhviudhfv wuirhv adknlkxjcier vafuvhkajn iuvhsf vasuif KJSHFKJ aeuihvasf akjfhiufe"** and index of "i" are going to be "no balls".


### Find the first and last no ball from the string.

#First no ball
message = "skdlfjnvuerhw qefnnaosfu qrhviudhfv wuirhv adknlkxjcier vafuvhkajn iuvhsf vasuif KJSHFKJ aeuihvasf akjfhiufe"
first_no_ball=message.find('i')
print(first_no_ball)


# Last no ball

# Print the first and last ball numbers
reverse_message=message[::-1]
last_no_ball=reverse_message.find('i')
print(last_no_ball)
last_no_ball=message.rfind('i')
print(last_no_ball)


## <u>Problem 9</u>

### You have given the information about fixing to the authorities and they are going to verify it during the match. But still you have to work on your strategy.

### It is in your hands to automate the decision on who goes on 4th position for batting depending on following criteria:

* if runs made by Team Shivalik is less than 50, Smith will play
* if runs are between 51 to 100 then Sir Jadeja will go
* if runs are above 100 then Hardik will play

# Your code below
B_runs = int(input())
if B_runs > 0 and B_runs <= 50:
  print('Smith will play')
elif B_runs >= 51 and B_runs <=100:
  print('Sir jadega will go')
elif B_runs >100:
  print('Hardik will play')
else:
  print('Invalid Input')






# Hurray! Turns out you won the match and the guilty players are punished as well. You should be proud of yourself!

