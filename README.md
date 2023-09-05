# dio_powerbi_desafio
O que foi feito?

# Antes do PowerBI:
1) Configurações do banco de dados MySQL
2) População das tabelas do banco
3) Integração do banco de dados com o PowerBI

# PowerBI:
## 1) Várias colunas renomeadas para facilitar o entendimento/padronizar melhor:

tabela departament
"Dname" -> "department_name", "Dnumber" -> "department_number",
"Mgr_ssn" -> "manager_ssn", "Mgr_start_date" -> "manager_start_date"
"Dept_create_date" -> "department_create_date"

tabela dependent
"Bdate" -> "birth_date", 
"Dependent_name" -> "dependent_name", 
"Relationship" -> "relationship"

tabela dept_locations
"Dnumber" -> "department_number"
"Dlocation" -> "department_location"

tabela employee
"Fname" -> "first_name"
"Lname" -> "last_name"
"Bdate" -> "birth_date"

tabela project
"Pname" -> "project_name"
"Pnumber" -> "project_number"
"Plocation" -> "project_location"
"Dnum" -> "deparment_number"

tabela works_on
"Pno" -> "project_number"

2) Mudança de tipos
tabela employee -> Salary é alterado para número decimal fixo

3) Separar colunas complexas
tabela employee -> Address foi separado em address, address_number, address_state, address_city

4) mescla de tabelas employee + department para criar uma nova tabela com os nomes de departamentos associados a cada
colaborador. Colunas desnecessárias foram removidas. 

5) criação de nova tabela com colaboradores e gerentes associados com mescla de colunas de nomes em uma unica

6) mescla de departamentos e localização 

7) mescla de dependente com nome de colaborador

8) mescla de works_on com nomes dos colaboradores, nomes e localização do projeto

9) mescla de nomes de departamentos e localização.
	Neste caso, podemos apenas utilizar o mesclar e não o atribuir porque queremos combinar os dados das duas tabelas na horizontal. Se usássemos o atribuir, iríamos unir os dados das duas tabelas na vertical, adicionando linhas à primeira tabela.

10) eliminação de colunas desnecessárias

11) criação de relatório básico: contagem de colaborador por gerente, contagem de projeto por localização, salários, número de dependentes por colaborador, número de dependente por relacionamento, número de colaboradores por sexo, nome do colaborador e horas empregadas em cada projeto.
