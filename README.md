# Avail_cli


## how to run 

```bash
git clone https://github.com/availproject/availup && cd availup
```

```bash
curl -sL1 avail.sh | bash
```
- or
```bash
wget --secure-protocol=TLSv1_2 -q -O - avail.sh | bash
```

- You can pass additional flags to the script like:

```bash
curl -sL1 avail.sh | bash -s -- --network turing
```
 
- đọc thêm ở bài github này : https://github.com/availproject/availup

```bash
2024-03-20T10:50:25.528628Z  INFO avail_light::light_client: Processing finalized block block_number=562690 block_delay=20
2024-03-20T10:50:25.528706Z  INFO avail_light::light_client: Random cells generated: 10 block_number=562690 cells_requested=10
2024-03-20T10:50:26.069497Z  INFO avail_light::network: Cells fetched from DHT block_number=562690 cells_total=10 cells_fetched=0 cells_verified=0 fetch_elapsed=540.755792ms proof_verification_elapsed=2.208µs
2024-03-20T10:50:28.322706Z  INFO avail_light::network: Cells fetched from RPC block_number=562690 cells_total=10 cells_fetched=10 cells_verified=10 fetch_elapsed=2.232714917s proof_verification_elapsed=20.404208ms
2024-03-20T10:50:28.322987Z  INFO avail_light::light_client: Confidence factor: 99.90234375 block_number=562690 confidence=99.90234375
2024-03-20T10:50:28.323134Z  INFO avail_light::light_client: Sleeping for 14.61143875s seconds
2024-03-20T10:50:28.323154Z  INFO avail_light::api::v2: Message published to clients topic=ConfidenceAchieved published=0 failed=0
2024-03-20T10:50:28.859369Z  INFO avail_light::network::p2p::event_loop: Cell upload success rate for block 562690: 0/10. Duration: 0
2024-03-20T10:50:41.535425Z  INFO avail_light::network::rpc::subscriptions: New justification at block no.: 562692, hash: 0x3b602253298ce9bec9b5b8f0c8767f14502ccaa17a003dfba77f9d90edeaf5da
2024-03-20T10:50:41.709011Z  INFO avail_light::network::rpc::subscriptions: Header no.: 562692
2024-03-20T10:50:41.709557Z  INFO avail_light::network::rpc::subscriptions: Number of matching signatures: 5/7 for block 562692, set_id 223
2024-03-20T10:50:41.709574Z  INFO avail_light::network::rpc::subscriptions: Storing finality checkpoint at block 562692
2024-03-20T10:50:41.709908Z  INFO avail_light::network::rpc::subscriptions: Sending finalized block 562692
2024-03-20T10:50:41.709966Z  INFO avail_light::api::v2: Message published to clients topic=HeaderVerified published=0 failed=0
2024-03-20T10:50:42.936699Z  INFO avail_light::light_client: Processing finalized block block_number=562691 block_delay=20
2024-03-20T10:50:42.936761Z  INFO avail_light::light_client: Random cells generated: 10 block_number=562691 cells_requested=10
2024-03-20T10:50:43.472932Z  INFO avail_light::network: Cells fetched from DHT block_number=562691 cells_total=10 cells_fetched=0 cells_verified=0 fetch_elapsed=536.136083ms proof_verification_elapsed=3.042µs
2024-03-20T10:50:46.513570Z  INFO avail_light::network: Cells fetched from RPC block_number=562691 cells_total=10 cells_fetched=10 cells_verified=10 fetch_elapsed=3.022786041s proof_verification_elapsed=17.810542ms
2024-03-20T10:50:46.513706Z  INFO avail_light::light_client: Confidence factor: 99.90234375 block_number=562691 confidence=99.90234375
2024-03-20T10:50:46.513785Z  INFO avail_light::light_client: Sleeping for 15.195224667s seconds
2024-03-20T10:50:46.513795Z  INFO avail_light::api::v2: Message published to clients topic=ConfidenceAchieved published=0 failed=0
2024-03-20T10:50:47.056255Z  INFO avail_light::network::p2p::event_loop: Cell upload success rate for block 562691: 0/10. Duration: 0
```


# nodes

