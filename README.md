# CodersCamp 2020 - Projekt HTML & CSS

## I. O Projekcie
Projekt Wizytówki / Portfolio opracowany wyłącznie na podstawie zagadnień związanych z HTML & CSS, bez użycia JavaScriptu ani żadnego innego frameworka. Nie użyto również gotowych bibliotek styli takich jak Bootstrap.

## II. Repozytorium 
W skład repozytorium projektu wchodzą:
- index.html - plik stanowiący stronę główną projektu;
- style.css (./static/css) - plik ze stylami strony;
- folder images (./static) ze zdjęciami wykorzystanymi na stronie - zdjęcia zostały pobrane ze strony www.unsplash.com

## III. Zawartość projektu i wykorzystane technologie
Strona główna została podzielona na cztery sekcje - About Me, Skills, Interests, Contact Me oraz posiada wydzielony nagłówek oraz stopkę strony. Poszczególne działy zostały podzielone oraz wyrównane za pomocą flexa oraz grida. Elementy oraz zagadnienia zawarte w projekcie zostały dokładnie przedstawione w dziale IV. 

Na stronie użyto google fonts: Barlow oraz Bree Serif, a także Font Awesome. 

## IV. Użyte zagadnienia oraz przykłady


### 1. Box Model

#### Margin, padding:

```
footer {
    background-color: var(--background-light);
    color: var(--font);
    margin: 20px 0px 0px 0px;
    padding: 20px;
    text-align: center;
    border-top: 2px var(--background-light) solid;
}
```

### 2. Kaskadowość CSS

style inline są ważniejsze niż style zdefiniowane w znaczniku \<style\> w sekcji head, natomiast w znaczniku head są ważniejsze niż te zdefiniowane w pliku css

#### style css o wyższej specyficzności
```
ul.no-bullets li a {
    color: var(--background-light);
    text-decoration: none; 
    display: block;
}
```


### 3. Selektory CSS

#### all elements
```
* {
    box-sizing: border-box;
}
```
#### root elements
```
:root {
   --background: #dfdfdf;
   --background-light: #F8F8F8;
   --font: #323031;
   --special: #DB3A34;
}
```
#### id

```
#skills {
    background-color: var(--background);
    color: var(--font);
}
```

#### class
```
.contact-title {
    font-size: 20px;
    font-weight: bold;
    margin: 0 0 8px 0;
}
```

#### element
```
footer {
    background-color: var(--background-light);
    color: var(--font);
    margin: 20px 0px 0px 0px;
    padding: 20px;
    text-align: center;
    border-top: 2px var(--background-light) solid;
}
```


#### pseudoklasa
```
ul.no-bullets li:hover {
    background-color: rgba(0, 0, 0, 0.8);
    font-weight: bold;
}
```

#### 
```
.container-contact-item:first-child {
    min-width: 300px;
    width: 100%;
}
```


### 4. Popularne tagi HTML

#### footer, div, table, tr, td
```html
<footer> 
    <div class="ball left-ball"></div>
    <div class="ball right-ball"></div>
        <table>
            <tr>
                <td>Copyrights &copy; </td>
                <td>2020 Konrad Reczek</td>
            </tr>
        </table>
</footer>
```

#### nav, ul, li, a
```
<nav> 
    <ul class="no-bullets">
        <li><a href="#about-me">About Me</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#interests">Interests</a></li>
        <li><a href="#contact-form">Contact Me</a></li>
    </ul>
</nav>
```        


### 5. Jak podpinać CSSa do HTMLa

#### Zewnętrzny arkusz CSS
```html
<link rel="stylesheet" href="./static/css/style.css">
```

#### Znaczniki \<style\> w sekcji head

```
<style>
    .head-style-element {
        color: goldenrod;
        text-decoration:underline;
    }
</style>
```

#### Style inline

```html
<span style="color: #f45b5b; font-weight:bold;">Duis aute irure dolor</span>
```

### 6. Zapisywanie kolorów

#### nazwa koloru
```
.head-style-element {
    color: goldenrod;
    text-decoration:underline;
}
```
#### kod RGB
```
input, textarea {
    background-color: rgb(0, 0, 0, 0.2);
    border: none;
    margin: 1px;
}
```
#### kolory zdefiniowane w root
```
#contact-form {
    background-color: var(--background);
    color: var(--font);
}
```


### 7. Stylowanie tekstu

#### tytuł sekcji
```
.skills-title {
    font-size: 20px;
    font-weight: bold;
    margin: 0px;
}
```
#### element listy
```
ul.no-bullets li {
    flex-grow: 1;
    text-transform: uppercase;
    text-align: center;
    transition: 0.3s linear background-color, font-weight;
    padding: 8px;
    cursor: pointer;
}

ul.no-bullets li a {
    color: var(--background-light);
    text-decoration: none; 
    display: block;
}
```
### 8. Zewnętrzne ikony/fonty (fontawesome, google fonts)

