# blockchair-dash-quarterlies

Ad-hoc quarterly aggregations of blockchair's dash data (for faster retrieval).

# How to Download

```sh
git clone https://github.com/dashhive/blockchair-dash-quarterlies.git
```

```sh
pushd ./blockchair-dash-quarterlies/
open .
```

# How to Update

1. Get [blockchair-dash-mirror](https://github.com/dashhive/blockchair-dash-mirror)
   ```sh
   mkdir -p ~/Projects/Dash/
   git clone https://github.com/dashhive/blockchair-dash-mirror.git ./dashblockchair
   ```
2. Download and generate the latest quarterly caches:

   ```sh
   pushd ~/Projects/Dash/dashblockchair/
   ./bin/blockchair_dash_quarter

   ./bin/blockchair_dash_download
   ./bin/blockchair_dash_quarter
   ```

3. Commit the updates
   ```sh
   pushd ./quarterlies/
   git add *.tsv
   git commit -m "feat: add cache of 20xx qX"
   git push
   ```
