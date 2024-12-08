# Ex.05 Design a Website for Server Side Processing
# Date:
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 300px;
        }

        h1 {
            text-align: center;
            margin-bottom: 20px;
        }

        .input-group {
            margin-bottom: 10px;
        }

        label {
            display: block;
            font-size: 14px;
            margin-bottom: 5px;
        }

        input {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #218838;
        }

        .result {
            text-align: center;
            font-size: 18px;
            font-weight: bold;
            margin-top: 20px;
        }
    </style>
</head>
<body style="background-color: rgb(212, 230, 173);">
    <div class="container">
        <h1>Lamp Power Calculator</h1>
        <form id="lampPowerForm">
            <div class="input-group">
                <label for="intensity">Intensity (I in Amperes):</label>
                <input type="number" id="intensity" placeholder="Enter Intensity" required>
            </div>
            <div class="input-group">
                <label for="resistance">Resistance (R in Ohms):</label>
                <input type="number" id="resistance" placeholder="Enter Resistance" required>
            </div>
            <button type="button" onclick="calculatePower()">Calculate Power</button>
        </form>
        <div class="result" id="result"></div>
    </div>

    <script>
        function calculatePower() {
            const intensity = parseFloat(document.getElementById('intensity').value);
            const resistance = parseFloat(document.getElementById('resistance').value);
            const resultElement = document.getElementById('result');

            if (isNaN(intensity) || isNaN(resistance)) {
                resultElement.textContent = "Please enter valid numbers for both Intensity and Resistance.";
                return;
            }

            // Calculate Power (P = I^2 * R)
            const power = Math.pow(intensity, 2) * resistance;
            resultElement.textContent = `Calculated Power: ${power.toFixed(2)} Watts`;
        }
    </script>
</body>
</html>

```
# SERVER SIDE PROCESSING:
# HOMEPAGE:
![image](https://github.com/user-attachments/assets/2aafa85e-100b-4686-b43d-a99ceb9ef05e)

# RESULT:
The program for performing server side processing is completed successfully.
