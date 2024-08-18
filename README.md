
CALCULATOR
//index.html//
!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>calculator By Vaibhavi</title>
</head>
<body>
    <div class="container">
        <h1>Calculator By vaibhavi</h1>


        <div class="calculator">
            <input type="text" name="screen" id="screen">
         <table>
            <tr>
                <td><button>(</button></td>
                <td><button>)</button></td>
                <td><button>C</button></td>
                <td><button>%</button></td>
                
            </tr>
            <tr>
                <td><button>7</button></td>
                <td><button>8</button></td>
                <td><button>9</button></td>
                <td><button>X</button></td>
                
            </tr>
            <tr>
                <td><button>4</button></td>
                <td><button>5</button></td>
                <td><button>6</button></td>
                <td><button>-</button></td>
                
            </tr>
            <tr>
                <td><button>1</button></td>
                <td><button>2</button></td>
                <td><button>3</button></td>
                <td><button>+</button></td>
                
            </tr>
            <tr>
                <td><button>0</button></td>
                <td><button>.</button></td>
                <td><button>/</button></td>
                <td><button>=</button></td>
                
            </tr>

         </table>
    </div>

    </div>
    
</body>
<script src="index.js"></script>
</html>

//style.css//

.container{
    text-align: center;
    margin-top: 23px;


}
table{
    margin: auto;
}

input{
    border-radius: 8px;
    border: 5px solid green;
    font-size: 33px;
    height: 55px;
}
button{
    border-radius: 15px;
    font-size: 40px;
    background-color: rgb(218, 246, 154);
    width: 102px;
    height: 75px;
}
.calculator{
    background-color: cornflowerblue;
    padding: 10px;
    border-radius: 9px;
    border: 2px solid black;
       display: inline-block;
}

//index.js//

let screen=document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for(item of buttons){
    item.addEventListener('click', (e)=>{
        buttonText = e.target.innerText;
        console.log('button text is ' , buttonText);
        if(buttonText=='X'){
       buttonText = '*';
       screenValue +=buttonText;
       screen.value = screenValue;
        }
        else if (buttonText =='C'){
            screenValue = "";
            screen.value = screenValue;
    

        }
        else if(buttonText =='='){
            screen.value = eval(screenValue);

        }
        else{
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}



TRIBUTE PAGE
//index.html//
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tribute page Website | Steve jobs</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
    <div class="content"></div>
    <section class="top_section"></section>  
    <div class="image_container"></div>   
    <img src="./steve jobs photo.jpg"alt="Tribute" /> 
    <div>
        <h1>
              <center> Steve Jobs</center>
        </h1>
        <h4>
          <center> (1955 - 2011)</center> 
        </h4>
    </div>   
    <section class="about_section">
     <center> <h2> Design is not just
             what it looks like </center>  
           <center> <h2>
                and feels like.
            design is how it works.
             </h2></center> 
            
        </h2>
    <section class="Biography">
         <h1>
          Biography:
      </h1>
        <p>
          Steven paul "Steve"  jobs was an american information technology etreprenuer and inventor.   
          he was the cofounder,chairman and CEO of apple inc,CEO and largest share holder of pixer
          animation studios;and founder,chairman,and CEO of next inc.jobs is widely recognised as pioneer 
          of the microcomputer revolution of the 1970's along with apple co-founder steve wozniak.
          "creative entrepreneur whose passion for perfection and ferocious six industries:
          personal computers,animated movies,music,phones,tablets,computing and digital publishing".
        </p>
    </section>

     <footer> <p>read more here made with apple by jorge sanz <a href="http://127.0.0.1:5500/index.html">wikipedia</a> </p> </footer>

    </div>
</body>
</html>

//styles.css//

*{

    margin: 0;
    padding: 0.2%;
    box-sizing: border-box;
}


.container{
    background-color: blanchedalmond;
   min-height: 200vh;
   border: 5px solid black;
}

.content{
    max-width: 900px;
    margin:auto;
    
}
.top_section{

     display: block;
     justify-content: space-between;
}
.top_section h1 {
              font-size: 60px;
              font-weight: bold;
              color: black;
}

.image_container,img{
     
    display: block;
    width: 40%;
    margin-left: auto;
    margin-right: auto;
}

.about_section {

    margin-top: 50px;

}
.about_section h2{
font-size: 40px;
font-weight: 1000;
margin-bottom: 20px;

}
.Biography {

    margin-left: 10%;
    margin-bottom: 10%;

}
.Biography h1 {
     margin-bottom: 4%;
    font-size: 50px;
}

.Biography p {
     
     font-size: 30px;
     line-height: 40px;
     text-align: justify;
     letter-spacing: 0.001cm;
     text-align: justify;
}
  footer{
      margin: 50px 0;
  }
   
  footer p {
        
       text-align: end;
  }

A BASIC TO DO WEBAPP

//index.html//

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <main>
          <div class="box">

            <input type="text" id="item" autofocus placeholder="write something here...">
            <ul id="to-do-box">
            </ul>
          </div>
         </main>
         <script src="https://kit.fontawesome.com/bf520e6492.js" crossorigin="anonymous"></script>
    <script src="app.js"></script>
</body>
</html>
//style.css//
* {
      padding: 0;
      margin: 0;
      box-sizing: border-box;
      font-family:'open sans',sans-serif;
}
main {

    width: 100%;
    height: 100vh;
    display:flex;
    justify-content: center;
    align-items: center;
    background-color: cornflowerblue;

}
.box {
    width: 600px;
  min-height:600px;
  background-color: white;
  border-radius: 5px;
  padding: 25px;

}
#item {
       padding: 10px;
       font-size: 30px;
       width: 100%;
       border: 0;
       outline: 0;
       display: block;
       font-weight: bold;
       box-shadow: 0px 0px 2px grey;
}

#to-do-box  {
        margin-top: 20px;
         list-style: none;
    
    
}

#to-do-box li {

        position: relative;
         background-color: darkslategrey;
         color: white;
         padding: 10px;
         border-radius: 5px;
         padding-right: 25px;
         margin-top: 10px;
         user-select: none;

}

#to-do-box li i {
      
        position: absolute;
        right: 10px;
        top: 10px;
}
.done{

    text-decoration: line-through;
    color: black;
    background-color: lightslategrey !important;
}

//app.js//

const item = document.querySelector("#item")
const toDoBox = document.querySelector("#to-do-box")

item.addEventListener(

    "keyup" ,
    function(event){
        if(event.key == "Enter") {

            addToDo(this.value)
            this.value = " "
        }

        
    }
)

const addToDo = (item) => {
     const listItem = document.createElement("li");
     listItem.innerHTML = `
     
     ${item}
     <i class="fas fa-times"></i>

     `;
     listItem.addEventListener(
        "click" ,

        function() {

            this.classList.toggle("done");
        }

     )
     listItem.querySelector("i").addEventListener(

        "click",
        function()
        {
            listItem.remove()
        }
     )
     toDoBox.appendChild(listItem)
     
     

}