##### Google Fonts
```html
<link href="https://fonts.googleapis.com/css2?family=Barlow:wght@300&family=Bree+Serif&display=swap" rel="stylesheet">
```
##### Font Awesome
```html
<script src="https://kit.fontawesome.com/ac69056d5c.js" crossorigin="anonymous"></script>
```

### 9. Flexbox i/lub CSS Grid

#### CSS GRID (sekcja about me)
```
.about-me-container {
    display: grid;
    gap: 16px;
    grid-template-columns: auto;
    grid-template-rows: auto auto auto auto;
    grid-template-areas: 
        "about-me-photo"
        "about-me-name"
        "about-me-contact"
        "about-me-info"
}

.about-me-container {
    text-align: center;
}

.about-me-photo {
    grid-area: about-me-photo;
}

.about-me-contact {
    grid-area: about-me-contact;
}

.about-me-name {
    grid-area: about-me-name;
}

.about-me-info {
    grid-area: about-me-info;
}
```

#### flex (sekcja interests)
```
    .container-interests {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }

    .interests-item {
        flex-grow: 1;
        width: 30%;
        height: 240px;
        position: relative;
        background-size: cover;
    }
```
### 10. Position (absolute, relative)

#### position: fixed 
pasek nawigacyjny jest nieruchomy w górnej części strony (pozycja ustalona za pomocą right, left, top);

```
nav {
    background-color: rgba(0, 0, 0, 0.6);
    color: var(--background-light);
    position: fixed;
    right: 0;
    left: 0;
    top: 0;
    z-index: 1000;
    max-width: 100vw;
}
```
#### position: absolute & position: relative
pasek postępu w sekcji Skills
```
.progress {
    width: 100%;
    min-width: 48px;
    height: 24px;
    background-color: lightgray;
    position: relative;
    margin-bottom: 16px;
}

.progress-value {
    background-color: green;
    top: 0;
    left: 0;
    bottom: 0;
    position: absolute;
}
```

### 11. Animacje keyframes

#### za pomocą animacji wykonanie okrągłego elementu, który zmienia swoją pozycję, widoczność oraz wielkość i działa w kółko

```
.ball {
    background-color: var(--font);
    width: 10px;
    height: 10px;
    border-radius: 50%;
    position: absolute;
}

.left-ball {
    left: 40%;
    animation: left-ball-move 5s linear 0s infinite;
}

.right-ball {
    left: 60%;
    animation: right-ball-move 5s linear 0s infinite;
}

@keyframes left-ball-move {
    0% {left: 40%; opacity: 1;}
    25% {left: 50%; opacity: 0.4; transform: scale(1.5);}
    50% {left: 60%; opacity: 1;}
    75% {left: 50%; opacity: 0.4; transform: scale(1.5);}
    100% {left: 40%; opacity: 1;}
}

@keyframes right-ball-move {
    0% {left: 60%; opacity: 1;}
    25% {left: 50%; opacity: 0.4; transform:scale(1.5);}
    50% {left: 40%; opacity: 1;}
    75% {left: 50%; opacity: 0.4; transform:scale(1.5);}
    100% {left: 60%; opacity: 1;}
}
```
### 12. Formularz (bez wysyłania)

```html
<p class="contact-title"> FORMULARZ</p>
    <form action="/my_page" method="post">
        <div> 
            <label for="contact-name">Name</label>
            <input type="text" id="contact-name" name="user_name">
        </div>
        <div>
            <label for="contact-mail">E-mail</label>
            <input type="email" id="contact-mail" name="user_email">
        </div>
        <div> 
            <label for="contact-message">Text</label>
            <textarea id="contact-message" name="user_message"></textarea>
        </div>
            <button type="submit">Send</button>
    </form>
```
### 13. Responsive Web Design
#### ustawienia sekcji about-me i css grid 
```
@media only screen and (min-width: 768px) {
    .about-me-container {
        display: grid;
        gap: 16px;
        grid-template-columns: 1fr 2fr 2fr;
        grid-template-rows: auto auto;
        grid-template-areas: 
            "about-me-photo about-me-name about-me-contact"
            "about-me-photo about-me-info about-me-info"
    }

    .about-me-photo {
        border-right: 3px var(--secondary) solid;
        padding-right: 16px;
    }

    .about-me-contact {
        text-align: right;
    }

    .about-me-name {
        text-align: left;
    }

    .about-me-info {
        text-align: justify;
    }
}
```