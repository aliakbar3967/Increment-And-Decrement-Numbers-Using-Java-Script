<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Increment And Decrement With Java-Script</title>
    <style>
        *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: sans-serif;
}
body{
    height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background: skyblue;
}
.wrapper{
    height: 120px;
    min-width: 380px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #ddd;
    border-radius: 12px;
    box-shadow: 0 5px 10px #000;
}
.wrapper span{
    width: 100%;
    text-align: center;
    font-size: 55px;
    font-weight: 600;
    cursor: pointer;
    user-select: none;
}
.wrapper span.num{
    font-size: 50px;
    border-right: 2px solid #000;
    border-left: 2px solid #000;
    pointer-events: none;
}
    </style>
</head>
<body>
    <div class="wrapper">
        <span class="minus">-</span>
        <span class="num">01</span>
        <span class="plus">+</span>
    </div>
    <script>
    const plus = document.querySelector(".plus"),
minus = document.querySelector(".minus"),
num = document.querySelector(".num");
let a = 1;
plus.addEventListener("click", ()=>{
    a++;
    a = (a < 10) ? "0" + a : a;
    num.innerText = a;
});

minus.addEventListener("click", ()=>{
    if(a > 1){
        a--;
        a = (a < 10) ? "0" + a: a;
        num.innerText = a;
    }
});
    </script>
</body>
</html>
