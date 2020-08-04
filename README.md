
# Next Level Week 2
## Requisições para a API Rest do Proffy

### Connections

 - GET: Total connections
	 - Não recebe parâmetros
	 - Retorna total de conexões realizadas
 - POST: Create connection
	 - Recebe user_id pelo corpo da requisição
	 - Cria conexão do usuário no banco


### Classes

- GET: List classes
	- Recebe **obrigatoriamente** por query:
		- week_day (int), subject (string) e time (string)
    - Retorna lista de aulas que conferem com os filtros
- POST: Create class 
	- Recebe por corpo da requisição:
		- name, avatar, whatsapp, bio, subject, cost
		- schedule com formato:	
			- { week_day: int, from: string, to: string }
    - Cria entradas em users, classes e class_schedule no banco
