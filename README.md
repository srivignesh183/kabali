<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kabali Holiday Planning</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background-color: #333;
            color: white;
            line-height: 1.6;
        }

        header {
            text-align: center;
            padding: 20px;
            background-color: #ff4500;
        }

        header h1 {
            font-size: 2.5rem;
        }

        header p {
            font-size: 1.2rem;
        }

        main {
            padding: 20px;
            text-align: center;
        }

        .form-container {
            margin: 0 auto;
            max-width: 400px;
            background-color: #444;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .form-container label {
            display: block;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .form-container input {
            width: 100%;
            padding: 8px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }

        button {
            background-color: #ff4500;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1.1rem;
        }

        button:hover {
            background-color: #e03e00;
        }

        .plan-container {
            margin-top: 30px;
            padding: 20px;
            background-color: #444;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        #planDetails p {
            font-size: 1.2rem;
            margin: 10px 0;
        }

        footer {
            text-align: center;
            padding: 10px;
            background-color: #222;
            margin-top: 30px;
        }

        .price-details {
            background-color: #666;
            padding: 15px;
            margin-top: 20px;
            border-radius: 8px;
        }

        .contact-details {
            margin-top: 20px;
            font-size: 1.1rem;
            padding: 10px;
            background-color: #666;
            border-radius: 8px;
        }

    </style>
</head>
<body>
    <header>
        <h1>Plan Your Kabali-Themed Holiday!</h1>
        <p>Enter your holiday details to plan your best Kabali adventure!</p>
    </header>
    <main>
        <div class="form-container">
            <label for="name">Enter Your Name:</label>
            <input type="text" id="name" placeholder="Your Name">

            <label for="destination">Destination:</label>
            <input type="text" id="destination" placeholder="Where do you want to go?">

            <label for="date">Holiday Date:</label>
            <input type="date" id="date">

            <label for="price">Holiday Price:</label>
            <input type="number" id="price" placeholder="Enter price in USD" min="0">

            <button onclick="generatePlan()">Generate Kabali Plan</button>
        </div>

        <div class="plan-container">
            <h2>Your Kabali Holiday Plan</h2>
            <div id="planDetails">
                <p id="nameDisplay"></p>
                <p id="destinationDisplay"></p>
                <p id="dateDisplay"></p>
                <p id="priceDisplay"></p>
            </div>
        </div>

        <div class="price-details">
            <h3>Price Breakdown</h3>
            <ul>
                <li><strong>Holiday Package:</strong> $<span id="packagePrice">0</span></li>
                <li><strong>Additional Costs:</strong> $<span id="additionalCost">50</span></li>
                <li><strong>Total Price:</strong> $<span id="totalPrice">50</span></li>
            </ul>
        </div>

        <div class="contact-details">
            <h3>Contact Details:</h3>
            <p>If you have any questions, please contact us:</p>
            <p>Email: kabali@holidays.com</p>
            <p>Phone: +1 800 123 4567</p>
        </div>
    </main>
    <footer>
        <p>&copy; 2025 Kabali Holiday Planner. All Rights Reserved.</p>
    </footer>

    <script>
        function generatePlan() {
            var name = document.getElementById("name").value;
            var destination = document.getElementById("destination").value;
            var date = document.getElementById("date").value;
            var price = document.getElementById("price").value;

            if (name === "" || destination === "" || date === "" || price === "") {
                alert("Please fill out all fields to generate your Kabali plan!");
                return;
            }

            document.getElementById("nameDisplay").innerHTML = "<strong>Holiday Planner Name:</strong> " + name;
            document.getElementById("destinationDisplay").innerHTML = "<strong>Destination:</strong> " + destination;
            document.getElementById("dateDisplay").innerHTML = "<strong>Holiday Date:</strong> " + date;
            document.getElementById("priceDisplay").innerHTML = "<strong>Holiday Price:</strong> $" + price;

            // Calculate total price (adding some fixed additional costs)
            var additionalCosts = 50;  // Fixed additional cost for the holiday
            var totalPrice = parseFloat(price) + additionalCosts;

            document.getElementById("packagePrice").innerText = price;
            document.getElementById("additionalCost").innerText = additionalCosts;
            document.getElementById("totalPrice").innerText = totalPrice;

            alert("Kabali Holiday Plan Generated! Ready to rock 'n roll!");
        }
    </script>
</body>
</html>
