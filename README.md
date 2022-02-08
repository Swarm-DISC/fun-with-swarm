# fun-with-swarm

Simple dashboard to use for fun outreach purposes and experiment with [Panel](https://panel.holoviz.org/). Comes with a suitable development environment defined in `environment.yml` including [jupyter-panel-proxy](https://github.com/holoviz/jupyter-panel-proxy) which enables a convenient Panel server accessible through Jupyter.

To set up locally:
```
conda env create --file environment.yml --name funswarm
conda activate funswarm
pre-commit install
jupyter lab &
```

Add notebooks to `notebooks/` and extend the list in `jupyter-panel-proxy.yml` to make them available to the Panel server.

Problems:
- https://github.com/holoviz/panel/issues/3170