- Đọc thêm ở đây https://github.com/availproject/avail/releases/
- https://docs.availproject.org/docs/operate-a-node/run-a-full-node/full-node


CPU: 4 - 8 core
Ram: 8 - 16 gb
ssd: 20 - 40 or 200 - 300 GB

## Ubuntu

```bash
wget https://github.com/availproject/avail/releases/download/v2.2.5.1/arm64-ubuntu-2004-avail-node.tar.gz
```

## Debian 

```bash
wget https://github.com/availproject/avail/releases/download/v2.2.5.1/x86_64-debian-12-avail-node.tar.gz
```

## extract
- Extract the downloaded file by opening a terminal in the location of the downloaded file and using the following command:
```bash
tar -xzvf <YOUR-SYSTEM-SPECIFIC-BINARY>.tar.gz
```


## run 
```bash
./avail-node --name a-random-name --chain mainnet -d ./output
```

## Your terminal output should look something like this:

```bash
2024-04-29 07:48:22 Avail Node    
2024-04-29 07:48:22 ✌️  version 2.1.1-8608dc47f00    
2024-04-29 07:48:22 ❤️  by Avail Project <info@availproject.org>, 2017-2024    
2024-04-29 07:48:22 📋 Chain specification: Avail Turing Network    
2024-04-29 07:48:22 🏷  Node name: possible-point-3102    
2024-04-29 07:48:22 👤 Role: FULL    
2024-04-29 07:48:22 💾 Database: ParityDb at ./output/chains/avail_turing_network/paritydb/full    
2024-04-29 07:48:27 🔨 Initializing Genesis block/state (state: 0x5603…9c01, header-hash: 0xd3d2…8b70)    
2024-04-29 07:48:27 👴 Loading GRANDPA authority set from genesis on what appears to be first startup.    
2024-04-29 07:48:29 👶 Creating empty BABE epoch changes on what appears to be first startup.    
2024-04-29 07:48:29 🏷  Local node identity is: 12D3KooWELgzaRZqsHNyUodhZZF7A1ydsRpgLsY7fojDegKni4YF    
2024-04-29 07:48:29 Prometheus metrics extended with avail metrics    
2024-04-29 07:48:29 💻 Operating system: linux    
2024-04-29 07:48:29 💻 CPU architecture: x86_64    
2024-04-29 07:48:29 💻 Target environment: gnu    
2024-04-29 07:48:29 💻 CPU: DO-Premium-Intel    
2024-04-29 07:48:29 💻 CPU cores: 4    
2024-04-29 07:48:29 💻 Memory: 7937MB    
2024-04-29 07:48:29 💻 Kernel: 5.15.0-105-generic    
2024-04-29 07:48:29 💻 Linux distribution: Ubuntu 22.04.4 LTS    
2024-04-29 07:48:29 💻 Virtual machine: yes    
2024-04-29 07:48:29 📦 Highest known block at #0    
2024-04-29 07:48:29 Running JSON-RPC server: addr=127.0.0.1:9944, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2024-04-29 07:48:29 🏁 CPU score: 950.72 MiBs    
2024-04-29 07:48:29 🏁 Memory score: 4.02 GiBs    
2024-04-29 07:48:29 🏁 Disk score (seq. writes): 845.72 MiBs    
2024-04-29 07:48:29 🏁 Disk score (rand. writes): 338.52 MiBs    
2024-04-29 07:48:29 〽️ Prometheus exporter started at 127.0.0.1:9615    
2024-04-29 07:48:30 🔍 Discovered new external address for our node: /ip4/139.59.94.121/tcp/30333/ws/p2p/12D3KooWELgzaRZqsHNyUodhZZF7A1ydsRpgLsY7fojDegKni4YF    
2024-04-29 07:48:34 ⚙️  Syncing, target=#137399 (9 peers), best: #1000 (0x9e8f…55ab), finalized #512 (0x0a9a…875a), ⬇ 316.3kiB/s ⬆ 14.2kiB/s    
2024-04-29 07:48:39 ⚙️  Syncing 235.4 bps, target=#137399 (9 peers), best: #2177 (0x5828…e9da), finalized #2048 (0x2f65…3b2e), ⬇ 113.3kiB/s ⬆ 5.5kiB/s    
2024-04-29 07:48:43 [3097] 💸 generated 8 npos targets    
2024-04-29 07:48:43 [3097] 💸 generated 8 npos voters, 8 from validators and 0 nominators    
2024-04-29 07:48:43 [#3097] 🗳  creating a snapshot with metadata SolutionOrSnapshotSize { voters: 8, targets: 8 }    
2024-04-29 07:48:43 [#3097] 🗳  Starting phase Signed, round 1.    
2024-04-29 07:48:44 [#3277] 🗳  Starting phase Unsigned((true, 3277)), round 1.    
2024-04-29 07:48:44 [#3278] 🗳  queued unsigned solution with score ElectionScore { minimal_stake: 184467440819699, sum_stake: 184467440819699, sum_stake_squared: 34028236722569152873026450601 }    
2024-04-29 07:48:44 ⚙️  Syncing 236.0 bps, target=#137400 (10 peers), best: #3357 (0x0c50…7d21), finalized #3072 (0x2803…c15b), ⬇ 244.0kiB/s ⬆ 20.2kiB/s    
2024-04-29 07:48:44 [#3457] 🗳  Starting phase Off, round 2.    
2024-04-29 07:48:44 [3457] 💸 new validator set of size 1 has been processed for era 1    
2024-04-29 07:48:49 ⚙️  Syncing 206.2 bps, target=#137400 (10 peers), best: #4388 (0x2d3d…6b93), finalized #4177 (0x58f8…9518), ⬇ 261.5kiB/s ⬆ 11.6kiB/s    
2024-04-29 07:48:54 ⚙️  Syncing 232.0 bps, target=#137400 (10 peers), best: #5548 (0x1aef…1c46), finalized #5120 (0x274f…e5d7), ⬇ 122.7kiB/s ⬆ 6.9kiB/s    
2024-04-29 07:48:59 ⚙️  Syncing 118.2 bps, target=#137400 (10 peers), best: #6139 (0x9e52…af00), finalized #5632 (0x5297…a001), ⬇ 66.5kiB/s ⬆ 4.9kiB/s    
2024-04-29 07:49:04 ⚙️  Syncing 185.7 bps, target=#137401 (10 peers), best: #7068 (0x911d…666a), finalized #6656 (0xdd79…2e5e), ⬇ 80.7kiB/s ⬆ 1.5kiB/s    
2024-04-29 07:49:05 [7417] 💸 generated 9 npos targets    
2024-04-29 07:49:05 [7417] 💸 generated 9 npos voters, 9 from validators and 0 nominators    
2024-04-29 07:49:05 [#7417] 🗳  creating a snapshot with metadata SolutionOrSnapshotSize { voters: 9, targets: 9 }    
2024-04-29 07:49:05 [#7417] 🗳  Starting phase Signed, round 2.    
2024-04-29 07:49:06 [#7597] 🗳  Starting phase Unsigned((true, 7597)), round 2.    
2024-04-29 07:49:06 [#7598] 🗳  queued unsigned solution with score ElectionScore { minimal_stake: 184447246591607, sum_stake: 1475577972732856, sum_stake_squared: 272166294201800640629142739592 }    
2024-04-29 07:49:07 [#7777] 🗳  Finalized election round with compute Unsigned.    
2024-04-29 07:49:07 [#7777] 🗳  Starting phase Off, round 3.    
2024-04-29 07:49:07 [7777] 💸 new validator set of size 8 has been processed for era 2    
2024-04-29 07:49:09 ⚙️  Syncing 206.2 bps, target=#137401 (10 peers), best: #8099 (0x559a…9c2e), finalized #7680 (0x84b6…abc0), ⬇ 103.9kiB/s ⬆ 0.9kiB/s    
2024-04-29 07:49:14 ⚙️  Syncing 204.4 bps, target=#137401 (10 peers), best: #9121 (0xf95e…5a17), finalized #8704 (0x6e49…33cd), ⬇ 98.0kiB/s ⬆ 1.5kiB/s
```
# Become a Validator
- đọc thêm ở đây https://docs.availproject.org/docs/operate-a-node/become-a-validator
