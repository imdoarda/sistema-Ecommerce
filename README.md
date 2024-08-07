# ÍNDICE
 
* [Introdução](#introdu%C3%A7%C3%A3o)  
* [Tabelas](#tabelas-codificadas-no-banco-de-dados)
* [Funcionalidades](#funcionalidades)
* [Tecnologias Utilizadas](#tecnologias-utilizadas)  
* [Autores](#autores)  



 ## Introdução

  Este projeto é um sistema para o cadastro de produtos de um supermercado, desenvolvido para gerenciar as informações dos produtos em um banco de dados. O sistema permite a inclusão, visualização e gerenciamento de categorias e marcas, além de armazenar detalhes dos produtos, como nome, descrição, estoque, preço, categoria e marca.
  
  ``Veja abaixo o funcionamento do site: ``  

  
           ![tela inicial](https://github.com/user-attachments/assets/3a51fbb9-bc8e-42d6-8e6f-75884cd3f8dc)>


## Tabelas codificadas no banco de dados:

``TABELA PARA CATEGORIAS:``

      CREATE TABLE `categoria` (
      `IDCATEGORIA` int(11) NOT NULL AUTO_INCREMENT,
      `DESCRICAO` varchar(255) NOT NULL,
      PRIMARY KEY (`IDCATEGORIA`)
    ) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=latin1;

``visualização dessa tabela: ``  


          ![Gravando 2024-08-06 230320](https://github.com/user-attachments/assets/94f9a401-b19e-4b3f-844a-6f258accd4c2)


``TABELA PARA MARCA:``

    CREATE TABLE `marca` (
      `IDMARCA` int(11) NOT NULL AUTO_INCREMENT,
      `DESCRICAO` varchar(255) NOT NULL,
      PRIMARY KEY (`IDMARCA`)
    ) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=latin1;

``visualização dessa tabela: ``  


          ![marca](https://github.com/user-attachments/assets/b44ff605-a771-4123-80e8-bad7239c1df5)

  
``TABELA PARA PRODUTOS:``

     CREATE TABLE `produtos` (
      `IDPROD` int(10) NOT NULL AUTO_INCREMENT,
      `IDCATEGORIA` int(10) NOT NULL,
      `IDMARCA` int(10) NOT NULL,
      `NOME` varchar(255) NOT NULL,
      `DESCRICAO` varchar(255) NOT NULL,
       `ESTOQUE` int(10) NOT NULL,
      `PRECO` double NOT NULL,
      PRIMARY KEY (`IDPROD`,`IDCATEGORIA`,`IDMARCA`),
      KEY `IDCATEGORIA` (`IDCATEGORIA`),
      KEY `IDMARCA` (`IDMARCA`),
      CONSTRAINT `produtos_ibfk_1` FOREIGN KEY (`IDCATEGORIA`) REFERENCES `categoria` (`IDCATEGORIA`),
      CONSTRAINT `produtos_ibfk_2` FOREIGN KEY (`IDMARCA`) REFERENCES `marca` (`IDMARCA`)
    ) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=latin1;

``visualização dessa tabela: ``  


         ![produtos](https://github.com/user-attachments/assets/b18a1e69-9cca-4a85-9e9f-6ad3a7a5298a)



## Funcionalidades:

* [``mysqli_query:``](https://www.php.net/manual/pt_BR/mysqli.query.php) Executa uma consulta no banco de dados. 
* [``mysqli_error:``](https://www.php.net/manual/pt_BR/mysqli.error.php) Retorna uma string descrevendo o último erro. 
* [``include:``](https://www.php.net/manual/pt_BR/function.include.php) A expressão include inclui e avalia o arquivo informado. 
* [``include_once:``](https://php.net/manual/pt_BR/function.include-once.php) inclui e avalia o arquivo informado durante a execução do script.  a única diferença entre ``include`` e ``include_once`` é que se o código do arquivo já foi incluído, não o fará novamente, e o ``include_once`` retornará true.
* [``mysqli_close:``](https://www.php.net/manual/pt_BR/mysqli.close.php) Fecha uma conexão ao banco de dados previamente aberta.
* [``mysqli_affected_rows:``](https://www.php.net/manual/en/mysqli.affected-rows.php) Retorna o número de linhas afetadas pela operação MySQL anterior
* [``EQUIV=REFRESH CONTENT:``](https://www.w3schools.com/tags/att_meta_http_equiv.asp) O http-equivatributo fornece um cabeçalho HTTP para as informações/valor do contentatributo. O http-equivatributo pode ser usado para simular um cabeçalho de resposta HTTP. 
* [``require_once:``´](https://www.php.net/manual/pt_BR/function.require-once.php) A expressão require_once é idêntica a require exceto que o PHP verificará se o arquivo já foi incluído, e em caso afirmativo, não o incluirá. 
* [``mysqli_connect:``](https://www.php.net/manual/pt_BR/function.mysqli-connect.php) Se o modo de exceção mysqli não estiver habilitado e uma conexão falhar, então mysqli_connect() retornará false ao invés de um objeto. 
* [``connect_error:``](https://www.php.net/manual/pt_BR/mysqli.connect-error.php) Retorna uma descrição do último erro de conexão
* [``set_charset:``](https://www.php.net/manual/pt_BR/mysqli.set-charset.php) Esta é a maneira preferida de alterar o conjunto de caracteres.


## Tecnologias Utilizadas

* 	``MySQL``
*   ``PHP 8.2``
*   ``HTML 5``
*   ``CSS3``
*   ``GIT HUB``
*   ``APACHE``
*   ``XAMPP``

## Autores

[<img loading="lazy" src="https://avatars.githubusercontent.com/u/127868962?v=4" width=115><br><sub>Maria Eduarda Mendes</sub>](https://github.com/imdoarda)
