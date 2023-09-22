project related to dom 

soltutoin-1

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style> 
     .button{  width:100px;
                height:100px;
            border:solid blue 2px;
         display:flex ;
           align-items: center; }
           .canvas {
  margin: 100px auto 100px;
  width: 80%;
  text-align: center;
}
span {
  display: block;}
 
    
    #pink{ background:pink}
    #yellow{ background:yellow}
    #red{ background:red}
    #green{ background:green}

    
    
    </style>
</head>
<body>

    <nav> <a href="https://stackblitz.com/edit/dom-project-chaiaurcode?file=1-"> home</a>
    
        <a href="https://stackblitz.com/edit/dom-project-chaiaurcode?file=1-"> insta</a>
    
    
    </nav>
    <div class="convas">
    <h1> colour scheme switcher</h1>
    <span class="button" id="pink"></span>
    <span class="button" id="yellow"></span>
    <span class="button" id="green"></span>
    <span class="button" id="red"></span>
    <h2> try clicking on one colors above to changethe background color ofthis page</h2>
</div>

<script>
    const buttons=document.querySelectorAll(".button");
    const body=document.querySelector("body");

    buttons.forEach(function(button){
        console.log(button);
        button.addEventListener("click", function (e){
            console.log(e);
            console.log(e.target);
            if (e.target.id=="yellow"){
                body.style.backgroundColor="yellow";
            }
            if (e.target.id=="red"){
                body.style.backgroundColor="red";
            }
            if (e.target.id=="pink"){
                body.style.backgroundColor="red";
            }
            if (e.target.id=="green"){
                body.style.backgroundColor="red";
            }
        });

    });
     













</script>
    </body>
</body>
</html>