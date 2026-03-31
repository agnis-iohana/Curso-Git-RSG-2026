# Curso-Git-RSG-2026
Repositorio para aula prática curso de Git RSG Brazil 2026

## Como instalar o Git
Instale o Git no seu terminal. Pode ser instalado tanto em Windows quanto no Linux.
1) Linux:
basta atualizar o sistema, conforme os comandos abaixo (Para distro Ubuntu).

```/bin/bash
sudo apt update
sudo apt install git
```
Para outras distros, acesse o [site](https://git-scm.com/install/linux).

2) Windows:
é facilmente instalável através de download do [site](https://git-scm.com/install/windows).

3) Mac:
pode ser instalado via Xcode, homebrew, MacPorts ou com o download de instalador binário, semelhante ao Windows. Bsata acessar [aqui](https://git-scm.com/install/mac)

## Iniciando um projeto
1) Crie uma conta no GitHub e abra um repositório, acessando "repositories" e clicando em "New" (botão verde). Faça as configurações desejadas. Depois, clone seu repositório em uma pasta local com o comando de exemplo abaixo:

```/bin/bash
git clone https://github.com/agnis-iohana/Curso-Git-RSG-2026.git .
```

> [!IMPORTANT]
> Talvez seja necessário configurar seu acesso com um token e/ou configurar o usuário. Para configuração do usuário, realize o comando abaixo:
> ```/bi/bash
> git config --global user.name <nome-do-usuario-github>
> git config --global user.email <email-que-usei-para-o-github>
> ```
>
> Se configurar e não conseguir clonar, então configure seus tokens de acesso em "settings" -> "developer settings -> "Personal access tokens" -> "Generate new token" -> selecione escopos -> Generate token -> copie o token e cole em bloco de notas -> cole na autenticação de senha.

2) Crie uma nova branch dentro do gitHub ou localmente.
Para criar a nova branch no GitHub, acesse "Branches" e clique em "New Branch". No seu repositório local, realize os comandos abaixo:

```/bin/bash
git fetch
git checkout new-branch
```
> [!NOTE]
> O comando fetch atualiza seu repositório local, trazendo a nova branch para que possa ser acessada.

Caso queira criar sua branch localmente, basta acrescentar a flag -b no seu comando de checkout, conforme abaixo:

```/bin/bash
git checkout -b new-branch
```
Esse comando cria a branch e realiza a troca da main para a branch recém criada.

3) Após acessar a nova branch, trabalhe com seus documentos, scripts e etc.

## Realizando commits
O commit é uma forma de documentar as alterações realizadas dentro do repositório. Para verificar quais arquivos foram modificados (deletados, alterados ou acrescentados), você pode acessar o status da chamada "staging area" com o comando *git status*.
Após as modificações e verificação com o comando anterior, você pode adicionar os arquivos que deseja no seu index (ou staging area) para serem commitados, conforme comando abaixo:

```/bin/bash
git add my-file
# ou
git add .
```

> [!NOTE]
> Caso você queira adicionar todos os arquivos modificados para serem commitados, basta acrescentar o ponto conforme comando acima. Tome cuidado para ter certeza que são todos mesmo.

Caso você queira remover um arquivo da staging area, pode realizar o comando abaixo:

```
git restore --staged my-unnecessary-file
```
O comando *restore* remove o arquivo da staging area, evitando de ser commitado e enviado para o repositório online.

Feitas as conferências, agora é hora de documentar suas alterações. Para isso, basta realizar o comando abaixo:

```/bin/bash
git commit -m "My new commit"
# ou -a para documentar mais de um commit
git commit [-a/--all]
```
Para documentação, verificar o site [aqui](https://git-scm.com/docs/git-commit).

> [!WARNING]
> Apesar de não recomendado, é possível desfazer um commit com o comando *reset*. Tenha cuidado, pois pode modificar todo o log, inclusive apagando todo seu histórico e perda de todo o trabalho não commitado.

## Fazendo push para o repositório
Pronto, após *commitar*, chegou a hora de enviar as modificações para o repositório online (no nosso caso, o GitHub). Para isso, basta realizar o comando de *push*, conforme abaixo:

```/bin/bash
git push
# ou
git push -u origin <branch>
# ou
git push origin <branch>
```
Pronto, agora você pode acessar o repositório online e partir para a última etapa: O *Pull Request*.

## Criando PR
O Pull Request é uma etapa onde você coloca para revisão suas alterações, solicitando o merge de sua branch com a principal (main, development, master...). Essa etapa pode ser configurada por repositório, sendo necessário mais de uma aprovação ou apenas uma aprovação para ser finalizada. Informe um título para seu PR, faça uma descrição e selecione seus revisores (pode ser você mesm(a/o/e).

Para mais informações, acesse a documentação disponível [aqui](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

## Hora de morfar, digo mergear
Após as devidas revisões, correções e commits necessários, você pode fazer o merge diretamente no GitHub. Assim, suas modificações entram dentro da branch principal e você pode  seguramente deletar a branch utilizada.

## MAIS INFORMAÇÕES LEGAIS
 - Você pode olhar seu histórico de commits com o comando **git log**.
 - Você pode realizar atualizações da branch local via **git pull** caso tenha commitado no repositório online via GitHub.
 - O **git pull** é uma mistura do método *fetch* e *merge*.
 - Você pode abrir *issues* dentro do seu repositório no GitHub e linkar novas branches a elas.
 - Você pode criar grandes projetos com vários repositórios!



*Com grandes poderes vêm grandes responsabilidades.* - Tio Ben

FIM!
