# JavaScript Odev - 01

Bu repo [Patika.Dev](www.patika.dev) JS Egitimindeki ilk odevdir.

## HTML Tarafi

*Oncelikle HTML tarafini kontrol ediyoruz.*

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="css/style.css" />
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/css/bootstrap.min.css"
      integrity="sha384-B0vP5xmATw1+K9KRQjQERJvTumQW0nPEzvF6L/Z6nronJ3oUOFUFpCjEUQouq2+l"
      crossorigin="anonymous"
    />
    <title>Kodluyoruz Javascript Saat Ödevi</title>
  </head>
  <body class="bg-dark">
      <div class="text-center">
      <img
        src="https://cdn.sanity.io/images/9kdepi1d/production/65c832d202a503b15d99e628f4313782f3ef50db-300x62.png"
        alt=""
        class="rounded"
      />
      <div class="text1 text-center">
        Merhaba, <strong><span id="myName"></span></strong>! Hoş geldin!
      </div>
      <div id="myClock" class="clock" onload="showTime()"></div>
      <div class="text2 text-center">
        tarihinde
        <strong>Kodluyoruz Frontend Web Development Patikası</strong>'nın
        Javascript bölümü 1. Ödevindesiniz.
      </div>
    </div>
    <script src="js/clock.js"></script>
  </body>
</html>
```

## Saat Tarafi

*Saat tarafinin calismasi icin de boyle bir yazim kullaniyoruz.*

```
let myName = prompt('Lutfen Adinizi Giriniz...!')

      function showTime() {
        const today = new Date();
        let h = today.getHours();
        let m = today.getMinutes();
        let s = today.getSeconds();
        m = checkTime(m);
        s = checkTime(s);
        document.getElementById('myClock').innerHTML =  h + ":" + m + ":" + s;
        setTimeout(showTime, 1000);
        
      }
      
      function checkTime(i) {
        if (i < 10) {i = "0" + i};  // add zero in front of numbers < 10
        return i;
      }
      showTime()

console.log (myName)

document.querySelector("#myName").innerHTML += myName;
```

## Lisans

[Lisans Secimi](https://choosealicense.com/)
$~$
![](https://i.im.ge/2022/09/23/15rwwx.Goruntu-000049.png)