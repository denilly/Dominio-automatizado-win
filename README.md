# DominioAutomatizado.ps1

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![SO](https://img.shields.io/badge/SO-Windows-deepskyblue.svg?logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pgo8IS0tIEdlbmVyYXRvcjogQWRvYmUgSWxsdXN0cmF0b3IgMTguMC4wLCBTVkcgRXhwb3J0IFBsdWctSW4gLiBTVkcgVmVyc2lvbjogNi4wMCBCdWlsZCAwKSAgLS0+CjwhRE9DVFlQRSBzdmcgUFVCTElDICItLy9XM0MvL0RURCBTVkcgMS4xLy9FTiIgImh0dHA6Ly93d3cudzMub3JnL0dyYXBoaWNzL1NWRy8xLjEvRFREL3N2ZzExLmR0ZCI+CjxzdmcgdmVyc2lvbj0iMS4xIiBpZD0iQ2FwYV8xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB4PSIwcHgiIHk9IjBweCIKCSB2aWV3Qm94PSIwIDAgMzcwIDM3MCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgMzcwIDM3MDsiIHhtbDpzcGFjZT0icHJlc2VydmUiPgo8Zz4KCTxwYXRoIGZpbGw9IiNmZmYiIGQ9Ik0zNjguMjk3LDQ1Ljc2N2MtMS40NTYtMS4yNzgtMy41Mi0xLjU5OC01LjI5OC0wLjgyNGMtMjEuNzUxLDkuNDk3LTQyLjU5OSwxNC4xMTMtNjMuNzM0LDE0LjExMwoJCWMtMTcuMzE4LDAtMzUuNDQ1LTIuOTg2LTU4Ljc3Ni05LjY4MmMtMi42NTktMC43NjUtNS40MTksMC43Ny02LjE4MywzLjQybC0zNC4zOCwxMTkuMTE5Yy0wLjM2OCwxLjI3NS0wLjIxNCwyLjY0NSwwLjQyOCwzLjgwNgoJCWMwLjY0MywxLjE2MiwxLjcyMSwyLjAyLDIuOTk2LDIuMzg3YzI0LjI2LDYuOTYzLDQzLjIzNywxMC4wNjksNjEuNTMxLDEwLjA2OWgwLjAwMWMtMjIuNTM4LDAsNDQuNjk3LTQuODg5LDY3LjczOS0xNC45NDYKCQljMS4zNjMtMC41OTUsMi4zOTItMS43NjcsMi44MDQtMy4xOTZsMzQuMzc5LTExOS4xMjFDMzcwLjM0Miw0OS4wNTEsMzY5Ljc1NCw0Ny4wNDUsMzY4LjI5Nyw0NS43Njd6Ii8+Cgk8cGF0aCBmaWxsPSIjZmZmIiBkPSJNNDguODIsMTczLjY0N2MwLjY3NiwwLDEuMzU2LTAuMTM3LDItMC40MTdjMjEuNzUxLTkuNDk3LDQyLjU5OS0xNC4xMTMsNjMuNzMyLTE0LjExM2MxNy4zMTcsMCwzNS40NDQsMi45ODYsNTguNzc2LDkuNjgyCgkJYzIuNjUyLDAuNzYxLDUuNDE4LTAuNzcsNi4xODItMy40MTlMMjEzLjg5LDQ2LjI2YzAuMzY4LTEuMjc1LDAuMjE0LTIuNjQ1LTAuNDI4LTMuODA2Yy0wLjY0My0xLjE2Mi0xLjcyMi0yLjAyLTIuOTk2LTIuMzg3CgkJYy0yNC4yNjUtNi45NjUtNDMuMjQzLTEwLjA3MS02MS41MzQtMTAuMDcxYy0yMi41MzksMC00NC42OTUsNC44ODktNjcuNzM0LDE0Ljk0N2MtMS4zNjQsMC41OTUtMi4zOTIsMS43NjctMi44MDUsMy4xOTYKCQlMNDQuMDE1LDE2Ny4yNmMtMC41MzgsMS44NjIsMC4wNSwzLjg2NywxLjUwNyw1LjE0NUM0Ni40NTEsMTczLjIyMSw0Ny42MjcsMTczLjY0Nyw0OC44MiwxNzMuNjQ3eiIvPgoJPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTE2OS42NDMsMTk0LjI4MmMtMC42NDItMS4xNjItMS43MjEtMi4wMi0yLjk5Ni0yLjM4NmMtMjQuMjY2LTYuOTY0LTQzLjI0NC0xMC4wNy02MS41MzUtMTAuMDcKCQljLTIyLjUzOSwwLTQ0LjY5Myw0Ljg4OS02Ny43MzIsMTQuOTQ2Yy0xLjM2NCwwLjU5NS0yLjM5MiwxLjc2Ny0yLjgwNCwzLjE5NkwwLjE5NywzMTkuMDg5Yy0wLjUzOCwxLjg2MiwwLjA1LDMuODY3LDEuNTA3LDUuMTQ1CgkJYzAuOTMsMC44MTUsMi4xMDYsMS4yNDEsMy4yOTgsMS4yNDFjMC42NzYsMCwxLjM1Ni0wLjEzNywyLTAuNDE3YzIxLjc1MS05LjQ5Nyw0Mi41OTktMTQuMTEzLDYzLjczMy0xNC4xMTMKCQljMTcuMzE4LDAsMzUuNDQ1LDIuOTg2LDU4Ljc3NSw5LjY4M2MyLjY1NiwwLjc2LDUuNDE5LTAuNzcxLDYuMTg0LTMuNDJsMzQuMzc4LTExOS4xMTkKCQlDMTcwLjQ0LDE5Ni44MTQsMTcwLjI4NSwxOTUuNDQ0LDE2OS42NDMsMTk0LjI4MnoiLz4KCTxwYXRoIGZpbGw9IiNmZmYiIGQ9Ik0zMTkuMTgyLDE5Ni43NzJjLTIxLjc1MSw5LjQ5Ny00Mi41OTksMTQuMTEzLTYzLjczMywxNC4xMTNjLTE3LjMxNiwwLTM1LjQ0NC0yLjk4Ni01OC43NzgtOS42ODIKCQljLTIuNjU1LTAuNzYyLTUuNDE5LDAuNzY5LTYuMTgzLDMuNDE5bC0zNC4zNzgsMTE5LjEyYy0wLjM2OSwxLjI3NS0wLjIxNSwyLjY0NSwwLjQyOCwzLjgwNmMwLjY0MiwxLjE2MiwxLjcyLDIuMDIsMi45OTYsMi4zODYKCQljMjQuMjYyLDYuOTYzLDQzLjIzOCwxMC4wNjgsNjEuNTI5LDEwLjA2OGMyMi41MzksMCw0NC42OTctNC44ODksNjcuNzQtMTQuOTQ2YzEuMzYzLTAuNTk1LDIuMzkxLTEuNzY3LDIuODA0LTMuMTk2bDM0LjM4LTExOS4xMjEKCQljMC41MzktMS44NjItMC4wNS0zLjg2OC0xLjUwNy01LjE0NkMzMjMuMDIzLDE5Ni4zMTksMzIwLjk2LDE5NS45OTgsMzE5LjE4MiwxOTYuNzcyeiIvPgo8L2c+Cjwvc3ZnPgo=)
![License](https://img.shields.io/badge/license-GPL--3.0-green.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)

## Descrição

Script para automatizar o ingresso de computadores no domínio Active Directory, com funcionalidades adicionais de movimentação para a Unidade Organizacional (OU) específica e adição ao grupo de segurança correspondente em ambiente Microsoft Windows.

> ✅ **Funcionalidades:**
>
> * Ingresso automático no domínio.
> * Movimentação do objeto de computador para a OU definida.
> * Adição ao grupo de segurança especificado.
> * Interface gráfica interativa (GUI) para preenchimento de informações.
> * Compatível com PowerShell 5.1 e 7+ (pode ser empacotado em .EXE).
> * Detecção automática de Domain Controllers (DCs) disponíveis via LDAPS.

---

## Autor

**Denilly Carvalho do Carmo**

📅 **Data de criação:** 11/12/2025

©️ **Copyright:** 2025 Denilly Carvalho do Carmo.

🛡️ **Licença:** GNU General Public License (GPL-3.0).

---

## Notas

Este script é fornecido "**como está**" e pode ser utilizado e modificado por terceiros, desde que os **créditos ao autor sejam mantidos**. Para uso em projetos, por favor, faça referência a este script e ao autor.

### Importante

* O script é executado diretamente e abre uma **interface gráfica** para preenchimento de campos obrigatórios (ex.: domínio, usuário, senha, tipo de equipamento e OU).
* Não requer argumentos de linha de comando, mas pode ser adaptado para execução silenciosa se necessário.
* Ajuste as configurações iniciais no código-fonte (ex.: mapeamento de OUs e grupos) conforme o seu ambiente Active Directory.
* Logs são exibidos na interface gráfica durante a execução para monitoramento em tempo real.

---

## Como usar

### 1. Criar o arquivo do script

```bash
notepad C:\caminho\para\os\seus\scripts\DominioAutomatizado.ps1
```

Cole o código `.ps1` deste repositório no editor. Ajuste os parâmetros indicados com `<--` conforme a necessidade (ex.: mapeamento de OUs e grupos) e salve.

> **💡 Importante:** Utilize codificação de caracteres UTF-8 com BOM para compatibilidade com PowerShell 5.1 e 7+ na criação do arquivo para a correta interpretação dos textos!

---

### 2. Checar políticas de execução de scripts no PowerShell, e, se necessário, ajustar conforme sua política interna:

```bash
Get-ExecutionPolicy -List
```

```bash
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force
```

---

### 3. Executar o script

```bash
.\DominioAutomatizado.ps1
```

> Isso abrirá a interface gráfica. Preencha os campos e clique em "INGRESSAR NO DOMÍNIO". O script executará as etapas automaticamente, exibindo logs na tela.

---

### 4. Recomendação

Mantenha uma cópia de segurança deste script no seu diretório de backup. Para ambientes de produção, teste em uma máquina de laboratório antes de aplicar em massa.

---

### 5. Geração de executável (.EXE)

Para facilitar a distribuição ao seu time de Suporte e assim executarem em máquinas de usuário, recomenda-se gerar um arquivo executável (.EXE).

**Instruções detalhadas, incluindo o uso de auto-py-to-exe (interface gráfica para PyInstaller), estão disponíveis na [Wiki do repositório](https://github.com/denilly/Dominio-automatizado-win/wiki).**

---

## Exemplos de uso

### Execução interativa (padrão):

```bash
C:\seu\caminho\para\o\script\DominioAutomatizado.ps1
```

> Abre a GUI para preenchimento manual. Após o processo, o script oferece a opção de reinício automático (recomendado para aplicar as mudanças).

### Execução do EXE gerado:

Basta clicar duas vezes no arquivo `.exe` gerado (seguindo as instruções da Wiki). Ele solicitará privilégios de administrador automaticamente.

---

## Contribuição

Contribuições são bem-vindas!
Sugestões, melhorias ou correções podem ser enviadas via **pull requests** ou **issues** neste repositório.

---

## Licença

Este projeto está licenciado sob a **GNU General Public License v3.0**.

---

</ul>
</body>
</html>
