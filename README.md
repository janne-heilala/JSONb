
### HTML Structure

First, set up your HTML structure with a button and icons. Use IDs or classes to target these elements with JavaScript and CSS.

```html
<div id="MenuButton" class="menu-button">
    <img id="MenuButtonIcon" src="path_to_default_icon" alt="Menu Icon" />
</div>
```

### CSS for Styling

Use CSS to style the button and icon. You might want to change the cursor to a pointer to indicate that the button is clickable.

```css
.menu-button {
    cursor: pointer;
    /* additional styling */
}

.menu-button img {
    /* styling for the icon */
}
```

### JavaScript for Interactivity

JavaScript will handle the mouse events. You'll need to change the icon source or class on mouse down and revert it on mouse up or mouse leave.

```javascript
document.getElementById('MenuButton').addEventListener('mousedown', function() {
    document.getElementById('MenuButtonIcon').src = 'path_to_pressed_icon';
});

document.getElementById('MenuButton').addEventListener('mouseup', function() {
    document.getElementById('MenuButtonIcon').src = 'path_to_default_icon';
});

document.getElementById('MenuButton').addEventListener('mouseleave', function() {
    document.getElementById('MenuButtonIcon').src = 'path_to_default_icon';
});
```

### Putting It All Together

1. **HTML**: Place your button within the HTML body.
2. **CSS**: Include your CSS in a `<style>` tag in the head of your HTML or in a separate stylesheet.
3. **JavaScript**: Include your JavaScript at the end of the body or in a separate script file.

When you run this in a web environment, moving the mouse over the button and pressing it will change the icon, demonstrating the interactive behavior.

To see this in action, you'll need to implement it in an actual HTML file and view it in a web browser. Remember to replace `'path_to_default_icon'` and `'path_to_pressed_icon'` with the actual paths to your icon images.
