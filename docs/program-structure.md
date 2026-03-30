# Program Structure

The OrbitFlare Infra Accelerator is a 4-week intensive program. Each week has a clear focus and expected deliverable.

---

## Week 1 - Assessment and Planning

The first week focuses on understanding where each project stands today and defining a realistic path to mainnet.

### Kickoff Call (Day 1)

- Welcome and program expectations
- Setup of a private communication channel between each team and OrbitFlare
- Establish check-in schedule (Tuesdays and Fridays)

### Architecture Review (Day 2-3)

Each team receives a dedicated session reviewing their codebase. We assess:

- Current state of on-chain programs
- Frontend and backend infrastructure
- External dependencies (oracles, APIs, indexers)
- Known technical debt from hackathon or prototype development

### Mainnet Blockers Audit (Day 3-4)

Based on the architecture review, we produce a mainnet blockers list. Common blockers include:

- Missing error handling or edge cases
- Hardcoded devnet addresses
- No transaction retry logic
- Missing input validation
- Lack of monitoring or logging
- Unchecked arithmetic in financial logic
- Missing access controls or authority checks

### Milestone Setting (Day 5)

Each team defines 3-4 clear milestones for the remaining three weeks. Milestones must be specific and verifiable.

- Not: "Improve security"
- Instead: "Add checked math to token calculations and write overflow edge-case tests"

**Week 1 Deliverable**: Mainnet blockers list and milestone plan.

---

## Week 2 - Core Development Sprint

This is the primary development sprint. Teams focus on resolving mainnet blockers and integrating OrbitFlare infrastructure.

### On-Chain Hardening

- Fix all items on the blockers list
- Add comprehensive error handling
- Ensure arithmetic safety checks
- Validate account constraints and authority checks
- Expand test coverage for adversarial scenarios

### RPC Integration

- Replace public RPC endpoints with OrbitFlare
- Implement proper transaction sending patterns
- Configure confirmation polling and retry logic
- Implement WebSocket subscriptions where required
- Configure gRPC streaming connections for Jetstream users

### Infrastructure Setup

Teams configure production-grade infrastructure including:

- Staging environment mirroring mainnet configuration
- Monitoring of transaction success rates and RPC latency
- Logging sufficient to debug production issues

**Week 2 Deliverable**: OrbitFlare RPC integrated, mainnet blockers resolved.

---

## Week 3 - Hardening and Testing

Development continues but the focus shifts toward resilience and stability. If something can break in production, it should break during this week.

### Stress Testing on Devnet

Teams simulate real-world load conditions:

- Burst transaction scenarios
- Concurrent users
- RPC timeouts and network congestion
- Slot skipping scenarios
- Duplicate transaction submissions
- Invalid inputs and expired blockhashes

### Security Review

We review projects for common Solana vulnerabilities including:

- Missing signer checks
- PDA seed collisions
- Reinitialization attacks
- Unsafe CPI calls
- Privilege escalation paths

**Week 3 Deliverable**: Stress testing complete, security review issues addressed.

---

## Week 4 - Mainnet Deployment and Launch

Everything built in the previous three weeks culminates in a live mainnet deployment.

### Pre-Launch Checklist

Before deploying:

- [ ] All blockers resolved
- [ ] Full test suite passes
- [ ] Stress testing completed
- [ ] Security review issues addressed
- [ ] Monitoring and alerting configured
- [ ] Program authority secured
- [ ] User documentation exists
- [ ] RPC endpoints pointed to OrbitFlare

### Mainnet Deployment

OrbitFlare engineers are available in real time for:

- Program deployment assistance
- Test transactions with real SOL
- Verifying addresses and program IDs
- Monitoring the first hours of production traffic

### Open to Users

- Flip the product live for users
- Monitor transaction success rates and logs
- Address issues that surface with real traffic
- Deploy hotfixes if required

### Public Launch

Each project should publish a mainnet launch thread or announcement describing:

- The product and what it does
- The journey from prototype to mainnet
- Key challenges solved during development
- The infrastructure used to support the deployment

### Retro and Next Steps

Each team receives a wrap-up call covering:

- What went well
- What could improve
- Remaining roadmap items
- Continued RPC access
- Introductions to relevant ecosystem partners where appropriate

**Week 4 Deliverable**: Live mainnet launch, public announcement published.

---

## Communication

- **Primary channel**: Private Telegram or Discord channel per team
- **Check-ins**: Tuesdays and Fridays, 30 minutes each
- **Async support**: Available at all times
- **Escalation**: Direct access for critical blockers
- **Cross-team**: Optional interaction between cohort teams

---

## Success Criteria

The program is successful if by the end of Week 4:

- Each team has a working product deployed on Solana mainnet
- Each team is using OrbitFlare RPC in production
- Each team has monitoring in place and can respond to production issues independently
- Each team has a clear roadmap beyond the accelerator
- Each team publicly shares their launch and acknowledges the infrastructure powering their deployment
