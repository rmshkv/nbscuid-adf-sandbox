# nbscuid-adf-sandbox 🦑☁️
# How to run
1. Install an environment that contains [`nbscuid`](https://github.com/rmshkv/nbscuid), e.g. with the instructions [here](https://nbscuid.readthedocs.io/en/latest/howtosetupdevelopment.html#how-to-set-up-an-nbscuid-development-environment)
2. Activate this environment (e.g. `conda activate nbscuid-dev`)
3. Clone this repo

   > **_NOTE:_**  ADF is currently set up as a submodule of this repo, inside `nbscuid-adf-sandbox/nblibrary/ADF`. For things to work out of the box, you need to either clone [ADF](https://github.com/NCAR/ADF) into this folder, or go into `config.yml` and change the parameter `adf_path:` to where you have ADF installed.
5. Navigate to the top-level folder, `nbscuid-adf-sandbox`
6. Run `nbscuid-run config.yml`

    > **_NOTE:_**  You can actually run this command from anywhere, just change `config.yml` to the full path relative to your location.
7. Run `nbscuid-build config.yml`

   > **_NOTE:_**  The built Jupyter Book files will appear in `computed_notebooks/adf-quick-run/_build`, try opening `index.html`!

# How to add stuff
Check out the `config.yml` file. [This page](https://nbscuid.readthedocs.io/en/latest/addingnotebookstocollection.html) has some instructions for how to add new notebooks and their parameters, and [this](https://github.com/rmshkv/nbscuid-examples/blob/main/testing-simplifying-features/config.yml) is an example of a config.yml file that uses some more options, including adding scripts.
