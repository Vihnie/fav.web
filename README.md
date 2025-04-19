# fav.web
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM Manipulation Example</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Welcome to the DOM Manipulation Example</h1>
     <div id="content">
        <p id="para">This is a sample paragraph.</p>
        <button id="changeTextBtn">Change Text</button>
        <button id="styleTextBtn">Change Text Style</button>
        <button id="removeElementBtn">Remove Paragraph</button>
    </div>

    <script src="script.js"></script>
</body>
</html>


script.js

```javascript // Change the text content dynamically
document.getElementById("changeTextBtn").addEventListener("click", function() {
    document.getElementById("para").innerHTML = "The text has been changed dynamically!";
});

// Modify CSS styles via JavaScript
document.getElementById("styleTextBtn").addEventListener("click", function() {
    document.getElementById("para").style.color = "blue";
    document.getElementById("para").style.fontSize = "20px";
});

// Remove an element when the button is clicked
document.getElementById("removeElementBtn").addEventListener("click", function() {
    var para = document.getElementById("para");
    para.parentNode.removeChild(para);
});
