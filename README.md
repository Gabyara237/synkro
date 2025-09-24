# Synkro – Engineer–Company Web Platform

**Synkro** is a full-stack web platform that connects engineers and companies, enabling project collaboration, streamlined hiring workflows, and transparent payments powered by blockchain technology.  

---

## Tech Stack

### Blockchain
- **Solidity** + **OpenZeppelin** (smart contracts)
- **Polygon** (scalable, low fees)
- **Hardhat** (testing & deployment)
- **Ethers.js** (blockchain integration)

### Backend
- **Node.js** + **TypeScript** + **Express**
- **Prisma ORM** + **PostgreSQL**
- RESTful APIs for service communication

### Frontend
- **React** + **TypeScript** + **Vite**
- **TailwindCSS** for responsive UI
- **React Router** for navigation

---

## Core Features (Planned)

- **User Authentication & Roles** (companies, engineers, admins)  
- **Project Management** (publish, apply, hire, complete)  
- **Escrow in MATIC** with automatic release  
- **Blockchain Transparency** for financial transactions  
- **Dashboards & Reporting** for companies, engineers, and admins  
- **Admin Tools** for dispute resolution and oversight  

---

## Business Flow

1. **Project Creation & Escrow Deposit**  
   A company publishes a project and deposits the full amount in **MATIC** into the escrow smart contract.  

2. **Engineer Application & Selection**  
   Engineers apply to the project.  
   The company selects one engineer to execute the work.  

3. **Project Delivery & Completion**  
   The engineer completes work and notifies completion.
   The company reviews and confirms project completion.

4. **Automatic Payment**  
   Once completion is confirmed, the contract automatically releases funds:  
   - **90% → Engineer**  
   - **10% → Platform commission**  

5. **Dispute Handling**  
   If a disagreement arises, a dispute can be created and resolved with admin intervention.  

---

## Data Architecture: On-Chain vs Off-Chain

### On-Chain (Blockchain Contracts)
Handles **critical contractual and financial logic**:
- Create Smart contracts with project reference, company, engineer, and amount (MATIC)  
- Escrow deposit by company  
- Mark project as completed (engineer)  
- Automatic payment release (90% engineer, 10% platform)  
- Dispute creation and resolution (with admin authority)  
- Emergency withdrawal function  

Immutable, transparent, and auditable, ensures trust and accountability.  

### Off-Chain (PostgreSQL)
Handles **operational and user-facing data** for flexibility and privacy:
- User profiles (personal data, credentials, contact info)  
- Projects (title, description, requirements, skills, attachments)  
- Proposals (cover letters, proposed prices, portfolios)  
- Messaging between users  
- Company & engineer dashboards (ratings, experience, stats)  
- Dispute details and resolutions  
- Blockchain sync logs and metadata  

Optimized for fast queries, frequent updates, and scalability while protecting sensitive data.  

---

## 📊 Reporting System

### Monthly Financial Reports
- Total paid to engineers: **X MATIC**  
- Total commissions earned: **Y MATIC**  
- Projects completed: **Z**  
- Average payout per project: **X/Z MATIC**  

### Company Dashboard
- Projects published (per month)  
- Total spent (MATIC)  
- Engineers hired  
- Completed vs pending projects  

### Engineer Dashboard
- Earnings (monthly/yearly)  
- Number of completed projects  
- Average earning per project  
- Payment history  

### Administrative Reports
- Registered users per month  
- Transaction volume  
- Top engineers by earnings  
- Top companies by spending  
- Commissions generated  

---

## Project Status

Currently in **early development**.  
- ✅ Repository initialized with backend structure  
- 🟡 Database design & API endpoint development (in progress)  
- 🔲 Smart contract development & testing  
- 🔲 Backend ↔ Blockchain integration  
- 🔲 Frontend development & integration  
- 🔲 Final testing & validation  

---

## Roadmap (Tutor-Aligned Phases)

1. **Database Design & API Development**  
   - Define schema (**Prisma + PostgreSQL**)  
   - Build & test core REST endpoints (**Express**)  

2. **Smart Contract Development & Testing**  
   - Implement with **Solidity + OpenZeppelin**  
   - Test & deploy via **Hardhat** on **Polygon**  

3. **Backend–Blockchain Integration**  
   - Connect services to contracts via **Ethers.js**  
   - Ensure secure transaction handling & sync logs  

4. **Frontend Development & Integration**  
   - Build UI (**React + Vite + TailwindCSS**)  
   - Implement routing (**React Router**)  
   - Integrate frontend with backend and blockchain APIs  

5. **Final Testing & Validation**  
   - Unit & integration tests across all layers  
   - End-to-end workflow validation  
   - Documentation & deployment  

---

## License
This project is currently in development. Future updates, documentation, and deployment guides will be added as the project evolves.
