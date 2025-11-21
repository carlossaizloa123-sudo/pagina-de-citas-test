<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Página de Citas - Gratis</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css">
</head>
<body class="bg-gray-50 text-gray-800">
  <header class="bg-white shadow p-4">
    <h1 class="text-2xl font-bold text-center">Citas Online</h1>
  </header>

  <main class="max-w-3xl mx-auto mt-8 p-4">
    <section class="bg-white shadow rounded-xl p-6">
      <h2 class="text-xl font-semibold">Agenda tu cita</h2>
      <p class="text-gray-600 mt-2">Completa el formulario para registrar una cita.</p>

      <form class="mt-4 space-y-4" onsubmit="event.preventDefault(); mostrarConfirmacion();">
        <div>
          <label class="block text-sm font-medium">Nombre completo</label>
          <input type="text" id="nombre" class="w-full p-2 border rounded-lg" required />
        </div>

        <div>
          <label class="block text-sm font-medium">Fecha de la cita</label>
          <input type="date" id="fecha" class="w-full p-2 border rounded-lg" required />
        </div>

        <div>
          <label class="block text-sm font-medium">Hora</label>
          <input type="time" id="hora" class="w-full p-2 border rounded-lg" required />
        </div>

        <div>
          <label class="block text-sm font-medium">Motivo</label>
          <textarea id="motivo" class="w-full p-2 border rounded-lg" rows="3" required></textarea>
        </div>

        <button type="submit" class="w-full bg-indigo-600 text-white py-2 rounded-lg hover:bg-indigo-700 transition">Registrar cita</button>
      </form>
    </section>

    <section id="confirmacion" class="hidden mt-6 bg-green-100 border border-green-300 text-green-800 p-4 rounded-lg">
      <strong>¡Cita registrada!</strong> Gracias, tu cita ha sido guardada.
    </section>
  </main>

  <script>
    function mostrarConfirmacion() {
      document.getElementById('confirmacion').classList.remove('hidden');
      document.getElementById('confirmacion').scrollIntoView({ behavior: 'smooth' });
    }
  </script>
</body>
</html>

