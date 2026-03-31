# Ceļošana pa Latviju

Šī ir tīmekļa vietne par ceļošanu Latvijā.

## Sadaļas:
- Sākumlapa
- Vietas
- Fotogalerija
- Kontakti

## Funkcionalitāte:
- Navigācijas izvēlne
- Attēlu galerija
- Forma ar validāciju
- JavaScript interaktivitāte

## Tehnoloģijas:
- HTML
- CSS
- JavaScript


/projekts
  index.html
  /css
    style.css
  /js
    script.js
  /images
    (bildes)

    <!DOCTYPE html>
<html lang="lv">
<head>
    <meta charset="UTF-8">
    <title>Ceļošana pa Latviju</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
    <h1>Ceļošana pa Latviju</h1>
    <nav>
        <a href="#sakums">Sākums</a>
        <a href="#vietas">Vietas</a>
        <a href="#galerija">Galerija</a>
        <a href="#kontakti">Kontakti</a>
    </nav>
</header>

<section id="sakums">
    <h2>Sveicināti!</h2>
    <p>Šī vietne ir par skaistākajām vietām Latvijā.</p>
</section>

<section id="vietas">
    <h2>Populāras vietas</h2>
    <ul>
        <li>Sigulda</li>
        <li>Jūrmala</li>
        <li>Kuldīga</li>
    </ul>
</section>

<section id="galerija">
    <h2>Fotogalerija</h2>
    <img src="images/img1.jpg" onclick="palielinat(this)">
    <img src="images/img2.jpg" onclick="palielinat(this)">
    <img src="images/img3.jpg" onclick="palielinat(this)">
</section>

<section id="kontakti">
    <h2>Pieteikšanās</h2>
    <form onsubmit="return validateForm()">
        <input type="text" id="name" placeholder="Vārds"><br>
        <input type="email" id="email" placeholder="E-pasts"><br>
        <textarea id="message" placeholder="Ziņa"></textarea><br>
        <button type="submit">Sūtīt</button>
    </form>
</section>

<footer>
    <p>© 2026</p>
</footer>

<script src="js/script.js"></script>
</body>
</html>
body {
    font-family: Arial;
    margin: 0;
}

header {
    background: darkgreen;
    color: white;
    padding: 10px;
}

nav a {
    color: white;
    margin: 10px;
    text-decoration: none;
}

nav a:hover {
    text-decoration: underline;
}

section {
    padding: 20px;
}

img {
    width: 200px;
    margin: 10px;
    cursor: pointer;
}

img:hover {
    transform: scale(1.1);

function validateForm() {
    let name = document.getElementById("name").value;
    let email = document.getElementById("email").value;

    if (name === "" || email === "") {
        alert("Lūdzu aizpildi visus laukus!");
        return false;
    }

    alert("Forma veiksmīgi nosūtīta!");
    return true;
}

function palielinat(img) {
    img.style.width = "400px";
}
