# 🏨 MauiAppHotel - Sistema de Gestão de Hospedagem

Aplicativo desenvolvido com **.NET MAUI** para cálculo, gerenciamento e reserva de hospedagem em hotel. Este projeto foi desenvolvido durante o curso **Técnico em Desenvolvimento de Sistemas** (Componente Curricular: *Desenvolvimento de Sistemas II* / *Programação Mobile I* — Agenda 13 e Agenda 14).

---

## 📱 Visão Geral do Projeto

O **MauiAppHotel** tem como objetivo explorar a construção de interfaces modernas com o .NET MAUI, aplicando o conceito de **Data Binding** e **BindingContext**, além da estrutura de navegação com **AppShell** e a implementação prática de **Programação Orientada a Objetos (POO)** em C#.

### 🚀 Funcionalidades da Aplicação:
- **Seleção de Suítes:** Escolha da categoria de acomodação através do componente `Picker`.
- **Controle de Hóspedes:** Incremento e decremento do número de adultos e crianças utilizando o controle numérico `Stepper`.
- **Período de Hospedagem:** Seleção das datas de entrada (*check-in*) e saída (*check-out*) via `DatePicker`, com validações de intervalos de datas.
- **Tela Sobre (Exigência do Fichário 13):** Apresentação clara das informações do desenvolvedor e ano de desenvolvimento em layout limpo com cartões (`Border`).
- **Navegação com AppShell:** Alternância entre páginas por meio de rotas integradas (menu lateral e abas).
- **Dimensionamento Responsivo no Windows:** Janela travada em 480 × 720 pixels no método `CreateWindow`, simulando com exatidão a visualização vertical de um smartphone.

---
## 🛠️ Tecnologias e Ferramentas

<p align="center">
  <img src="assets/icons/csharp-3d.png" width="85" alt="C#"/>
  <img src="assets/icons/dotnet-maui-3d.png" width="85" alt=".NET MAUI"/>
  <img src="assets/icons/visual-studio-3d.png" width="85" alt="Visual Studio"/>
  <img src="assets/icons/git-3d.png" width="85" alt="Git"/>
  <img src="assets/icons/github-3d.png" width="85" alt="GitHub"/>
  <img src="assets/icons/notepadpp-3d.png" width="85" alt="Notepad++"/>
</p>

---

## 📸 Demonstração da Aplicação (Capturas de Tela)



| Tela Principal (Hospedagem) | Tela Sobre (Desenvolvedor) |

---

## ⚙️ Desafios Técnicos Enfrentados e Solução de Versões do SDK

Durante o ciclo de compilação e teste no ambiente local, foram diagnosticadas e superadas divergências técnicas entre as cargas de trabalho do Visual Studio e as versões do SDK:

### 1. Incompatibilidade de Pacotes e Cargas de Trabalho Legadas
- **Cenário:** O repositório herdado continha avisos de pacotes sem versão explícita (`NU1015`) e workloads apontando para versões descontinuadas do .NET com alertas de fim de suporte (`NETSDK1202`).
- **Solução:** O projeto foi reconstruído em cima de uma estrutura nova e limpa do template oficial do .NET MAUI, permitindo que as dependências fossem restauradas perfeitamente via NuGet.

### 2. Conflito do Gerador Experimental de XAML (`MauiXamlInflator=SourceGen`)
- **Cenário:** Em compilações com SDKs recentes/previews (`net10.0` / SDK `11.0.100-rc.3`), o recurso experimental `MauiXamlInflator=SourceGen` causou falha na geração das classes parciais em tempo de compilação, disparando o erro:
  > `error CS0103: O nome "InitializeComponent" não existe no contexto atual`
- **Solução:** A tela `Sobre` foi refatorada e implementada em **C# puro (Code-Behind Declarativo)** no arquivo `Views/Sobre.cs`. Isso eliminou a dependência do analisador de XAML experimental em pré-compilação, garantindo 100% de estabilidade e execução imediata com código de saída limpo `0 (0x0)`.

### 3. Ajuste de Tamanho de Janela para Desktop
- Controle da dimensão da janela no Windows configurado diretamente no método `CreateWindow` do arquivo `App.xaml.cs`, garantindo estabilidade visual e proporções ideais para testes móveis no PC.

---

## 📁 Estrutura do Projeto

```text
MauiAppHotel/
├── Platforms/            # Configurações de plataforma (Windows, Android, etc.)
├── Resources/            # Estilos, ícones, fontes e imagens
│   └── Images/           # Ícones e imagens do aplicativo
├── Views/                # Telas da aplicação
│   ├── ContratacaoHospedagem.xaml     # Tela principal de seleção da reserva
│   ├── HospedagemContratada.xaml      # Tela de resumo e cálculo de diárias
│   └── Sobre.cs                       # Tela Sobre em C# (Layout limpo com Cards)
├── App.xaml / App.xaml.cs             # Configuração inicial e tamanho de janela
├── AppShell.xaml / AppShell.xaml.cs   # Definição das rotas de navegação
└── MauiProgram.cs                     # Ponto de entrada (builder) da aplicação
👨‍💻 Desenvolvedor
Nome: Marcos Paulo Correa
Ano de Desenvolvimento: 2026
Curso: Técnico em Desenvolvimento de Sistemas
Componente Curricular: Desenvolvimento de Sistemas II / Programação Mobile I (Agenda 13)

