# hello-world
My first repository
#aula devan 18/10/2022
#sistema de informações:
#1 é igual calculadora e 2 é igual conversor de bitcoin

nome = str(input("Insira seu nome completo: "))
cpf = int(input("Digite seu CPF (somente números): "))
endere = str(input("Insira seu enderço: "))
email = str(input("Digite se e-mail: "))
telefo = float(input("Digite seu telefone: "))
parent = str(input("Digite o 1º nome da sua mãe: "))
verifica = "Ruth"

tentativas = 0

print("Ok, agora para concluir seu cadastro crie uma senha !")
senha1 = str(input("Crie uma senha: "))
print("Para logar no sistema digite sua senha !")
senha = senha1
login = email and senha1

while login and tentativas <3:
    senha = input("Insira sua senha: ")
    if login == senha:
        print("Acesso ok !")
        break

    else:
        print("Acesso negado !")
        tentativas = tentativas + 1

print("Verificação em 2 etapas")

while verifica and tentativas <3:
    etapa = str(input("Primeiro nome da sua mãe: "))

    if etapa == verifica:
        print("Login ok !")
        break
    else:
        print("Errado !")
        tentativas = tentativas +1

print("Agora selecione uma das ferramentas: (1) Calculadora (2) Conversor de Bitcoin: ")

Calculadora = 1
Conversor = 2

ferra = int(input("informe qual quer usar:"))
if ferra == 1:
    C = "S"
    while C != "N":
        C = str(input("Quer realizar um calculo ?: ")).strip().upper()
        if C == "N":
            break

        numero1 = int(input("Digite um número: "))
        numero2 = int(input("Digite mais um número: "))
        print("=" * 30)
        print("[1] Soma"
              "\n[2] Subtrai"
              "\n[3] Multiplica"
              "\n[4] Divide")
        print("=" * 30)
        operacao = int(input("Digite qual a operação: "))
        if operacao == 1:
            print("{}".format(numero1 + numero2))
        elif operacao == 2:
            print("{}".format(numero1 - numero2))
        elif operacao == 3:
            print("{}".format(numero1 * numero2))
        elif operacao == 4:
            print("{}".format(numero1 / numero2))
elif ferra == 2:
    bit = float(input("Valor em Bitcoin: "))
    reais = 101000.40
    bit_real = bit + reais
    print("Conversão de Bitcoin para Reais equivale", bit_real)


