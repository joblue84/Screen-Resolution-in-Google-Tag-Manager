# Mobile Tablet Screen Resolution in Google Tag Manager
How to create a custom variable to capture screen resolution and effectively use it in our triggers.

1. Navigate to Variables in GTM (left side panel) and click the <b>New button</b> to create a <b>new variable.</b>
2. Edit the variable to set its type, and then select <b>Custom JavaScript</b> from the options on the right panel.
3. <b>Add the following JavaScript code snippet</b> and name the variable <b>“Screen Resolution”</b>
   
```javascript
function () {
  var width = window.innerWidth,
  screenType;
  if (width <= 520) {
    screenType = "mobile";
  } else if (width <= 820) {
    screenType = "tablet";
  } else {
    screenType = "desktop";
  }
  return screenType;
}
```
4. Save the variable.
5. You can use it for creating triggers. Choose <b>Screen Resolution</b> in conditions dropdown.
6. Set it to<b> “contains" "mobile|table”</b>(you can type in the value "mobile|table” in lowercase).
7. Save the trigger.
