alunos = []

while True:
    print("\n1 - Cadastrar")
    print("2 - Listar")
    print("3 - Sair")
    opcao = input("Escolha: ")

    if opcao == "1":
        nome = input("Nome: ")
        matricula = input("Matrícula: ")
        n1 = float(input("Nota 1: "))
        n2 = float(input("Nota 2: "))
        media = (n1 + n2) / 2
        if media >= 7:
            situacao = "Aprovado"
        elif media >= 5:
            situacao = "Recuperação"
        else:
            situacao = "Reprovado"
        alunos.append([nome, matricula, n1, n2, media, situacao])
        print("Aluno cadastrado!")

    elif opcao == "2":
        for a in alunos:
            print(a)

    elif opcao == "3":
        break

    else:
        print("Opção inválida")
