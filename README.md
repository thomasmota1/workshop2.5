## CI/CD

O pipeline de Integração Contínua roda automaticamente a cada `push` ou `pull request`
na branch `main`, executando lint (flake8) e os testes automatizados (pytest). olas

Veja o workflow em `.github/workflows/ci.yml`.

## Preparação para o workshop

### Acesso ao repositório de exemplo

O projeto usado na prática está disponível em:

[https://github.com/Guiscoob7/WorkShop-Git-Actions](https://github.com/Guiscoob7/WorkShop-Git-Actions)

Antes do workshop:

1. Faça login no GitHub;
2. Acesse o link acima e clique em **Fork** (canto superior direito), para ter sua própria cópia do repositório;
3. Clone o seu fork para a sua máquina:

```bash
git clone https://github.com/Guiscoob7/WorkShop-Git-Actions.git
cd WorkShop-Git-Actions
```

### Teste final

1. Dentro da pasta do projeto clonado, instale as dependências:

```bash
pip install -r requirements.txt
```

2. Rode os testes automatizados do projeto:

```bash
python -m pytest tests/ -v
```

3. O resultado esperado é algo parecido com:

```
tests/test_calculadora.py::test_somar PASSED
tests/test_calculadora.py::test_subtrair PASSED
tests/test_calculadora.py::test_multiplicar PASSED
tests/test_calculadora.py::test_dividir PASSED
tests/test_calculadora.py::test_dividir_por_zero PASSED

===================== 5 passed in 0.02s =====================
```

Se os 5 testes passaram, seu ambiente está pronto. Se algo não funcionar, procure a
gente antes do dia do workshop que ajudamos a resolver.
