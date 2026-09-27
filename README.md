# REALM — the collection

The 1,111 finished beings, and a Metaplex JSON for each.

This repository is **storage, not a website**. `realm-site` is the site.

```
images/1.png … images/1111.png      2400 x 2400
metadata/1.json … metadata/1111.json
drop.json                           every being, its tier and its traits
provenance.json                     every image's hash, and the one that counts
```

## The provenance hash

`provenance.json` holds the hash of every image, and the single hash made by
joining them in token order and hashing that.

**It has to be published before the mint opens** — on the site, on X, anywhere
time-stamped. Published afterwards it proves nothing, because the whole point
is that it existed before anybody could see what they were buying.

Afterwards anyone can repeat the calculation on the finished collection. If a
single being had been altered, or two swapped over, it would not match.

What it proves: the collection handed out is the collection that was hashed.
What it does not prove: how mint order was assigned to token number — that is
the launchpad's shuffle.

## Before minting: these images need a permanent home

The `image` field in each metadata file is a bare filename. It has to be
rewritten to point at wherever the art actually ends up.

**Do not serve them from GitHub.** If this repository is ever renamed, made
private or deleted, every NFT in the collection breaks. GitHub is where the
files are *kept*, not where they are *served*.

They belong on Arweave or IPFS, which is permanent and content-addressed. Most
Solana launchpads do that upload as part of listing a collection — ask yours
before you commit to it, because the answer decides how much work launch day is.

## The 1,111th

`images/1111.png` is the Source. It is the one picture in the collection that
was not generated: it was composed by hand and is used as drawn. Everything
else comes out of `tools/drop.py` in `realm-site`.
