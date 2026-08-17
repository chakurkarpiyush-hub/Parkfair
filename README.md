# ParkFair: Decentralized Parking Allocation Engine

### The Problem
In high-density residential societies, parking allocation is chaotic and informal, leading to disputes and wasted infrastructure. Financial bidding models fail because they make parking a luxury only wealthy residents can afford.

### The Solution
ParkFair is a zero-fiat, credit-based internal allocation system. Residents bid non-monetary points for temporary access to shared parking spots, backed by an algorithmic fairness tiebreaker that prevents resource hoarding. 

### System Architecture
* **Frontend:** React.js (High-frequency API polling for live bid updates)
* **Backend Engine:** Python FastAPI
* **Database:** PostgreSQL (Strict transaction-level locking to prevent double-spending and race conditions)

### Core Features
1. **Algorithmic Fairness:** Uses a wait-time tiebreaker math formula to prioritize residents starved of parking the longest.
2. **Atomic DB Transactions:** Ensures credit deductions and spot allocations happen simultaneously without concurrency errors.
3. **Release Bonus:** Incentivizes traveling owners to temporarily release deeded spots to the community pool in exchange for credits.

*Note: Full architectural documentation, database schema (DDL), and API endpoint designs are available in the attached project document.*
