<h1>Desafio mi banco</h1>

<p>Este proyecto implementa un sistema bancario simple a través de una interfaz de línea de comandos (CLI) utilizando Node.js y PostgreSQL. Permite realizar diferentes tipos de transacciones bancarias, como consultas de saldo y transferencias entre cuentas.</p>

<h2>Configuración</h2>

<h3>Instalación de dependencias</h3>

<p>Asegúrate de tener Node.js y PostgreSQL instalados en tu sistema. Luego, instala las dependencias del proyecto utilizando npm:</p>

<pre><code>npm install
</code></pre>

<h3>Configuración de la base de datos</h3>

<p>Antes de ejecutar el programa, asegúrate de tener una base de datos PostgreSQL configurada y operativa. Debes crear una base de datos llamada "banco" y ejecutar el script SQL proporcionado en <code>baseDeDatos.sql</code> para crear las tablas necesarias y realizar algunas inserciones de prueba.</p>

<pre><code>psql -U tu_usuario -f baseDeDatos.sql banco
</code></pre>

<h3>Configuración de variables de entorno</h3>

<p>Crea un archivo <code>.env</code> en la raíz del proyecto y configura las variables de entorno necesarias para la conexión a la base de datos:</p>

<pre><code>DB_USER=tu_usuario
DB_PASSWORD=tu_contraseña
DB_HOST=localhost
</code></pre>

<h2>Uso</h2>

<p>El programa se ejecuta a travez de la terminal y acepta diferentes tipos de transacciones bancarias como argumentos. A continuación se muestran algunos ejemplos de uso:</p>

<pre><code>node index.js nueva 1 '2024-04-24' 'Transferencia de prueba' 100 2
</code></pre>

<p>Realiza una nueva transferencia de $100 desde la cuenta 1 a la cuenta 2 con la fecha de hoy.</p>

<pre><code>node index.js consulta-saldo 1
</code></pre>

<p>Consulta el saldo de la cuenta 1.</p>

<pre><code>node index.js consulta 1
</code></pre>

<p>Consulta las últimas 10 transferencias de la cuenta 1.</p>

<h2>Estructura del proyecto</h2>

<ul>
  <li><strong>bdConfig.js:</strong> Configuración de la conexión a la base de datos.</li>
  <li><strong>consultas.js:</strong> Funciones para realizar consultas de saldo y transferencias.</li>
  <li><strong>transacciones.js:</strong> Función para realizar una nueva transferencia.</li>
  <li><strong>index.js:</strong> Punto de entrada del programa.</li>
</ul>

