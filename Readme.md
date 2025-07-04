# Web Developer Portfolio

This project is a personal portfolio website for a fictional web developer, Mary Hardy. It is built purely with HTML5 and CSS3, demonstrating a clean, modern, and multi-section responsive layout.

## Project Overview

The website serves as a comprehensive digital resume and showcase of skills. It is designed to give a full overview of the developer's profile.

### Key Features

- **Responsive Design**: The layout is designed to adapt to different screen sizes, from mobile devices to large desktops.
- **Semantic HTML5**: Uses modern HTML5 tags like `<header>`, `<nav>`, `<main>`, `<section>`, and `<footer>` for better structure and accessibility.
- **Multi-Section Layout**: Includes several distinct sections:
  - A hero **Banner** with a call-to-action.
  - An **About Me** section with personal details.
  - A **What I Do** section to showcase skills.
  - A **Resume** summary with education and experience.
  - A **Contact** footer with social links and a message form.
- **Custom Fonts**: Utilizes Google Fonts ('Open Sans') for clean and professional typography.
- **CSS3 Styling**: Styled with a dedicated stylesheet, using classes for modularity and reusability.

## File Structure

The project is organized into the following key files:

- `index.html`: The main HTML file containing the structure of the entire webpage.
- `style/style.css`: The stylesheet containing all the visual rules.
- `images/`: A directory containing all the images and icons used in the project.

## Key Sections Breakdown

The `index.html` file is built with semantic tags to create a well-organized and accessible layout.

### 1. `<head>` Section

The head contains the metadata for the page, including character encoding, viewport settings for responsiveness, and the page title.

- **Fonts**: It imports the 'Open Sans' font from Google Fonts.
- **Stylesheet**: It links to an external stylesheet located at `style/style.css`.

### 2. `<header>` Section

This section acts as the main header for the page and is styled with the classes `header` and `secondary-bg`. It contains two primary components:

- **Navigation (`<nav>`)**:
  - **Logo/Title**: A heading `<h3>` with the text "Mary", where the letter 'r' is styled differently using a `<span>`.
  - **Links**: An unordered list (`<ul>`) provides navigation links and a "Hire Me" button.
- **Banner (`<div class="banner">`)**:
  - This is the "hero" section of the page, designed to make a strong first impression.
  - It contains a greeting, the developer's name, a short description, and two call-to-action buttons.
  - A profile picture is displayed alongside the text.

### 3. `<main>` Section

This tag encloses the main, unique content of the page, divided into logical sections.

- **About Section (`<section class="about">`)**:
  - This section provides more details about the developer. It has a title ("About Me") and a more detailed paragraph description.
  - It includes a flex container (`.about-items`) to neatly display key-value information like Name, Email, Date of Birth, and Location.

- **Skills Section (`<section class="skills">`)**:
  - Titled "What I do," this section describes the developer's technical abilities.
  - It features a container (`.skills-container`) that holds four individual skill cards (`.skill`).
  - Each card includes an icon, a skill title (e.g., "Vanilla Javascript"), and a brief description.

- **Resume Section (`<section class="resume">`)**:
  - This section provides "A summary of My Resume."
  - It uses a two-column layout (`.resume-container`) to separate "My Education" from "My Experience."
  - Each column contains multiple entries with a title, subtitle/date, and description, separated by a horizontal rule (`<hr>`).
  - A "Download CV" button is included at the bottom.

### 4. `<footer>` Section

The footer is styled with the `secondary-bg` class and is split into two columns.

- **Left Column (`.footer-column`)**:
  - Titled "Lets Connect," this column contains a brief message and social media icons (Facebook, Twitter, Instagram) that link to the respective profiles.
- **Right Column (`.footer-column`)**:
  - Titled "Let's Message me," this column features a contact form.
  - The form includes fields for a name, email, and a message, along with a "Submit" button.

## Code Quality and Suggestions

The codebase is well-organized and uses descriptive class names. The use of semantic HTML is a strong point. Here are some suggestions for improvement:

1.  **Improve Form Accessibility**: The contact form inputs currently lack `<label>` tags. Labels are crucial for screen readers and improve the user experience by allowing users to click the text to focus on the input field.

    **Suggestion:**
    ```html
    <form action="">
      <label for="name">Your Name</label>
      <input type="text" name="name" id="name" placeholder="Your name">

      <label for="email">Your Email</label>
      <input type="email" name="email" id="email" placeholder="Your Email">

      <label for="message">Message</label>
      <textarea name="message" id="message" cols="50" rows="10" placeholder="Message"></textarea>

      <input class="btn-primary" type="submit" value="Submit">
    </form>
    ```
    *(Note: The labels can be visually hidden with CSS if you prefer not to show them).*

2.  **Avoid Using `<br>` for Layout**: In the "About Me" and "What I do" sections, `<br>` tags are used to create line breaks. This is not ideal for responsive design, as it can cause awkward text wrapping on different screen sizes.

    **Suggestion**: Remove the `<br>` tags and control the width of the text containers (e.g., `.section-description`) using CSS `max-width` and `margin: 0 auto;` properties. This allows the text to flow naturally and adapt to the viewport.

3.  **Semantic Replacements for `<hr>`**: The `<hr>` tags in the resume section are used for visual separation. A more modern approach is to use CSS borders.

    **Suggestion**: Remove the `<hr>` tags and add a `border-bottom` to the `.experience` class in your CSS file. This keeps your HTML cleaner and gives you more styling control.

    ```css
    .experience {
      border-bottom: 1px solid #d1d1d1; /* Or your preferred color */
      margin-bottom: 20px;
      padding-bottom: 20px;
    }
    /* Make sure to remove the border from the last element in each column */
    .resume-column .experience:last-child {
      border-bottom: none;
      margin-bottom: 0;
    }
    ```

4.  **Check Social Media Links**: In the footer, the link for the Twitter icon currently points to Instagram. This should be corrected to point to the correct social media platform.

    **Current Code:**
    ```html
    <a href="https://www.instagram.com/" target="_blank"><img src="images/icons/twitter.png" alt="twitter"></a>
    ```

    **Suggested Fix:**
    ```html
    <a href="https://www.twitter.com/" target="_blank"><img src="images/icons/twitter.png" alt="twitter"></a>
    ```

## How to Run

1.  Clone this repository to your local machine.
2.  Open the `index.html` file in your web browser to view the website.

