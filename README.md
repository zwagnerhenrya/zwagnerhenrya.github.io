# PhD Portfolio Website - Jekyll Version

A personal portfolio website for a PhD Engineering student at the University of Wisconsin-Madison, built with Jekyll. This website includes an introduction, contact information, projects showcase, and resume sections.

## Features

- Clean, responsive design that works on mobile, tablet, and desktop
- Navigation tabs for Home, Projects, and Resume sections
- Easy-to-edit content using Markdown and HTML
- Modern UI with Tailwind CSS

## Getting Started

### Prerequisites

- Ruby (v2.5.0 or higher)
- RubyGems
- GCC and Make (for some gem installations)

### Installation

1. Clone this repository
2. Navigate to the project directory
3. Install Jekyll and Bundler:

```bash
gem install jekyll bundler
```

4. Install dependencies:

```bash
bundle install
```

5. Start the development server:

```bash
bundle exec jekyll serve --livereload
```

6. Open your browser and visit `http://localhost:4000`

## How to Edit Content

This website is designed to be easily editable. Here's how to modify different sections:

### General Information

The main site configuration is in `_config.yml`. This file contains:
- Site title and description
- Your personal information
- Social media links

```yaml
# Example: Update your personal information
personal_info:
  name: Your Name
  title: PhD Engineering Student
  university: University of Wisconsin-Madison
  department: Department of Engineering
  location: Madison, WI
  office: Building Name, Room Number
```

### Editing Pages

The main pages are written in Markdown with HTML and are located in the root directory:

1. **Home Page**: `index.md`
   - Update your introduction
   - Modify research interests
   - Change contact information
   - Edit social media links

2. **Projects Page**: `projects.md`
   - Add or remove project cards
   - Update project descriptions, images, and links

3. **Resume Page**: `resume.md`
   - Update education details
   - Modify research experience
   - Edit publications list
   - Update skills and awards

### Adding Images

1. Place your images in the `assets/images` directory
2. Reference them in your Markdown files:
   ```markdown
   ![Alt text](/assets/images/your-image.jpg)
   ```
   
   Or in HTML:
   ```html
   <img src="{{ '/assets/images/your-image.jpg' | relative_url }}" alt="Description" class="profile-image">
   ```

### Changing Styles

This project uses Tailwind CSS for styling:

1. Global styles are in `assets/css/main.css`
2. Component-specific styles are applied directly in the HTML using Tailwind classes
3. To customize Tailwind, you would need to set up a local Tailwind installation

## Project Structure

```
phd-portfolio/
├── _config.yml          # Site configuration
├── _data/               # Data files for the site
├── _includes/           # Reusable components
│   ├── footer.html      # Site footer
│   └── header.html      # Navigation header
├── _layouts/            # Page templates
│   └── default.html     # Main layout template
├── assets/              # Static assets
│   ├── css/             # Stylesheets
│   ├── images/          # Images
│   └── js/              # JavaScript files
├── index.md             # Home page
├── projects.md          # Projects page
├── resume.md            # Resume page
└── README.md            # This file
```

## Customization Tips

1. **Changing Colors**: Edit the color classes in the HTML (e.g., `bg-blue-600` to `bg-green-600`)
2. **Adding New Pages**: Create a new Markdown file in the root directory with the appropriate front matter
3. **Custom Fonts**: Add custom font CSS to `assets/css/main.css`

## Deployment

To build the website for production:

```bash
bundle exec jekyll build
```

This will create a `_site` directory with static files ready for deployment to any web hosting service.

## Troubleshooting

- If you encounter issues with gem dependencies, try running `bundle update`
- For build errors, check the console output for specific error messages
- Make sure all image paths are correct when adding new images

## License

This project is open source and available for personal use.
