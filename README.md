<p></p>

<h2 align="center">ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ПРОФЕССИОНАЛЬНОГО ОБРАЗОВАНИЯ <br> «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ» <br> КАФЕДРА ИНФОРМАТИКИ </h2>
<p align="center">Лабораторная работа №8 <br>
по курсу «Web-технологии, языки и средства создания web-приложений» 

<p align="center"><b>"Разработка серверных скриптов"</b><p>
<p align="right"><b>Выполнила: </b> студентка 331 группы Витковская Полина</p>
<p  align="right"><b>Принял: </b> Соболев Е. И., старший преподователь</p>
<br>
<br>
<br>
<p align="center">Южно-Сахалинск <br> СахГУ <br> 2024</p>
<h2> Введение </h2>
<p>Лабораторные работы по дисциплине «Web-технологии, языки и средства создания web-приложений» предназначены для освоения полученных теоретических знаний на практике. Перед началом лабораторной работы были поставлены цели: <br>
<ol>
  <li>Используя PHP, решить задачи.
  <li>Сделать задачи на Node.js</li>
</ol>
В соответствии с данными целями необходимо решить следующие задачи:
<ol>
   <li> Написать скрипты для решения данных задач.
   </ol>
Для реализации данной работы будет использоваться Visual Studio Code. Выполнение кода будет происходить в браузере Google Chrome с использованием node.js.
</p>
<h2>Решение задач</h2>

<p>Код на php:</p>
<p>https://www.w3schools.com/php/phptryit.asp?filename=tryphp_compiler</p>

