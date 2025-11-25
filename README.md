<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Connexion</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
            
            background-image: url('https://i.pinimg.com/736x/8c/df/3c/8cdf3c53ca5d2bd0103cb3bfe2ac14a6.jpg'); /* REMPLACEZ PAR VOTRE CHEMIN/URL */
            background-size: cover; /* Assurez-vous que l'image couvre toute la zone */
            background-position: center; /* Centre l'image */
            background-repeat: no-repeat;



        }

        .login-box {
            width: 350px;
            padding: 30px;
            border-radius: 15px;
            background: rgba(0,0,0,0.35);
            backdrop-filter: blur(10px);
            color: white;
            text-align: center;
        }

        .login-box h2 {
            margin-bottom: 25px;
        }

        .input-box {
            display: flex;
            align-items: center;
            background: rgba(255,255,255,0.1);
            border-radius: 30px;
            padding: 12px 15px;
            margin-bottom: 15px;
        }

        .input-box input {
            width: 100%;
            border: none;
            background: transparent;
            color: white;
            outline: none;
            margin-left: 10px;
        }

        button {
            width: 100%;
            padding: 12px;
            margin-top: 10px;
            background: white;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            font-weight: bold;
        }

        .links {
            margin-top: 10px;
            font-size: 14px;
        }

        .links a {
            color: #ccc;
            text-decoration: none;
        }

        .links a:hover {
            text-decoration: underline;
        }
    </style>
</head>

<body>
    <div class="login-box">
        <h2>Connexion</h2>

        <div class="input-box">
            <span>👤</span>
            <input type="text" placeholder="Nom d'utilisateur">
        </div>

        <div class="input-box">
            <span>🔒</span>
            <input type="password" placeholder="Mot de passe">
        </div>

        <label style="font-size:14px;">
            <input type="checkbox"> Se souvenir de moi
        </label>

        <p class="links">
            <a href="#">Mot de passe oublié ?</a>
        </p>

        <button>Connexion</button>

        <p class="links">
            Vous n’avez pas de compte ? <a href="#">Inscrivez-vous</a>
        </p>
    </div>
</body>
</html>
