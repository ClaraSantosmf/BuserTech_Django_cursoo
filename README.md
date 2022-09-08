Sempre que inserido novas dependências, é preciso listar ela ou em desenvolvimento ou em produção. Depois compile tudo hasheado.
2) pip-compile --generate-hashes requirements-dev.in > requirements-dev.txt
1) pip-compile --generate-hashes requirements.in > requirements.txt
Agora rode o pip sync para atualizar partindo do -dev.txt, visto que é esse que tem o gancho para o requirements.txt
3) pip-sync requirements-dev.txt


### BO PARA RESOLVER
pip-sync requirements-dev.txt Não está funcionando que preste, isso não está puxando o "-r requirements.in"