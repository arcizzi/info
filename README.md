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
            <label for="selectVielas">Izvēlies vielu:</label><br>
            <select id="selectVielas" name="selectVielas"></select><br><br>
            <input type="submit" value="Nosūtīt">
        </form>
    </div>
    <script src="script.js"></script>
</body>
</html>
document.addEventListener("DOMContentLoaded", function() {
    // Ielādējam vielu sarakstu no JSON faila
    fetch('vielas.json')
        .then(response => response.json())
        .then(data => {
            // Atrodam select elementu
            const selectVielas = document.getElementById('selectVielas');
            // Pārklājam vielu sarakstu
            data.vielas.forEach(viela => {
                // Izveidojam option elementu
                const option = document.createElement('option');
                // Uzstādām vērtību un tekstu
                option.value = vielas.id;
                option.text = vielas.nosaukums;
                // Pievienojam option elementu select elementam
                selectVielas.appendChild(option);
            });
        })
        .catch(error => console.error('Kļūda:', error));
});
