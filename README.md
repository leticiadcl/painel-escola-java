# Easy English - Sistema de Controle Acadêmico

Projeto desenvolvido para a disciplina **COM220 – Computação Orientada a Objetos** do curso de **Ciência da Computação da UNIFEI**.

## 📚 Sobre o Projeto

A escola de idiomas **Easy English** contratou nossa equipe para desenvolver um sistema de controle acadêmico com o objetivo de facilitar a gestão administrativa e acadêmica da instituição.

O sistema foi desenvolvido utilizando os conceitos de **Programação Orientada a Objetos (POO)** em Java e contempla o gerenciamento de cursos, professores, turmas, alunos, matrículas e notas.

---

# 🎯 Objetivos do Sistema

O sistema deve permitir:

* Cadastro de professores;
* Criação e gerenciamento de turmas;
* Matrícula e renovação de matrícula de alunos;
* Lançamento e alteração de notas;
* Emissão de históricos escolares;
* Emissão de relatórios de concluintes;
* Emissão de relatórios de turmas.

---

# 📖 Cursos Oferecidos

A Easy English oferece dois tipos de cursos:

## 👦 Curso Kids

Destinado a crianças com até **12 anos de idade**.

### Características

* Duração de **6 semestres**;
* Os semestres são identificados pela letra **K** seguida de um número sequencial;
* Exemplos:

  * K1 → 1º semestre
  * K2 → 2º semestre
  * K3 → 3º semestre

### Certificação

Ao concluir o curso, o aluno recebe o **Certificado Kids**.

Após a conclusão, o aluno pode ingressar diretamente no **5º semestre do Curso Regular (R5)**.

---

## 👨‍🎓 Curso Regular

Destinado a adolescentes e adultos com **13 anos ou mais**.

### Características

* Duração de **8 semestres**;
* Os semestres são identificados pela letra **R** seguida de um número sequencial;
* Exemplos:

  * R1 → 1º semestre
  * R2 → 2º semestre
  * R3 → 3º semestre

### Certificação

Ao concluir o curso, o aluno recebe o **Certificado Easy English**.

---

# 👨‍🏫 Cadastro de Professores

O sistema deve permitir o cadastro de professores contendo:

* Nome;
* CPF;
* Cursos nos quais pode atuar:

  * Kids;
  * Regular;
  * Ambos.

---

# 🏫 Gerenciamento de Turmas

Cada turma deve possuir:

* Código;
* Semestre letivo (1 ou 2);
* Ano;
* Capacidade máxima de alunos;
* Horário;
* Curso/Semestre;
* Professor responsável.

## Formação do Código da Turma

O código da turma é composto por:

```
Identificação do horário + Identificação do curso/semestre
```

### Exemplo

Uma turma do curso **K3**, ministrada nos dois primeiros horários da noite de quarta-feira:

```
4N12K3
```

---

# 📝 Matrículas

## Primeira Matrícula

Na primeira matrícula, o sistema deve cadastrar:

### Dados do aluno

* Nome;
* CPF;
* E-mail;
* Data de nascimento.

### Menores de idade

Caso o aluno seja menor de idade, também devem ser cadastrados:

* Nome do responsável;
* Tipo de responsável (pai, mãe ou outro);
* CPF do responsável.

### Regras

* Alunos com até 12 anos devem iniciar obrigatoriamente em **K1**;
* Alunos com 13 anos ou mais devem iniciar obrigatoriamente em **R1**.

---

## Renovação de Matrícula

O sistema deve:

1. Identificar o último semestre concluído com aprovação;
2. Matricular o aluno automaticamente no semestre seguinte.

### Exemplos

| Última Aprovação | Nova Matrícula |
| ---------------- | -------------- |
| R1               | R2             |
| R2               | R3             |
| R3               | R4             |
| K3               | K4             |

### Regra Especial

Caso o aluno conclua o curso Kids:

| Última Aprovação |
| ---------------- |
| K6               |

A próxima matrícula deverá ser:

```
R5
```

---

## Controle de Vagas

Uma matrícula só poderá ser realizada se houver vaga disponível na turma.

Caso a turma esteja lotada, uma nova turma deverá ser criada para atender o aluno.

---

# 📊 Lançamento de Notas

O sistema deve permitir que a secretária registre duas avaliações por turma:

* N1
* N2

## Fluxo de Lançamento

1. Selecionar a turma;
2. Escolher a avaliação (N1 ou N2);
3. Exibir a lista de alunos matriculados;
4. Informar as notas;
5. Salvar ou cancelar a operação.

### Alteração de Notas

A mesma tela utilizada para lançamento deve permitir a alteração de notas já cadastradas.

Ao abrir uma avaliação existente, os valores devem ser carregados automaticamente para edição.

---

# 📄 Histórico Escolar

O sistema deve permitir consultar o histórico de um aluno utilizando seu CPF.

O relatório deve exibir:

* Ano/Semestre cursado;
* Curso/Semestre;
* Nota obtida.

### Exemplo

| Ano/Semestre | Curso | Nota |
| ------------ | ----- | ---- |
| 2025/1       | K1    | 8,5  |
| 2025/2       | K2    | 7,0  |
| 2026/1       | K3    | 9,0  |

---

# 🎓 Relatórios de Concluintes

O sistema deve gerar dois relatórios:

## Concluintes do Curso Kids

Exibir:

* Nome;
* CPF.

Dos alunos matriculados em:

```
K6
```

## Concluintes do Curso Regular

Exibir:

* Nome;
* CPF.

Dos alunos matriculados em:

```
R8
```

---

# 📋 Relatório de Turma

A partir do código da turma, o sistema deve gerar um relatório contendo:

### Dados dos alunos

* Nome;
* CPF.

### Notas

* N1;
* N2.

### Regras

* Se apenas uma nota estiver lançada, exibir somente a nota disponível;
* Se ambas as notas estiverem cadastradas:

  * Exibir N1;
  * Exibir N2;
  * Calcular a média aritmética;
  * Informar situação do aluno.

### Critério de Aprovação

```
Média >= 6,0 → APROVADO
Média < 6,0 → REPROVADO
```

---

# 🛠️ Tecnologias Utilizadas

* Java
* Programação Orientada a Objetos (POO)
* UML
* Git
* GitHub

---

# 👥 Equipe

Projeto acadêmico desenvolvido para a disciplina **COM220 – Computação Orientada a Objetos** da **Universidade Federal de Itajubá (UNIFEI)**.
