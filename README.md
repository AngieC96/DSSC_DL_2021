# DSSC_DL_2021
Repository for the DL Course AA 2020-2021 @ DSSC UniTS



## Linux Setup

Download, clone or fork (your choice) this repository in a directory `PATH_TO_DIR/`, then run.

```bash
cd PATH_TO_DIR/DSSC_DL_2021/
```

Create a virtual environment using `python3` (commands are provided for *Debian-like* GNU/Linux distributions). If it's the first time you use `pip` and create a virtual environment, run

```bash
# Install pip for Python 3:
sudo apt-get install python3-pip
# Install virtualenv
python3 -m pip install --user virtualenv
```

If you have already installed `pip` and `virtualenv`, then skip them.

Then run

```bash
python3 -m virtualenv -p "$(which python3)" venv
```

Now you should see `PATH_TO_DIR/DSSC_DL_2021/venv/` folder.
Activate the environment and install the requirements (don't specify the versions of the packages, so you'll get the latest versions):

```bash
source venv/bin/activate
python3 -m pip install -r ./requirements.txt
```

Register the just-installed virtual environment for use with Jupyter:

```bash
python3 -m ipykernel install --user --name DSSC_DL_2021 --display-name "Python (DL virtualenv)"
```

Then type:

```bash
pip freeze
```

and save the output in the file `requirements.txt`, overwriting the previous file.

Too see the dependencies of a package, run

```bash
pip3 show <name_package>
```

Open your notebooks using jupyter-notebook (or jupyter-lab):

```bash
python3 -m jupyter notebook
```

To deactivate the environment use `deactivate` command.



To convert the `.ipynb` file in `HTML` use the following command

```bash
jupyter nbconvert --to html notebook.ipynb
```
