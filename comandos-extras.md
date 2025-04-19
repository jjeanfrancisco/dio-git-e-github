🔍 Comandos para Comparação e Diferenças (git diff)
Ver alterações não adicionadas (working directory vs. staging area):

bash
git diff
Ver alterações adicionadas (staging area vs. último commit):

bash
git diff --staged
Comparar entre dois branches:

bash
git diff branch1..branch2
Ver diferenças em um arquivo específico:

bash
git diff arquivo.txt
Comparar com um commit antigo (usando hash do commit):

bash
git diff abc1234..HEAD
🕰️ Comandos para Histórico e Logs Avançados
Ver histórico com gráfico de branches:

bash
git log --oneline --graph --all
Filtrar commits por autor:

bash
git log --author="Nome"
Buscar commits por mensagem:

bash
git log --grep="bugfix"
Ver alterações de um commit específico:

bash
git show abc1234
🔄 Comandos para Trabalho com Remotos (GitHub/GitLab)
Listar repositórios remotos:

bash
git remote -v
Renomear um remote:

bash
git remote rename origin novo-nome
Atualizar branch local com o remoto (fetch + merge):

bash
git pull --rebase origin main  # Evita commits de merge desnecessários
Forçar push (use com cautela!):

bash
git push --force origin main
🛠️ Comandos para Resolver Conflitos
Abortar um merge em conflito:

bash
git merge --abort
Usar uma versão específica de um arquivo (durante conflitos):

bash
git checkout --ours arquivo.txt    # Usa a sua versão
git checkout --theirs arquivo.txt  # Usa a versão do remoto
Adicionar arquivo resolvido após conflito:

bash
git add arquivo.txt
git commit  # Finaliza o merge
🧹 Comandos para Limpeza e Otimização
Limpar arquivos não rastreados:

bash
git clean -n  # Simulação (mostra o que será removido)
git clean -f  # Remove arquivos de verdade
Compactar o repositório (gc = garbage collector):

bash
git gc
Listar arquivos ignorados:

bash
git ls-files --others --ignored --exclude-standard
🌟 Extras Úteis
Criar um alias para comandos frequentes:

bash
git config --global alias.lg "log --oneline --graph --all"
Depois use:

bash
git lg
Ver quem modificou uma linha de código (blame):

bash
git blame arquivo.txt -L 10,20  # Linhas 10 a 20
Recuperar um arquivo deletado:

bash
git checkout abc1234 -- arquivo.txt  # Restaura do commit abc1234
📌 Exemplo Prático com git diff
bash
# Comparar mudanças entre o último commit e o working directory:
git diff HEAD

# Ver diferenças entre dois commits específicos:
git diff abc1234 def5678 -- estatisticas.txt
🎯 Quando Usar?
git diff: Ideal para revisar alterações antes de commitar.

git log --graph: Para entender o histórico de branches.

git blame: Para rastrear bugs em códigos herdados.