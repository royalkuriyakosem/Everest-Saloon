# index.html 🏠
The **Home** page serves as the central hub of the Everest Unisex Salon website. It introduces visitors to the salon’s offerings, team, and encourages engagement through a contact form and “Book Appointment” call-to-action.

## Key Sections
- **Header & Navigation**: Global logo, responsive menu linking to all pages  
- **Hero Banner**: Prominent tagline and “Book Appointment” button  
- **About Snippet**: Brief welcome message with “Learn More” link  
- **Our Teams**: Profiles of stylists with images and roles  
- **Featured Services**: Preview of three top services with “Book Now” links  
- **Customer Reviews**: Highlighted testimonial  
- **Contact Form**: Quick message form for inquiries  
- **Footer**: Social links, contact details, copyright

## Navigation Menu
| Link Text   | Destination             |
| ----------- | ----------------------- |
| Home        | index.html              |
| Services    | services.html           |
| About       | about.html              |
| Contact     | contacts.html           |
| Book Now    | bookappointment.html    |

```html
<header class="header">
  <a href="index.html" class="logo">
    <img src="https://…/logo.svg" alt="Company Logo" />
  </a>
  <input type="checkbox" id="side-menu" class="side-menu" />
  <label for="side-menu" class="hamb">
    <span class="hamb-line"></span>
  </label>
  <nav class="nav">
    <ul class="menu">
      <li><a href="index.html">Home</a></li>
      <li><a href="services.html">Services</a></li>
      <li><a href="about.html">About</a></li>
      <li><a href="contacts.html">Contact</a></li>
      <li class="book-now-menu">
        <a href="bookappointment.html">Book Now</a>
      </li>
    </ul>
  </nav>
</header>
```

## Assets & Relationships
- Styles: `css/headerfooter.css`, `css/style.css`  
- Script: `js/gallery.js` (loaded but only used for the Gallery on **contacts.html**)  
- Internal links connect to **services.html**, **about.html**, **contacts.html**, **bookappointment.html**  

---

# services.html ✂️
The **Services** page lists all salon offerings with visuals, descriptions, and pricing. Visitors can jump straight to booking each service.

## Page Structure
- **Hero Section** (`#top-hero`): Page title “Services”  
- **Service List** (`#service-list`): Grid of service cards  
- **Footer**: Same global footer as other pages  

## Service Card Overview
| Service Name | Description                                    | Price |
| ------------ | ---------------------------------------------- | ----- |
| FAUXHAWK     | Upright center with shorter sides             | $35   |
| BOLD PIXIE   | Cropped sides, longer textured top             | $40   |
| LAYERED      | Multi-length cuts for volume & movement        | $57   |

```html
<div class="service-each">
  <img src="https://…/cut2.jpg" alt="Fauxhawk" />
  <h6 class="service-name">FAUXHAWK</h6>
  <p class="service-desc">
    Center of the head is styled to stand upright...
  </p>
  <p class="service-price">$35</p>
  <p class="book-now-button">
    <a href="bookappointment.html">BOOK NOW</a>
  </p>
</div>
```

## Assets & Relationships
- Inherits **header** & **footer** from global layout  
- Styles: adds `css/services.css` on top of global styles  
- “Book Now” buttons link to **bookappointment.html**  

---

# about.html ℹ️
The **About Us** page tells the salon’s story, mission, and values, combining imagery with narrative text in a two-column layout.

## Main Components
- **Hero Section** (`#top-hero`): Title “About Us”  
- **About Content** (`#about-page`):  
  - Left: Introductory image  
  - Right: Vision statement and origin story  
- **Footer**: Consistent global footer  

```html
<section id="about-page">
  <div class="container about-text-wrapper">
    <div class="row">
      <div class="col-left">
        <img src="https://…/about-banner.png" alt="Intro image" />
      </div>
      <div class="col-right">
        <h5 class="about-text-title company-blue-bold">
          We transform your salon experience into a tranquil…
        </h5>
        <p class="about-text-subtitle">
          "Our journey began in 2013 with a simple yet profound vision…"
        </p>
      </div>
    </div>
  </div>
</section>
```

## Assets & Relationships
- Global styles + `css/about.css` for page-specific tweaks  
- Navigation and footer identical to **index.html** and **services.html**  

