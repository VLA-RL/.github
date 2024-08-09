# VLA-RL

## Prerequisite
1. Install CoppeliaSim 4.1
    - You can use the following command:
        ```Bash
        wget https://downloads.coppeliarobotics.com/V4_1_0/CoppeliaSim_Edu_V4_1_0_Ubuntu20_04.tar.xz
        mkdir -p $HOME/CoppeliaSim && tar -xf CoppeliaSim_Edu_V4_1_0_Ubuntu20_04.tar.xz -C $HOME/CoppeliaSim --strip-components 1
        rm -rf CoppeliaSim_Edu_V4_1_0_Ubuntu20_04.tar.xz
        ```
    - Alternatively
      - Download CoppeliaSim 4.1 from this link: https://www.coppeliarobotics.com/previousVersions.
      - In the folder you install it in
        ``` Bash
        tar -xf CoppeliaSim_Edu_V4_1_0_Ubuntu20_04.tar.xz
        mv CoppeliaSim_Edu_V4_1_0_Ubuntu20_04 ~/
        ```
      - change the name of the folder to CoppeliaSim 
2. Set up environment variables:
   - **(Recommended)** Use Virtual Environment:
     - Create Virtual Environment:
       ```Bash
        python -m venv <virtual environment name>
       ```
     - Add the following to your `<virtual environment name>/bin/activate` (ex. `nvim <virtual environment name>/bin/activate`)file:
       ```Bash
        # set env variables
        export COPPELIASIM_ROOT=${HOME}/CoppeliaSim
        export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$COPPELIASIM_ROOT
        export QT_QPA_PLATFORM_PLUGIN_PATH=$COPPELIASIM_ROOT
       ```
     - Activate the Virtual Environment:
       ```Bash
        source venv/bin/activate  # On Windows use `.\venv\Scripts\activate`
       ```
  - If not using a virtual environment, add the following to your `~/.bashrc` (ex. `nvim ~/.bashrc`) file:
    ```Bash
    # set env variables
    export COPPELIASIM_ROOT=${HOME}/CoppeliaSim
    export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$COPPELIASIM_ROOT
    export QT_QPA_PLATFORM_PLUGIN_PATH=$COPPELIASIM_ROOT
    ```
