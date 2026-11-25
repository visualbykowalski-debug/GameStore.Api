# GameStore API

A backend web service built with **C# and ASP.NET Core (.NET 10)** that powers the catalog management of a digital video game store. It allows applications to create, browse, update, and remove games and genres while storing data reliably in a relational database.

## Live Demonstration :
A quick 45-second intro video, showcasing API walkthrough: link coming soon!

## Key Capabilities :
- **Catalog Management (CRUD):** Handles the full lifecycle of game listings-adding new titles, retrieving individual or full catalog lists, updating pricing and removing entries.
- **Genre Categorization:** Organizes games into structured categories through a dedicated relational database model.
- **Data Integrity & Validation:** Uses structured Data Transfer Objects (DTOs) and input validation rules to ensure only clean, valid data enters the system.
- **Automated Database Setup:** Automatically applies database migrations on startup so the data schema stays consistent without manual intervention.
  
## Technologies Used : 
- **Language & Framework:** C#, .NET 10, ASP.NET Core (Minimal APIs)
- **Database & Data Access:** Entity Framework Core, SQLite (Relational Database)
- **API Testing:** REST Client (`games.http`)

## How the Project is Organized
- **`Endpoints/`** - Defines the public web routers where the external apps request or send game and genre data.
- **`Dtos/`** - Controls the exact shape of data entering and leaving the API, keeping internal database models protected.
- **`Models/`** - Represents the core business entities (`Game` and `Genre`).
- **`Data/`** - Manages the database connection, table relationships, and schema migrations.

## API Overview

| Action | Method | Route | What It Does |
| :--- | :--- | :--- | :--- |
| **List all games** | `GET` | `/games` | Returns the complete catalog of registered games |
| **Find a game** | `GET` | `/games/{id}` | Looks up details for one specific game |
| **Add a game** | `POST` | `/games` | Validates and saves a new game to the catalog |
| **Edit a game** | `PUT` | `/games/{id}` | Updates details of an existing game |
| **Remove a game** | `DELETE` | `/games/{id}` | Deletes a game from the catalog |
| **List genres** | `GET` | `/genres` | Returns all available game genres |

## Acknowledgements 
Built while completing the *"ASP.NET Core Full Course (.NET 10)"* by [Julio Casal](https://www.youtube.com/@juliocasal) to practice backend architecture, RESTful API design, and relational database modeling.