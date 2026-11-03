# 06_bitcoin_full_node_rpc — Bitcoin full-node RPC — practical demonstrations

A **subspecialty of general Bitcoin** dedicated to useful, repeatable read-only Bitcoin Core RPC experiments and the “what can you do with a full node?” series.

## Put here

- Cross-platform Python examples of getblockchaininfo/getblockhash/getblockheader, gettxoutsetinfo, getmempoolinfo, getpeerinfo, getblockstats, estimatesmartfee and related methods.
- Example terminal output captured from local/test nodes (clearly labeled network/version/height/date), source URLs, screenshots, reproducible scripts and usage notes.
- Performance/pruning/index caveats and correct interpretation of results, especially that UTXO totals are not all historical bitcoin issued.

## Keep elsewhere / avoid

- Broader node philosophy or consensus education without an RPC demonstration → `../05_bitcoin_independent/`.
- No live RPC passwords, cookies, auth headers, private keys, user peer IPs or other sensitive machine details in a public GitHub repo.
- Do not assume methods or fields are available in every Bitcoin Core version; label version/network.

## V15 full-node RPC episode ideas

- `utxo-total` — `gettxoutsetinfo`: current UTXO set BTC total vs total issued/circulating limitations.
- `genesis-timestamp` — `getblockhash` + `getblockheader`: UTC header timestamp, not exact wall-clock proof.
- `genesis-message` — `getblockhash` + `getblock`: parse genesis coinbase ASCII from RPC hex, no disk offsets.
- `raw-genesis-block` — `getblock` verbosity 0: serialised genesis block bytes vs blk*.dat on-disk wrapper.
- `block-time-by-height` — `getblockhash` + `getblockheader`: investigate a known historic height.
- `block-statistics` — `getblockstats`: counts, fees, subsidy, sat/vB conversion.
- `mempool-local-view` — `getmempoolinfo`: local transactions/bytes and policy.
- `peer-diversity` — `getnetworkinfo` + `getpeerinfo`: connection counts, inbound/outbound and Tor/I2P visibility caveats; never publish peer IPs.
- `chain-sync-status` — `getblockchaininfo`: headers, blocks, progress, IBD vs synced.
- `difficulty` — `getdifficulty`: current active-chain difficulty vs estimated hash rate.
- `utxo-count` — `gettxoutsetinfo`: count of unspent outputs, not wallets or people.
- `reorg-tips` — `getchaintips`: branch tips, status labels; don't equate side branches with consensus failure.
- `median-time-past` — `getblockheader`: compare header time and mediantime, understand limitations.
- `pruning` — `getblockchaininfo`: verify pruned/pruneheight; what it does and doesn't store.
- `fee-market` — `getmempoolinfo` + `estimatesmartfee`: node-local estimation and dynamic policy, do not promise confirmation times.
- `chainwork` — `getblockchaininfo`: cumulative proof of work; distinguish raw count from valid most-work chain.
- `block-transaction-count` — `getblockstats`: transactions in a selected block, no unsupported chainwide claim.
- `height-versus-clock` — `getblockhash` and headers: node-validated height vs timestamp caveats.

*The Bash commands supplied during kit planning are examples, not the limit of this category; continue discovering new read-only RPC use cases.*

## Primary starting references

- https://bitcoincore.org/en/doc/31.0.0/rpc/
- https://bitcoincore.org/en/doc/

## Example filenames

- `gettxoutsetinfo_utxo_total_python.py`
- `getblockstats_height_840000_notes.md`

## Filing routine (keep the folder flat)

1. Save papers, images, code, links, screenshots, notes and finished posters **directly in this folder**. No required child folders.
2. Give every sourced item a readable filename; include the project/version/date when that affects accuracy. Preserve the official original filename of authentic product photos when possible.
3. For anything used in a public tweet/poster, keep the **primary source URL, checked date, relevant release/network version, and usage/redistribution rights** in a nearby `.md` note or directly below in this README.
4. Treat source documents as evidence, not permission to alter branded artwork. Before publishing, recheck time-sensitive claims and avoid exposing wallet secrets, authentication material or private user data.

### Add sources here

| Item / filename | Original URL or citation | Verified date / version | Notes / reuse permission |
|---|---|---|---|
| _Add new sources here_ | | | |
