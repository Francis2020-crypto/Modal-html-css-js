# Modal-html-css-js
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Modal 3</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 100px;
    }

    /* Estilos del fondo del modal */
    #miModal {
      display: none;
      position: fixed;
      z-index: 1;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0, 0, 0, 0.5);
    }

    /* Contenido del modal */
    .contenido-modal {
      background-color: #fff;
      margin: 15% auto;
      padding: 20px;
      border: 1px solid #888;
      width: 80%;
      max-width: 400px;
      border-radius: 10px;
    }

    /* Botón cerrar */
    .cerrar {
      color: #aaa;
      float: right;
      font-size: 28px;
      font-weight: bold;
      cursor: pointer;
    }

    .cerrar:hover {
      color: black;
    }
  </style>
</head>
<body>

  <h1>¡Hola!</h1>
  <p>Presiona el botón para ver el modal.</p>

  <button onclick="mostrarModal()">Mostrar Modal</button>

  <!-- Estructura del modal -->
  <div id="miModal">
    <div class="contenido-modal">
      <span class="cerrar" onclick="cerrarModal()">&times;</span>
      <h2>Este es el Modal 3</h2>
      <p>¡Funciona perfecto!</p>
    </div>
  </div>

  <script>
    function mostrarModal() {
      document.getElementById("miModal").style.display = "block";
    }

    function cerrarModal() {
      document.getElementById("miModal").style.display = "none";
    }

    // Cerrar si el usuario hace clic fuera del modal
    window.onclick = function(event) {
      const modal = document.getElementById("miModal");
      if (event.target == modal) {
        modal.style.display = "none";
      }
    }
  </script>

</body>
</html>
