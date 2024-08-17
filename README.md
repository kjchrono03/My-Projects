# Porfolio
# Portfolio Website Code Explanation
This code creates a personal portfolio website for Kevin Joseph, highlighting his skills, services, and projects.

# HTML Code Explanation:

1. **HTML Structure**

* The document is structured using semantic HTML5 elements like `<header>`, `<section>`, and `<nav>`.
* The content is divided into various sections: Home, About, Services, Portfolio, and Contact.

2. **Head Section**:

* The `<head>` section includes the meta tags for character set (`UTF-8`) and viewport settings to ensure responsiveness.
* The Font Awesome library is linked via CDN to provide icons used throughout the website.

3. **Header and Navigation**:

* The `<header>` element contains the navigation bar (`<nav>`) with links to different           sections of the page. The menu icon (`fa-bars`) is designed to be used for a mobile-           friendly collapsible menu.
*  The logo and navigation links are styled and positioned for a clean, responsive header.

4. **Home Section**:

* The `<section>` with class "home" serves as the introductory area, displaying a welcome       message, Kevin Joseph's name, and a brief description of his role.
* Social media links, including LinkedIn, are provided, and there is a button to download       Kevin's CV.

5. **About Section**:
* The "About" section gives a brief introduction to Kevin Joseph. It includes an image and       descriptive text about his background.

6. **Services Section**:
* The "Services" section lists the professional services offered by Kevin, such as Web         Development, MS Excel, and SQL.
* Each service is represented with a Font Awesome icon and includes a brief description.

7. **Portfolio Section**:

* The "Portfolio" section showcases Kevin's latest projects. Each project is displayed with an image and a brief description that appears on hover.
* The projects highlight various skills, such as Web Design, Data Science, Web Development, and AI Prediction.

8. **Icons and Styling**:

* The website utilizes Font Awesome icons for visual appeal and functionality. These icons enhance the user interface by making navigation and interaction more intuitive.

9. **External Files**:

* The CSS for the website's styling is linked externally (`styles.css`), allowing for a clean separation of content and design.

# CSS Code Explanation:

The CSS file (styles.css) is responsible for the visual design and layout of the portfolio website. Below is a breakdown of how the styles are applied to various elements of the website.

1. **General Styles**

* Box-Sizing: `box-sizing: border-box;` is applied globally to ensure that padding and borders are included within the element’s width and height.
* Fonts: Custom fonts are used for different sections, and Font Awesome icons are styled to match the design.

2. **Body and Base Styles**

* The `body` is styled with a specific font family, background color, and default margin and padding set to zero to remove any unwanted spaces around the edges.
* The `background-color` and `color` are set for a clean and modern look.

3. **Header Styles**

* The header is styled to be fixed at the top, with a background color and padding for a consistent look across the page.
* The logo and navigation links within the header are styled for alignment, spacing, and hover effects.
* The menu icon (`#menu-icon`) is hidden on larger screens and only displayed on smaller screens (for mobile responsiveness).

4. **Navigation Bar (Navbar)**
* The `navbar` is designed as a flex container to align the navigation links horizontally.
Active links are highlighted with a different color to indicate the current section.

5. **Home Section**

* The `.home` class styles the introduction section with a background image or color, and the text is centered using flexbox.
* The heading and subheadings within the home section are given specific font sizes, colors, and spacing to make them stand out.
* The `.social-media` icons are styled to be consistent in size, color, and hover effects.

6. **About Section**

* The `.about` section is styled with a two-column layout, where one column contains an image and the other contains text.
* The `.about-content` is styled with padding, font adjustments, and a button that links to further details.

7. **Services Section**

* The `.services` section uses a grid layout to display each service in a box.
* Each `.services-box` is styled with padding, margin, and a background color. Icons and headings are given specific styles to maintain consistency.
* The hover effects are used to provide interactivity, making the service boxes change color or size when hovered over.

8. **Portfolio Section**

* The `.portfolio-container` is a grid that displays project thumbnails.
* Each `.portfolio-box` has a hover effect that reveals additional information about the project.
* The `.portfolio-layer` is an overlay that appears on hover, providing a brief description and a link icon.
9. **Responsive Design**

* Media queries are used to ensure that the website is fully responsive. Specific styles are applied depending on the screen size, such as adjusting font sizes, hiding/showing elements, and stacking content vertically for smaller screens.

10. **Buttons**

* The `.btn` class is used for buttons across the site, with consistent padding, background color, border-radius, and hover effects to enhance user experience.
* Buttons change appearance when hovered to indicate they are clickable.

11. **Images**

* Images within sections like `.home-img`, `.about-img`, and `.portfolio-box img` are styled to be responsive, with max-widths set to ensure they scale appropriately across different devices.
# Javascript Code Explanation:

The JavaScript code in the portfolio website is responsible for adding interactivity and dynamic features to the user interface. Below is an overview of how the JavaScript functions enhance the website's functionality:

1. **Menu Toggle Functionality**

* **Menu Icon Toggle**:
The `menu-icon` is used to show or hide the navigation menu on smaller screens. When the menu icon is clicked, the `navbar` class is toggled to show or hide the menu
items.

* **Code Implementation**:
  ```javascript
  let menuIcon = document.querySelector('#menu-icon');
  let navbar = document.querySelector('.navbar');

  menuIcon.onclick = () => {
    navbar.classList.toggle('active');
  };
* This code allows users to easily navigate the website on mobile devices by toggling the visibility of the navigation menu.

2. **Sticky Header on Scroll**

* **Sticky Header**: The header becomes sticky (remains at the top of the viewport) when the user scrolls down the page. This is achieved by adding a class to the header when the page is scrolled beyond a certain point.

* **Code Implementation**:
  ```javascript
  let header = document.querySelector('header');

  window.onscroll = () => {
    header.classList.toggle('sticky', window.scrollY > 100);
    navbar.classList.remove('active');
  };
* This ensures that the navigation header remains accessible as the user scrolls through the page, providing a better user experience.
3. **Scroll Reveal Animations:**

* **Reveal on Scroll**: Elements on the page are animated when they come into view as the user scrolls down. This is often used to create a smooth and engaging user experience.
* **Library Used**: The code likely uses the ScrollReveal.js library to handle these animations, which is popular for implementing scroll-triggered animations.
* **Code Implementation**:
  ```javascript
  ScrollReveal({
    reset: true,
    distance: '80px',
    duration: 2000,
    delay: 200
  });

  ScrollReveal().reveal('.home-content, .heading', { origin: 'top' });
  ScrollReveal().reveal('.home-img, .services-container, .portfolio-box, .contact form', {   origin: 'bottom' });
  ScrollReveal().reveal('.home-content h1, .about-img', { origin: 'left' });
  ScrollReveal().reveal('.home-content p, .about-content', { origin: 'right' });

* Effect: As the user scrolls, various elements (e.g., text, images) will fade in or slide into view from different directions, creating a dynamic and visually appealing effect.

4. **Typing Animation**:

* **Typing Effect**:
       The JavaScript code creates a typing animation for a specific element, where text appears to be typed out one character at a time.
* **Library Used**:
   The code might use the Typed.js library, which is a popular tool for creating typing animations.
* **Code Implementation**:
    ```javascript
    const typed = new Typed('.multiple-text', {
    strings: ['Web Developer', 'Data Scientist', 'Freelancer'],
    typeSpeed: 100,
    backSpeed: 100,
    backDelay: 1000,
    loop: true
    });
* **Effect**:
   The words "Web Developer," "Data Scientist," and "Freelancer" appear one by one in a typing animation, adding an interactive and dynamic element to the website's home section.
