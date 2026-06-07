# CCNA EIGRP Lab

## Objective

Demonstrate how EIGRP selects successor and feasible successor routes.

## Topology

Insert a screenshot of the Packet Tracer topology here.

## Verification Commands

```bash
show ip eigrp topology
show ip route eigrp
```

## Key Concepts

- Successor = Best route to a destination network.
- Feasible Successor = Backup route that meets the feasibility condition.
- A route can become a feasible successor only if its Reported Distance (RD) is less than the successor's Feasible Distance (FD).

## Example Analysis

### Destination Network
10.10.10.0/24

| Router | Reported Distance |
|----------|----------|
| R2 | 1000 |
| R3 | 800 |
| R4 | 1500 |

### Successor
- R3

### Feasible Successor
- R2

### Not a Feasible Successor
- R4

## Lessons Learned

- EIGRP uses the feasibility condition to help prevent routing loops.
- Multiple feasible successors can exist.
- Not every backup route qualifies as a feasible successor.
