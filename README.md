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
