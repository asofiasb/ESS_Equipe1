# Sistema de Reserva de Salas e Equipamentos - Equipe 1

Este repositório contém o monorepo do projeto desenvolvido para a disciplina de **Engenharia de Software e Sistemas (ESS)**, lecionada pelo professor **Breno Miranda** no período **2026.1** no **CIn - UFPE**.

## 📌 O Projeto
A aplicação tem como objetivo principal gerenciar a reserva de salas e computadores de laboratório, além de permitir solicitações de manutenção. O sistema atende a diferentes perfis de usuários (Discentes, Docentes e Administradores) com fluxos de aprovação integrados.

---

## 🛠 Stack Tecnológica

O projeto foi construído utilizando tecnologias modernas para garantir escalabilidade e simplicidade:

* **Frontend:** React, JavaScript e CSS puro.
* **Backend:** FastAPI (Python).
* **Banco de Dados:** (Definir conforme implementação, ex: PostgreSQL/SQLite).

---

## 👥 Perfis de Usuário e Funcionalidades

### 🎓 Usuários (Discentes e Docentes)
* **Cadastro e Perfil:** Registro obrigatório com CPF, nome, senha e vínculo.
    * **Discentes:** Devem informar Curso e Matrícula.
    * **Docentes:** Devem informar o SIAPE.
* **Reservas:** Efetuar, editar, cancelar e visualizar o histórico de reservas de salas ou computadores.
* **Solicitações (Docentes):** Criar solicitações de manutenção para salas específicas.
* **Avaliações:** Realizar reviews de salas e equipamentos.

### 🔑 Administradores
* **Gestão de Salas:** Cadastro (Nome, Capacidade, Descrição e total de Computadores), edição e remoção de salas.
* **Moderação:** Confirmar ou negar reservas e solicitações de manutenção.
* **Controle de Manutenção:** Definir períodos de manutenção, o que bloqueia automaticamente novas reservas e nega pendências existentes.

---

## 📋 Regras de Negócio Importantes

* **Prioridade:** Reservas feitas por professores têm prioridade visual na fila de aprovação do administrador.
* **Restrição de Horário:** Um usuário só pode possuir **uma única reserva** por data/horário].
* **Edição/Cancelamento:** Só é permitido editar ou cancelar reservas e solicitações que ainda estejam com o status **Pendente**.
* **Estados da Reserva:**
    1.  **Pendente:** Aguardando admin.
    2.  **Confirmada:** Aprovada pelo admin.
    3.  **Negada:** Rejeitada pelo admin.
    4.  **Concluída:** Quando o horário da reserva confirmada já passou.
* **Segurança:** O login é realizado via CPF e Senha (máximo 128 caracteres). Não há recuperação de senha ou foto de perfil.

---

## 🗂️ Estrutura de Dados (Principais Objetos)

| Objeto | Atributos Principais |
| :--- | :--- |
| **Sala** | Nome, Capacidade, Descrição, Qtd Computadores, Status Manutenção |
| **Usuário** | Nome, CPF, Senha, Tipo (Docente/Discente), SIAPE/Matrícula, Curso |
| **Reserva de Sala** | Usuário, Sala, Horário Início, Horário Fim, Status |
| **Reserva de Computador** | Usuário, Sala, Qtd Computadores, Horário Início/Fim, Status |
| **Solicitação Manutenção**| Usuário, Sala, Descrição, Data Início/Fim |

---

## 🚀 Como Executar (Em breve)

*(Espaço reservado para instruções de `npm install`, `pip install -r requirements.txt`, etc)*

---
**Equipe 1 - ESS 2026.1**
