## SlideCard CSS Layout Free Source Code By NorthFox Developers

#### Join Our Telegram Channel [ProgHub09](http://t.me/ProgHub09) and Also Download Our App.

![Video Here](https://github.com/princu09/SlideCard/blob/master/SlideCard.gif?raw=true)


#### HTML File

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Slide Card</title>
    <link rel="stylesheet" href="style.css">
    <link rel="icon" href="https://princu09.github.io/nfwebbuilder/img/logo.png" type="image/png" sizes="16x16">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" integrity="sha384-wvfXpqpZZVQGK6TAh5PVlGOfQNHSoD2xbE+QkPxCAFlNEevoEH3Sl0sibVcOQVnN" crossorigin="anonymous">
</head>

<body>
    <div class="container">
        <div class="card">
            <div class="imgBx" data-text="Design">
                <i class="fa fa-magic" aria-hidden="true"></i>
            </div>
            <div class="content">
                <div>
                    <h3>Design</h3>
                    <p>First You can choose a theme of your website.</p>
                    <a href="#">Read More</a>
                </div>
            </div>
        </div>
        <div class="card">
            <div class="imgBx" data-text="Code">
                <i class="fa fa-code" aria-hidden="true"></i>
            </div>
            <div class="content">
                <div>
                    <h3>Code</h3>
                    <p>After Choosing Theme We code that theme.</p>
                    <a href="#">Read More</a>
                </div>
            </div>
        </div>
        <div class="card">
            <div class="imgBx" data-text="Launch">
                <i class="fa fa-rocket" aria-hidden="true"></i>
            </div>
            <div class="content">
                <div>
                    <h3>Launch</h3>
                    <p>We Launch your website online after code. </p>
                    <a href="#">Read More</a>
                </div>
            </div>
        </div>
        <div class="card">
            <div class="imgBx" data-text="Earn">
                <i class="fa fa-inr" aria-hidden="true"></i>
            </div>
            <div class="content">
                <div>
                    <h3>Earn</h3>
                    <p>We Collect Payment after Launch.</p>
                    <a href="#">Read More</a>
                </div>
            </div>
        </div>
    </div>
</body>

</html>
```


#### CSS File

```
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap');
* {
    margin: 0;
    padding: 0;
    font-family: 'Poppins', sans-serif;
    box-sizing: border-box;
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    background: url('BG.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    min-height: 100vh;
}

.container {
    position: relative;
    width: 800px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin: 20px;
}

.container .card {
    position: relative;
    height: 250px;
    background: #fff;
    display: flex;
    width: 40%;
    margin: 30px 0;
}

.container .card .imgBx {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: orange;
    z-index: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    transition: 0.5s ease-in-out;
}

.container .card:hover .imgBx {
    width: 150px;
    height: 150px;
    left: -75px;
    top: 20%;
    transition: 0.5s ease-in-out;
    background: orangered;
}

.container .card .imgBx:before {
    content: attr(data-text);
    position: absolute;
    bottom: 0px;
    left: 0;
    width: 100%;
    text-align: center;
    font-size: 2em;
    opacity: .5;
    color: white;
    font-weight: 700;
}

.container .card .imgBx i {
    color: white;
    font-size: 8rem;
    justify-content: center;
    align-items: center;
    text-align: center;
    transition: 0.5s ease-in-out;
}

.container .card:hover .imgBx i {
    font-size: 5rem;
}

.container .card .content {
    position: absolute;
    right: 0;
    width: calc(100% - 75px);
    height: 100%;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.container .card .content h3 {
    margin-bottom: 5px;
    font-size: 24px;
}

.container .card .content a {
    display: inline-block;
    margin-top: 10px;
    padding: 5px 10px;
    background: #333;
    text-decoration: none;
    color: white;
}

.header h1 {
    color: #fff;
    position: absolute;
    top: 20%;
    left: 50%;
    font-size: 50px;
    -ms-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
}

.header h3 {
    font-weight: 600;
    letter-spacing: 5px;
    color: #fff;
    font-size: 15px;
    position: absolute;
    top: 24%;
    left: 50%;
    -ms-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
}

@media(max-width: 992px) {
    .container {
        width: 100%;
        flex-direction: column;
        align-items: center;
    }
    .container .card {
        width: 400px;
    }
}

@media (max-width: 768px) {
    .container .card {
        max-width: 300px;
        flex-direction: column;
        height: auto;
    }
    .container .card .imgBx {
        position: relative;
    }
    .container .card .imgBx,
    .container .card:hover .imgBx {
        width: 100%;
        height: 200px;
        left: 0;
    }
    .container .card .content {
        position: relative;
        width: 100%;
    }
}
```