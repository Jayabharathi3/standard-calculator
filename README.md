# Design of a Standard Calculator

## AIM:

To design a web application for a standard calculator.

## DESIGN STEPS:

###Step 1:

Clone the github repository and create Django admin interface.

###Step 2:

Change settings.py file to allow request from all hosts.

###Step 3:

Use CSS for creating attractive colors.

###Step 4:

Write JavaScript program for implementing five different operations.

###Step 5:

Validate the HTML and CSS code.

###Step 6:

Publish the website in the given URL.


## PROGRAM :
```

cal.html


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="/static/css/style.css">
    <title>Calculator</title>
</head>

<body>
    <div class="container">
        <h1>Calculator</h1>

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
<script src="/static/js/index.js"></script>

</html>


style.css

.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #53e236;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: whitesmoke;
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid #d61a13;
    background-color: #1170ec ;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}


index.js

let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}

```

## OUTPUT:

## CLIENT OUTPUT:


![calculator1](https://github.com/Jayabharathi3/standard-calculator/assets/120367796/e782a45b-fcc2-4069-bdef-f17c37518dba)


![calculator2](https://github.com/Jayabharathi3/standard-calculator/assets/120367796/69ad5498-51e5-4400-ae5e-6bb69bf68dfc)


## SERVER OUTPUT:

![servercal](https://github.com/Jayabharathi3/standard-calculator/assets/120367796/d69d3629-4962-4da7-8623-fa2a18fb0f94)




## Result:

The program for creating a simple calculator using javascript is executed successfully.

