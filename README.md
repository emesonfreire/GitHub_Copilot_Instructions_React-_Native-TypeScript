# 📱 React Native Enterprise Framework (Copilot Optimized)

![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Clean Architecture](https://img.shields.io/badge/Clean_Architecture-FAANG_Standard-green?style=for-the-badge)

Este repositório utiliza um framework de **Instruções Personalizadas para o GitHub Copilot**. Ele força a IA a agir como um Engenheiro Mobile Sênior, garantindo que todo o código gerado siga padrões rigorosos de arquitetura e segurança.

---

## 🎯 Objetivo do Framework

Transformar o Copilot em um parceiro de pair programming que domina:
- **Clean Architecture:** Separação clara entre Domínio, Dados e Apresentação.
- **SOLID Completo:** Código modular, extensível e fácil de testar.
- **Enterprise Grade:** Focado em performance (FlatList, Memo) e segurança (Keychain).

---

## 🛠️ Como Configurar no Projeto

Para que o Copilot siga as regras automaticamente, o arquivo de instruções deve estar no local correto:

1. Clone este repositório.
2. Certifique-se de que o arquivo `.github/copilot-instructions.md` existe.
3. No VS Code, o Copilot lerá este arquivo e passará a sugerir códigos dentro dos padrões definidos.

---

## 🏗️ Estrutura de Camadas (Clean Arch)

O projeto segue o fluxo de dependência: **Presentation → Domain ← Data**.

| Camada | Responsabilidade |
| :--- | :--- |
| **Domain** | Entidades, Interfaces (Contratos) e Casos de Uso (Regras de Negócio). |
| **Data** | Implementação de Repositórios, Chamadas API (Axios) e Mappers (DTO). |
| **Presentation** | Telas (JSX), Componentes e Hooks (ViewModels). |
| **Infrastructure** | Configurações globais, Injeção de Dependência e Storage Seguro. |

---

## 📜 Regras de Ouro para o Desenvolvedor

Sempre que solicitar algo ao Copilot, ele seguirá estas diretrizes:

1. **Interfaces Primeiro:** Nunca implementamos nada sem antes definir o contrato TypeScript.
2. **Zero Any:** O uso de `any` é estritamente proibido. Usamos `unknown` ou Tipagem Branded.
3. **Padrão AAA nos Testes:** Todo código deve vir acompanhado de testes no formato *Arrange, Act, Assert*.
4. **Segurança Mobile:** Nunca salvamos tokens no AsyncStorage. Usamos o `SecureStorage` configurado na camada de infraestrutura.
5. **Acessibilidade:** Todo componente interativo deve ter `accessibilityLabel` e área de toque mínima de `48dp`.

---

## 🚀 Exemplo de Prompt para usar com este Framework

> *"Crie a funcionalidade de Login. Comece definindo a interface no Domain, mapeie os erros de autenticação conforme a Parte 8 das instruções e gere a implementação do repositório usando Axios."*

---

## 👨‍💻 Autor

**Emerson Mathias** *Systems Analyst & Mobile Developer* Especialista em TI Infrastructure e Engenharia de Redes.
