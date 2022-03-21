# fun-with-swarm

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Swarm-DISC/fun-with-swarm/main) [![Binder-Panel](https://img.shields.io/badge/launch-binder--panel-orange)](https://mybinder.org/v2/gh/Swarm-DISC/fun-with-swarm/main?urlpath=panel)

Simple dashboard to use for fun outreach purposes and experiment with [Panel](https://panel.holoviz.org/). Comes with a suitable development environment defined in `environment.yml` including [jupyter-panel-proxy](https://github.com/holoviz/jupyter-panel-proxy) which enables a convenient Panel server accessible through Jupyter.

To set up locally:

0. Clone this project
    ```
    git clone https://github.com/Swarm-DISC/fun-with-swarm.git`
    cd fun-with-swarm
    ```
1. Install [rubberband](https://breakfastquay.com/rubberband/) (e.g. `sudo apt install rubberband-cli`)
2. Install the conda environment:
    ```
    conda env create --file environment.yml --name funswarm
    conda activate funswarm
    ```
3. Launch Jupyter:
    ```
    jupyter lab &
    ```

Add notebooks to `notebooks/` and extend the list in `jupyter-panel-proxy.yml` to make them available to the Panel server.

Problems:
- https://github.com/holoviz/panel/issues/3170
- Binder is often slow... how to speed up? 
    - Every time the repo changes, the images will need to be rebuilt. Could set up a separate repository to define a good environment that won't change often, use that to launch the binder and then nbgitpuller to add this one? (https://discourse.jupyter.org/t/how-to-reduce-mybinder-org-repository-startup-time/4956)
    - Set up a dedicated panel server