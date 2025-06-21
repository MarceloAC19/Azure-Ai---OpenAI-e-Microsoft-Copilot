
Gerado por IA
## Exemplo: Resultado da Geração de Código



Este arquivo mostra o resultado obtido a partir do prompt de geração de código Python.

### Prompt Utilizado
> **System:** Você é um assistente de programação sênior, especialista em Python e em escrever código limpo e eficiente.
>
> **User:** Escreva uma função em Python chamada `validar_email`. A função deve receber uma string como argumento e usar expressões regulares (regex) para verificar se a string corresponde a um formato de e-mail válido. A função deve retornar `True` se o e-mail for válido e `False` caso contrário. Adicione comentários explicando o padrão regex utilizado.

### ✅ Resultado Gerado pela IA

```python
import re

def validar_email(email: str) -> bool:
    """
    Valida se uma string fornecida corresponde a um formato de e-mail padrão.

    Args:
        email: A string a ser validada.

    Returns:
        True se o e-mail for válido, False caso contrário.
    """
    # Padrão de expressão regular para um e-mail comum.
    # ^                  - Início da string.
    # [a-zA-Z0-9._%+-]+  - Parte do nome do usuário (um ou mais caracteres permitidos).
    # @                  - O símbolo de "arroba".
    # [a-zA-Z0-9.-]+     - Parte do nome do domínio (um ou mais caracteres permitidos).
    # \.                 - O ponto que separa o domínio da extensão.
    # [a-zA-Z]{2,}       - A extensão do domínio (pelo menos 2 letras).
    # $                  - Fim da string.
    padrao = r"^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$"

    if re.match(padrao, email):
        return True
    else:
        return False

# --- Exemplos de uso ---
email1 = "contato@exemplo.com"
email2 = "usuario.123@sub.dominio.co.uk"
email_invalido1 = "meu-email.com"
email_invalido2 = "usuario@dominio."

print(f"'{email1}': {validar_email(email1)}") # Esperado: True
print(f"'{email2}': {validar_email(email2)}") # Esperado: True
print(f"'{email_invalido1}': {validar_email(email_invalido1)}") # Esperado: False
print(f"'{email_invalido2}': {validar_email(email_invalido2)}") # Esperado: False

```

---
**Análise:** O código gerado é funcional, limpo e bem documentado. A IA não apenas criou a lógica correta com a expressão regular, mas também adicionou uma docstring clara, comentários explicativos e exemplos de uso, seguindo as melhores práticas de desenvolvimento.
