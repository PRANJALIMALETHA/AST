<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rule Engine with AST</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }
        .container {
            width: 80%;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        h2 {
            color: #3498db;
            margin-bottom: 10px;
        }
        p {
            line-height: 1.6;
        }
        code {
            background-color: #f9f9f9;
            padding: 2px 4px;
            font-family: 'Courier New', Courier, monospace;
            color: #d6336c;
        }
        .video-link {
            text-align: center;
            margin-bottom: 20px;
        }
        .video-link a {
            text-decoration: none;
            color: #e74c3c;
            font-weight: bold;
            font-size: 18px;
        }
        ul {
            margin-top: 10px;
            padding-left: 20px;
        }
        .section {
            margin-bottom: 20px;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-left: 5px solid #3498db;
            overflow-x: auto;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Rule Engine with AST</h1>

        <div class="vedio_link">
            <p><strong>Video Demo:</strong> <a href="https://youtu.be/Ng-_2iG_IAM" target="_blank">Watch on YouTube</a></p>
        </div>

        <div class="section">
            <h2>Objective</h2>
            <p>
                Develop a 3-tier rule engine application that evaluates user eligibility based on attributes like age, department, income, and spend.
                The system will use an Abstract Syntax Tree (AST) to represent conditional rules and allow dynamic creation, combination, and
                modification of these rules.
            </p>
        </div>

        <div class="section">
            <h2>1. Project Setup</h2>
            <p><strong>Prerequisites:</strong></p>
            <ul>
                <li>IDE: PyCharm or any other IDE of your choice.</li>
                <li>Python Version: 3.8+ (Ensure Python is installed, and a virtual environment is set up if needed).</li>
            </ul>
            <p>Initial Package Installations:</p>
            <pre><code>pip install Flask
pip install pymongo
pip install jsonschema</code></pre>
        </div>

        <div class="section">
            <h2>2. Running the Application</h2>
            <ul>
                <li>Clone the Repository: <code>git clone https://github.com/PRANJALIMALETHA/AST.git</code></li>
                <li>Start the Application:</li>
            </ul>
            <pre><code>python app.py</code></pre>
        </div>

        <div class="section">
            <h2>3. Stack Summary</h2>
            <ul>
                <li><strong>Frontend:</strong> HTML, CSS, JavaScript</li>
                <li><strong>Backend:</strong> Flask (Python), AST Parsing (Python)</li>
                <li><strong>Database:</strong> MongoDB</li>
                <li><strong>Testing:</strong> unittest (Python)</li>
                <li><strong>Package Management:</strong> pip</li>
            </ul>
        </div>

        <div class="section">
            <h2>Key Features of the Application</h2>
            <p>
                This application provides a user interface for managing rules in a rule engine system. Users can:
            </p>
            <ul>
                <li><strong>Create New Rules:</strong> Input a rule string and submit it to the backend to create a new rule.</li>
                <li><strong>View Existing Rules:</strong> Display existing rules in a card format when the page loads.</li>
                <li><strong>Update Rules:</strong> Modify and update rules using an editable form.</li>
                <li><strong>Delete Rules:</strong> Remove rules using a delete button on each rule card.</li>
                <li><strong>Evaluate Rules:</strong> Evaluate a rule by providing user data, and get a result (True/False) based on whether the data matches the rule.</li>
            </ul>
        </div>

        <div class="section">
            <h2>Abstract Syntax Tree (AST)</h2>
            <p>The key components of the AST implementation include:</p>
            <ul>
                <li><strong>Node Class:</strong> Represents nodes in the AST with properties for type, value, and child nodes.</li>
                <li><strong>create_rule Function:</strong> Parses a rule string (e.g., <code>"age &gt; 30 AND department = 'Sales'"</code>) to create an AST.</li>
                <li><strong>combine_rules Function:</strong> Combines multiple ASTs into a single AST using a specified operator (default is "AND").</li>
                <li><strong>evaluate_rule Function:</strong> Evaluates the AST against user data, returning a boolean result and detailed logs of the evaluation process.</li>
                <li><strong>from_dict_to_node Function:</strong> Converts a dictionary representation of a node back into a Node object.</li>
            </ul>
        </div>

    </div>

</body>
</html>
