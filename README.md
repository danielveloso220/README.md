# 🏥 ClínicaApp

## 📌 Status do projeto
> Em desenvolvimento 🚧  

---

## 💻 Tecnologias utilizadas
- **Java 17**
- **Swing (interfaces gráficas)**
- **MySQL**
- **JDBC**
- **Git/GitHub**

---

## 👥 Time de desenvolvedores
- Daniel Veloso (Projeto Integrador - Etapa 5)

---

## 🎯 Objetivo
O **ClínicaApp** é um sistema desktop desenvolvido em **Java** para auxiliar no gerenciamento de uma clínica médica.  
Ele permite **controle de usuários, cadastro de pacientes e agendamento de consultas**, oferecendo uma interface simples e eficiente.

---

## ⚙️ Funcionalidades principais
- ✅ **Login de usuários** (com autenticação no banco de dados)  
- ✅ **Cadastro de pacientes** (inserir, listar e gerenciar)  
- ✅ **Agendamento de consultas** (criar e visualizar)  
- ✅ **Conexão com banco de dados MySQL**  
- ✅ **Interface desktop em Java Swing**

---

## 📂 Estrutura do projeto

---

## 🖼️ Telas do sistema
- Tela de **Login**  
- Tela de **Gerenciamento de Pacientes**  
- Tela de **Gerenciamento de Consultas**  

---

## 🛠️ Como executar
1. Clone este repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/ClinicaApp.git
   
---

cd "C:/Users/danie/Documentos/ClinicaApp"


# 1) Remover o ZIP do GitHub (se ainda estiver lá)
git rm --cached "atividade 5.zip"
git commit -m "Removendo arquivo zip do repositório"
git push

# 2) Adicionar todo o código-fonte real
git add .
git commit -m "Subindo código-fonte do ClinicaApp"
git push

# 3) Criar pasta de banco e adicionar script SQL
mkdir database
echo "-- Script do banco clinicaapp
CREATE DATABASE IF NOT EXISTS clinicaapp;
USE clinicaapp;

DROP TABLE IF EXISTS usuarios;
CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    senha VARCHAR(50) NOT NULL
);

INSERT INTO usuarios (username, senha) VALUES 
('admin', '123'),
('joao', 'senha123');

DROP TABLE IF EXISTS pacientes;
CREATE TABLE pacientes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    cpf VARCHAR(15) NOT NULL UNIQUE
);

INSERT INTO pacientes (nome, cpf) VALUES
('Maria Silva', '11111111111'),
('Carlos Souza', '22222222222');

DROP TABLE IF EXISTS consultas;
CREATE TABLE consultas (
    id INT AUTO_INCREMENT PRIMARY KEY,
    paciente VARCHAR(100) NOT NULL,
    data VARCHAR(20) NOT NULL
);

INSERT INTO consultas (paciente, data) VALUES
('Maria Silva', '2025-09-22'),
('Carlos Souza', '2025-09-25');" > database/clinicaapp.sql

# 4) Adicionar script ao repositório
git add database/clinicaapp.sql
git commit -m "Adicionado script SQL do banco clinicaapp"
git push

# 5) Conferir histórico de commits
git log --oneline
