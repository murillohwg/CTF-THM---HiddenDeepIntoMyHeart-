🔐 Hidden Deep Into My Heart - Writeup

Write-up do desafio da plataforma TryHackMe focado em enumeração web e análise de informações expostas.

📌 Informações do Desafio
Plataforma: TryHackMe
Nome: Hidden Deep Into My Heart
Categoria: Web
Dificuldade: Easy/Medium
Objetivo: Obter a flag explorando a aplicação web
🧠 Metodologia

A abordagem utilizada seguiu uma metodologia clássica de pentest:

Reconhecimento
Enumeração
Análise de arquivos expostos
Descoberta de credenciais
Exploração e obtenção da flag
🌐 Reconhecimento

Após conectar à VPN da plataforma, foi possível acessar o alvo através do endereço IP fornecido.

🔍 Enumeração

Foi utilizada a ferramenta gobuster para realizar brute force de diretórios e arquivos:

gobuster dir -u http://IP:PORT/ \
-w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt \
-x txt,bak,zip
📄 Descoberta do robots.txt

Durante a enumeração, foi identificado o arquivo:

/robots.txt

Este arquivo continha informações sensíveis que foram utilizadas posteriormente como credenciais.

📂 Descoberta do Painel Administrativo

Uma nova enumeração revelou o diretório:

/administrator

Ao acessá-lo, foi apresentada uma página de login.

🔐 Exploração

Utilizando as informações obtidas:

Usuário: admin
Senha: encontrada no robots.txt

Foi possível realizar login com sucesso.

🏁 Flag

Após a autenticação, o sistema redirecionou diretamente para a página contendo a flag.

⚠️ Flag omitida para evitar spoilers.
