# Quanta

**Quanta** is a modular Solana project made up of multiple programs that work together — starting with **Quanta Mint** (for token creation) and **Quanta Vault** (for time-locked staking).  
Each module lives in its own repository and is linked here for clarity.

---

## Quanta Mint
**Quanta Mint** handles minting and managing the QNT token on Solana.

### Quick Run
```bash
# install
npm install

# run the mint script (from project root)
npx ts-node --esm mint.ts
```

---

## Quanta Vault
**Quanta Vault** is a time-locked staking vault built for QNT tokens.  
Users can stake their tokens for a chosen duration to earn rewards after maturity.

### Quick setup & run (devnet)
```bash
# set Solana config to devnet
solana config set --url devnet

# build (if you changed the program)
anchor build

# (if redeploying) deploy program
anchor deploy

# initialize or stake (demo)
yarn ts-node app/execute_vault.ts

# fund the vault rewards pool (admin)
yarn ts-node app/fund_vault.ts

# check vault state / stake status
yarn ts-node app/check_vault_status.ts

# claim (after maturity)
yarn ts-node app/claim_rewards.ts
```

---

## How They Work Together
1. **Quanta Mint** creates and manages the **QNT** token — this is your core SPL token.
2. **Quanta Vault** uses the QNT mint address to lock user tokens for staking and rewards.
3. Together, they form the foundation of the Quanta ecosystem — secure minting, fair staking, and future extensibility.

---

## Coming Soon
- **Quanta Escrow:** Time-based QNT transfers (e.g., vesting or delayed payments)
- **Quanta Dashboard:** Simple UI to track stakes and rewards

---
