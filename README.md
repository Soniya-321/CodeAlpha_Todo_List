To-Do List Application Documentation
    This document explains the code for a web-based to-do list application built with HTML, CSS, and JavaScript.

1. HTML Structure (index.html):
    Defines the basic layout of the web page.
    Contains elements for the heading, user input area, to-do list container, and stylesheet link.
    Uses a <div> with the class todos-bg-container to encompass the entire application content.
    Within the container, the structure utilizes Bootstrap classes for responsiveness.

2. CSS Styling (style.css):
    Defines the visual appearance of various elements in the application.
    Leverages Bootstrap classes for basic layout and styling.
    Includes custom styles for specific elements like headings, input field, button, and to-do items.
    Uses Google Fonts (imported separately) for a more visually appealing look.

3. JavaScript Functionality (script.js):
    Provides interactivity and dynamic behavior to the application.
    Key functionalities include:
      Storing Initial Data:
        todoItemsContainer: Holds a reference to the HTML element displaying to-do items.
        todoList: An array containing initial to-do items (text and unique ID).
        todoCount: Tracks the total number of to-do items.
      Event Handling Functions:
        onTodoItemHasChanged(checkboxId, labelId):
          Called when a checkbox is clicked.
          Toggles the "checked" class on the corresponding label to visually indicate completion.
        onDeleteTodo(deleteId):
          Called when a delete icon is clicked.
          Removes the associated to-do item element from the list.
      Creating and Appending To-Do Items:
        createAndAppendTodo(todo):
          Dynamically generates the HTML structure for a to-do item based on a provided todo object.
          Creates elements for checkbox, label, and delete icon with unique IDs.
          Attaches event listeners to the checkbox and delete icon for handling clicks.
          Appends the created elements to the to-do list container.
        Rendering Initial To-Do Items:
          Iterates through the todoList array and calls createAndAppendTodo for each item, populating the initial list.
        Handling New To-Do Addition:
          onAddTodo():
            Retrieves the user's input text from the input field.
            Validates the input to ensure it's not empty.
            Creates a new to-do object with the entered text and a unique ID.
            Calls createAndAppendTodo to dynamically add the new item to the list.
            Clears the user input field after successful addition.
      Button Click Event Listener:
        Attaches a click event listener to the "Add" button.
        When the button is clicked, it calls the onAddTodo function to handle adding a new to-do item.
    
    Overall Functionality:
        The application displays a to-do list.
        Users can add new to-do items by entering text and clicking the "Add" button.
        Checkbox clicks toggle the completion status of a to-do item (visually with a strikethrough).
        Users can delete to-do items by clicking the delete icon associated with each item.
    
    Additional Notes:
        The code utilizes Bootstrap for a responsive layout that adapts to different screen sizes.
        The provided documentation serves as a high-level explanation. You can further enhance it with comments within the code itself for more detailed explanations.
