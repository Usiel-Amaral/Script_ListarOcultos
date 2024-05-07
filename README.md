# Script_ListarOcultos
lista arquivos e diretórios ocultos no linux, em shell script.

Como usar o script:
    Salve o script com um nome, por exemplo, listar_ocultos.sh.
    Dê permissão de execução ao script: chmod +x listar_ocultos.sh
    Execute o script passando o diretório que deseja listar como argumento: ./listar_ocultos.sh /home/usuario/Documentos

Explicação do script:
    #!/bin/bash: Indica que o script deve ser executado com o interpretador Bash.

    if [ -z &quot;$1&quot; ]: Verifica se o primeiro argumento ($1) está vazio. Se estiver, significa que o usuário não passou um diretório e o script exibe uma mensagem de uso.

    if [ ! -d &quot;$1&quot; ]: Verifica se o diretório passado como argumento existe. Se não existir, o script exibe uma mensagem de erro.

    find &quot;$1&quot; -type d -name &quot;.*&quot; -print: Usa o comando find para procurar por diretórios ( -type d) cujo nome começa com "." ( -name &quot;.*&quot;) dentro do diretório passado como argumento e imprime ( -print) os resultados.

    find &quot;$1&quot; -type f -name &quot;.*&quot; -print: Usa o comando find para procurar por arquivos ( -type f) cujo nome começa com "." ( -name &quot;.*&quot;) dentro do diretório passado como argumento e imprime ( -print) os resultados.
