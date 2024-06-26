# Project Plan: Vigilante Portfolio Website

## Project Overview
**Company Name:** Vigilante  
**Description:** Vigilante provides a wide variety of IT solutions including security cameras, alarms, smart homes (installing and selling online), and web design and development (both static and dynamic).

## Teams and Responsibilities
- **Team 1: Website Design and Layout**
- **Team 2: Website Development and Integration**

## Tools and Technologies
- **Design:** Adobe XD, Figma
- **Development:** WordPress, HTML, CSS, JavaScript, PHP
- **Plugins:** Elementor, Yoast SEO, WooCommerce (for e-commerce functionality), Contact Form 7
- **Version Control:** Git, GitHub
- **Project Management:** Trello, Slack

## Day-by-Day Plan

### Day 1: Planning and Setup
- **Team 1: Website Design and Layout**
  - Research modern web design trends and create a mood board.
  - Sketch wireframes for the homepage and key sections (Services, Partners, Contact).
- **Team 2: Website Development and Integration**
  - Set up the development environment.
  - Install WordPress on the server and configure basic settings.

### Day 2: Initial Design and Basic Setup
- **Team 1: Website Design and Layout**
  - Create high-fidelity designs in Adobe XD or Figma.
  - Review designs with the team and iterate based on feedback.
- **Team 2: Website Development and Integration**
  - Choose and install a suitable WordPress theme.
  - Install and configure essential plugins (Elementor, Yoast SEO, Contact Form 7).

### Day 3: Design Finalization and Content Structure
- **Team 1: Website Design and Layout**
  - Finalize the designs for all key sections.
  - Create design assets (logos, icons, images) and prepare them for development.
- **Team 2: Website Development and Integration**
  - Create the basic page structure (Home, Services, Partners, Contact).
  - Integrate initial content and placeholder text/images.

### Day 4: Advanced Development
- **Team 1: Website Design and Layout**
  - Collaborate with Team 2 to ensure design feasibility.
  - Adjust designs based on development constraints.
- **Team 2: Website Development and Integration**
  - Implement the homepage using Elementor.
  - Start working on the Services page, detailing all IT solutions provided by Vigilante.

### Day 5: Services and Partners Pages
- **Team 1: Website Design and Layout**
  - Create detailed designs for the Services and Partners pages.
- **Team 2: Website Development and Integration**
  - Develop the Services page with detailed descriptions.
  - Create a Partners page template, placeholder for the partner list.

### Day 6: Testing and Optimization
- **Team 1: Website Design and Layout**
  - Review the entire website for design consistency.
  - Prepare design handoff documentation.
- **Team 2: Website Development and Integration**
  - Test website on different browsers and devices for responsiveness.
  - Optimize website performance (image compression, minify CSS/JS).

### Day 7: Final Review and Handoff
- **Team 1: Website Design and Layout**
  - Final design adjustments based on feedback.
  - Ensure all design elements are correctly implemented.
- **Team 2: Website Development and Integration**
  - Conduct a final review and debugging.
  - Prepare documentation for website maintenance and updates.

## Detailed Description of Harder Tasks

### Implementing the Homepage with Elementor
1. **Install Elementor Plugin**: Navigate to Plugins > Add New, search for Elementor, and install it.
2. **Create a New Page**: Go to Pages > Add New, and select "Edit with Elementor".
3. **Design the Layout**:
   - Use the drag-and-drop feature to add sections and widgets.
   - Customize the header with the company logo and navigation menu.
   - Add a hero section with a background image, headline, and call-to-action button.
4. **Save and Preview**: Save changes and preview the page to ensure it matches the design.

### Creating a Custom Services Page
1. **Install Custom Post Type UI Plugin**: For creating a custom post type for services.
2. **Add New Post Type**: Go to CPT UI > Add/Edit Post Types, create a new post type named "Services".
3. **Design the Services Page with Elementor**:
   - Use Elementor to create a template for the services post type.
   - Include sections for each service category (security cameras, alarms, smart homes, web development).
