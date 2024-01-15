# Dados da introdução do projeto
## Introdução
Recebi uma nova demanda: desenvolver uma API Rest para o gerenciamento de cursos e aulas de uma escola de modalidade EAD. Neste projeto final, fui encarregado de criar uma aplicação que permitisse aos usuários acessar e gerenciar de forma eficiente e intuitiva todos os aspectos relacionados aos cursos, inscrições, aulas e outros recursos do ambiente de ensino a distância.


## URL da documentação da API Kanvas
url_documentacao = "https://m5-projeto-final-kanva.onrender.com/api/docs/"

## Observações sobre a disponibilidade da documentação
**Observações:**
- <span style="color:red">Caso a documentação não esteja acessível, pode ser devido ao projeto ter sido excluído do Render devido ao plano gratuito ou por ter sido excluído para dar espaço a outros projetos.</span>
## Preparando ambiente para execução dos testes

1. Verifique se os pacotes **pytest**, **pytest-testdox** e/ou **pytest-django** estão instalados globalmente em seu sistema:
```shell
pip list
```

2. Caso eles apareçam na listagem, rode os comandos abaixo para realizar a desinstalação:

```shell
pip uninstall pytest pytest-testdox pytest-django -y
```

3. Após isso, crie seu ambiente virtual:
```shell
python -m venv venv
```

4. Ative seu ambiente virtual:

```shell
# Linux e Mac:
source venv/bin/activate

# Windows (PowerShell):
.\venv\Scripts\activate

# Windows (GitBash):
source venv/Scripts/activate
```

5. Instale as bibliotecas necessárias:

```shell
pip install model_bakery pytest-testdox pytest-django
```


## Execução dos testes:

Para rodar a bateria de todos os testes, utilize:
```shell
pytest --testdox -vvs
```
---

Caso você tenha interesse em rodar apenas um diretório de testes específico, utilize os comandos abaixo:

Accounts:
```python
pytest --testdox -vvs tests/accounts/
```

Contents:
```python
pytest --testdox -vvs tests/contents/
```

Courses:
```python
pytest --testdox -vvs tests/courses/
```

---

Você também pode rodar cada método de teste isoladamente:

```shell
pytest --testdox -vvs caminho/para/o/arquivo/de/teste::NomeDaClasse::nome_do_metodo_de_teste
```

**Exemplo**: executar somente "test_user_login_without_required_fields".

```shell
pytest --testdox -vvs tests/accounts/tests_views.py::TestLoginAccountView::test_login_without_required_fields
```
