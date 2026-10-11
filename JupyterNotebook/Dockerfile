FROM quay.io/jupyter/scipy-notebook:2026-09-01

USER ${NB_UID}

RUN mamba install --yes \
    -c conda-forge \
    plotly \
    xgboost \
    lightgbm \
    pyarrow \
    polars \
    requests \
    tqdm \
    python-dotenv \
    && mamba clean --all -f -y \
    && fix-permissions "${CONDA_DIR}" \
    && fix-permissions "/home/${NB_USER}"

WORKDIR /home/jovyan/work