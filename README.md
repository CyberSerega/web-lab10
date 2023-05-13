<h1 align="center" paddin> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>

<p align="center">Лабораторная работа №8 "JavaScript" </p>

<p align="right">Выполнил: Рогаль Сергей Александрович</p>
<p align="right">Проверил: Соболев Е. И.</p>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">JavaScript — это язык программирования, который используют для написания frontend- и backend-частей сайтов, а также мобильных приложений.JS поддерживают все популярные браузеры. Во frontend-части сайтов язык используют для создания интерактива (анимаций, всплывающих форм, автозаполнения), так как он связан с HTML и CSS и может ими манипулировать. В backend-части с языком JavaScript работают на платформе Node.js. С ее помощью, например, разрабатывают серверные веб-приложения и подключают библиотеки. В поисковике Google на JavaScript работает строка автозаполнения, а Netflix, Uber, eBay используют его в своем backend. Уже 6 лет JS — самый популярный язык среди разработчиков по версии GitHub.
</p>

<h2 align="center">Цели и задачи</h2>
<palign="justify">Цели: решить задачи с применением языка JavaScript</p>
<palign="justify">Задачи: применить технологии JavaScript.</p>

<h2>Решение задач</h2>
<p>1</p>
<pre>
<script>
let arr = [12,15,16,24,30];
let del = 4;
function Func(array,number)
{
	let count=0;
	let res = [];
	for(let i=0; i<array.length; i++)
	{
		if (array[i]%number==0)
		{
			res[count]=array[i];
			count++;
		}
	}
	return res;
}
let res = Func(arr,del);
for(let i=0; i<res.length; i++)
	{
		console.log(res[i]);
	}
</script>
</pre>
<p>2</p>
<pre>
<script>
var str1 = 'fgfggg';
var str2 = 'fgggggfffFFFGG';
function Compare(str1,str2)
{
	str1=str1.toLowerCase();
	str2=str2.toLowerCase();
	str1=str1.replaceAll(' ', '');
	str2=str2.replaceAll(' ', '');
	if (str1.length<str2.length)
	{
		let temp=str1;
		str1=str2;
		str2=temp;
	}
	for (let i=0;i<str1.length;i++)
	{
		if (!str2.includes(str1[i]))
		{
			return false;
		}
	}
	return true;
}
if (Compare(str1,str2)) alert('это анаграммы')
else alert('это не анаграммы');
</script>
</pre>
<p>3</p>
<pre>
<script>
var str = "Sergey";
function FindGlas(str)
{
	let count=0;
	let glasn = 'aeiou'
	for (let i=0;i<str.length;i++)
	if (glasn.includes(str[i])) count++;
	return count;
}
alert(FindGlas(str));
</script>
</pre>
<p>4</p>
<pre>
<script>
var str='#';
for (let i=1;i<=7;i++)
{
	document.write(str+'<br>');
	str+='#';
}
</script>
</pre>
<p>5</p>
<pre>
<script>
for (let i=1;i<=100;i++)
{
	let str=i+" ";
	if (i%3==0) str+='Fizz';
	if (i%5==0) str+='Buzz';
	console.log(str);
}
</script>
</pre>
<p>6</p>
<pre>
<script>
var str="";
var size=8;
for (let i=0;i<size;i++)
{
	for (let j=0;j<size;j++)
		{
			if ((i+j)%2!=0) str+="#"
				else str+=" ";
		}
	str+="\n";
}
console.log(str);
</script>
</pre>
<p>7</p>
<pre>
<script>
function Min(a,b)
{
	res = a<b ? a : b;
	return res;
}
alert("Сравнение чисел 3 и 7...");
alert(Min(3,7)+" меньше");
</script>
</pre>
<p>8</p>
<pre>
<script>
function isEven(x)
{
	if (x<0) return false;
	if (x==0) return true;
	if (x==1) return false;
	return isEven(x-2);
}
alert("Четное ли число 50?"+"\n"+" - "+ isEven(50));
alert("Четное ли число 75?"+"\n"+" - "+ isEven(75));
console.log(isEven(-1));
</script>
</pre>
<p>9</p>
<pre>
<script>
function countBs(str)
{
	let count=0;
	for (let i=0;i<=str.length;i++)
	{
		if (str[i]=='B') count++;
	}
	return count;
}
function countChar(str,symbol)
{
	let count=0;
	for (let i=0;i<=str.length;i++)
	{
		if (str[i]==symbol) count++;
	}
	return count;
}
var str="BOBS"
console.log("Количество символов В в строке <<BOBS>> равно " + countBs(str));
str="Web-technologies";
var symbol='e'
console.log(`Количество символов В в строке <<${str}>> равно ` + countChar(str,symbol));
</script>
</pre>
<p>10</p>
<pre>
<script>

function range(begin,end,step=1)
{
	let res = [];
	let count=0;
	if (step<0)
	{
		begin*=-1;
		end*=-1;
		step*=-1;
	}
	for(let i=begin; i<=end; i+=step)
	{
		res[count]=Math.abs(i);
		count++;
	}
	return res;
	
}
function sum(array)
{
	let res=0;
	for(let i=0; i<array.length; i++)
	{
		res+=array[i];
	}
	return res;
}
arr1 = range(5,1,-1);
for(let i=0; i<arr1.length; i++)
	{
		console.log(arr1[i]);
	}
console.log("Сумма чисел массива: " + sum(arr1));
</script>
</pre>
<p>11</p>
<pre>
<script>

function reverseArray(array)
{
	let res = [];
	for(let i=0; i<array.length; i++)
		res[i]=array[array.length-1-i];
	return res;
}
function reverseArrayInPlace(array)
{

	for(let i=0; i<array.length; i++)
		array[i]=array[array.length-1-i];
	return;
}

function printArray(array)
{
	let res="";
	for(let i=0; i<array.length; i++)
	{
		res+=array[i]+" ";
	}
	console.log(res);
}

var arr = [12,15,16,24,30];
console.log("Исходный массив: ");
printArray(arr);

var newArr = reverseArray(arr);
console.log("Новый массив после reverseArray: ");
printArray(newArr);

reverseArrayInPlace(arr);
console.log("Исходный массив после reverseArrayInPlace: ");
printArray(arr);
</script>
</script>
</pre>
<p>12</p>
<pre>
function deepEqual(arg1, arg2)
{
    if(typeof(arg1) != 'object' && typeof(arg2) != 'object') return arg1 === arg2;

    if(arg1 == null && arg2 == null) return true;
    if(arg1 == null || arg2 == null) return false;

    let keys1 = Object.keys(arg1);
    let keys2 = Object.keys(arg2);

    if(keys1.length != keys2.length) return false;

    for(key of keys1)
        if(!keys2.includes(key) || !deepEqual(arg1[key], arg2[key])) return false;

    return true;
}
</pre>
<p>13</p>
<pre>
<script>
var arr2 = [
  1,
  [2, 3,8],
  [4, 5, 6],
];
var newArr=[];
const sumWithInitial = arr2.reduce((Arr, current) => Arr.concat(current), newArr);

var res = sumWithInitial;
for(let i=0;i<res.length;i++) console.log(res[i]);
</script>
</pre>
<h2 align="center">Вывод</h2>
<p align="justify">Таким образом, я закрепил навык работы с JavaScript, лучше стал ориентироваться в нём, все поставленные цели были выполнены. </p>
