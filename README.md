<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Données visibles – SNT</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Informations visibles par un site web</h1>

    <ul>
        <li id="ip">IP : chargement...</li>
        <li id="nav">Navigateur : chargement...</li>
        <li id="lang">Langue : chargement...</li>
        <li id="screen">Résolution écran : chargement...</li>
    </ul>

    <p style="color:gray;">
        Aucune donnée n’est enregistrée. Affichage uniquement.
    </p>

    <script>
        // IP publique
        fetch("https://api.ipify.org?format=json")
            .then(r => r.json())
            .then(d => {
                document.getElementById("ip").textContent =
                    "IP : " + d.ip;
            })
            .catch(() => {
                document.getElementById("ip").textContent =
                    "IP : non disponible";
            });

        // Navigateur
        document.getElementById("nav").textContent =
            "Navigateu
