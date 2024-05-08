<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Forma</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h2>Forma</h2>
        <form id="myForm">
            <label for="name">Vārds:</label><br>
            <input type="text" id="name" name="name"><br>
            <label for="email">E-pasts:</label><br>
            <input type="email" id="email" name="email"><br><br>
            <input type="submit" value="Nosūtīt">
        </form>
    </div>
</body>
</html> 
.container {
    width: 50%;
    margin: auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

input[type="text"],
input[type="email"],
input[type="submit"] {
    width: 100%;
    padding: 12px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

input[type="submit"] {
    background-color: #4CAF50;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
{
    "vielas": [
        {"id": 1, "nosaukums": "Viela 1"},
        {"id": 2, "nosaukums": "Viela 2"},
        {"id": 3, "nosaukums": "Viela 3"}
    ]
}