```javascript
<!DOCTYPE html>
<html>
<body>

<?php

//	1.
echo "Задание 1 <br>";
//  Автор: Витковская Полина
/* 
    Дата выполнения: 25.01.2024
*/
echo "Проснулись, улыбнулись!";
echo "<br><br>";

//	2.
$tvChannel;		//	название телеканала
$manAdress;		//	адрес производителя
$carColor;		//	цвет автомобиля
$waterTemp;		//	температура воды
$phoneModel;	//	модель телефона

//	3.
echo "Задание 3 <br>";
$three = 3;
$five = 5;
$eight = 8;
echo "$three, $five, $eight";
echo "<br>";

$sum = $three + $five + $eight;
echo $result = 2 + 6 + 2 / 5 - 1;
echo "<br><br>";

//	4.
echo "Задание 4 <br>";
$a = 1;
$b = 2;
echo "$a, $b";
echo "<br>";
$c = $a;
$d = $b;
echo "$c, $d";
echo "<br>";
$a = 3;
$b = 4;
echo "$a, $b, $c, $d";
echo "<br><br>";

// 5.
echo "Задание 5 <br>";
define("const1", 41);
define("const2", 33);
echo const1 + const2;
echo "<br><br>";

//	6.
echo "Задание 6 <br>";
$a = 152;
$b = '152';
$c = 'London';
$d = array(152);
$e = 15.2;
$f = false;
$g = true;
var_dump($a, $b, $c, $d, $e, $f, $g);
echo "<br><br>";

//	7.
echo "Задание 7 <br>";
echo "\$a = $a, \$b = $b", PHP_EOL;
echo "<br><br>";

//	8.
echo "Задание 8 <br>";
$first = "Доброе утро";
$second = "дамы";
$third = "и господа";
echo $first . ", " . $second . " " . $third, PHP_EOL;
echo "<br><br>";

// 9.
echo "Задание 9 <br>";
$arr1 = [1, 2, 3, 4, 5];
$arr2 = [6, 7, 8, 9, 10];
$arr1["element"] = 25;

unset($arr2[0]);
echo $arr1[2]." ". $arr2[2];
echo "<br>";

var_dump($arr1, $arr2);
echo "<br>";
echo count($arr1)." ". count($arr2);
echo "<br><br>";

//	10.
echo "Задание 10 <br>";
define("N", 5);

for ($i = 0; $i < N; $i++) {
	echo random_int(-21, 35);
	echo "<br>";
}
echo "<br><br>";

//	11.
echo "Задание 11 <br>";
$sum = 0;
for ($i = 0; $i < N; $i++) {
	$sum += random_int(-21, 35);
}
echo $sum;
echo "<br><br>";

// 12.
echo "Задание 12 <br>";
for ($i = 0, $last = null; $i < N; $i++) {
	$num = random_int(-50, 50);
	echo $num;

	if ($last != null)
		if ($num > $last)
			echo " - Больше предыдущего";
		else if ($num < $last)
			echo " - Меньше предыдущего";
		else
			echo " - Равны";
	$last = $num;
	echo "<br>";
}
echo "<br><br>";

//	13.
echo "Задание 13 <br>";
function Fibb($n)
{
	if ($n <= 1) return 0;

	if ($n == 2) return 1;

	return Fibb($n - 1) + Fibb($n - 2);
}

echo N, " число Фибоначчи = ", Fibb(N);
echo "<br><br>";

//	14.
echo "Задание 14 <br>";
$number = 12345;
do {
	echo $number % 10;
	$number = ($number - $number % 10) / 10;
} while ($number > 0);
echo "<br><br>";

//	15.
echo "Задание 15 <br>";
$number = 12345;
$hasOdds = false;
do {
	$num = $number % 10;
	if ($num % 2 != 0) {
		$hasOdds = true;
		echo $num;
	}
	$number = ($number - $number % 10) / 10;
} while ($number > 0);
if (!$hasOdds) echo "Нечетных цифр не обнаружено!";
echo "<br><br>";

//	16.
echo "Задание 16 <br>";
for ($i = 0; $i < 7; $i++) {
	$arr[$i] = random_int(-10, 10);
}
for ($i = 0; $i < 7; $i++) {
	echo $arr[$i], " ";
}
echo "<br><br>";

//	17.
echo "Задание 17 <br>";
$m = 5;
$n = 5;
for ($i = 0; $i < $m; $i++) {
	$arr[$i] = [];
	for ($j = 0; $j < $n; $j++) {
		$arr[$i][$j] = random_int(-10, 10);
	}
}
echo "<br>";
for ($i = 0; $i < $m; $i++) {
	for ($j = 0; $j < $n; $j++) {
		echo str_pad($arr[$i][$j], 4, " ");
	}
	echo "<br>";
}
echo "<br><br>";

//	18.
echo "Задание 18 <br>";
$N = 20;
for ($i = 1; $i <= $N; $i++) {
	$arr[$i - 1] = $i;
}

//1
echo "Первый вариант<br>";
echo "1 | ";
for ($i = 0, $j = 0, $k = 1; $i < $N; $i++) {
	echo $arr[$i], " ";
	if (++$j >= $k) {
		echo "<br>";
		$j = 0;
		$k++;
        echo $k." | ";
	}
}

//	2)
echo "<br>Второй вариант<br>";
echo "1 | ";
for ($i = 1, $j = 0, $k = 1; $i <= $N; $i++) {
	echo $i, " ";
	if (++$j >= $k) {
		echo "<br>";
		$j = 0;
		$k++;
        echo $k." | ";
	}
}
echo "<br><br>";

//	19.
echo "Задание 19 <br>";
echo max($arr);
echo "<br><br>";

//	20.
echo "Задание 20 <br>";
echo min($arr);
echo "<br><br>";

//	21.
echo "Задание 21 <br>";
$arr1 = [];
$arr2 = [];

for ($i = 0; $i < 20; $i++) {
	$arr1[$i] = $arr2[$i] = random_int(-10, 10);
}
for ($i = 2, $j = 1; $i < 20; $i += 3, $j += 2) {
	if ($arr1[$i] > $arr2[$j])
		echo "$arr1[$i] больше $arr2[$j] <br>";
	else if ($arr1[$i] < $arr2[$j])
		echo "$arr1[$i] меньше $arr2[$j] <br>";
	else
		echo "$arr1[$i] и $arr2[$j] равны <br>";
}
echo "<br><br>";

//	22.
echo "Задание 22 <br>";
function func($arr)
{
	foreach ($arr as $num) {
		switch ($num) {
			case 5:
				$res = "пять";
				break;
			case 6:
				$res = "шесть";
				break;
			case 7:
				$res = 7;
				break;
			default:
				$res = "какое-то другое число";
				break;
		}

		echo $res;
		echo "<br>";
	}
}
echo func([4,5,6,7,8]);
echo "<br><br>";

// 23.
echo "Задание 23 <br>";
$a = [];
for ($i = 0; $i < 10; $i++) {
	$a[$i] = random_int(1, 20);
}
$b = [12, 5, 17, 6, 4];

//	1)
echo "1)<br>";
$counter = [];
for ($i = 0; $i < count($b); $i++) {
	$counter[$b[$i]] = 1;
}
for ($i = 0; $i < 10; $i++) {
	if (empty($counter[$a[$i]])) echo $a[$i], " ";
}
//	2)
echo "<br>2)<br>";
for ($i = 0; $i < 10; $i++) {
	if (!in_array($a[$i], $b)) echo $a[$i], " ";
}
?> 

</body>
</html>

```
<p>app.js</p>

