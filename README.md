## Jupyter notebook with Rust setup

1. Setup Rust from [official website](https://www.rust-lang.org/tools/install).
2. Setup Jupyter Notebook (or Jupyter Lab) from [official website](https://jupyter.org/)
3. Install Evcxr Jupyter Kernel. See [repository](https://github.com/evcxr/evcxr) for more details.

```bash
cargo install --locked evcxr_jupyter

# Make sure reloaded path environment variable
evcxr_jupyter --install

# Make sure that you have rust-src component installed
rustup component add rust-src

# Launch Jupyter Notebook
jupyter-lab
```

## Note

Don't ask Jupyter to "interrupt kernel", it won't work. Rust threads can't be interrupted.

## Uninstall

```bash
evcxr_jupyter --uninstall
cargo uninstall evcxr_jupyter
```
