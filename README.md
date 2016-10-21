# PseudoORM
App de persistência Genérica para fins didáticos usando a interface do PDO.

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/7e760cb85d6a461683513671c36df91a)](https://www.codacy.com/app/eniebercunha/PseudoORM?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=PHPMT/PseudoORM&amp;utm_campaign=Badge_Grade)

## Getting started

 * Clone o repositorio  para sua maquina ` git clone https://github.com/HoraExtraSinop/PseudoORM `
 * Altere as configurações do banco no arquivo `index.php` que é apenas um arquivo de exemplo.

Para criar novas classes, basta criar uma entidade na pasta `model/Entity/` extendendo da classe `EntidadeBase` e criar a respectiva tabela no banco de dados, e está pronto para usar.

Para modificar o comportamento padrão, basta criar um Arquivo de persistencia extendendo a classe `GenericDAO` dentro da pasta `DAO/impl` podendo sobrescrever métodos existentes e/ou adicionar novos. 


## Para gerar script de criação do BD para Postgresql use:


```
$dao = AppFactory::getRepository(new Usuario());

echo $dao->generate(new PseudoORM\Services\PostgreSQLDataBaseCreator());

```


