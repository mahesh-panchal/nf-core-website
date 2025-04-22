---
title: "Using Pixi to run Nextflow"
subtitle: "How to use the Pixi package manager to run and develop pipelines"
pubDate: "Scheduled publication date and time (the post will go live post-website rebuild if the current date surpasses this timestamp). Format: YYYY-MM-DDTHH:MM:SS+HH:MM" (without quotes!)
authors: 
  - "mahesh-panchal"
label:
  - "Pixi"
---

## What is Pixi and why use it?

[Pixi](https://pixi.sh/) is a package management tool, that works with [Conda](https://anaconda.org/anaconda/conda) channels.
It has several advantages over Conda, including speed, reproducibility, tasks, and multi-platform support. Pixi uses two files,
`pixi.toml` (or `pyproject.toml`) and `pixi.lock`, which live in the root of your project (You are running your analyses in a 
project folder, right?). When shared with others, it allows them to create the same environment you used too.

Although Nextflow can be installed globally, there are times when it's useful to fix the version to project. By including Nexflow
with Pixi, you're guaranteed it's available in the environment, and can use it with Pixi tasks. Pixi environments can also rebuilt
quickly if they're removed, thanks to the lock file, and with multi-platform support, means it'll work identically across platforms.
