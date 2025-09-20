## luxorpen website

the website uses react at its core, but has tons of issues.

it takes more than 30s to load.

### Review Issues

- **Performance:**  
  - Extremely slow load time (>30s).  
  - High Total Blocking Time and Speed Index (see Lighthouse report).
  - Large images and GIFs are not optimized.
  - Unused CSS and JS increase bundle size.
  - Cumulative Layout Shift is high (0.8).

- **SEO:**  
  - No meta description tag.
  - Images lack `alt` attributes.
  - Links are not crawlable.
  - Missing canonical tags.

- **Code Quality:**  
  - Unused components and styles are present.
  - Poor asset management.
  - Inefficient rendering and resource usage.

### Improvements

1. **Optimize Media:**
   - Compress and resize images/GIFs.
   - Use modern formats (WebP, AVIF).
   - Implement lazy loading for images.

2. **Clean Up Code:**
   - Remove unused CSS, JS, and components.
   - Split code using React lazy and code-splitting.
   - Audit dependencies and remove unused packages.

3. **Improve SEO:**
   - Add meta description and canonical tags in `<head>`.
   - Ensure all images have descriptive `alt` attributes.
   - Make links crawlable (use `<a>` tags with valid `href`).

4. **Performance Tuning:**
   - Minimize main thread work and blocking scripts.
   - Use server-side rendering or static site generation if possible.
   - Cache assets and enable gzip/Brotli compression.

5. **Accessibility:**
   - Add `aria` labels and roles where needed.
   - Ensure color contrast and keyboard navigation.

6. **Monitor and Test:**
   - Use Lighthouse and WebPageTest regularly.
   - Set up automated performance and SEO checks in CI/CD.

---

**Summary:**  
Focus on media optimization, code cleanup, and SEO basics to improve load time, crawlability, and user experience.
