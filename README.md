
Sandbox to Simulate Grasping in Gazebo with the iCub
====================================================

## 🌐 Instructions to run the sandbox on the web

We make use of the [Gitpod Cloud IDE](https://gitpod.io) as infrastructure. Find out more on [YARP-enabled Gitpod workspaces][1].

1. Click on the following badge to start off the sandbox:

    [![Gitpod](https://gitpod.io/button/open-in-gitpod.svg)][2]

1. Once the sandbox workspace is ready, build and install the project:
    ```sh
    $ cd /workspace/icub-gazebo-grasping-sandbox 
    $ mkdir build && cd build
    $ cmake ../
    $ make install
    ```
1. Open the browser at the port `6080` from within Gitpod.
1. Open a terminal and run the grasping experiment:
   ```sh
   $ icub-grasp.sh
   ```

<p align="center">
    <img src="./assets/showcase.png">
</p>

## 🐳 Instructions to run the sandbox locally
To run the sandbox locally using [Docker](https://www.docker.com), go through the following steps:
1. Pull the docker image:
    ```sh
    $ docker pull pattacini/vvv-school
    ```
1. Launch the container:
    ```sh
    $ docker run -it --rm -p 6080:6080 --user gitpod pattacini/vvv-school
    ```
1. From within the container shell, launch the following scripts:
    ```sh
    $ init-icubcontrib-local.sh
    $ start-vnc-session-local.sh
    ```
1. Open up the browser and connect to **`localhost:6080`**.
1. Clone and build/install the project:
    ```sh
    $ git clone https://github.com/icub-tech-iit/icub-gazebo-grasping-sandbox.git /workspace/icub-gazebo-grasping-sandbox
    $ cd /workspace/icub-gazebo-grasping-sandbox 
    $ mkdir build && cd build
    $ cmake ../
    $ make install
    ```
1. Run the grasping experiment:
   ```sh
   $ icub-grasp.sh
   ```
1. Once done, from the container shell press **CTRL+D**.

### 🙏 Acknowledgements
Special thanks go to [xEnVrE](https://github.com/xEnVrE) for his help on simulating visuomanipulation tasks in Gazebo.

### 🆕 Contributing
Check out our [CONTRIBUTING guidelines](./.github/CONTRIBUTING.md).

[1]: https://spectrum.chat/icub/technicalities/yarp-enabled-gitpod-workspaces-available~73ab5ee9-830e-4b7f-9e99-195295bb5e34
[2]: https://gitpod.io/#https://github.com/icub-tech-iit/icub-gazebo-grasping-sandbox
