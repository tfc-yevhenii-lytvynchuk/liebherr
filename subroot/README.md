# Liebherr B2B Product Portal

A lightweight, responsive HTML/CSS implementation of the Liebherr B2B Product Portal, designed for future integration with .NET backend.

## Design System

### Colors
- Primary: `#2779C4`
- Success: `#006800`
- Warning: `#EB6F25`
- Background: `#F0F3F6`

### Typography
- Headings: LiebherrHead-Black
- Body: LiebherrText-Regular
- Bold: LiebherrText-Bold
- Medium: LiebherrText-Medium

### Components
- Navigation
- Product Cards
- Category Cards
- Search Forms
- Buttons
- Breadcrumbs

## Notes for .NET Developers

### Dynamic Content Areas
The following sections are designed to be populated dynamically:

1. **Product Categories**
   - Located in the main product categories section
   - Each category card is wrapped in an `<a>` tag
   - Images are stored in `assets/images/categories/`

2. **Best Sales Section**
   - Tab navigation for different product categories
   - Product cards will be dynamically populated
   - Current implementation uses placeholder content

3. **Search Functionality**
   - Search form in the banner section
   - Navigation search form
   - Both forms are ready for .NET integration

### Integration Points

1. **Forms**
   - Product search form: `id="product-search-form"`
   - Navigation search form: `id="nav-search-form"`
   - Newsletter subscription form `id="newsletter-form"`

2. **Dynamic Content Classes**
   - Product cards: `liebherr-product-card`
   - Category cards: `liebher-product-category-card`
   - Navigation items: `nav-link`

3. **Image Handling**
   - Product images should maintain aspect ratio
   - Category images are set to `object-fit: contain`
   - Banner images use `object-fit: cover`

## CSS Architecture

The project uses a combination of:
- Custom CSS reset
- Bootstrap 5 for grid and components
- Custom utility classes
- Component-specific styles

### CSS Organization Strategy
- `styles.css`: Contains only global styles, utility classes, and shared components
- Page-specific styles: Included directly in the respective HTML files using `<style>` tags
  - This approach clearly indicates which styles are specific to each page
  - Makes it easier to identify and maintain page-specific styles
  - New pages will follow the same pattern with their own scoped styles

### Key CSS Files
- `styles.css`: Main stylesheet for global styles
- `bootstrap.min.css`: Bootstrap framework
- `liebherr-fonts.css`: Custom font definitions
- `bootstrap-icons.css`: Icon library

## Responsive Design

The implementation is fully responsive with breakpoints at:
- Mobile: < 768px
- Tablet: 768px - 991px
- Desktop: > 992px

## Future Considerations

3. **SEO**
   - Add meta descriptions