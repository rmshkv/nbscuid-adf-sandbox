# nbscuid-adf-sandbox 🦑☁️
# How to run

1. Install an environment that contains [`nbscuid`](https://github.com/rmshkv/nbscuid), e.g. with the instructions [here](https://nbscuid.readthedocs.io/en/latest/howtosetupdevelopment.html#how-to-set-up-an-nbscuid-development-environment)
2. Activate this environment (e.g. `conda activate nbscuid-dev`)
3. Clone this repo

   > **_NOTE:_**  ADF is currently set up as a submodule of this repo, inside `nbscuid-adf-sandbox/nblibrary/ADF`. For things to work out of the box, you need to either clone [ADF](https://github.com/NCAR/ADF) into this folder, or go into `config.yml` and change the parameter `adf_path:` to where you have ADF installed.
5. Navigate to the top-level folder, `nbscuid-adf-sandbox`
6. Install the environment specified by mom6-environment.yml: `mamba env create -f mom6-environment.yml`, or if you don't have `mamba` installed, `conda env create -f mom6-environment.yml`. (It'll probably be a lot faster with `mamba`!) 

    > **_NOTE:_**  This will create an environment called `mom6-tools-nbscuid`. There's no need to activate it--it'll just be used when `nbscuid` runs the `surface` notebook, since it has `mom6-tools-nbscuid` specified as its `kernel_name` in `config.yml`. 
    
7. Run `nbscuid-run config.yml`, making sure you're still in an environment with `nbscuid` installed

    > **_NOTE:_**  You can actually run this command from anywhere, just change `config.yml` to the full path relative to your location.
8. Run `nbscuid-build config.yml`

   > **_NOTE:_**  The built Jupyter Book files will appear in `computed_notebooks/adf-quick-run/_build`, try opening `index.html`!
   
# How to add stuff
Check out the `config.yml` file. [This page](https://nbscuid.readthedocs.io/en/latest/addingnotebookstocollection.html) has some instructions for how to add new notebooks and their parameters, and [this](https://github.com/rmshkv/nbscuid-examples/blob/main/testing-simplifying-features/config.yml) is an example of a config.yml file that uses some more options, including adding scripts.
