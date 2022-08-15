# dio-desafio-github
Comandos básicos de git para cada situação

(MOVIMENTAR ENTRE PASTAS)
cd .. = volta uma pasta
cd <nome da pasta> = vai até a pasta específica se a mesma estiver contida na pasta atual
cd = volta todas as pastas
  
(CRIAR REPOSITÓRIO GIT)
 1. se mover até a pasta onde será criada o repositório git com o comando CD
 2. escrever git init e dar enter (pasta oculta .git é criada)
 3. caso queira criar alguma pasta/repositório, usar o comando mkdir <nome do repositório>
  
 (LINKAR PROJETO COM UM REPOSITPORIO REMOTO)
  1. criar o repositório no github (ou em qualquer outro serviço usado para a mesma finalidade)
  2. copiar o endereço HTTPS ou SSH 
  3. escrever o comando git remote add origin <endereço do passo 2>
  4. git remote -v (para checar se está tudo certo)
  5. git branch -M "main" (mudar da branch master para a main)
  6. git push origin main

(SUBIR PROJETOS PARA UM REPOSITORIO GIT)
  1. criar repositório git na máquina (git init)
  2. adicionar os arquivos que irão para o github (git add <nome do arquivo>)
  3. escrever a mensagem de commit (git commit -m "mensagem desejada")
  4. criar/trocar para a branch "main" (git branch -M main)
  5. escrever o link para onde os arquivos serão direcionados (git remote add origin HTTPS/SSH)
  6. subir os arquivos (git push origin main)
  
  (CRIAR NOVA BRANCH)
  1. git branch <nome da branch a ser criada>
  1.1. ou git branch -b <nome da branch a ser criada>
  2. git checkout <nome da branch criada> (para trocar para a branch desejada)
  3. git branch -d <nome da branch a ser deletada>
  
  (CHAVE SSH E AGENTE SSH)
  1. comanda ssh-keygen -t ed25519 -C "seuemailgit@exemplo.com"
  2. aceitar local padrão para salvar as chaves
  3. criar senha ou não
  4. navegar até a pasta onde as pastas estão salvas com o comando 'cd'
  5. comando cat "id_chave.pub"
  6. copiar output do passo 5 e colar no github
  7. comando "eval $(ssh-agent -s)" -> será gerado um Agent pid
  8. comando "ssh-add id_chave privada"
  9. digitar senha git
  
  (CONFLITOS DE MERGE)
  1. git pull
  2. resolver o conflito na sua máquina
  3. git add <arquivo de conflito resolvido>
  4. git commit -m "mensagem explicativa"
  5. git push origin <nome da branch de onde foi feito o commit>
  
  (LISTA DE COMMITS FEITOS)
  1. git log (existem várias configurações para se ver de diferentes formas essa lista) ex: git log --oneline (mostra a lista de cada commit em uma linha)
  
  (COMANDOS GENÉRICOS - WINDOWS)
  1. ls = lista os arquivos dentro de uma pasta (ls -a para arquivos ocultos como o .git)
  2. git config --(global/local) user.(name/email) (configura para apenas aquele projeto "LOCAL" ou para todos os outros "GLOBAL", o nome "user.name" ou o email "user.email" que irá aparecer nos commits)
  3. git clone <endereço https ou ssh do repositório a ser clonado>
  4. git status (mostra as mudanças de arquivo no diretório atual)
  5. git add . (adiciona todos os arquivo do diretório)
  6. git pull origin master (baixa todas as mudanças da origin)
  
