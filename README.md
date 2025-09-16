# MWAD-EX_03-To-Do-List-using-JavaScript
## Date: 16-09-2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To Do Aoo</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="todo-container">
    <h1>✅ Things To-Do</h1>
    <div class="input-group">
      <input type="text" id="taskInput" placeholder="Enter a task...">
      <button id="addBtn">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>


```

style.css
```
body {
  font-family: Arial, sans-serif;
  background: linear-gradient(to right, #ff9a9e, #fad0c4, #fad390, #fbc2eb);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  background: #fff;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  width: 320px;
  text-align: center;
}

h1 {
  margin-bottom: 20px;
  color: #333;
}

.input-group {
  display: flex;
  margin-bottom: 15px;
}

#taskInput {
  flex: 1;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 8px 0 0 8px;
  outline: none;
}

#addBtn {
  padding: 0 15px;
  border: none;
  background: #4CAF50;
  color: white;
  border-radius: 0 8px 8px 0;
  cursor: pointer;
}

#addBtn:hover {
  background: #45a049;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  background: #4e896f;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed span::before {
  content: "✔ ";
  color: green;
  font-weight: bold;
}

button.delete {
  background: #e74c3c;
  border: none;
  color: white;
  padding: 5px 10px;
  border-radius: 6px;
  cursor: pointer;
}

button.delete:hover {
  background: #c0392b;
}


```

script.js
```
const addBtn = document.getElementById("addBtn");
const taskInput = document.getElementById("taskInput");
const taskList = document.getElementById("taskList");

addBtn.addEventListener("click", addTask);
taskInput.addEventListener("keypress", (e) => {
  if (e.key === "Enter") addTask();
});

function addTask() {
  const taskText = taskInput.value.trim();
  if (taskText === "") {
    alert("Please enter a task!");
    return;
  }

  const li = document.createElement("li");
  const taskSpan = document.createElement("span");
  taskSpan.textContent = taskText;

  // Toggle completion
  taskSpan.addEventListener("click", () => {
    li.classList.toggle("completed");
  });

  // Delete button
  const deleteBtn = document.createElement("button");
  deleteBtn.textContent = "Delete";
  deleteBtn.classList.add("delete");
  deleteBtn.addEventListener("click", () => {
    taskList.removeChild(li);
  });

  li.appendChild(taskSpan);
  li.appendChild(deleteBtn);
  taskList.appendChild(li);

  taskInput.value = "";
}


```

## OUTPUT



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
