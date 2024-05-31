# Calculator Project

This is a simple web-based calculator project that performs basic arithmetic operations. The calculator allows users to input numbers and operators, and it evaluates the expressions entered.

## Set Up the Environment

1. **Prerequisites:**
    - A web browser (e.g., Google Chrome, Firefox, Edge)
    - A text editor or IDE (e.g., Visual Studio Code, Sublime Text)

2. **Clone the Repository:**
    ```sh
    git clone https://github.com/yourusername/calculator-project.git
    cd calculator-project
    ```

## Download Programs and Related Documentation

1. **HTML and JavaScript Files:**
    - `index.html`: Contains the structure and logic of the calculator.
    - No additional programs or libraries are required for this project.

## Process of Program Execution

1. **Open the Project:**
    - Navigate to the project directory and open the `index.html` file in your web browser.
    - Alternatively, you can use a live server extension in your text editor to view the project.

2. **Using the Calculator:**
    - Enter numbers and arithmetic operators using the on-screen buttons.
    - Click the `=` button to evaluate the expression.
    - Click the `Clear` button to reset the input field.

## Design and Implementation

The calculator is designed using HTML for the structure, CSS for styling, and JavaScript for functionality. Below is a brief description of each component:

- **HTML:** Provides the structure of the calculator, including the input field and buttons.
- **CSS:** Adds styling to the calculator, such as borders, spacing, and layout.
- **JavaScript:** Implements the functionality, including handling button clicks and performing calculations using the `eval` function.

![Calculator Design](https://raw.githubusercontent.com/Senedaa/Online-Calculator/main/design.png)



### JavaScript Functions

- **`addToScreen(value)`:** This function takes a value (number or operator) as an argument and appends it to the calculator's input screen. It is called whenever a button is pressed.
- **`clearScreen()`:** This function clears the calculator's input screen. It is called when the "Clear" button is pressed.
- **`calculateResult()`:** This function evaluates the expression currently displayed on the input screen using the `eval` function and updates the screen with the result. If the expression is invalid, it displays "Error".

```javascript
function addToScreen(value) {
    var screen = document.getElementById("screen");
    screen.value += value;
}

function clearScreen() {
    document.getElementById("screen").value = "";
}

function calculateResult() {
    var screen = document.getElementById("screen");
    try {
        screen.value = eval(screen.value);
    } catch (error) {
        screen.value = "Error";
    }
}
```

## IDE Requirements

It is recommended to use Visual Studio Code (VSCode) for editing and running this project. VSCode provides a rich set of features and extensions that enhance the development experience:

- Syntax highlighting and code formatting
- Integrated terminal

To set up VSCode:

1. Download and install VSCode from the official website: [Visual Studio Code](https://code.visualstudio.com/)
2. Open the project directory in VSCode.
3. Install the Live Server extension from the Extensions marketplace.
4. Right-click the `index.html` file and select "Open with Live Server".

## Screenshot of Execution Results

![Calculator Screenshot](image1_result.png)
![Calculator Screenshot](image2_result.png)

## Note on the eval Function

The calculator uses the `eval` function in JavaScript to evaluate the arithmetic expressions entered by the user. While `eval` is a powerful function, it should be used with caution as it can execute arbitrary code and pose security risks if not handled properly. In this project, it is used in a controlled manner to safely evaluate mathematical expressions.

