# 🧪 Laboratório: Criação de Máquina Virtual no Microsoft Azure

Este repositório documenta o processo de criação e configuração de uma máquina virtual (VM) no Microsoft Azure, com o objetivo de praticar e consolidar conhecimentos sobre a plataforma.

## 📋 Sumário

- [🎯 Objetivo](#-objetivo)
- [🛠️ Pré-requisitos](#-pré-requisitos)
- [🚀 Passo a Passo](#-passo-a-passo)
  - [1. Acessar o Portal do Azure](#1-acessar-o-portal-do-azure)
  - [2. Criar uma Nova Máquina Virtual](#2-criar-uma-nova-máquina-virtual)
  - [3. Configurar os Detalhes da Instância](#3-configurar-os-detalhes-da-instância)
  - [4. Configurar a Conta de Administrador](#4-configurar-a-conta-de-administrador)
  - [5. Configurar as Regras de Porta de Entrada](#5-configurar-as-regras-de-porta-de-entrada)
  - [6. Revisar e Criar](#6-revisar-e-criar)
  - [7. Conectar-se à VM via RDP](#7-conectar-se-à-vm-via-rdp)
  - [8. Instalar o Servidor Web IIS (Opcional)](#8-instalar-o-servidor-web-iis-opcional)


## 🎯 Objetivo

Praticar o processo de criação e configuração de uma máquina virtual na plataforma Microsoft Azure, documentando cada etapa para facilitar revisões futuras e auxiliar outros estudantes ou profissionais interessados no tema.

## 🛠️ Pré-requisitos

- Conta ativa no [Microsoft Azure](https://azure.microsoft.com/pt-br/free/)
- Acesso ao [Portal do Azure](https://portal.azure.com/)
- Cliente de Área de Trabalho Remota (RDP) instalado

## 🚀 Passo a Passo

### 1. Acessar o Portal do Azure

- Navegue até [https://portal.azure.com](https://portal.azure.com) e faça login com sua conta Microsoft.

### 2. Criar uma Nova Máquina Virtual

- No menu lateral, clique em **"Máquinas virtuais"**.
- Clique em **"Criar"** e selecione **"Máquina virtual"**.

### 3. Configurar os Detalhes da Instância

- **Nome da máquina virtual**: `myVM`
- **Região**: Selecione a região mais próxima de você.
- **Imagem**: `Windows Server 2022 Datacenter: Azure Edition - x64 Gen2`
- **Tamanho**: Escolha um tamanho adequado às suas necessidades.

### 4. Configurar a Conta de Administrador

- **Nome de usuário**: `azureuser`
- **Senha**: Insira uma senha segura (mínimo de 12 caracteres, incluindo letras maiúsculas, minúsculas, números e símbolos).

### 5. Configurar as Regras de Porta de Entrada

- **Permitir portas selecionadas**: Marque as opções **RDP (3389)** e **HTTP (80)**.

### 6. Revisar e Criar

- Clique em **"Revisar + criar"**.
- Após a validação, clique em **"Criar"** para iniciar a implantação da VM.

### 7. Conectar-se à VM via RDP

- Após a implantação, vá para a página da VM no portal.
- Clique em **"Conectar"** e selecione **"RDP"**.
- Baixe o arquivo `.rdp` e abra-o para iniciar a conexão.
- Insira as credenciais configuradas anteriormente.

### 8. Instalar o Servidor Web IIS (Opcional)

- Conecte-se à VM via RDP.
- Abra o **PowerShell** como administrador.
- Execute o seguinte comando:

  ```powershell
  Install-WindowsFeature -name Web-Server -IncludeManagementTools
