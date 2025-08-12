# 📝 ReactTodolist_0808
I rebuilt [To do Lists_0725](https://github.com/michelle5434123/To-do-Lists_250725) with React to help user to organize their events. This React-based To-Do List application allows to add, view, and clear tasks. Tasks include a category, name, date, and description.

![image](https://github.com/user-attachments/assets/d4c4cd6e-a0a9-4cfc-b0e3-d2e809ed82d8)

## Features
- Add tasks with:
  - Category (Work, Family, Me, or blank)
  - Task name
  - Date (defaults to today’s date)
  - Description
- Dynamic task table that updates as tasks are added.
- Clear all tasks with a single button click.
- Graceful handling of empty inputs (stores them as null).


## How It Works
- **State** `formDataList` holds an array of task objects.
- Each `input` is wraped with **`label` for accessability**
- Adding a Task: **`addTask()`**
  - When the form is submitted, `addTask()`:
    - Loops over all expected fields (`selectCategory`, `taskname`, `datename`, `descriptionname`)
    - **Retrieves and `trims()`** the value.
    - Stores `null` if the field is empty.
    - Appends the newtask to `formDataList`.
- Displaying Tasks: **`formDate()` maps over `formDataList` to generate `<tr>` table rows.**
- Deleting All Tasks: The **"Delete All"** button clears `formDataList`.


## Notes
- Today is dynamically generated using `const today = new Date().toISOString().split("T")[0];`


## How to Run This Project Locally
These instructions assume you have **Node.js** and **npm** installed on your computer. If not, download them from [nodejs.org](https://nodejs.org/).

### 1. Clone or Download the Repo
Click on the green **Code** button and choose **Download ZIP** or use Git:
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```
### 2. Install Dependencies:
Make sure react, react-dom, and vite are included in your package.json
```bash
npm install
```
### 3. Start the Development Server
If you’re using Vite (recommended for this setup):
```bash
npm run dev
```
This will start the server and Open the link in your browser.