4. **Add Service Details**: Populate the services post type with detailed descriptions and images.

## Sample Code Snippets

### Custom Post Type Registration (functions.php)
```php
function vigilante_custom_post_types() {
    register_post_type('services', array(
        'labels' => array(
            'name' => __('Services'),
            'singular_name' => __('Service')
        ),
        'public' => true,
        'has_archive' => true,
        'supports' => array('title', 'editor', 'thumbnail')
    ));
}
add_action('init', 'vigilante_custom_post_types');
```

### Custom Elementor Widget (sample-widget.php)

```php
class Custom_Service_Widget extends \Elementor\Widget_Base {
    public function get_name() {
        return 'custom_service';
    }

    public function get_title() {
        return __('Custom Service', 'plugin-name');
    }

    public function get_icon() {
        return 'fa fa-code';
    }

    protected function _register_controls() {
        $this->start_controls_section(
            'content_section',
            [
                'label' => __('Content', 'plugin-name'),
                'tab' => \Elementor\Controls_Manager::TAB_CONTENT,
            ]
        );

        $this->add_control(
            'title',
            [
                'label' => __('Title', 'plugin-name'),
                'type' => \Elementor\Controls_Manager::TEXT,
                'default' => __('Service Title', 'plugin-name'),
            ]
        );

        $this->end_controls_section();
    }

    protected function render() {
        $settings = $this->get_settings_for_display();
        echo '<h2>' . $settings['title'] . '</h2>';
    }
}

```



## Project Overview
**Company Name:** Vigilante  
**Description:** Vigilante provides a wide variety of IT solutions including security cameras, alarms, smart homes (installing and selling online), and web design and development (both static and dynamic).

## Teams and Responsibilities
- **Team 1: Website Design and Layout**
- **Team 2: Website Development and Integration**

## Tools and Technologies
- **Design:** Adobe XD, Figma
- **Development:** WordPress, HTML, CSS, JavaScript, PHP
- **Plugins:** Elementor, Yoast SEO, WooCommerce (for e-commerce functionality), Contact Form 7
- **Version Control:** Git, GitHub
- **Project Management:** Trello, Slack

## Project Workflow

| **Day** | **Team 1: Website Design and Layout** | **Team 2: Website Development and Integration** |
|---------|---------------------------------------|-------------------------------------------------|
| **Day 1** | - Research modern web design trends and create a mood board. <br> - Sketch wireframes for the homepage and key sections (Services, Partners, Contact). | - Set up the development environment. <br> - Install WordPress on the server and configure basic settings. |
| **Day 2** | - Create high-fidelity designs in Adobe XD or Figma. <br> - Review designs with the team and iterate based on feedback. | - Choose and install a suitable WordPress theme. <br> - Install and configure essential plugins (Elementor, Yoast SEO, Contact Form 7). |
| **Day 3** | - Finalize the designs for all key sections. <br> - Create design assets (logos, icons, images) and prepare them for development. | - Create the basic page structure (Home, Services, Partners, Contact). <br> - Integrate initial content and placeholder text/images. |
| **Day 4** | - Collaborate with Team 2 to ensure design feasibility. <br> - Adjust designs based on development constraints. | - Implement the homepage using Elementor. <br> - Start working on the Services page, detailing all IT solutions provided by Vigilante. |
| **Day 5** | - Create detailed designs for the Services and Partners pages. | - Develop the Services page with detailed descriptions. <br> - Create a Partners page template, placeholder for the partner list. |
| **Day 6** | - Review the entire website for design consistency. <br> - Prepare design handoff documentation. | - Test website on different browsers and devices for responsiveness. <br> - Optimize website performance (image compression, minify CSS/JS). |
| **Day 7** | - Final design adjustments based on feedback. <br> - Ensure all design elements are correctly implemented. | - Conduct a final review and debugging. <br> - Prepare documentation for website maintenance and updates. |

