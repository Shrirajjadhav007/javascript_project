# javascript_project
<!-- html -->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>counter page</title>
    <link rel="stylesheet" href="shriraj.css">
</head>
<body>
    <div id="main-continer">
        <header>
            <h1>Counter</h1>
        </header>
        
        <div id="count-display">
            <h1  id="count">0</h1>
        </div>
       
        <div id="container">
            <button id="Descrese" class="button" >Decrease</button>
            <button id="Reset" class="button">Reset</button>
            <button id="Increse" class="button">Increase</button>
        </div> 
    </div>
     <script src="./shriraj.js"></script> 
</body>
</html>
<!-- css file -->
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
   display: flex;
   justify-content: center;
   align-items: center;
}

#main-continer{
    min-width: 30%;
    min-height: 380px;
    background-color: antiquewhite;
    display: flex;
    flex-direction: column;
    /* gap: 20px; */
    border-radius: 16px;
}

header{
     width: auto;
     height: 100px;
     /* background-color: aliceblue; */
     display: flex;
     justify-content: center;
     align-items: center;
     font-size: 25px;
     color: rgb(209, 166, 250);
}
#count-display{
     width: auto;
     min-height: 200px;
     /* background-color: aqua; */
     text-align: center;
     position: relative;
     /* bottom: 5%; */

}
#count{
    font-size: 100px;
    /* position: relative; */
    /* top: 30px; */
    color: rgb(241, 94, 170);
}
#container{
  width: auto;
  height: 60px;
  display: inline-flex;
  justify-content: center;
  justify-content: space-around;
}

.button{
    width:30%;
    height:30px;
    background-color: aliceblue;
    border: none;
    border-radius: 16px;
}

@media screen and (max-width: 300px) {
    
    #container{
        display: inline-flex;
        flex-direction: column;
        gap: 10px;
    }
    .button{
        width: 100%;
    }
  }
<!--javascript script  -->
let acces_Des=document.getElementById("Descrese")
let acces_Reset=document.getElementById("Reset");
let acces_Inc=document.getElementById("Increse");

let i=0;

acces_Des.addEventListener("click",function(){
        if(i >=1 ){
          i--
          document.getElementById("count").innerText=i;
        }else if(i < 1){
          document.getElementById("count").innerText="0"
          alert("alerdy zero don`t decrease more");
        }
        
});

acces_Inc.addEventListener("click",function(){
  i++       
  document.getElementById("count").innerText=i;
})

acces_Reset.addEventListener('click',function(){
       if(i===0){
        alert("alerdy reset")
       }
       i=0;
       document.getElementById("count").innerText="0";
})
