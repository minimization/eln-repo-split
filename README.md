# eln-repo-split


## Usage

### Step 1: Get configs

First, you'll need configs. You can clone the [github.com/minimization/content-resolver-input](https://github.com/minimization/content-resolver-input) repository and use the `configs` directory.

Or you can put your own configs to a local directory:

```
$ mkdir configs
$ vim configs/config.yml
```

See the [config spec](https://github.com/minimization/content-resolver/blob/master/config_specs/eln-repo-splitter.yaml) for reference.

### Step 2: Run the script

For initial run, the script will download data from [Content Resolver](https://tiny.distro.builders). This can take a minute.

```
$ mkdir output
$ ls configs  # <--- this needs to have the configs. You can of course point to a different location.
$ ./eln_repo_split.py ./configs ./output
```

For repetitive runs, you can use the cashed data and save a lot of time.

```
$ ./eln_repo_split.py --use-cache ./configs ./output
```

A summary will be printed on the standard output and text files with the results will be in the `./output` directory.