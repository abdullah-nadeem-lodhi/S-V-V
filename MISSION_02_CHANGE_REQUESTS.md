# Mission 2: Mission Control Sends Change Requests
## UPDATE FROM MISSION CONTROL

The rover engineering team has changed the mission requirements. Below are three critical change requests that must be incorporated into the system design.

---

## Change Request CR-01 — Emergency Safety

**Requirement Affected:** FR-05 (Safe Mode Activation)

### Original Requirement
**FR-05:**
```
The rover shall enter Safe Mode when a critical battery or thermal condition is detected.
```

### New Requirement
**FR-05 (UPDATED):**
```
The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds 
the critical threshold or battery capacity falls below the defined emergency level.
```

### Analysis
- **Change Type:** Functional enhancement with performance constraint
- **Impact:** Adds specific timing constraint (3 seconds max response time)
- **Impact:** Specifies trigger conditions (temperature threshold, battery capacity level)
- **Criticality:** HIGH - Safety-critical system requirement
- **Rationale:** Mars environment requires rapid response to prevent equipment damage

---

## Change Request CR-02 — Mission Expansion

**Requirement Affected:** NFR-03 (Multi-Rover Support)

### Original Requirement
**NFR-03:**
```
The system should support communication with multiple rovers simultaneously.
```

### New Requirement
**NFR-03 (UPDATED):**
```
The system shall support at least 20 simultaneously connected rovers.
```

### Analysis
- **Change Type:** Non-functional requirement clarification and quantification
- **Impact:** Makes requirement measurable and testable
- **Impact:** Establishes minimum capacity threshold of 20 rovers
- **Criticality:** MEDIUM - Operational scalability
- **Rationale:** Mission Control needs specific capacity planning guidance for infrastructure

---

## Change Request CR-03 — Security Upgrade

**Requirement Affected:** NFR-04 (Security and Authorization)

### Original Requirement
**NFR-04:**
```
Only authenticated Mission Control operators shall be permitted to issue rover commands.
```

### New Requirement
**NFR-04 (UPDATED):**
```
The system shall require authenticated and role-authorized operators before 
accepting rover commands.
```

### Analysis
- **Change Type:** Security enhancement - role-based access control (RBAC)
- **Impact:** Adds authorization layer beyond simple authentication
- **Impact:** Enables granular permission management
- **Criticality:** HIGH - Security requirement
- **Rationale:** Different operators may have different command permissions (e.g., movement vs. diagnostics)

---

## Summary of Changes

| CR ID | Requirement | Original | Updated | Type | Criticality |
|-------|-------------|----------|---------|------|------------|
| CR-01 | FR-05 | Generic Safe Mode | 3-second threshold-based Safe Mode | Functional Enhancement | HIGH |
| CR-02 | NFR-03 | Unspecified multiple rovers | Min 20 simultaneous rovers | Quantification | MEDIUM |
| CR-03 | NFR-04 | Authentication only | Authentication + Role Authorization | Security Enhancement | HIGH |

---

## Impact Assessment

### System Architecture Impact
- **Safety System:** Requires real-time monitoring and rapid response mechanisms
- **Scalability:** Infrastructure must support 20+ concurrent connections
- **Security:** Role-based access control system needed

### Implementation Priorities
1. **CR-01** (Emergency Safety) - Address first (safety-critical)
2. **CR-03** (Security Upgrade) - Address second (security-critical)
3. **CR-02** (Mission Expansion) - Address third (operational requirement)

