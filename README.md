README
====================

The [website](https://umswc.github.io) for the University of Michigan chapter of Software and Data Carpentry


## Updating the workshops page

After creating a workshop repository and filling in the required information, fork it into this organization.
Then you can update the workshops listed on the website by running the [`update-workshops`]('update-workshops') script from the website repo's working directory.

Dependences are listed in [`env.yaml`](env.yaml).
You can install them with your preferred package manager, or use [conda](https://docs.conda.io/en/latest/miniconda.html):

```
conda env create -f env.yaml
conda activate umswc
```

Update the workshops page:
```
python update-workshops.py
```

Workshops with a start date before today (the day you run the script) will be removed from the page;
workshops with a start date after today date will be added.

Make sure you're happy with the changes in `workshops/_posts`, then commit & push them to make the changes go live.
