# Quanta

**Quanta** is a small on-chain project built on **Solana**.  
It’s made up of different programs that work together — starting with a token mint and a staking vault.

Right now, there are two working parts:
- **QuantaMint** → creates and manages the `$QNT` token  
- **QuantaVault** → lets users lock (stake) their QNT for some time

---

## QuantaMint
The **mint program** for the `$QNT` token.  
It handles creating new tokens and defines who can mint more.  
This is the base for everything else in Quanta.

**What it does:**
- Creates the `$QNT` token
- Sets the mint authority
- Keeps track of total supply

---

## QuantaVault
The **vault program** lets users stake their `$QNT` tokens for a set amount of time.  
After that time passes, they can withdraw them again.

**How it works:**
- You deposit your `$QNT` into the vault
- Tokens stay locked for a chosen time period
- Once the lock ends, you can take your tokens back (and maybe rewards later)

---

## Upcoming Features
| Program | Description | Status |
|----------|--------------|--------|
| QuantaMint | Creates the QNT token | ✅ Done |
| QuantaVault | Time-locked staking | ⚙️ Working |
| QuantaEscrow | Token escrow with unlock conditions | 🔜 Coming soon |

---

## How to Run It
### Prerequisites
Make sure you have these installed:
- Solana CLI  
- Anchor Framework  
- Yarn / Node.js

### Steps
```bash
git clone git@github.com:VedanshShuklaa/Quanta.git
cd Quanta
anchor build
anchor deploy
```