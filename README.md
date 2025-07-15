# 🗓️ Offline Content Calendar

This is a simple, client-side, offline-first content calendar that helps you organize your tasks by date and category. All your data is saved directly in your browser's local storage, meaning it's always available even without an internet connection.

-----

## ✨ Features

  * **Intuitive Navigation**: Easily navigate through months and years.
  * **Offline First**: All your content tasks are saved locally in your browser.
  * **Task Management**:
      * **Double-click a date** to quickly add a new task.
      * Mark tasks as **completed** with a checkbox.
      * **Edit** task descriptions by clicking on them.
      * **Delete** tasks with a click.
  * **Categorization**: Assign categories to your tasks, which are visually represented with color coding and shortened keywords (e.g., "YouTube" becomes "YT").
  * **Data Management**:
      * **Export** your calendar data as a JSON file for backup.
      * **Import** tasks from a JSON file.
  * **Print & Export**: Print your calendar directly or export it as a PDF.

-----

## 🚀 How to Use

1.  **Save the File**: Save the provided HTML code as an `.html` file (e.g., `content_calendar.html`).
2.  **Open in Browser**: Open the `content_calendar.html` file in your web browser.

That's it\! The calendar will load, and your previously saved tasks (if any) will appear.

### Adding a Task

1.  **Double-click** on the date cell where you want to add a task.
2.  A prompt will appear asking for the **task description**. Enter your task and click "OK".
3.  Another prompt will appear asking for the **category**. You can use the full category names (YouTube, Facebook, LinkedIn, Instagram, BlogPost) or their shortened versions (YT, FB, LI, IG, BP). Enter your chosen category and click "OK".

### Editing a Task

1.  Click on the **text** of the task you wish to edit.
2.  The text will become an input field. Type your changes.
3.  Press `Enter` or click outside the input field to save the changes.

### Marking a Task as Complete

1.  Click the **checkbox** next to the task.

### Deleting a Task

1.  Click the **"×" button** next to the task.
2.  Confirm the deletion when prompted.

### Navigating the Calendar

  * Use the **"\< Prev"** and **"Next \>"** buttons to move between months.
  * Use the **month dropdown** and **year input field** to jump to a specific date.

### Importing/Exporting Data

  * **Export Data**: Click the "Export Data" button to download your current tasks as a `calendar_backup.json` file.
  * **Import Data**: Click the "Import Data" button, then select a `calendar_backup.json` file from your computer. **Be careful: importing data will overwrite your current calendar tasks.**

### Printing/Exporting to PDF

  * **Print**: Click the "Print" button to open your browser's print dialog.
  * **Export PDF**: Click the "Export PDF" button to download a PDF version of your current calendar view.

-----

## 🛠️ Customization

You can customize the categories and their associated colors by modifying the `<style>` block and the `categories` object in the JavaScript.

### CSS Variables for Colors

In the `<style>` section, you'll find CSS variables for category background colors:

```css
:root {
    /* ... other variables ... */
    --cat-youtube-bg: #ffcccc;
    --cat-facebook-bg: #cce5ff;
    --cat-linkedin-bg: #d4edda;
    --cat-instagram-bg: #fff3cd;
    --cat-blog-post-bg: #f8d7da;
}
```

You can change these hex codes to adjust the colors.

### JavaScript Categories Mapping

In the `<script>` section, the `categories` object maps the full category names to their shortened versions:

```javascript
const categories = {
    "YouTube": "YT",
    "Facebook": "FB",
    "LinkedIn": "LI",
    "Instagram": "IG",
    "BlogPost": "BP"
};
// Map shortened categories to CSS classes
const categoryCssClasses = {
    "YT": "category-YT",
    "FB": "category-FB",
    "LI": "category-LI",
    "IG": "category-IG",
    "BP": "category-BP"
};
```

To add a new category, add an entry to the `categories` object (e.g., `"New Category": "NC"`). Then, add a corresponding CSS class in the style block (e.g., `.category-NC { background-color: #yourcolor; }`) and update the `categoryCssClasses` object. Remember to also update the legend in the `<footer>` if you add new categories.

-----
