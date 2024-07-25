
The OpenSim Team will host a hands-on software workshop on Wednesday July 31st at the [19th International Symposium on Computer Methods in Biomechanics and Biomedical Engineeering (CMBBE 2024)](https://www.cmbbe-symposium.com/2024/). Details about the workshop content and instructions for setting up simulation environments for the hands-on software demos can be found below.

# OpenSim: Tools for rapid, large-scale musculoskeletal simulations

Musculoskeletal simulations provide a way to gain deep insights into how movement is coordinated. New tools for rapidly developing musculoskeletal simulations are enabling more researchers to leverage simulations by reducing the barrier to entry. In this workshop, we will present how our ecosystem of OpenSim tools for rapidly creating simulations, including from smartphone videos using OpenCap, and new features we’ve added to our Python and Jupyter notebook interfaces make it easier to generate simulations. With a combination of didactic portions and hands-on examples, participants will learn about OpenSim’s tools for creating simulations, and how to import movement data, create muscle-driven simulations, and analyze the results.

Attendees will learn:

- To understand the capabilities of tools available in the OpenSim ecosystem, including OpenCap for motion capture with smartphones
- To write Python code and use Jupyter notebooks to generate, analyze, and share simulations
- To understand validation approaches and potential research applications of the software

# Setup instructions

The first portion of the workshop will demonstrate [OpenCap](https://www.opencap.ai/). There is no hands-on coding segment for this software demonstration, but use the following link to open an interactive OpenCap session with pre-recorded data:

* [Demo 1: Recording movement data from smartphones with OpenCap](https://app.opencap.ai/session/c601e008-4fd0-492a-b675-04667c4df1c4)

The second and third portions of the workshop will demonstrate how to utilize the Python scripting interface in OpenSim to perform analyses, create visualizations, and generate muscle-driven simulations. We will use interactive Jupyter notebooks to demonstrate the OpenSim Python interface, and you may use these notebooks follow along with each software demonstration during the workshop.

Please follow the instructions below to set up each Jupyter notebook using either Google Colab (recommended) or via manual installation.

## Google Colab

Google Colab is a free service for hosting Jupyter notebooks in the cloud along with computing services. The [condacolab](https://github.com/conda-incubator/condacolab) project enables install Conda environments directly into a Jupyter notebook. We have designed this workshop around Google Colab and condacolab to streamline setting up Python environments with OpenSim, and we highly recommmend participants use this option.

To get started, simply click the links below to open the interactive Jupyter notebook for each software demonstration.

* [Demo 2: Analyzing movement data with OpenSim scripting in Python](https://githubtocolab.com/opensim-org/CMBBE2024/blob/main/Demo2_OpenSimIKPipeline/Demo%202%20-%20Analyzing%20movement%20data%20with%20OpenSim%20scripting%20in%20Python.ipynb)
* [Demo 3: Creating muscle-driven simulations with OpenSim Moco](https://githubtocolab.com/opensim-org/CMBBE2024/blob/main/Demo3_OpenSimMoco/Demo%203%20-%20Creating%20muscle-driven%20Simulations%20with%20OpenSim%20Moco.ipynb)

## Manual installation (not recommended)

The following instructions briefly describe how to set up a local Python environment in which you can run the Jupyter notebooks. Note that since the workshop materials are designed around Google Colab, certain sections of the notebooks will not work when running locally (see below). If choosing this approach, we assume that you are comfortable with Conda and Python.

1. Clone this repository.
```
git clone https://github.com/opensim-org/CMBBE2024.git
```

2. Create a new Conda environment.
```
conda create -n cmbbe2024 python=3.10
conda activate cmbbe2024
```

3. Install OpenSim.
```
conda install opensim-org::opensim
```

4. Install the `ipykernel` package.
```
conda install anaconda::ipykernel
```

5. Install the following additional packages.
```
conda install ipywidgets matplotlib scikit-learn
```

6. Open the notebook in an IDE that supports Jupyter notebooks (e.g., Visual Studio Code). Choose the enviroment that you created above (e.g., `cmbbe2024`) as the notebook kernal.

You should now be able to run the notebooks locally, with the following limitations:

1. Skip any sections involving installing `condacolab`.
2. Skip any sections involving installing the OpenSim Conda package, since we just did that above.
3. Skip any sections involving downloading resources, they will be included in the cloned repository.
4. Any sections involving the OpenSim Viewer are not guaranteed to work out-of-the-box and should likely be skipped. In Demo 3, uncommenting lines similar to `study.visualize(solution)` will enable visualization with the Simbody visualizer.


# Resources

* View the [OpenSim 4.5.1 API documentation here](https://simtk.org/api_docs/opensim/api_docs451/).
* View the [Scripting with Python Confluence page](https://opensimconfluence.atlassian.net/wiki/spaces/OpenSim/pages/53085346/Scripting+in+Python), for more information about creating OpenSim scripting environments in Python.
* View the [workshop Confluence page](https://opensimconfluence.atlassian.net/wiki/spaces/OpenSim/pages/226394116/CMBBE+2024+OpenSim+Workshop) for additional resources, including the workshop presentation slides.
