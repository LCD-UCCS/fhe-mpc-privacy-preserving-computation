# FHE and MPC Based Privacy-Preserving Computation

This umbrella repository points to the two implementation repositories for the
privacy-preserving computation system:

- FHE system: `fhe-compute-system`
- MPC system: `multi-party-compute-system`

The FHE system contains a central FHE server and a local data-owner app. The MPC
system contains the multi-party computation workflow and MP-SPDZ integration.

## Repository Layout

Recommended layout after the implementation repositories have been pushed:

```text
fhe-mpc-privacy-preserving-computation/
  ├─ fhe/   # git submodule -> fhe-compute-system
  ├─ mpc/   # git submodule -> multi-party-compute-system
  ├─ docs/
  └─ README.md
```

## Add Submodules

After the FHE and MPC repositories have initial commits on GitHub, add them as
submodules from this repository:

```bash
git submodule add https://github.com/LCD-UCCS/fhe-compute-system.git fhe
git submodule add https://github.com/LCD-UCCS/multi-party-compute-system.git mpc
git submodule update --init --recursive
```

Clone this umbrella repo later with:

```bash
git clone --recurse-submodules https://github.com/LCD-UCCS/fhe-mpc-privacy-preserving-computation.git
```

## Documentation

### System Overview

![FHE system architecture](docs/images/system-architecture.png)

### FHE Detailed Design

![FHE detailed design](docs/images/detailed-design.png)

### MPC Architecture

![MPC architecture](docs/images/mpc-architecture.png)

The project paper, Table 1 comparison, and quick-start links should live here
once the child repositories have been pushed.

Suggested contents:

- Table 1 comparison from the paper.
- Link to the FHE repository README.
- Link to the MPC repository README.
- Link to the paper PDF.
- Demo setup matrix for FHE server, data-owner app, and MPC server.
