var trex ,trex_running,chao;

function preload(){
  trex_running=loadAnimation("trex1.png","trex3.png","trex4.png");
  
}

function setup(){
  createCanvas(600,200)
  
 chao=createSprite(200,180,400,20);
 trex=createSprite(50,170,20,50);
 trex.addAnimation("running",trex_running);
 trex.scale=0.5;
}

function draw(){
  background("green")

  if(keyDown("space")){
    trex.velocityY=-10;
  }

  trex.velocityY += 0.8;

  trex.collide(chao)
  
  drawSprites();
}
