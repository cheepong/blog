# Project Overview

This directory contains a Quarto website project, primarily functioning as a technical blog titled "cheekypong". It is designed for publishing articles, tutorials, and other content, leveraging Quarto's capabilities for reproducible research and dynamic document generation. The project structure allows for easy creation and organization of blog posts, with automatic listing and navigation features.

# Key Files and Directories

*   `_quarto.yml`: The main configuration file for the Quarto project. It defines the website's title, navigation structure (navbar), output directory (`docs/`), and overall theme (`cosmo`).
*   `index.qmd`: The primary content file for the homepage. It configures the listing of blog posts from the `posts/` directory, displaying them in descending order of date.
*   `about.qmd`: Contains content for the "About" page of the website.
*   `styles.css`: A custom CSS file intended for overriding or adding styles to the `cosmo` theme. (Currently empty, indicating default theme styling is used).
*   `profile.jpg`, `sigtuna.jpeg`: Image assets used within the website.
*   `posts/`: This directory contains all individual blog posts. Each post is typically a `.qmd` file (Quarto Markdown) within its own subdirectory, along with any associated images or data. Example posts include `frequentist_vs_bayesian/freq_vs_bayes.qmd` and `motorbike/motorbike.qmd`.
*   `docs/`: This directory is the output location for the rendered website. After running `quarto render`, the static HTML files, CSS, JavaScript, and other assets that make up the website are generated here.

# Usage

The project is built and rendered using the Quarto publishing system.

## Rendering the Website

To build the static website files, navigate to the root directory of this project in your terminal and run the following command:

```bash
quarto render
```

This command will process all `.qmd` files and generate the complete website within the `docs/` directory.

## Viewing the Website

After rendering, you can view the generated website by opening `docs/index.html` in your web browser.

## Adding New Posts

To add a new blog post:
1.  Create a new subdirectory within the `posts/` directory (e.g., `posts/my_new_post/`).
2.  Inside this new subdirectory, create a new `.qmd` file (e.g., `posts/my_new_post/my_new_post.qmd`).
3.  Add YAML front matter to your `.qmd` file, including `title`, `author`, `date`, and `categories`.
4.  Write your content using Markdown and Quarto's extensions.
5.  Run `quarto render` to update the website with your new post.

# Development Conventions

*   **Content Format**: All primary content, especially blog posts, should be written in Quarto Markdown (`.qmd`) files.
*   **Styling**: Custom styling should be added to `styles.css`.
*   **Asset Management**: Images and other assets specific to a post should ideally be placed in the same subdirectory as the post's `.qmd` file.
