# Task Management System 📝

Il **Task Management System** è un'applicazione **Spring Boot** progettata per semplificare la gestione delle attività quotidiane. Grazie a un'interfaccia RESTful, permette agli utenti di **creare**, **aggiornare**, **organizzare** e **monitorare i propri task**, assegnando loro **priorità** e **stati di avanzamento**.

Questa applicazione include un sistema di **autenticazione sicura** basato su **JWT (JSON Web Token)** e un'architettura scalabile, perfetta per l'integrazione con altri sistemi o piattaforme di produttività.

## 🎯 Obiettivi del progetto
- ✅ Offrire una piattaforma flessibile per la gestione delle attività
- ✅ Permettere agli utenti di classificare le attività in base a **stato** e **priorità**
- ✅ Garantire sicurezza e protezione dei dati con **Spring Security** e **JWT**
- ✅ Fornire un'architettura **scalabile** e **modulare**, adatta a future espansioni

## 🚀 Funzionalità
- 🔐 **Autenticazione e autorizzazione** → Registrazione e login con JWT
- 📌 **Creazione e gestione dei task** → CRUD completo per le attività
- 📊 **Stati delle attività** → Suddivise in **PENDING, IN_PROGRESS, COMPLETED, CANCELLED**
- 🔥 **Priorità dei task** → Classificazione in **LOW, MEDIUM, HIGH, PRIORITY**
- 🛡️ **Sicurezza avanzata** → Protezione API con Spring Security
- 📡 **API RESTful** → Facile integrazione con frontend o altre applicazioni

## 🏗 Possibili estensioni future
🔹 Integrazione con **notifiche email** per i task in scadenza 📧
<br>
🔹 Dashboard interattiva con **grafici di produttività** 📊
<br>
🔹 Implementazione di un **ruolo admin** per la gestione degli utenti 👤

## 🛠 Tecnologie Usate
- Java 17 ☕
- Spring Boot 3 🌱
- Spring Security 🔐
- Hibernate & JPA 🗄️
- PostgreSQL/MySQL 📦
- JSON Web Token (JWT) 🏷️

## 📌 Installazione
1. Clona il repository:
   ```sh
   git clone https://github.com/michelealiffi/java-task-management-system.git
   cd task-management-system

2. Configura il database nel file `application.properties`:
   ```ini
   spring.datasource.url=jdbc:mysql://localhost:3306/task_db
   spring.datasource.username=root
   spring.datasource.password=yourpassword

3. Esegui l'applicazione:
   ```sh
   mvn spring-boot:run

## 🛠 API Endpoints
### Autenticazione
| **Metodo** |	**Endpoint** |	**Descrizione** |
|------------|---------------|------------------|
| POST |	`/api/auth/register` |	Registra un nuovo utente |
| POST |	`/api/auth/login` |	Login utente |

### Task
| **Metodo** |	**Endpoint** |	**Descrizione** |
|------------|---------------|------------------|
| GET |	`/api/tasks` |	Ottiene tutti i task |
| POST |	`/api/tasks` |	Crea un nuovo task |
| PUT |	`/api/tasks/{id}` |	Aggiorna un task |
| DELETE |	`/api/tasks/{id}` |	Elimina un task |

## Struttura del Progetto

```
task-management-system/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/
│   │   │   │   ├── example/
│   │   │   │   │   ├── task_management_system/
│   │   │   │   │   │   ├── controller/
|   │   │   │   │   │   │   ├── TaskController.java
|   │   │   │   │   │   │   ├── UserController.java
│   │   │   │   │   │   ├── exception/
|   │   │   │   │   │   │   ├── ResourceNotFoundException.java
│   │   │   │   │   │   ├── model/
|   │   │   │   │   │   │   ├── Task.java
|   │   │   │   │   │   │   ├── TaskPriority.java
|   │   │   │   │   │   │   ├── TaskStatus.java
|   │   │   │   │   │   │   ├── User.java
│   │   │   │   │   │   ├── repository/
|   │   │   │   │   │   │   ├── TaskRepository.java
|   │   │   │   │   │   │   ├── UserRepository.java
│   │   │   │   │   │   ├── service/
|   │   │   │   │   │   │   ├── TaskService.java
|   │   │   │   │   │   │   ├── UserService.java
│   ├── resources/
│   │   ├── application.properties
│   │   ├── static/
│   │   ├── templates/
└── pom.xml or build.gradle
```
