📌 Configuração Inicial
Configurar usuário (nome e email):

bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
Verificar configurações:

bash
git config --list
📂 Repositório Local
Iniciar um repositório Git:

bash
git init
Verificar status dos arquivos:

bash
git status
Adicionar arquivos ao staging area:

bash
git add nome_do_arquivo      # Adiciona um arquivo específico
git add .                    # Adiciona TODOS os arquivos modificados
Commit (salvar alterações):

bash
git commit -m "Mensagem descritiva do commit"
Ver histórico de commits:

bash
git log
git log --oneline            # Versão resumida
🔄 Repositório Remoto (GitHub)
Conectar repositório local a um remoto:

bash
git remote add origin https://github.com/seu-usuario/repositorio.git
Enviar commits para o GitHub:

bash
git push -u origin main      # Primeiro push (defina o branch principal)
git push                     # Push após o primeiro
Clonar um repositório existente:

bash
git clone https://github.com/seu-usuario/repositorio.git
Atualizar repositório local com alterações remotas:

bash
git pull origin main
🌿 Branches (Ramificações)
Criar um novo branch:

bash
git checkout -b nome-do-branch
Listar branches:

bash
git branch
Mudar de branch:

bash
git checkout nome-do-branch
Mesclar branches:

bash
git merge nome-do-branch    # Mescla o branch atual com outro
Deletar branch:

bash
git branch -d nome-do-branch
⚠️ Correções e Emergências
Desfazer alterações antes do commit:

bash
git restore nome_do_arquivo  # Descarta modificações não adicionadas
Desfazer um commit (mantendo alterações):

bash
git reset --soft HEAD~1
Desfazer um commit (perde alterações):

bash
git reset --hard HEAD~1
Corrigir mensagem do último commit:

bash
git commit --amend -m "Nova mensagem"
📊 Extras Úteis
Ver diferenças entre arquivos:

bash
git diff
Ignorar arquivos (.gitignore):
Crie um arquivo .gitignore e liste pastas/arquivos que não devem ser rastreados (ex: node_modules/, .env).

Salvar temporariamente alterações:

bash
git stash                   # Guarda alterações não commitadas
git stash pop               # Recupera alterações
📌 Dica Final
Sempre use git status para verificar o estado do seu repositório antes de executar comandos críticos (como reset ou merge).