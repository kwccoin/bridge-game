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