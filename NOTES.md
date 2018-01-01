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