```JavaScript
const express = require('express');
const app = express();
const nodemailer = require('nodemailer');
const jimp = require('jimp');
const fs = require('fs');

app.use(express.static(__dirname + "/public"));

app.get('/', function(req, resp){
    response.sendFile("index.html");
});
//1
let data = require('./package.json');
let string = JSON.stringify(data);
let res = JSON.parse(string);
for (var key in res){
    var value = res[key];
    console.log(key + ": " + value);
}
//2

dir = "C:\\Users\\pvitk\\Desktop\\школа\\3курс\\Вебы\\lab8";
fs.readdir(dir, (err, files) => {
    if (err) throw err;
    console.log(files);
});


app.get("/sendmessage", function(req, resp){
    const email = 'p.vitkovskaya@gmail.com'
    //console.log(email);
    let transporter = nodemailer.createTransport({
        host: 'smtp.yandex.ru',
    port:'465',
    secure: true,
    auth: {
        user:"vitkovsckaya.polina@yandex.ru",
        pass: "vcsxeihlyeyrereb",
    },
    }); 

    var mailOptions = {
        from: 'vitkovsckaya.polina@yandex.ru',
        to: email,
        subject: 'Письмо о каком-то событии',
        text: 'Событие произошло!!'
    };
    transporter.sendMail(mailOptions, (error, info) => {
        if (error) {
          console.error('Ошибка отправки письма:', error);
        } else {
          console.log('Письмо успешно отправлено:', info.response);
        }
      });
});

async function chaosedImage(path){
    let image = await jimp.read(path);
    image.invert();
    image.dither565();
    image.rotate(90);
    image.writeAsync(path);
}
chaosedImage("cats.jpg");
console.log('Image modified');

app.listen(3003, function(req, resp){
    console.log("Server online.")

}); 
```
<p>index.html</p>

```JavaScript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <p><a href="sendmessage?email=exxxample@exmaple.com"><button> Отправить email</button></a></p>
   
    <p id="quote">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptas,
        magni.
      </p>
    
    <h3 id="author">Lorem, ipsum.</h3>
        <button id="btn">Get Quote</button>
   
   <script>
    let quote = document.getElementById("quote");
let author = document.getElementById("author");
let btn = document.getElementById("btn");
const url = "https://api.quotable.io/random";
let getQuote = () => {
  fetch(url)
    .then((data) => data.json())
    .then((item) => {
      quote.innerText = item.content;
      author.innerText = item.author;
    });
};
window.addEventListener("load", getQuote);
btn.addEventListener("click", getQuote);
   </script>
</body>
</html>
```

<h2>Вывод</h2>
<p>В ходе лабораторной работы были решены задачи на PHP, решены задачи с Codewars.</p>
