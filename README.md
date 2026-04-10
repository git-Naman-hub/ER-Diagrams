📌 Overview

This project presents the Entity-Relationship Diagram (ERD) for a smart elevator control platform designed for large-scale infrastructure such as:

Corporate buildings,
Shopping malls,
Airports,
Hospitals,
High-rise residential complexes.

The system is built to manage multiple buildings, each containing multiple elevators operating across many floors, handling thousands of ride requests efficiently.

🧩 Entities & Description


🏢 Buildings
Represents each infrastructure unit

One building contains multiple floors and shafts

🧱 Floors
Belong to a building

Identified by floor number

Used for generating ride requests

🛗 Elevator Shafts

Physical vertical structures inside buildings

Each shaft contains exactly one elevator

🛗 Elevators

Assigned to a shaft

Stores static configuration like capacity and weight limit

🔗 Elevator Floors (Junction Table)

Defines which floors an elevator can serve

Handles many-to-many relationship

🎯 Floor Requests

Represents user intent (source → destination)

Tracks request lifecycle:

pending

assigned

completed

🎟️ Ride Assignments

Maps a request to an elevator

Tracks execution lifecycle:

assigned

in_progress

completed

🛠️ Maintenance Logs

Tracks elevator downtime and issues

Stores start/end time of maintenance events

🔗 Relationships

Key Relationships:

Building → Floors → One-to-Many

Building → Shafts → One-to-Many

Shaft → Elevator → One-to-One

Elevator ↔ Floors → Many-to-Many (via elevator_floors)

Floor → Requests → One-to-Many

Request → Assignment → One-to-One

Elevator → Assignments → One-to-Many

Elevator → Maintenance Logs → One-to-Many
