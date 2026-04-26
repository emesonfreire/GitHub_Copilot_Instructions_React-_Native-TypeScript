# 📱 React Native Enterprise Framework (Copilot Optimized)

[![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactnative.dev/docs/getting-started)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/docs/)
[![Clean Architecture](https://img.shields.io/badge/Clean_Architecture-FAANG_Standard-green?style=for-the-badge)](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)

Este repositório utiliza um framework de **Instruções Personalizadas para o GitHub Copilot**. Ele força a IA a agir como um Engenheiro Mobile Sênior.

---

## 🎯 Objetivo do Framework

Transformar o Copilot em um parceiro de pair programming que domina:
- **Clean Architecture:** Separação clara entre Domínio, Dados e Apresentação.
- **SOLID Completo:** Código modular, extensível e fácil de testar.
- **Enterprise Grade:** Focado em performance (FlatList, Memo) e segurança (Keychain).

---

##🛠️ Como Configurar no VS Code (Passo a Passo)
Para que o GitHub Copilot assuma a persona de Engenheiro Sênior e aplique as regras automaticamente, siga estas etapas:
---
###1. Preparação do Ambiente
Certifique-se de que você tem a extensão GitHub Copilot ou GitHub Copilot Chat instalada no seu VS Code.
---
###2. Criação da Estrutura
O segredo está na localização do arquivo. O Copilot busca instruções específicas dentro da pasta oculta .github.

Na raiz do seu projeto, crie uma pasta chamada .github (não esqueça o ponto inicial).

Dentro dela, crie um arquivo chamado copilot-instructions.md.
---
###3. Implementação das Regras
Copie todo o conteúdo do framework (Persona, SOLID, Clean Arch) e cole dentro desse arquivo.

Salve o arquivo.
---
###4. Ativação
Não é necessário rodar comandos. O VS Code detecta o arquivo automaticamente, mas para garantir a indexação imediata:

Pressione Ctrl + Shift + P (Windows/Linux) ou Cmd + Shift + P (Mac).

Digite Developer: Reload Window e dê Enter.

Abra o chat do Copilot (Ctrl + I ou no painel lateral) e comece a digitar.

💡 Dica de Ouro: Para confirmar que ele está lendo as regras, pergunte no chat: "Qual é a sua stack obrigatória e persona para este projeto?". Se ele responder "Engenheiro Sênior especializado em React Native e Clean Architecture", a configuração foi um sucesso!
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

### 🚀 Exemplos de Uso (Engenharia de Prompt)

Com este framework configurado, o GitHub Copilot reconhece "gatilhos" técnicos específicos. Utilize os exemplos abaixo para obter resultados de nível Sênior:

#### 1. 🧪 TDD e Lógica de Negócio (Camada Domain)
> "Preciso criar o Caso de Uso para **[NOME DA FEATURE]**. Seguindo a **Parte 4.4**, gere primeiro os testes unitários simulando sucesso e erro de repositório. Após a minha aprovação, implemente a classe correspondente no Domain."

#### 2. 🧹 Refatoração SOLID (Clean Code)
> "Este componente violou o limite de linhas estabelecido na **Parte 1.4**. Atue como Engenheiro Sênior: extraia a lógica para um **Hook Personalizado** e divida a interface em subcomponentes atômicos, respeitando o princípio de responsabilidade única (SRP)."

#### 3. 🔐 Segurança e Infraestrutura (Data Layer)
> "Implemente a persistência de credenciais na camada de Infrastructure. Utilize obrigatoriamente o **SecureStorage** e garanta que qualquer log gerado passe pela função **maskSensitive()**, conforme as diretrizes da **Parte 10**."

#### 4. ♿ Acessibilidade e UI (WCAG 2.2)
> "Gere um componente de **[BOTÃO/INPUT]** seguindo a **Parte 12**. Garanta uma área de toque mínima de 48dp, suporte a tipos dinâmicos (fontes do sistema) e um `accessibilityLabel` que seja devidamente descritivo."

#### 5. ⚡ Otimização de Performance (Mobile First)
> "A minha lista de **[DADOS]** apresenta baixo desempenho durante a rolagem. Aplique as otimizações da **Parte 11**: implemente `getItemLayout` e `React.memo`, e configure o `windowSize` para garantir a máxima performance mobile."

---

### 💡 Por que utilizar estes prompts?
* **Concordância Técnica:** Os termos foram ajustados para que a IA entenda exatamente a ação (verbo) e o objeto (substantivo) da solicitação.
* **Padronização:** Garante que o código do **"Plantão"** ou do **"Laços Diários"** mantenha a mesma qualidade profissional.
* **Eficiência:** Evita ambiguidades, fazendo com que o Copilot entregue a solução correta logo na primeira tentativa.
---

### 💡 Por que usar estes prompts?
* **Contexto Imediato:** Você não precisa explicar o que é SOLID ou Clean Architecture todas as vezes; o Copilot já sabe o que fazer consultando o ficheiro de instruções.
* **Consistência:** Garante que, quer estejas trabalhando em um projeto chamado **"Plantão"** ou no **"Laços Diários"**, o padrão de código seja o mesmo.
* **Qualidade Sênior:** Força a IA a evitar soluções "preguiçosas" e a entregar código pronto para produção (Enterprise-Grade).
---

## 👨‍💻 Autor

**Emeson Freire** *AI Developer | Prompt Engineer | LLM & Automação com IA | Suporte de Infraestrutura de TI & Redes | analista de sistemas | PCD* Especialista em TI Infrastructure e Engenharia de Redes.