---

# contacts.html 📞
The **Contact Us** page provides multiple ways to reach the salon: phone, email, physical address, an embedded map, and a gallery of work with an interactive slideshow.

## Key Sections
- **Hero Section** (`#top-hero`): Title “Contact Us”  
- **Contact Info** (`.contact-info`):  
  - Phone  
  - Email  
  - Location  
- **Map Embed** (`.maps`): Google Maps iframe  
- **Gallery** (`.slideshow-container`): Image carousel powered by `js/gallery.js`  
- **Footer**: Standard global footer  

```html
<section class="contact-info">
  <div class="icon-container">
    <i class="fa-solid fa-phone"></i>
    <h4>Phone</h4>
    <a href="tel:647-000-0000"><p>647-000-0000</p></a>
  </div>
  <!-- Email & Location similar structure -->
</section>

<section class="maps">
  <h4 class="company-blue-bold">FIND US IN MAP</h4>
  <div class="map-container">
    <iframe src="https://www.google.com/maps/embed?pb=…" allowfullscreen></iframe>
  </div>
</section>

<section id="customer-review" class="container-fluid">
  <h5 class="customer-title">Gallery</h5>
  <div class="slideshow-container">
    <div class="mySlides fade">
      <div class="numbertext">1 / 3</div>
      <img src="https://…/salon1.jpg" style="width:100%;height:400px;object-fit:cover;">
    </div>
    <!-- Additional slides… -->
    <a class="prev" onclick="plusSlides(-1)">❮</a>
    <a class="next" onclick="plusSlides(1)">❯</a>
  </div>
  <div style="text-align:center">
    <span class="dot" onclick="currentSlide(1)"></span>
    <span class="dot" onclick="currentSlide(2)"></span>
    <span class="dot" onclick="currentSlide(3)"></span>
  </div>
</section>
```

## Assets & Relationships
- Styles: `css/contacts.css` alongside global styles  
- Script: `js/gallery.js` enables carousel controls  

---

# bookappointment.html 📅
The **Book Appointment** page displays opening hours in a clear timetable. Visitors can plan their visit and navigate back to main sections via the shared header/footer.

## Page Elements
- **Hero Section** (`#top-hero`): Title “Book an Appointment”  
- **Opening Hours Table**:  
  - Days of the week  
  - Opening & closing times  
- **Footer**: Common footer layout  

```html
<section class="available-table">
  <h4 id="working_hour">Opening Hours</h4>
  <p class="working-subtitle">
    Book an Appointment. Check the available time table below.
  </p>
  <div class="wrapper">
    <table>
      <thead>
        <tr>
          <th></th>
          <th>Opening Time</th>
          <th>Closing Time</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="day">Monday</td>
          <td class="open">9:00 AM</td>
          <td class="close">6:00 PM</td>
        </tr>
        <!-- Additional days… -->
      </tbody>
    </table>
  </div>
</section>
```

## Assets & Relationships
- Global styles + `css/style.css`  
- Shares header/nav and footer with other pages  

---

# js/gallery.js 📸
This JavaScript file implements a simple **carousel** for the gallery section. It controls slide visibility and active indicator dots.

## Core Functions
- `showSlides(n)`: Displays slide at index *n*, hides others, updates dots  
- `plusSlides(n)`: Advances or reverses slide index  
- `currentSlide(n)`: Jumps directly to slide *n*  

```js
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  const slides = document.getElementsByClassName("mySlides");
  const dots   = document.getElementsByClassName("dot");
  if (n > slides.length) slideIndex = 1;
  if (n < 1)             slideIndex = slides.length;
  Array.from(slides).forEach(s => s.style.display = "none");
  Array.from(dots).forEach(d => d.className = d.className.replace(" active", ""));
  slides[slideIndex - 1].style.display = "block";
  dots[slideIndex - 1].className += " active";
}
```

## Usage
- Loaded on all pages but only **contacts.html** leverages it for the Gallery  
- Hooks into elements with classes `.mySlides` and `.dot`  

---

> All HTML pages share a **common header** and **footer**, consistent styling via `headerfooter.css`, and navigation links that interconnect the site’s primary sections. Custom CSS files (`about.css`, `services.css`, `contacts.css`) refine each page’s unique layout.
