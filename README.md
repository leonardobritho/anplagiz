# anplagiz
Antiplagio
def verificar_plagio(texto1, texto2):
    # dividir os textos em uma lista de palavras
    lista_palavras1 = texto1.split()
    lista_palavras2 = texto2.split()
    
    # criar um conjunto de palavras únicas para cada texto
    conjunto_palavras1 = set(lista_palavras1)
    conjunto_palavras2 = set(lista_palavras2)
    
    # verificar se há sobreposição entre os conjuntos de palavras
    sobreposicao = conjunto_palavras1 & conjunto_palavras2
    
    # se houver sobreposição, calcular a porcentagem de similaridade
    if sobreposicao:
        porcentagem_similaridade = len(sobreposicao) / len(conjunto_palavras1)
        return porcentagem_similaridade
    else:
        return 0

texto1 = 'Este é um texto de exemplo.'
texto2 = 'Este é outro texto de exemplo.'

porcentagem = verificar_plagio(texto1, texto2)

if porcentagem > 0:
    print('Os textos são similares em {:.2f}%'.format(porcentagem * 100))
else:
    print('Os textos são diferentes.')
