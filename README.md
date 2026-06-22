# SRBMiner Docker

<p align="center">
  <!--<img src="https://img.shields.io/docker/pulls/dablincx/SRBMiner-docker?style=for-the-badge" />
  <img src="https://img.shields.io/docker/image-size/dablincx/SRBMiner-docker?style=for-the-badge" />-->
  <img src="https://img.shields.io/github/actions/workflow/status/dablincx/SRBMiner-docker/docker-publish.yml?branch=latest&style=for-the-badge" />
  <img src="https://img.shields.io/github/v/release/doktor83/SRBMiner-Multi?style=for-the-badge&label=Upstream%20Version" />
</p>

---

## about

fork of https://github.com/commoodor/SRBMiner-docker without forced cpu

**upstream version:**  
![upstream version](https://img.shields.io/github/v/release/doktor83/SRBMiner-Multi?label=Latest%20Release)

---

## quick start compose file

```yaml
services:
  SRBMiner:
    container_name: SRBMiner
    image: ghcr.io/dablincx/srbminer-docker:latest
    restart: unless-stopped
    tty: true
    mem_limit: 2g
    gpus: all
    environment:
      ALGO: pearlhash
      POOL_ADDRESS: prl.kryptex.network:7048
      WALLET_USER: prl1p6mjua9hzcnalvqn8rah3d6vsga3pe26mlcpx2v6ne43rpjulyg9s4s5e6d
      WORKER: unconfiguredgithubcopy
      # PASSWORD: x
      EXTRAS: --disable-cpu
    logging:
      driver: "json-file"
      options:
        max-size: "10m"
        max-file: "3"
```

---

## environment variables

| Variable        | Description              | Example                                      |
|----------------|--------------------------|----------------------------------------------|
| `ALGO`         | Mining algorithm         | `pearlhash`                                  |
| `POOL_ADDRESS` | Mining pool address      | `prl.kryptex.network:7048`    |
| `WALLET_USER`  | Wallet address or user   | `prl1p6mjua9hzcnalvqn8rah3d6vsga3pe26mlcpx2v6ne43rpjulyg9s4s5e6d`           |
| `WORKER`       | Worker name              | `Saturn`                                     |
| `PASSWORD`     | Pool password (optional) | `x`                                          |
| `EXTRAS`       | Extra SRBMiner flags     | `-t 4`                                       |

---

## support development

<details>
<summary>click to view donation addresses</summary>

<br>

<img src="https://img.shields.io/badge/Bitcoin-ff9900?style=for-the-badge&logo=bitcoin&logoColor=white" />
<br/>
<code>bc1pma9e2v5pj06y75xhfl46quyt5dzlmjcvkvn7gtpcfs0edu2mp6ysdw5axv</code>
<br/>
<br/>

<img src="https://img.shields.io/badge/Ethereum-627eea?style=for-the-badge&logo=ethereum&logoColor=white" />
<br/>
<code>0xC97Af2150C59C55196EDf0900D4Af34dCE1C2AEF</code>
<br/>
<br/>

<img src="https://img.shields.io/badge/Monero-ff6600?style=for-the-badge&logo=monero&logoColor=white" />
<br/>
<code>842aa8LDTDbiknxbabhqxHVdi9WLL2oPPciLKzzeQx9bKVggeVV9JtnHpLWdu819UYV35CQHqS8sNEprMP9wu8ez6WZx4SC</code>

</p>

</details>

---

## license

This project redistributes official **SRBMiner-Multi** binaries.  
Please refer to the upstream repository for full license details:

- https://github.com/doktor83/SRBMiner-Multi

