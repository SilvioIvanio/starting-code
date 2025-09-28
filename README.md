# Lab 5: Design & Development Report

This report explains the design choices and the problems I solved in Lab 5 about styling a web app.

## 1. Design Decisions and Approach

My goal was to make a clean and modern user interface and keep the styles easy to manage.

- I styled one group of components at a time. This helped me finish each part completely before moving on.
- I used CSS variables like `--primary` and `--card-bg` for colors and themes. With variables, I could change the theme in one place, and it updated everywhere. This also made it easy to add a dark theme.

## 2. Challenges and Solutions

I had some layout problems and fixed them.

- Problem: Calendar days did not fit and were overflowing the mini calendar grid.
    - Cause: The grid used flexible columns (1fr), but each day had a fixed width (30px). These did not work well together.
    - Fix: I removed the fixed width from `.calendar-day`. Then the items became flexible and fit the grid correctly.
- Problem: The last emoji in the mood tracker was cut off.
    - Cause: The emojis were large (font-size: 1.8rem) and the container used `justify-content: space-between`, pushing the last emoji to the edge.
    - Fix: I reduced the emoji size to 1.6rem. Now all emojis fit without being cut.

## 3. Key Learnings

I learned how styling can work with elements created by JavaScript.

- The `.toast` notification elements were not in the static HTML. They were created in `scripting.js` at runtime.
- I learned to check the JavaScript to see which classes are added dynamically, then write CSS for those classes.

## Summary

- Use CSS variables for easy theming.
- Make grid and flex items flexible to avoid overflow.
- Check JavaScript for dynamic elements when styles seem to be missing.

**Live:** https://silvioivanio.github.io/starting-code/
