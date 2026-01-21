# Dominio Automatizado – Active Directory - v2.1

![Version](https://img.shields.io/badge/version-2.1-blue.svg)
![SO](https://img.shields.io/badge/SO-Windows-deepskyblue.svg?logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pgo8IS0tIEdlbmVyYXRvcjogQWRvYmUgSWxsdXN0cmF0b3IgMTguMC4wLCBTVkcgRXhwb3J0IFBsdWctSW4gLiBTVkcgVmVyc2lvbjogNi4wMCBCdWlsZCAwKSAgLS0+CjwhRE9DVFlQRSBzdmcgUFVCTElDICItLy9XM0MvL0RURCBTVkcgMS4xLy9FTiIgImh0dHA6Ly93d3cudzMub3JnL0dyYXBoaWNzL1NWRy8xLjEvRFREL3N2ZzExLmR0ZCI+CjxzdmcgdmVyc2lvbj0iMS4xIiBpZD0iQ2FwYV8xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB4PSIwcHgiIHk9IjBweCIKCSB2aWV3Qm94PSIwIDAgMzcwIDM3MCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgMzcwIDM3MDsiIHhtbDpzcGFjZT0icHJlc2VydmUiPgo8Zz4KCTxwYXRoIGZpbGw9IiNmZmYiIGQ9Ik0zNjguMjk3LDQ1Ljc2N2MtMS40NTYtMS4yNzgtMy41Mi0xLjU5OC01LjI5OC0wLjgyNGMtMjEuNzUxLDkuNDk3LTQyLjU5OSwxNC4xMTMtNjMuNzM0LDE0LjExMwoJCWMtMTcuMzE4LDAtMzUuNDQ1LTIuOTg2LTU4Ljc3Ni05LjY4MmMtMi42NTktMC43NjUtNS40MTksMC43Ny02LjE4MywzLjQybC0zNC4zOCwxMTkuMTE5Yy0wLjM2OCwxLjI3NS0wLjIxNCwyLjY0NSwwLjQyOCwzLjgwNgoJCWMwLjY0MywxLjE2MiwxLjcyMSwyLjAyLDIuOTk2LDIuMzg3YzI0LjI2LDYuOTYzLDQzLjIzNywxMC4wNjksNjEuNTMxLDEwLjA2OWgwLjAwMWMtMjIuNTM4LDAsNDQuNjk3LTQuODg5LDY3LjczOS0xNC45NDYKCQljMS4zNjMtMC41OTUsMi4zOTItMS43NjcsMi44MDQtMy4xOTZsMzQuMzc5LTExOS4xMjFDMzcwLjM0Miw0OS4wNTEsMzY5Ljc1NCw0Ny4wNDUsMzY4LjI5Nyw0NS43Njd6Ii8+Cgk8cGF0aCBmaWxsPSIjZmZmIiBkPSJNNDguODIsMTczLjY0N2MwLjY3NiwwLDEuMzU2LTAuMTM3LDItMC40MTdjMjEuNzUxLTkuNDk3LDQyLjU5OS0xNC4xMTMsNjMuNzMyLTE0LjExM2MxNy4zMTcsMCwzNS40NDQsMi45ODYsNTguNzc2LDkuNjgyCgkJYzIuNjUyLDAuNzYxLDUuNDE4LTAuNzcsNi4xODItMy40MTlMMjEzLjg5LDQ2LjI2YzAuMzY4LTEuMjc1LDAuMjE0LTIuNjQ1LTAuNDI4LTMuODA2Yy0wLjY0My0xLjE2Mi0xLjcyMi0yLjAyLTIuOTk2LTIuMzg3CgkJYy0yNC4yNjUtNi45NjUtNDMuMjQzLTEwLjA3MS02MS41MzQtMTAuMDcxYy0yMi41MzksMC00NC42OTUsNC44ODktNjcuNzM0LDE0Ljk0N2MtMS4zNjQsMC41OTUtMi4zOTIsMS43NjctMi44MDUsMy4xOTYKCQlMNDQuMDE1LDE2Ny4yNmMtMC41MzgsMS44NjIsMC4wNSwzLjg2NywxLjUwNyw1LjE0NUM0Ni40NTEsMTczLjIyMSw0Ny42MjcsMTczLjY0Nyw0OC44MiwxNzMuNjQ3eiIvPgoJPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTE2OS42NDMsMTk0LjI4MmMtMC42NDItMS4xNjItMS43MjEtMi4wMi0yLjk5Ni0yLjM4NmMtMjQuMjY2LTYuOTY0LTQzLjI0NC0xMC4wNy02MS41MzUtMTAuMDcKCQljLTIyLjUzOSwwLTQ0LjY5Myw0Ljg4OS02Ny43MzIsMTQuOTQ2Yy0xLjM2NCwwLjU5NS0yLjM5MiwxLjc2Ny0yLjgwNCwzLjE5NkwwLjE5NywzMTkuMDg5Yy0wLjUzOCwxLjg2MiwwLjA1LDMuODY3LDEuNTA3LDUuMTQ1CgkJYzAuOTMsMC44MTUsMi4xMDYsMS4yNDEsMy4yOTgsMS4yNDFjMC42NzYsMCwxLjM1Ni0wLjEzNywyLTAuNDE3YzIxLjc1MS05LjQ5Nyw0Mi41OTktMTQuMTEzLDYzLjczMy0xNC4xMTMKCQljMTcuMzE4LDAsMzUuNDQ1LDIuOTg2LDU4Ljc3NSw5LjY4M2MyLjY1NiwwLjc2LDUuNDE5LTAuNzcxLDYuMTg0LTMuNDJsMzQuMzc4LTExOS4xMTkKCQlDMTcwLjQ0LDE5Ni44MTQsMTcwLjI4NSwxOTUuNDQ0LDE2OS42NDMsMTk0LjI4MnoiLz4KCTxwYXRoIGZpbGw9IiNmZmYiIGQ9Ik0zMTkuMTgyLDE5Ni43NzJjLTIxLjc1MSw5LjQ5Ny00Mi41OTksMTQuMTEzLTYzLjczMywxNC4xMTNjLTE3LjMxNiwwLTM1LjQ0NC0yLjk4Ni01OC43NzgtOS42ODIKCQljLTIuNjU1LTAuNzYyLTUuNDE5LDAuNzY5LTYuMTgzLDMuNDE5bC0zNC4zNzgsMTE5LjEyYy0wLjM2OSwxLjI3NS0wLjIxNSwyLjY0NSwwLjQyOCwzLjgwNmMwLjY0MiwxLjE2MiwxLjcyLDIuMDIsMi45OTYsMi4zODYKCQljMjQuMjYyLDYuOTYzLDQzLjIzOCwxMC4wNjgsNjEuNTI5LDEwLjA2OGMyMi41MzksMCw0NC42OTctNC44ODksNjcuNzQtMTQuOTQ2YzEuMzYzLTAuNTk1LDIuMzkxLTEuNzY3LDIuODA0LTMuMTk2bDM0LjM4LTExOS4xMjEKCQljMC41MzktMS44NjItMC4wNS0zLjg2OC0xLjUwNy01LjE0NkMzMjMuMDIzLDE5Ni4zMTksMzIwLjk2LDE5NS45OTgsMzE5LjE4MiwxOTYuNzcyeiIvPgo8L2c+Cjwvc3ZnPgo=)
![License](https://img.shields.io/badge/license-GPL--3.0-green.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)

<p align="center">
 <img width="400" alt="Formulário de inserção no domínio" src="https://github.com/user-attachments/assets/89d7f4d6-875a-4588-9f15-72402c0bc8ba" />
</p>

---

## Descrição

Script PowerShell para automatizar o ingresso de computadores no domínio **Active Directory**, com funcionalidades adicionais de **movimentação para Unidade Organizacional (OU)**, **gerenciamento de grupos de segurança** e **padronização da descrição do equipamento**, em ambiente Microsoft Windows.

A versão **2.1** introduz melhorias focadas em **segurança**, **robustez operacional** e **confiabilidade**, mantendo compatibilidade total com versões anteriores.

> ✅ **Funcionalidades:**
>
> * Ingresso automático no domínio Active Directory.
> * Detecção automática se o computador já está ingressado no domínio.
> * Alteração opcional do hostname, com validações conforme padrão Microsoft.
> * Movimentação automática do objeto do computador para a OU selecionada.
> * Gerenciamento de grupos de segurança:
>
>   * Adiciona o computador ao grupo correspondente à OU.
>   * Remove automaticamente de outros grupos gerenciados pelo script.
> * Definição e aplicação da **Descrição do equipamento**, tanto no Windows quanto no Active Directory.
> * Interface gráfica em formato **Wizard** (GUI moderna e orientada ao time de suporte).
> * **Sistema de ajuda contextual integrado (botão “?”)**:
>
>   * Permite ao operador clicar no botão de ajuda da janela e, em seguida, em qualquer campo do formulário.
>   * Exibe orientações rápidas e objetivas sobre o preenchimento correto de cada campo.
> * Logs detalhados em tempo real na interface.
> * **Geração opcional de log em arquivo**, com seleção interativa do diretório de salvamento.
> * Comunicação segura com o Active Directory:
>
>   * Prioriza **LDAPS (porta 636 – SSL/TLS)** quando disponível.
>   * **Fallback automático para LDAP seguro (porta 389 com signing)** quando o cliente ainda não possui o certificado da CA do domínio.
> * Garantia de limpeza das credenciais em memória ao final da execução.
> * Controle aprimorado do fluxo de reinicialização, assegurando a execução completa do bloco de finalização.
> * Compatível com **PowerShell 5.1 e PowerShell 7+**.

---

## Autor

**Denilly Carvalho do Carmo**

📅 **Data de criação:** 11/12/2025
📅 **Última atualização:** 01/2026

©️ **Copyright:** 2026 Denilly Carvalho do Carmo

🛡️ **Licença:** GNU General Public License (GPL-3.0)

🔗 **Repositório:**
[https://github.com/denilly/Dominio-automatizado-win](https://github.com/denilly/Dominio-automatizado-win)

---

## Notas

Este script é fornecido **“como está”** e pode ser utilizado e modificado por terceiros, desde que os **créditos ao autor sejam mantidos**. Para uso em projetos corporativos ou acadêmicos, faça referência a este repositório e ao autor.

### Padronização da Descrição do Equipamento

O campo **Descrição do equipamento** segue um padrão institucional e é **fundamental** para:

* Inventário e auditoria de ativos.
* Identificação rápida da localização e função do equipamento.
* Padronização, organização e governança do Active Directory.
* Apoio direto ao trabalho do time de Suporte e Infraestrutura.

---

## Importante

* O script é executado diretamente e abre uma **interface gráfica (GUI)** para preenchimento dos campos obrigatórios (domínio, tipo de equipamento, OU e descrição).
* As credenciais de domínio são solicitadas de forma segura via `Get-Credential`, **não sendo digitadas diretamente na interface**.
* Não requer parâmetros de linha de comando.
* Pode ser adaptado para execução silenciosa, se necessário.
* As configurações iniciais (mapeamento de OUs e grupos) devem ser ajustadas no código-fonte conforme o ambiente Active Directory.
* Logs são exibidos em tempo real na interface e **podem ser gravados em arquivo opcionalmente**.

---

## Requisitos

* Sistema operacional: **Windows 10 / 11 / Windows Server**
* PowerShell **5.1 ou superior**
* Execução com **privilégios de Administrador**
* Conectividade com o Active Directory
* Conta com permissões para:

  * Ingressar computadores no domínio
  * Mover objetos de computador entre OUs
  * Gerenciar associação a grupos

---

## Como usar

### 1. Criar o arquivo do script

```bash
notepad C:\caminho\para\os\seus\scripts\DominioAutomatizado.ps1
```

Cole o código `.ps1` deste repositório no editor, ajuste os parâmetros indicados com `<--` (ex.: mapeamento de OUs e grupos) e salve o arquivo.

> 💡 **Importante:**
> Utilize codificação **UTF-8 com BOM** para garantir compatibilidade com PowerShell 5.1 e 7+.

---

### 2. Verificar a política de execução de scripts

```bash
Get-ExecutionPolicy -List
```

Caso necessário:

```bash
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force
```

---

### 3. Executar o script

```bash
.\DominioAutomatizado.ps1
```

> ⚠️ **Atenção:**
> O script verifica automaticamente se está sendo executado como **Administrador**.
> Caso contrário, a execução é interrompida com mensagem informativa.

Ao executar, será aberta a interface gráfica. Preencha os campos solicitados e clique em **“INGRESSAR NO DOMÍNIO”**. O processo será executado automaticamente, com logs exibidos na tela.

---

## Geração de executável (.EXE)

Para facilitar a distribuição ao time de Suporte, é possível gerar um executável `.EXE` a partir do script.

📘 **Instruções detalhadas**, incluindo o uso de ferramentas gráficas para empacotamento, estão disponíveis na Wiki do repositório:
[https://github.com/denilly/Dominio-automatizado-win/wiki](https://github.com/denilly/Dominio-automatizado-win/wiki)

---

## Exemplos de uso

### Execução interativa (padrão)

```bash
C:\seu\caminho\para\o\script\DominioAutomatizado.ps1
```

> Abre a GUI para preenchimento manual.
> Ao final, o script oferece a opção de **reinício automático**, recomendada para aplicação completa das alterações.

### Execução do EXE gerado

Basta executar o arquivo `.exe` gerado. O UAC solicitará privilégios de administrador automaticamente.

---

## Contribuição

Contribuições são bem-vindas!
Sugestões, melhorias ou correções podem ser enviadas via **issues** ou **pull requests** neste repositório.

---

## Licença

Este projeto está licenciado sob a **GNU General Public License v3.0**.

---
