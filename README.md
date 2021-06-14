# THIeve-GaMe
var back=createSprite(200,200);
back.setAnimation("gradient_20_1");
back.scale=1.3;
var thieve=createSprite(10,10,10,10);
var carrot=createSprite(300,200);![carrot](https://user-images.githubusercontent.com/85548460/121851539-e37ebb80-cd0b-11eb-882d-f50486925372.png)
![gradient_20_1](https://user-images.githubusercontent.com/85548460/121851737-19bc3b00-cd0c-11eb-832a-a36794a3db89.png)
![thieve](https://user-images.githubusercontent.com/85548460/121851746-1d4fc200-cd0c-11eb-936c-2c528d0b78a3.png)

carrot.setAnimation("gamefood12_1");
var l1=createSprite(100,200,200,10);
var l2=createSprite(300,200,200,10);
l1.shapeColor="red";
l2.shapeColor="red";

//var l3=createSprite()
var start=createSprite(200,200);
start.setAnimation("start_button_1");
var gameState;
//gameState="PLAY";
thieve.shapeColor="navy";



  function draw()
{
  background(0);
  drawSprites();
  if(mousePressedOver(start))
  {
    gameState="PLAY";
  }
  if(gameState==="PLAY")
  {
   pLAy();
  }
  /*if(gameState==="END")
  {
   eNd();
  }
}*/
}
function pLAy()
{
   start.visible=false;
    l1.velocityY=5;
    l2.velocityY=-5;
    if(l1.y>380)
    {
      l1.velocityY=-5;
    }
    if(l1.y<1)
    {
      l1.velocityY=5;
    }
    carrot.visible=true;
}
/*function eNd()
{
  l1.velocityX=0;
   l2.velocityY=0;
}*/
