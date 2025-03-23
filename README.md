# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript and DOM Manipulation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
        }
        button {
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background-color: #4CAF50;
            color: white;
            font-size: 1em;
        }
        button:hover {
            background-color: #45a049;
        }
        #dynamic-container {
            margin-top: 20px;
            padding: 10px;
            border: 1px solid #ddd;
        }
    </style>
</head>
<body>
    <header>
        <h1 id="main-heading">Welcome to JavaScript DOM Manipulation</h1>
    </header>
    <main>
        <p id="dynamic-text">Click the button below to change this text.</p>
        <button id="change-text-button">Change Text</button>
        
        <button id="add-element-button">Add New Element</button>
        <button id="remove-element-button">Remove Element</button>
        <div id="dynamic-container">
            <!-- New elements will be added here -->
        </div>
    </main>
    <footer>
        <p>Created with 💻 and ☕</p>
    </footer>
    <script>
        // Change text dynamically
        const changeTextButton = document.getElementById("change-text-button");
        const dynamicText = document.getElementById("dynamic-text");

        changeTextButton.addEventListener("click", () => {
            dynamicText.textContent = "You have successfully changed this text!";
            dynamicText.style.color = "blue";
            dynamicText.style.fontWeight = "bold";
        });

        // Add a new element
        const addElementButton = document.getElementById("add-element-button");
        const dynamicContainer = document.getElementById("dynamic-container");

        addElementButton.addEventListener("click", () => {
            const newElement = document.createElement("p");
            newElement.textContent = "This is a dynamically added element!";
            newElement.style.color = "green";
            dynamicContainer.appendChild(newElement);
        });

        // Remove an element
        const removeElementButton = document.getElementById("remove-element-button");

        removeElementButton.addEventListener("click", () => {
            if (dynamicContainer.lastChild) {
                dynamicContainer.removeChild(dynamicContainer.lastChild);
            } else {
                alert("No more elements to remove!");
            }
        });
    </script>
</body>
</html>
