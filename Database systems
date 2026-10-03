<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Database Systems Assignment</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f4f6f8;
            color: #222;
            line-height: 1.6;
        }

        header {
            background: #1f2937;
            color: white;
            text-align: center;
            padding: 35px 20px;
        }

        header h1 {
            margin-bottom: 8px;
        }

        main {
            width: 90%;
            max-width: 900px;
            margin: 30px auto;
        }

        .question {
            background: white;
            padding: 25px;
            margin-bottom: 25px;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }

        .question h2 {
            color: #2563eb;
            margin-bottom: 10px;
        }

        pre {
            background: #111827;
            color: #f9fafb;
            padding: 20px;
            margin: 15px 0;
            border-radius: 8px;
            overflow-x: auto;
        }

        code {
            font-family: Consolas, monospace;
        }

        button {
            background: #2563eb;
            color: white;
            border: none;
            padding: 10px 18px;
            border-radius: 6px;
            cursor: pointer;
        }

        button:hover {
            background: #1d4ed8;
        }

        footer {
            text-align: center;
            padding: 25px;
            background: #1f2937;
            color: white;
            margin-top: 40px;
        }

        @media (max-width: 600px) {
            main {
                width: 95%;
            }

            .question {
                padding: 18px;
            }

            pre {
                font-size: 13px;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>Database Systems Assignment</h1>
        <p>SQL Queries and Aggregate Functions</p>
    </header>

    <main>

        <!-- QUESTION 1 -->
        <section class="question">
            <h2>Question 1</h2>

            <p>
                Show the total payment amount for each payment date,
                sorted by the latest payment dates and display only 5 records.
            </p>

            <pre><code>
SELECT
    paymentDate,
    SUM(amount) AS total_amount
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;
            </code></pre>

            <button onclick="copyCode(this)">
                Copy Code
            </button>
        </section>


        <!-- QUESTION 2 -->
        <section class="question">
            <h2>Question 2</h2>

            <p>
                Find the average credit limit of each customer.
            </p>

            <pre><code>
SELECT
    customerName,
    country,
    AVG(creditLimit) AS average_credit_limit
FROM customers
GROUP BY customerName, country;
            </code></pre>

            <button onclick="copyCode(this)">
                Copy Code
            </button>
        </section>


        <!-- QUESTION 3 -->
        <section class="question">
            <h2>Question 3</h2>

            <p>
                Find the total price of products ordered.
            </p>

            <pre><code>
SELECT
    productCode,
    quantityOrdered,
    SUM(quantityOrdered * priceEach) AS total_price
FROM orderdetails
GROUP BY productCode, quantityOrdered;
            </code></pre>

            <button onclick="copyCode(this)">
                Copy Code
            </button>
        </section>


        <!-- QUESTION 4 -->
        <section class="question">
            <h2>Question 4</h2>

            <p>
                Find the highest payment amount for each check number.
            </p>

            <pre><code>
SELECT
    checkNumber,
    MAX(amount) AS highest_amount
FROM payments
GROUP BY checkNumber;
            </code></pre>

            <button onclick="copyCode(this)">
                Copy Code
            </button>
        </section>

    </main>


    <footer>
        <p>Database Systems Assignment</p>
        <p>Power Learn Project</p>
    </footer>


    <script>
        function copyCode(button) {

            const code = button
                .parentElement
                .querySelector("code")
                .innerText;

            navigator.clipboard.writeText(code);

            button.innerText = "Copied!";

            setTimeout(function() {
                button.innerText = "Copy Code";
            }, 1500);
        }
    </script>

</body>
</html>
