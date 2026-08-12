# Banco-de-Dados

### SSH
É um protocolo de segurança usado para conectar e controlar um servidor ou terminal remoto pela linha de comando de forma criptografada. Serve para entrar no terminal de um servidor distante (ou na máquina da escola/trabalho) para executar comandos SQL, gerenciar arquivos ou administrar o sistema.

* Exemplo de uso: ssh adryan.oliveira@10.111.9.113

### Criar tabela
Comando usado para construir a estrutura de uma nova tabela no banco de dados, definindo suas colunas, os tipos de dados (texto, número, data) e as regras/restrições.

* Exemplo:
  
```SQL
CREATE TABLE clientes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100)
);
```

### Dropar Tabela
Comando usado para excluir completamente a estrutura de uma tabela e todos os dados contidos nela. É uma ação permanente.

* Exemplo:
```SQL
DROP TABLE IF EXISTS clientes;
```

### Inserir
Comando DML (Data Manipulation Language) usado para adicionar novos registros (linhas) dentro de uma tabela já existente.

* Exemplo:
```SQL
INSERT INTO clientes (nome, email) 
VALUES ('Adryan', 'adryan@email.com');
```

### Selecionar
Comando usado para consultar, buscar e ler dados salvos nas tabelas. Permite filtrar resultados, ordenar e escolher quais colunas exibir.

* Exemplo:
```SQL
-- Seleciona todos os clientes
SELECT * FROM clientes;

-- Seleciona apenas o nome de quem tem id = 1
SELECT nome FROM clientes WHERE id = 1;
```

### Alterar
Dependendo do contexto, "alterar" pode significar duas coisas:

ALTER TABLE (Alterar a estrutura): Adiciona, remove ou modifica colunas da tabela.
```SQL
ALTER TABLE clientes ADD COLUMN telefone VARCHAR(20);
```
UPDATE (Alterar dados registrados): Modifica os valores contidos nas linhas já cadastradas. (Atenção: use sempre com WHERE para não alterar a tabela inteira).
```SQL
UPDATE clientes SET email = 'novo_email@email.com' WHERE id = 1;
```

### Deletar
Comando usado para remover registros (linhas) específicos de uma tabela, sem apagar a tabela em si.

* Exemplo de uso: (Atenção: use sempre com WHERE para não apagar todos os dados da tabela).
```SQL
DELETE FROM clientes WHERE id = 1;
```


  
