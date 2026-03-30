# Application Guidelines

This document provides detailed guidance on writing a strong application for the OrbitFlare Infra Accelerator.

---

## General Advice

**Be specific, not aspirational.** We want to see what you have built, what is broken, and what it will take to get to mainnet. Vague descriptions of your vision are less useful than a clear-eyed assessment of your current state.

**Show your work.** Link to repositories, deployed programs, demo videos, or anything we can interact with. Applications backed by working code are significantly stronger than those backed only by descriptions.

**Be honest about blockers.** Every devnet project has gaps. Listing them clearly shows maturity and helps us understand where OrbitFlare support will have the most impact. We are not looking for perfection - we are looking for teams that understand what stands between them and the mainnet.

---

## Section-by-Section Guidance

### Project Overview

- The tagline should make it immediately clear what your product does
- The description should cover: what the product is, who uses it, and what problem it solves
- Avoid jargon-heavy descriptions that obscure the actual functionality

### Team

- Include GitHub profiles for every technical team member
- We review contribution history and code quality - active profiles strengthen your application
- Be clear about time commitment - the 4-week program is intensive and requires dedicated development time
- If you have relevant prior experience building on Solana or in the same problem domain, highlight it

### Technical Details

- The architecture overview should give us a clear mental model of how your system works
- List every external dependency - we need to know what your project relies on beyond your own code
- For on-chain programs: describe the instruction set, key accounts, and data flow
- If your code is private, describe the structure and be prepared to share access during review

### Current Status

- Be precise about what works. "The app is functional on devnet" is too vague. Walk us through exactly what a user can do today.
- Known limitations are valuable. A team that says "we have no issues" either has not tested their code or is not being transparent.
- Provide devnet links. We will try to interact with your prototype.

### Path to Mainnet

This is the most important section of your application.

- **Blockers**: List every technical issue standing between your current state and a production deployment. Common examples:
  - Unchecked arithmetic in financial calculations
  - Hardcoded devnet addresses
  - No transaction retry or confirmation logic
  - Missing input validation
  - No monitoring or logging
  - Missing access controls
  - No error handling for edge cases
  - Untested concurrent user scenarios

- **Milestones**: Must be specific and verifiable. Each milestone should describe a concrete deliverable, not a general area of improvement.
  - Bad: "Improve security"
  - Good: "Add checked math to token swap calculations, add signer verification to all admin instructions, write tests for overflow and unauthorized access scenarios"

- **Infrastructure needs**: Be detailed about your RPC requirements. This directly shapes the OrbitFlare plan we build for you.

### Ecosystem Fit

- Show evidence that the problem you are solving is real. Link to user complaints, forum posts, tweets, or data.
- If competitors exist, explain what you do differently - not why they are bad, but why your approach serves users better.

### Post-Program Plans

- We invest in teams that will continue building after the accelerator
- Describe how you will cover infrastructure costs, fund ongoing development, or generate revenue
- A clear 3-6 month roadmap shows you are thinking beyond the initial launch

---

## Common Reasons Applications Are Rejected

- No working code or prototype
- Project has already launched on mainnet
- Application sections are incomplete or filled with placeholder text
- Team cannot commit sufficient time during the program
- Project is not built on Solana
- No response to reviewer feedback within 7 days

---

## Application Format

- File must be named `your_project_name.md` using lowercase and underscores
- Place the file in the `applications/` directory
- Use the provided template without modifying the section structure
- Delete all instructional text (lines starting with >) before submitting
- Your PR should contain only your application file

---

## After Submitting

1. The OrbitFlare team will review your application within 2 weeks
2. We may leave comments on your PR requesting clarification or additional detail
3. Respond to all feedback within 7 days
4. Accepted applications are merged and the team is contacted for onboarding
5. Rejected applications receive feedback explaining the decision
