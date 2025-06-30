# Web Developer Portfolio

This project is a personal portfolio website for a fictional web developer, Mary Hardy. It is built with HTML5 and CSS3, demonstrating a clean, modern, and responsive layout.

## Project Overview

The website serves as a digital resume and showcase of skills. It features a prominent header with a hero banner, an "About Me" section with personal details, and is structured to be easily expandable with additional sections like "Skills," "Resume," and "Contact."

### Key Features

- **Responsive Design**: The layout is designed to adapt to different screen sizes, from mobile devices to large desktops.
- **Semantic HTML5**: Uses modern HTML5 tags like `<header>`, `<nav>`, `<main>`, and `<section>` for better structure and accessibility.
- **Custom Fonts**: Utilizes Google Fonts ('Open Sans' and 'Work Sans') for clean and professional typography.
- **CSS3 Styling**: Features advanced CSS properties like Flexbox for layout, multiple background images, and a clean class structure.

## File Structure

The project is organized into the following key files:

- `index.html`: The main HTML file containing the structure of the entire webpage.
- `style/style.css`: The stylesheet containing all the visual rules for the website.
- `images/`: A directory containing all the images used in the project.

## Key Sections Breakdown

This HTML file, `index.html`, serves as the structural foundation for a personal portfolio website for a developer named Mary Hardy. It uses modern HTML5 semantic tags to create a well-organized and accessible layout.

### 1. `<head>` Section

The head contains the metadata for the page, including character encoding, viewport settings for responsiveness, and the page title.

- **Fonts**: It imports two fonts from Google Fonts: 'Open Sans' and 'Work Sans'. These are likely used for body text and headings, respectively, to create a clean and professional typographic hierarchy.
- **Stylesheet**: It links to an external stylesheet located at `style/style.css`, which is responsible for all the visual styling of the page.

### 2. `<body>` Section

The body contains all the visible content of the webpage. A global class `open-sans-normal` is applied, likely setting the default font for the entire page to 'Open Sans'.

### 3. `<header>` Section

This section acts as the main header for the page and is styled with the classes `header` and `secondary-bg`. It contains two primary components:

- **Navigation (`<nav>`)**:
  - **Logo/Title**: A heading `<h3>` with the text "Mary", where the letter 'r' is wrapped in a `<span class="text-primary">` to give it a distinct color.
  - **Links**: An unordered list (`<ul>`) provides navigation to "Portfolio", "Blog", and a "Hire Me" call-to-action button. The `href=""` attributes are currently empty and should be updated to point to the correct pages or sections.
- **Banner (`<div class="banner">`)**:
  - This is the "hero" section of the page, designed to make a strong first impression.
  - It's split into two main parts: a text container (`banner-container`) and a profile image (`banner-profile-pic`).
  - The text includes a greeting, the developer's name, a short description, and two call-to-action buttons ("Download CV" and "Contact").

### 4. `<main>` Section

This tag encloses the main, unique content of the page.

- **About Section (`<section class="about">`)**:
  - This section provides more details about the developer. It has a title ("About Me") and a more detailed paragraph description.
  - The `<br />` tags are used to force line breaks. While functional, a more flexible approach would be to control the width of the text container with CSS.
- **Info Items (`<div class="about-items">`)**: This container uses a flexbox or grid layout (implied by the class name) to neatly display key-value information like Name, Email, Date of Birth, and Location. This is a very clean and readable way to present this data.

### 5. `<footer>` Section

The `<footer>` is currently empty. It serves as a placeholder for future content, which would typically include social media links, copyright information, or additional navigation.

## Code Quality and Suggestions

The codebase is well-organized and uses descriptive class names. The use of semantic HTML is a strong point.

One key suggestion for improvement was already implemented to enhance accessibility:

```html
<img
  class="banner-profile-pic"
  src="images/hardy.png"
  alt="A portrait of Mary Hardy"
/>
```

Adding descriptive `alt` text ensures that screen readers can convey the image's content to visually impaired users.

## How to Run

1.  Clone this repository to your local machine.
2.  Open the `index.html` file in your web browser to view the website.
