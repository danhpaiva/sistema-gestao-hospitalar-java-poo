# Exercício Prático Avançado: <br>Sistema de Gestão Hospitalar (POO em Java)

**Disciplina:** Algoritmos e Programação  
**Professor / Desenvolvedor:** Daniel Paiva
**Objetivo:** Consolidar conceitos avançados de Programação Orientada a Objetos (POO) em Java — incluindo hierarquias complexas de herança, interfaces, polimorfismo, tratamento de exceções e relações de associação/agregação — através do desenvolvimento de um sistema corporativo robusto.

## 🏥 Contextualização do Problema

Você foi contratado por uma rede de saúde para desenvolver o núcleo de um **Sistema de Gestão Hospitalar**. <br>O software precisa automatizar os fluxos de atendimento de pacientes, controle de corpo clínico, internações, prescrição de medicamentos, exames laboratoriais e emissão de faturamento/convênios.

Dada a complexidade do domínio hospitalar, o seu projeto deverá ser arquitetado utilizando **no mínimo 14 (quatorze) classes**, todas devidamente integradas e interagindo na classe principal `Programa.java`.

---

## 🛠️ Requisitos de Implementação

Para atingir a robustez esperada, sua aplicação deve contemplar as seguintes classes e estruturas essenciais:

### 1. Núcleo de Pessoas e Herança (Mínimo de 4 classes)
1. **`Pessoa`** (Classe Abstrata Base): Contém atributos comuns como nome, CPF, data de nascimento e contato.
2. **`Paciente`** (Herda de `Pessoa`): Atributos específicos como prontuário, tipo sanguíneo e convênio.
3. **`Medico`** (Herda de `Pessoa`): Atributos específicos como CRM, especialidade médica e valor da consulta.
4. **`Enfermeiro`** (Herda de `Pessoa`): Atributos específicos como COREN e setor de atuação.

### 2. Módulo de Atendimento e Clínica (Mínimo de 4 classes)
5. **`Consulta`**: Gerencia o agendamento/realização do atendimento (associa Médico, Paciente, data, horário e valor).
6. **`Prontuario`**: Histórico médico do paciente, contendo histórico de evoluções e diagnósticos.
7. **`Prescricao`**: Medicamentos e dosagens receitadas durante o atendimento.
8. **`Medicamento`**: Detalhes do remédio (nome, princípio ativo, laboratório, estoque).

### 3. Módulo de Internação e Exames (Mínimo de 3 classes)
9. **`Leito`**: Representa um leito hospitalar (número, tipo [Enfermaria/UTI], status de ocupação).
10. **`Internacao`**: Controla a entrada e saída do paciente em um leito, ligando-o ao médico responsável.
11. **`Exame`**: Representa exames laboratoriais ou de imagem solicitados (tipo, status de realização, laudo).

### 4. Módulo Financeiro e Gestão (Mínimo de 3 classes)
12. **`Faturamento`** ou **`ContaHospitalar`**: Acumula custos de consultas, internações e exames para gerar a fatura final do paciente.
13. **`Convenio`**: Gerencia planos de saúde parceiros e regras de cobertura (nome, CNPJ, percentual de desconto).
14. **`Hospital`** (Classe Gerenciadora/Sistema): Classe central que armazena as coleções globais (`List<Paciente>`, `List<Medico>`, `List<Internacao>`, etc.) e centraliza as regras de negócio.

---

### 🚀 A Classe Principal (`Programa.java`)

A classe `Programa.java` deve conter o método `public static void main(String[] args)` e realizar uma simulação completa do fluxo hospitalar:

1. Instanciar a classe gerenciadora (`Hospital`).
2. Cadastrar médicos e enfermeiros no sistema.
3. Cadastrar pacientes (alguns associados a um `Convenio`).
4. Realizar o agendamento e execução de uma **`Consulta`**.
5. Realizar a **`Internacao`** de um paciente em um **`Leito`**.
6. Emitir uma **`Prescricao`** de **`Medicamento`** e solicitar um **`Exame`**.
7. Calcular e exibir o **`Faturamento`** final do atendimento.
8. Imprimir no console o panorama geral do hospital através de métodos `toString()` bem estruturados.

---

## 📋 Critérios de Avaliação

* **Arquitetura e Modularidade:** Divisão clara das 14 classes com responsabilidades bem definidas (Princípio da Responsabilidade Única - SRP).
* **Encapsulamento Rigoroso:** Atributos privados e uso adequado de construtores, getters e setters.
* **Polimorfismo e Sobrescrita:** Uso correto de classes abstratas e reescrita de métodos (como `calculaCusto()` ou exibição de dados).
* **Tratamento de Coleções:** Uso eficiente de `ArrayList` ou estruturas similares para gerenciar os cadastros no escopo da classe gerenciadora.
* **Execução Limpa:** Código funcional em `Programa.java` sem erros de compilação ou exceções não tratadas.

Bons códigos e excelente projeto! 🩺📊
