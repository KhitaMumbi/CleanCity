# CleanCity Lighthouse Report

## Summary of Results

| Page Tested       | Performance | Accessibility | Best Practices | SEO  |
|-------------------|-------------|---------------|----------------|------|
| Home Page         | 89          | 95            | 100            | 100  |
| Dashboard         | 92          | 100           | 96             | 80   |
| Download Page     | 96          | 100           | 96             | 80   |

## Key Issues

### Common Across All Pages
⚠ **404 Errors**  
- Lighthouse couldn't reliably load some pages (server response issues)
- Recommendation: Verify all URLs return 200 status codes

⚠ **Slow Loading**  
- All pages exceeded time limits during testing
- Average LCP: 2.7s (should be <2.5s)

  **Lighthouse documentation**
  
[home.pdf](https://github.com/user-attachments/files/21265690/home.pdf)

[dashboard lh.pdf](https://github.com/user-attachments/files/21265721/dashboard.lh.pdf)

[community.pdf](https://github.com/user-attachments/files/21265726/community.pdf)

### Performance Issues
```diff
# Home Page (89)
- Render-blocking resources (1.4s potential savings)
- Uncompressed JavaScript (112KiB savings possible)
- 7 long main-thread tasks


# Dashboard (92)
- 1.5s render-blocking resources
- 5 long main-thread tasks
