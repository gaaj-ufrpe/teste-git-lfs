  * Selecionar a opção `Clone from GitLab (https://gitlab.ufal.br)`
  * Selecionar o repositório referente ao `bi-app`
  * Selecionar a opção de URL com o https (`https://gitlab.ufal.br/nees/pne/dev/bi-app.git`)
  * Irá aparecer um popup solicitando o login, onde vc deve informar o seu cpf e o seu token. Apesar do campo de cpf aparecer como opcional, este deve ser informado.
* Configurar email do git
  * Abra o terminal do VSCode e digite:
    * `git config --global user.name "[CPF]"`
    * `git config --global user.email "[email do nees]"`
* Configurar o Git LFS (para arquivos grandes)
  * Abra o terminal e digite `git lfs install` para instalar o `lfs`
  * Digite os comandos abaixo para que o `lfs` faça o track dos arquivos com os dados.
    * Adicionar um arquivo no `lfs`: `git lfs track "*.csv"`
    * Adicionar uma pasta (e suas subpastas) no `lfs`: `git lfs track "data/**"`
    * Migrar um arquivo do repositório para o `lfs`: `git lfs migrate import --include="*.parquet"`
    * listar arquivos gerenciados pelo `lfs`: `git lfs ls-files`
    