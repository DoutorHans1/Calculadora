#calculadora
#calculadora simples usando while em python

while True:
    
    numero1 = input('Digite um número: ')
    numero2 = input('Digite outro número: ')
    operador = input('Digite um operador: ')
    
    operadores_permitidos = '+-*/'
    
    try:


        numero_float1 = float(numero1)
        numero_float2 = float(numero2)

        if operador == '+':
            print(numero_float1 + numero_float2)

        elif operador == '-':
            print(numero_float1 - numero_float2)
        
        elif operador == '*':
            print(numero_float1 * numero_float2)

        elif operador == '/':
            print(numero_float1 / numero_float2)

        elif operador not in operadores_permitidos:
            print('Digite um operador permitido.')

        elif len(operador) < 1:
            print('Digite pelo menos um operador.')
            
    

    except:
        
        if numero1 or numero2 == None:
            print('Um ou mais números estão inválidos. Por favor, digite números válidos.')
            continue

        
    sair = input('Você deseja sair? [s]: ')

    if 's' in sair.lower():
        print('Saindo...')
        break
