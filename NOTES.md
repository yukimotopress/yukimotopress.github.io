# Notes


## How to add a new book

Move to octobook (single-source reference) - why? why not?



### Step 1:  Add a submodule with the book sources (in manuscripts format)

Note: change the name of the repo to start with underscore (`_`)
e.g. `blockchains` becomes `_blockchains`.

```
$ git submodule add --name _blockchains https://github.com/yukimotopress/blockchains _blockchains
```


### Step 2:  Copy all ("private") images to ("shared") images folder

For example, copy all images in `_blockchains/i` to the top-level shared images folder `/i`.

Todo/fix:
- octobook will automate this step  
- in a future version symlink images - possible on github? works with pages?


### Step 3: Add book contents and meta info

In the `_data` folder add a new folder for the book e.g. `_data/blockchains`
and add a `book.yml` file with the contents and meta info:

``` yaml
############################
#  Book (Meta) Info

title:   "Programming Cryptocurrencies and Blockchains (Book Edition)"
author:
  name:  "Gerald Bauer, et al"


#############################
#   Extras

github:
  url: https://github.com/yukimotopress/blockchains

######################
#  Table of Contents

contents:
- title: 1. Digital $$$ Alchemy - What's a Blockchain?
  path:  01__Introduction.md
  sections:
  - title: How-To Turn Digital Bits Into $$$ or €€€?
  - title: Decentralize Payments. Decentralize Transactions. Decentralize Blockchains.
  - title: The Proof of the Pudding is ... The Bitcoin (BTC) Blockchain(s)


- title: 2. Building Blockchains from Scratch
  path:  02__Blockchains_from_scratch.md
  sections:
  - title: A Blockchain in Ruby in 20 Lines! A Blockchain is a Data Structure
  - title: What about Proof-of-Work? What about Consensus?
  - title: Find the Lucky Number - Nonce == Number Used Once

# [...]
```



### Step 4: Add book page


Example: `blockchains.html`

```
---
layout: book

book:   blockchains          ## book id used for site.data[ page.book ] lookups
---
```
