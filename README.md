<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Registro - Mantenimiento de Computadoras</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f0f0f0;
            padding: 20px;
        }
        .container {
            max-width: 450px;
            margin: auto;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h2 {
            text-align: center;
        }
        label {
            font-weight: bold;
        }
        input, select {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .btn {
            width: 100%;
            padding: 12px;
            margin-top: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .btn.ingresar {
            background-color: #007bff;
            color: white;
        }
        .btn.continuar {
            background-color: #28a745;
            color: white;
        }
        .database-box {
            background: #eef;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
        }
        pre {
            background: #333;
            color: #fff;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Registro de Mantenimiento</h2>

        <label for="nombre">Nombre completo</label>
        <input type="text" id="nombre" placeholder="Ingrese su nombre" />

        <label for="correo">Correo electrónico</label>
        <input type="email" id="correo" placeholder="Ingrese su correo" />

        <label for="equipo">Tipo de equipo</label>
        <select id="equipo">
            <option>Laptop</option>
            <option>PC de Escritorio</option>
            <option>Todo en uno</option>
            <option>Otro</option>
        </select>

        <label for="fallas">Descripción de fallas</label>
        <input type="text" id="fallas" placeholder="Describa el problema" />

        <button class="btn ingresar">Ingresar</button>
        <button class="btn continuar">Continuar</button>

        <div class="database-box">
            <h3>Base de Datos (Ejemplo)</h3>
            <p>Este sería el modelo de tabla para guardar los registros:</p>
            <pre>
CREATE TABLE mantenimiento (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100),
    correo VARCHAR(100),
    equipo VARCHAR(50),
    fallas TEXT,
    fecha_registro TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
            </pre>
        </div>
    </div>
</body>
</html>
