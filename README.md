# Gerador de Senhas Aleatórias em Python

Este código em Python cria uma função para gerar senhas aleatórias com até 8 caracteres, utilizando letras (maiúsculas e minúsculas), números e símbolos.

## Código

```python
import random
import string

def gerar_senha(tamanho=8):
    caracteres = string.ascii_letters + string.digits + string.punctuation
    # Garante que o tamanho não ultrapasse 8
    tamanho = min(tamanho, 8)
    senha = ''.join(random.choice(caracteres) for _ in range(tamanho))
    return senha

# Gerando uma senha com até 8 caracteres
print("Sua senha gerada é:", gerar_senha(8))
