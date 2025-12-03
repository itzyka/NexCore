
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Login - TechStore</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0a0f1f, #111a33, #0d162b);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #ffffff;
        }

        .login-container {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            padding: 40px;
            width: 350px;
            border-radius: 20px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
        }

        .login-container h1 {
            margin-bottom: 20px;
            font-size: 26px;
            font-weight: 600;
            letter-spacing: 1px;
            color: #4da6ff;
        }

        .input-group {
            text-align: left;
            margin-bottom: 20px;
        }

        .input-group label {
            font-size: 14px;
            display: block;
            margin-bottom: 6px;
            color: #b8c6ff;
        }

        .input-group input {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: none;
            outline: none;
            font-size: 15px;
            background: rgba(255, 255, 255, 0.12);
            color: white;
            border: 1px solid transparent;
            transition: 0.3s;
        }

        .input-group input:focus {
            border: 1px solid #4da6ff;
        }

        .btn-login {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            background: #1a73e8;
            color: white;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-login:hover {
            background: #4da6ff;
        }

        .footer-text {
            margin-top: 18px;
            font-size: 13px;
            color: #8899cc;
        }

        .footer-text a {
            color: #4da6ff;
            text-decoration: none;
        }

        .footer-text a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h1>NexCore Login</h1>

        <div class="input-group">
            <label for="usuario">Usuario:</label>
            <input type="text" id="usuario" placeholder="Ingresa tu usuario" />
        </div>

        <div class="input-group">
            <label for="password">Contraseña:</label>
            <input type="password" id="password" placeholder="Ingresa tu contraseña" />
        </div>

        <button class="btn-login">Iniciar Sesión</button>

        <p class="footer-text">¿No tienes cuenta? <a href="#">Regístrate aquí</a></p>
    </div>
    <script>
        const btn = document.querySelector('.btn-login');

        btn.addEventListener('click', () => {
            btn.innerHTML = 'Cargando...';
            btn.style.background = '#264d73';
            btn.disabled = true;

            setTimeout(() => {
                // Palomita de listo
                btn.innerHTML = '✔';
                btn.style.background = '#28a745';

                // Pantalla de bienvenida
                setTimeout(() => {
                    document.body.innerHTML = `
                        <div style="
                            width: 100%;
                            height: 100vh;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            flex-direction: column;
                            background: linear-gradient(135deg, #0a0f1f, #111a33, #0d162b);
                            color: white;
                            text-align: center;
                            font-family: 'Segoe UI', sans-serif;
                        ">
                            <h1 style="font-size: 45px; margin-bottom: 20px; color:#4da6ff;">¡Bienvenido!</h1>
                            <p style="font-size: 18px; width: 60%; color:#b8c6ff;">Preparando tu experiencia en NexCore...</p>
                        </div>
                    `;
                }, 900);

            }, 2000);
        });
    </script>
</body>
</html>
