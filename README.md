# Link‑Us 🩺 — Connecting Doctors, Patients & Pharmacies (Java + MongoDB)

A **desktop application** that creates a seamless link between **doctors, patients, and medical stores** by keeping every patient’s medical record in a single, shareable MongoDB database.  
With Link‑Us, clinicians can instantly retrieve a patient’s history, prescribe medication, and notify the nearest pharmacy—streamlining treatment and reducing paperwork.

> **Tech Stack**  Java 8 • Swing/JavaFX (NetBeans project) • MongoDB • JDBC / MongoDB Java Driver

---

## Key Features

| Module | Highlights |
|--------|------------|
| **Patient** | • Register / update demographic details<br>• View consultation history & prescriptions |
| **Doctor** | • Search patients via ID or name<br>• Add diagnoses & e‑prescriptions<br>• One‑click follow‑up scheduling |
| **Pharmacy** | • Real‑time notification of new prescriptions<br>• Stock management & low‑inventory alerts |
| **Auth & Roles** | Role‑based login for admins, doctors, pharmacists, and patients |
| **Reporting** | Daily appointment logs, drug‑dispense reports, basic analytics (patients per doctor, top diagnoses) |

---

## Project Structure

```
Link-Us/
├── build/                 # NetBeans build artefacts (generated)
├── dist/                  # Packaged application JAR + libraries
├── nbproject/             # NetBeans project metadata (.xml)
└── src/
    └── linkus/            # All Java source packages
        ├── gui/           # Swing UI frames & dialogs
        ├── dao/           # MongoDB data‑access objects
        ├── model/         # Plain‑old Java objects (Patient, Doctor, Drug, …)
        └── util/          # Helpers (DB connection, validators, constants)
```

*(Folder names derived from the repo; some sub‑packages are illustrative placeholders.)*

---

## Getting Started

### 1. Prerequisites

* **JDK 8** or higher  
* **NetBeans IDE 8.x** *(project uses NetBeans build files)*  
* **MongoDB Server 6+** running locally on `mongodb://localhost:27017`  
  *Change the connection string in `src/linkus/util/DBConnection.java` if needed.*

### 2. Clone & Build

```bash
git clone https://github.com/akshay-kamloo/Link-Us.git
cd Link-Us

# NetBeans users:
#   File ▸ Open Project… ▸ select Link-Us
# or build from CLI with Ant:
ant clean dist     # outputs dist/Link-Us.jar
```

### 3. Seed Database *(optional)*

```bash
mongo
> use linkus
> db.patients.insertOne({ _id: "P0001", firstName: "John", lastName: "Doe" })
```

### 4. Run

```bash
java -jar dist/Link-Us.jar
```

---

## Screenshots

| Login | Doctor Dashboard |
|-------|------------------|
| _coming soon_ | _coming soon_ |

*(Feel free to update with fresh screenshots!)*

---

## Contributing

1. Fork → feature branch → Pull Request.  
2. Follow the existing package structure; GUI classes live under `linkus.gui.*`.  
3. Run `ant test` before opening a PR.

---

## License

This project is released under the **MIT License**. See `LICENSE` for details.

---

## Authors & Acknowledgements

**Akshay Kamloo** · **Mayur Kadam** · **Prateek Gupta** (original university capstone).  
Thanks to the MongoDB and NetBeans communities for open‑source tooling that made Link‑Us possible.
