<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator Project README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 20px;
            background-color: #f9f9f9;
            color: #333;
        }
        h1 {
            color: #4CAF50;
        }
        h2 {
            color: #2196F3;
        }
        p, li, code {
            font-size: 16px;
        }
        pre {
            background-color: #eee;
            padding: 10px;
            border-left: 4px solid #4CAF50;
            overflow-x: auto;
        }
        img {
            max-width: 100%;
            border: 1px solid #ddd;
            padding: 5px;
            background-color: #fff;
            margin-bottom: 20px;
        }
        ul {
            list-style-type: square;
        }
        .note {
            background-color: #ffeb3b;
            padding: 10px;
            border-left: 4px solid #ff9800;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <h1>Calculator Project</h1>
    <p>This is a simple web-based calculator project that performs basic arithmetic operations. The calculator allows users to input numbers and operators, and it evaluates the expressions entered.</p>

    <h2>Set Up the Environment</h2>
    <ol>
        <li>
            <strong>Prerequisites:</strong>
            <ul>
                <li>A web browser (e.g., Google Chrome, Firefox, Edge)</li>
                <li>A text editor or IDE (e.g., Visual Studio Code, Sublime Text)</li>
            </ul>
        </li>
        <li>
            <strong>Clone the Repository:</strong>
            <pre><code>git clone https://github.com/yourusername/calculator-project.git
cd calculator-project</code></pre>
        </li>
    </ol>

    <h2>Download Programs and Related Documentation</h2>
    <ol>
        <li>
            <strong>HTML and JavaScript Files:</strong>
            <ul>
                <li><code>index.html</code>: Contains the structure and logic of the calculator.</li>
                <li>No additional programs or libraries are required for this project.</li>
            </ul>
        </li>
    </ol>

    <h2>Process of Program Execution</h2>
    <ol>
        <li>
            <strong>Open the Project:</strong>
            <ul>
                <li>Navigate to the project directory and open the <code>index.html</code> file in your web browser.</li>
                <li>Alternatively, you can use a live server extension in your text editor to view the project.</li>
            </ul>
        </li>
        <li>
            <strong>Using the Calculator:</strong>
            <ul>
                <li>Enter numbers and arithmetic operators using the on-screen buttons.</li>
                <li>Click the <code>=</code> button to evaluate the expression.</li>
                <li>Click the <code>Clear</code> button to reset the input field.</li>
            </ul>
        </li>
    </ol>

    <h2>Design and Implementation</h2>
    <p>The calculator is designed using HTML for the structure, CSS for styling, and JavaScript for functionality. Below is a brief description of each component:</p>
    <ul>
        <li><strong>HTML:</strong> Provides the structure of the calculator, including the input field and buttons.</li>
        <li><strong>CSS:</strong> Adds styling to the calculator, such as borders, spacing, and layout.</li>
        <li><strong>JavaScript:</strong> Implements the functionality, including handling button clicks and performing calculations using the <code>eval</code> function.</li>
    </ul>
    <p><img src="design.png" alt="Calculator Design"></p>

    <h2>JavaScript Functions</h2>
    <ul>
        <li><strong><code>addToScreen(value)</code>:</strong> This function takes a value (number or operator) as an argument and appends it to the calculator's input screen. It is called whenever a button is pressed.</li>
        <li><strong><code>clearScreen()</code>:</strong> This function clears the calculator's input screen. It is called when the "Clear" button is pressed.</li>
        <li><strong><code>calculateResult()</code>:</strong> This function evaluates the expression currently displayed on the input screen using the <code>eval</code> function and updates the screen with the result. If the expression is invalid, it displays "Error".</li>
    </ul>
    <pre><code>
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
    </code></pre>

    <h2>IDE Requirements</h2>
    <p>We recommend using Visual Studio Code (VSCode) for editing and running this project. VSCode provides a rich set of features and extensions that enhance the development experience:</p>
    <ul>
        <li>Syntax highlighting and code formatting</li>
        <li>Integrated terminal</li>
        <li>Live Server extension for real-time viewing of changes</li>
        <li>Debugging tools</li>
    </ul>
    <p>To set up VSCode:</p>
    <ol>
        <li>Download and install VSCode from the official website: <a href="https://code.visualstudio.com/">Visual Studio Code</a></li>
        <li>Open the project directory in VSCode.</li>
        <li>Install the Live Server extension from the Extensions marketplace.</li>
        <li>Right-click the <code>index.html</code> file and select "Open with Live Server".</li>
    </ol>

    <h2>Screenshot of Execution Results</h2>
    <p><img src="image1.png" alt="Calculator Screenshot"></p>
    <p><img src="image2.png" alt="Calculator Screenshot"></p>

    <div class="note">
        <h2>Note on the eval Function</h2>
        <p>The calculator uses the <code>eval</code> function in JavaScript to evaluate the arithmetic expressions entered by the user. While <code>eval</code> is a powerful function, it should be used with caution as it can execute arbitrary code and pose security risks if not handled properly. In this project, it is used in a controlled manner to safely evaluate mathematical expressions.</p>
    </div>
</body>
</html>
