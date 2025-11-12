# meu-blog-atividades123
Atividade 1

def f(nums: list[int], alvo: int) -> tuple[int, int]:
    complementos = {}
    
    for indice_atual, num_atual in enumerate(nums):
        complemento_necessario = alvo - num_atual
        
        if complemento_necessario in complementos:
            indice_complemento = complementos[complemento_necessario]
            indice_do_atual = indice_atual
            
            return (indice_complemento, indice_do_atual)
        
        complementos[num_atual] = indice_atual

Atividade 2
def f(nums: list[int]) -> tuple[int, int]:
    n = len(nums)
    num_duplicado = -1
    
    elementos_vistos = set()
    
    for num in nums:
        if num in elementos_vistos:
            num_duplicado = num
        else:
            elementos_vistos.add(num)
            
    for i in range(1, n + 1):
        if i not in elementos_vistos:
            num_ausente = i
            return (num_duplicado, num_ausente)
            
    return (-1, -1)

Atividade 3
def f(lista: list[tuple[int, str]], busca: int) -> str | None:
    for numero, nome in lista:
        if numero == busca:
            return nome
            
    return None
