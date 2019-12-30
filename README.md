# bridge-game
bridge-game  2017.01  
  
# How to run 
  Run the server with nodejs.  
  connect to port 5566.  
    (Dennis: http://localhost:5566 only give your "Hello World")
           : need to use http://localhost:5566/index.html 
  Press findgame to join a room.  
  press add bot if you need one.  
  
# component
It's made up with NodeJs server and a webpage in HTML, Javascript, and CSS.   
Server and client communicate with Socket.IO module, so Socket.IO module will be needed to run the server.   
The webpage receive socket emit from server and change the Page with JQuery.  
The game is rendered with HTML canvas.  
   
some issue:  
The bot is not fully functional, it still has some bug in it.  
Due to the bot issue, the interface is still simple.  
I'm trying to improved the code.  
  
I have two roomate when I was a college student. Sometimes, when we want to play bridge, we need to find another person. So I made this bridge game with bots that can be the 4th person and play with us.   
   
# download (Dennis: not sure any need of this)
with module:  
https://drive.google.com/drive/folders/1TOdWGkGAGCK-pTNYNpX0eAAfvUIdQnnS

#need to install required modules under npm such as

```
npm install -g socket.io
```

and amend the var io to point to the absoulte address.

Dennis TODO:

1. bidding history
2. clear the table when done
3. clear instruction of the the pointer
4. the 1-7 should be clear and in fact should start with the default not blank or cannot be -1 so and so
5. chats
6. bot to be investigated
7. network seems to be left???
8. Use east west south north is better 

some log:

node server.js
Connection
Connection
Connection
Connection
Connection
Connection
new user: test1 logged XGQQEvYOUA3d5KqmAAAA
Finding for test1 XGQQEvYOUA3d5KqmAAAA
A game start in room 1
[ 'test1', 'Harry', 'Daniel', 'Owen' ]
bot2
bot2 called ♥ 1
bot3
bot3 called ♣ 2
test1 left.
undefined left.
Connection
Connection
Connection
Connection
Connection
Connection
Connection
new user: test2 logged VftvIhYmyx2o4FSVAAAC
Finding for test2 VftvIhYmyx2o4FSVAAAC
A game start in room 2
[ 'Colin', 'David', 'test2', 'Quinn' ]
bot0
bot0 called ♣ 1
bot1
bot1 called ♥ 1
bot3
bot3 called ♠ 1
bot0
bot0 called ♣ 2
bot1
bot1 called ♥ 2
bot3
bot3 called ♠ 2
bot0
bot0 passed
bot1
bot1 passed
Room 2 set goal at 8,6
bot0
[ '♣ 3', '♣ 5', '♣ 6', '♣ 7', '♣ 10', '♣ A' ]
[ '♦ 3', '♦ 6', '♦ 8' ]
[ '♥ 5', '♥ K' ]
[ '♠ 4', '♠ 10' ]
in case 0: there is no card on the table
	♣ matches rule 1, try to win this round with ♣ 
bot0 picked: ♣ A
[
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ]
]
bot1
[ '♣ 2', '♣ 8' ]
[ '♦ 9', '♦ J', '♦ K' ]
[ '♥ 7', '♥ 9', '♥ J', '♥ A' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 1: there is 1 card on the table
	try to win with target color
true
false
false
	failed: enemy is less on target color
bot1 picked: ♣ 2
bot3
[ '♣ 9', '♣ Q', '♣ K' ]
[ '♦ 5', '♦ 10' ]
[ '♥ 2', '♥ 8' ]
[ '♠ 2', '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 3: there are 3 cards on the table
	enemy win: try to win this round
	try to win with target color
	failed: bot's cards of target color is not big enough
bot3 picked: ♣ 9
bot0
[ '♣ 3', '♣ 5', '♣ 6', '♣ 7', '♣ 10' ]
[ '♦ 3', '♦ 6', '♦ 8' ]
[ '♥ 5', '♥ K' ]
[ '♠ 4', '♠ 10' ]
in case 0: there is no card on the table
	♣ matches rule 1, try to win this round with ♣ 
	♦ matches rule 1, try to win this round with ♦ 
	♥ matches rule 1, try to win this round with ♥ 
	 No match for rule 1
	 No match for rule 2
	partner call nothing at bidding state
	 No match for rule 3
	♣ matches rule 4, try to win this round with ♣ 
	♦ matches rule 4, try to win this round with ♦ 
	♥ matches rule 4, try to win this round with ♥ 
	 No match for rule 4
	♠ matches rule 6, try to win this round with king color
	 No match for rule 6
	 throw a useless card
bot0 picked: ♣ 3
[
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ]
]
bot1
[ '♣ 8' ]
[ '♦ 9', '♦ J', '♦ K' ]
[ '♥ 7', '♥ 9', '♥ J', '♥ A' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 1: there is 1 card on the table
	try to win with target color
true
true
false
	failed: enemy is less on target color
bot1 picked: ♣ 8
bot3
[ '♣ Q', '♣ K' ]
[ '♦ 5', '♦ 10' ]
[ '♥ 2', '♥ 8' ]
[ '♠ 2', '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 3: there are 3 cards on the table
	enemy win: try to win this round
	try to win with target color
	found the smallest card that can win this round: ♣ Q
bot3 picked: ♣ Q
bot3
[ '♣ K' ]
[ '♦ 5', '♦ 10' ]
[ '♥ 2', '♥ 8' ]
[ '♠ 2', '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 0: there is no card on the table
	♦ matches rule 1, try to win this round with ♦ 
	♥ matches rule 1, try to win this round with ♥ 
	 No match for rule 1
	 No match for rule 2

♥  
matches rule 3, try to feed partner, expecting partner to win with one of these color
bot3 picked: ♥ 2
[
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ]
]
bot0
[ '♣ 5', '♣ 6', '♣ 7', '♣ 10' ]
[ '♦ 3', '♦ 6', '♦ 8' ]
[ '♥ 5', '♥ K' ]
[ '♠ 4', '♠ 10' ]
in case 1: there is 1 card on the table
	try to win with target color
true
true
false
	failed: enemy is less on target color
bot0 picked: ♥ 5
bot1
[]
[ '♦ 9', '♦ J', '♦ K' ]
[ '♥ 7', '♥ 9', '♥ J', '♥ A' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 2: there are 2 cards on the table
	throw any card
bot1 picked: ♥ 7
[
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ]
]
bot3
[ '♣ K' ]
[ '♦ 5', '♦ 10' ]
[ '♥ 8' ]
[ '♠ 2', '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 1: there is 1 card on the table
	try to win with target color
true
false
false
	failed: enemy is less on target color
bot3 picked: ♥ 8
bot0
[ '♣ 5', '♣ 6', '♣ 7', '♣ 10' ]
[ '♦ 3', '♦ 6', '♦ 8' ]
[ '♥ K' ]
[ '♠ 4', '♠ 10' ]
in case 2: there are 2 cards on the table
	throw any card
bot0 picked: ♥ K
bot1
[]
[ '♦ 9', '♦ J', '♦ K' ]
[ '♥ 9', '♥ J', '♥ A' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 3: there are 3 cards on the table
	enemy win: try to win this round
	try to win with target color
	found the smallest card that can win this round: ♥ A
bot1 picked: ♥ A
bot1
[]
[ '♦ 9', '♦ J', '♦ K' ]
[ '♥ 9', '♥ J' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 0: there is no card on the table
	♦ matches rule 1, try to win this round with ♦ 
	 No match for rule 1
	 No match for rule 2
	partner call nothing at bidding state
	 No match for rule 3
	♦ matches rule 4, try to win this round with ♦ 
	♥ matches rule 4, try to win this round with ♥ 
bot1 picked: ♥ 9
[
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ]
]
bot3
[ '♣ K' ]
[ '♦ 5', '♦ 10' ]
[]
[ '♠ 2', '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 2: there are 2 cards on the table
	throw any card
bot3 picked: ♦ 5
bot0
[ '♣ 5', '♣ 6', '♣ 7', '♣ 10' ]
[ '♦ 3', '♦ 6', '♦ 8' ]
[]
[ '♠ 4', '♠ 10' ]
in case 3: there are 3 cards on the table
	enemy win: try to win this round
	bot don't have target color
	try to win with king color
	enemy is winning with target color
bot0 picked: ♠ 4
king recorded: ♠ 4
bot0
[ '♣ 5', '♣ 6', '♣ 7', '♣ 10' ]
[ '♦ 3', '♦ 6', '♦ 8' ]
[]
[ '♠ 10' ]
in case 0: there is no card on the table
	♦ matches rule 1, try to win this round with ♦ 
	 No match for rule 1
	 No match for rule 2
	partner call nothing at bidding state
	 No match for rule 3
	♣ matches rule 4, try to win this round with ♣ 
	♦ matches rule 4, try to win this round with ♦ 
	 No match for rule 4
	♠ matches rule 6, try to win this round with king color
	 No match for rule 6
	 throw a useless card
bot0 picked: ♦ 3
[
  [ false, false, false, true ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, true, false, false ]
]
bot1
[]
[ '♦ 9', '♦ J', '♦ K' ]
[ '♥ J' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 1: there is 1 card on the table
	try to win with target color
true
true
false
	failed: enemy is less on target color
bot1 picked: ♦ 9
bot3
[ '♣ K' ]
[ '♦ 10' ]
[]
[ '♠ 2', '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 3: there are 3 cards on the table
	enemy win: try to win this round
	try to win with target color
	failed: bot's cards of target color is not big enough
bot3 picked: ♦ 10
[
  [ false, false, false, true ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, true, false, false ]
]
bot3
[ '♣ K' ]
[]
[]
[ '♠ 2', '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 1: there is 1 card on the table
	bot don't have target color
	try to win with king color
bot3 picked: ♠ 2
king recorded: ♠ 2
bot0
[ '♣ 5', '♣ 6', '♣ 7', '♣ 10' ]
[ '♦ 6', '♦ 8' ]
[]
[ '♠ 10' ]
in case 2: there are 2 cards on the table
	throw any card
bot0 picked: ♦ 6
bot1
[]
[ '♦ J', '♦ K' ]
[ '♥ J' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 3: there are 3 cards on the table
	enemy win: try to win this round
	try to win with target color
	failed: bot's cards of target color is not big enough
bot1 picked: ♦ J
[
  [ false, false, false, true ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, true, false, true ]
]
bot3
[ '♣ K' ]
[]
[]
[ '♠ 3', '♠ 6', '♠ 7', '♠ Q', '♠ K' ]
in case 1: there is 1 card on the table
	try to win with target color
	failed: bot's cards of target color is not big enough
bot3 picked: ♠ 3
bot0
[ '♣ 5', '♣ 6', '♣ 7', '♣ 10' ]
[ '♦ 8' ]
[]
[ '♠ 10' ]
in case 2: there are 2 cards on the table
	throw any card
bot0 picked: ♠ 10
bot1
[]
[ '♦ K' ]
[ '♥ J' ]
[ '♠ 5', '♠ 8', '♠ 9', '♠ J' ]
in case 3: there are 3 cards on the table
	enemy win: try to win this round
	try to win with target color
	failed: bot's cards of target color is not big enough
bot1 picked: ♠ 5
delete room 2
Finding for test2 VftvIhYmyx2o4FSVAAAC
Connection
Connection
Connection
new user: testb logged ExX_mXIvqA7EtCDzAAAD
Connection
Connection
Connection
new user: testc logged 6pl2jZlBal3pk6IiAAAE
Connection
Connection
Connection
new user: test4 logged Zb9rhsJweiXyQSfeAAAF
Finding for test4 Zb9rhsJweiXyQSfeAAAF
Finding for testb ExX_mXIvqA7EtCDzAAAD
Finding for testc 6pl2jZlBal3pk6IiAAAE
A game start in room 3
[ 'test4', 'testb', 'test2', 'testc' ]
Room 3 set goal at 8,6
[
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ],
  [ false, false, false, false ]
]
king recorded: ♠ 4
[
  [ false, false, false, false ],
  [ false, false, false, true ],
  [ false, false, false, false ],
  [ false, false, false, false ]
]
Connection
Connection
Connection
Connection
new user: Ip11 logged jPOCDQ0Bh9QpJ1YiAAAG
Ip11 left.
undefined left.
new user: Ip11 logged 7mAMGoF2_VmXz-F7AAAI
Finding for Ip11 7mAMGoF2_VmXz-F7AAAI
A game start in room 4
[ 'Kevin', 'Elliot', 'Yale', 'Ip11' ]
bot0
bot0 called ♠ 1
bot1
bot1 called ♣ 2
bot2
bot2 called ♥ 2
Ip11 left.
Connection
undefined left.
testb left.
test4 left.
testc left.
test2 left.