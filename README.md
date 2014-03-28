Khan-Acadamy-Code
=================

My game
noStroke();  
    
    //Title Screen Variables

var badCircle=20;
var circleY=20;
var speed=3;
var how=21;
var howto = false;
var game = false;
var draw= function() {
    if(howto===false&&game===false){
        
    
    //Title Screen Circles
    
    background(255, 255, 255);
     fill(0, 0, 0);
    
    ellipse(badCircle,circleY+50,20,20);
    ellipse(badCircle,circleY+100,20,20);
    ellipse(badCircle,circleY+150,20,20);
    ellipse(badCircle,circleY+200,20,20);
    ellipse(badCircle,circleY+250,20,20);
    ellipse(badCircle,circleY+300,20,20);
    ellipse(badCircle,circleY+350,20,20);
    
    //Animation of Title Screen Circles
    
    badCircle=badCircle+speed;
    
    if(badCircle>390){
    speed+=-3;
    }
    if(badCircle<10){
    speed+=3;
    }
    
    //Title
    
    fill(0, 0, 0);
    textSize(20);
    text("DEATH CIRCLES",128,28);
    
    //Buttons
    
    fill(13, 255, 0);
    rect(135,100,138,85); //Play
    fill(255, 0, 0);
    rect(135,250,138,85); //How to Play
    text("Play",185,148);
    fill(13, 255, 0);
    text("How to Play",152,297);
    }
    //How to Play
   if(howto===true){
       background(255, 255, 255);
       fill(0, 0, 0, 0);
       rect(-5, -5, 75, 55, 10);
       
       fill(0, 0, 0);
        textSize(20);
        text("How to Play",145,28);
        text("Use the arrow keys to move the red ball",how,88);
        text("around the screen.",how,123);
        text("Avoid the black balls flying around the",how,176);
        text("screen.",how,201);
        text("Get to the other side of the screen to",how,254);
        text("pass the level.",how,289);
        textSize(25);
        text("BACK", -1, 30);
        text("Good luck and don't die!",75,343);
   }
    
    if(game === true){
    
        background(255, 255, 255);
        fill(0, 0, 0);
        rect(-5, -5, 75, 55, 10);
        fill(0, 0, 0);
        textSize(25);
        text("BACK", -1, 30);
    }   
    
    
};
   
   var mouseClicked = function(){
       if(mouseX>150 && mouseX<250 && mouseY>250 && mouseY<340){
        howto = true;
    }
    if(howto === true&&mouseX<70&&mouseY<50){
        howto = false;
    }
    
    //Play
    
    if(mouseX>150&&mouseX<250&&mouseY>100&&mouseY<200&&howto===false&&game===false){
        game = true;
    }
    if(game===true&&mouseX<70&&mouseY<50){
        game = false;
    }
   };

//Problems:

//On the title screen, the ellipses move back and forth and in sinc.  How do I make it so that the ellipses bounce all over the place?
