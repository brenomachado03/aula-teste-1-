<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sistema de Login</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    }

    body {
      background: linear-gradient(135deg, #1f2937, #111827);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1rem;
    }

    .login-card {
      background: #ffffff;
      padding: 2.5rem 2rem;
      border-radius: 12px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
      width: 100%;
      max-width: 380px;
    }

    .login-card h2 {
      margin-bottom: 0.5rem;
      color: #111827;
      text-align: center;
    }

    .login-card p.subtitle {
      color: #6b7280;
      font-size: 0.9rem;
      text-align: center;
      margin-bottom: 1.5rem;
    }

    .form-group {
      margin-bottom: 1.25rem;
    }

    .form-group label {
      display: block;
      font-size: 0.875rem;
      font-weight: 600;
      color: #374151;
      margin-bottom: 0.4rem;
    }

    .form-group input {
      width: 100%;
      padding: 0.75rem 1rem;
      border: 1px solid #d1d5db;
      border-radius: 8px;
      font-size: 0.95rem;
      outline: none;
      transition: border-color 0.2s, box-shadow 0.2s;
    }

    .form-group input:focus {
      border-color: #2563eb;
      box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.2);
    }

    button.btn-submit {
      width: 100%;
      background: #2563eb;
      color: white;
      border: none;
      padding: 0.75rem;
      border-radius: 8px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      transition: background 0.2s;
      margin-top: 0.5rem;
    }

    button.btn-submit:hover {
      background: #1d4ed8;
    }

    /* Mensagens de feedback */
    .message {
      margin-top: 1.25rem;
      padding: 0.75rem;
      border-radius: 8px;
      font-size: 0.9rem;
      text-align: center;
      display: none;
    }

    .message.error {
      display: block;
      background: #fee2e2;
      color: #991b1b;
      border: 1px solid #f87171;
    }

    .message.success {
      display: block;
      background: #dcfce7;
      color: #166534;
      border: 1px solid #4ade80;
    }
  </style>
</head>
<body>

  <main class="login-card">
    <h2>Acesso ao Sistema</h2>
    <p class="subtitle">Insira suas credenciais abaixo</p>

    <form id="loginForm">
      <div class="form-group">
        <label for="username">Usuário</label>
        <input 
          type="text" 
          id="username" 
          placeholder="Digite o usuário" 
          required 
          autocomplete="off"
        />
      </div>

      <div class="form-group">
        <label for="password">Senha</label>
        <input 
          type="password" 
          id="password" 
          placeholder="Digite a senha" 
          required 
        />
      </div>

      <button type="submit" class="btn-submit">Entrar</button>

      <!-- Área de exibição de status -->
      <div id="feedbackMessage" class="message"></div>
    </form>
  </main>

  <script>
    const form = document.getElementById('loginForm');
    const userInput = document.getElementById('username');
    const passInput = document.getElementById('password');
    const feedback = document.getElementById('feedbackMessage');

    form.addEventListener('submit', function (event) {
      event.preventDefault(); // Evita recarregar a página

      const user = userInput.value.trim();
      const pass = passInput.value.trim();

      // Regra: usuário e senha devem ser "123456"
      if (user === '123456' && pass === '123456') {
        feedback.className = 'message success';
        feedback.textContent = '✅ Acesso liberado! Login realizado com sucesso.';
        
        // Limpa a senha após o sucesso
        passInput.value = '';
      } else {
        feedback.className = 'message error';
        feedback.textContent = '❌ Usuário ou senha incorretos. Tente novamente.';
      }
    });
  </script>
</body>
</html>
