# 🏨 App Hotel — Gerenciador de Hospedagem em .NET MAUI

Aplicativo multiplataforma desenvolvido em **C#** com **.NET MAUI**, criado como atividade prática do curso técnico em Desenvolvimento de Sistemas (Agendas 13 e 14). O projeto simula a contratação e o cálculo de reservas de um hotel, aplicando conceitos fundamentais de interface gráfica e Programação Orientada a Objetos (POO).

---

## 🚀 Funcionalidades

- **Seleção de Hóspedes (`Stepper`)**: Controle interativo da quantidade de adultos e crianças.
- **Escolha da Acomodação (`Picker`)**: Listagem dinâmica de suítes com valores diferenciados por diária.
- **Definição do Período (`DatePicker`)**: Seleção de datas de check-in e check-out com regras de validação de estadia mínima.
- **Vinculação de Dados (`BindingContext`)**: Passagem e exibição em tempo real do resumo e valor total da reserva contratada.
- **Tela Sobre (Identificação)**: Tela dedicada com as informações do desenvolvedor, ano e versão do projeto.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** C#
- **Framework:** .NET MAUI (.NET 11.0 / .NET 8.0)
- **Marcação Visual:** XAML
- **Paradigma:** Programação Orientada a Objetos (Classes, Encapsulamento, Coleções)

---

## 📂 Estrutura do Projeto

```text
MauiAppHotel/
├── Models/              # Classes de dados e regras de cálculo (Quarto, Hospedagem)
├── Views/               # Telas do aplicativo (XAML e Code-Behind)
│   ├── ContratacaoHospedagem.xaml
│   ├── HospedagemContratada.xaml
│   └── Sobre.xaml
└── Resources/           # Fontes, estilos, ícones e imagens
👤 Desenvolvedor
Nome: [Seu Nome Completo Aqui]
Ano de Desenvolvimento: 2026
Curso: Técnico em Desenvolvimento de Sistemas

---

### Dica rápida para colocar no GitHub:
1. No seu repositório no GitHub, clique no botão **"Add a README"** (ou crie um arquivo chamado `README.md`).
2. Cole o texto acima e apenas substitua o campo **`[Seu Nome Completo Aqui]`** pelo seu nome.
3. Clique em **Commit changes...** para salvar!
