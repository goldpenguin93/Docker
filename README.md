<h1>It is Doker Tutorial. </h2> 


https://www.slideshare.net/pyrasis/docker-docker-38286477 (KOR.ver)



https://docker-curriculum.com/ (ENG.ver)




# Docker
Docker is a computer program that performs operating-system-level virtualization, also known as "containerization". It was first released in 2013 and is developed by Docker, Inc.

Docker is used to run software packages called "containers". Containers are isolated from each other and bundle their own tools, libraries and configuration files; they can communicate with each other through well-defined channels. All containers are run by a single operating system kernel and are thus more lightweight than virtual machines. Containers are created from "images" that specify their precise contents. Images are often created by combining and modifying standard images downloaded from publi

<h2>Technology</h2>

Docker can use different interfaces to access virtualization features of the Linux kernel.
Docker is developed primarily for Linux, where it uses the resource isolation features of the Linux kernel such as cgroups and kernel namespaces, and a union-capable file system such as OverlayFS and others to allow independent "containers" to run within a single Linux instance, avoiding the overhead of starting and maintaining virtual machines (VMs). The Linux kernel's support for namespaces mostly isolates an application's view of the operating environment, including process trees, network, user IDs and mounted file systems, while the kernel's cgroups provide resource limiting for memory and CPU.[Since version 0.9, Docker includes the libcontainer library as its own way to directly use virtualization facilities provided by the Linux kernel, in addition to using abstracted virtualization interfaces via libvirt, LXC and systemd-nspawn.

Building on top of facilities provided by the Linux kernel (primarily cgroups and namespaces), a Docker container, unlike a virtual machine, does not require or include a separate operating system. Instead, it relies on the kernel's functionality and uses resource isolation for CPU and memory,and separate namespaces to isolate the application's view of the operating system. Docker accesses the Linux kernel's virtualization features either directly using the libcontainer library, which is available as of Docker 0.9, or indirectly via libvirt, LXC (Linux Containers) or systemd-nspawn.

<h2>Components</h2>

The Docker software is a service consisting of three components:

Software: The Docker daemon, called dockerd, is a persistent process that manages Docker containers and handles container objects. The daemon listens for requests sent via the Docker Engine API.The Docker client program, called docker, provides a command-line interface that allows users to interact with Docker daemons.
Objects: Docker objects are various entities used to assemble an application in Docker. The main classes of Docker objects are images, containers, and services.
A Docker container is a standardized, encapsulated environment that runs applications. A container is managed using the Docker API or CLI.
A Docker image is a read-only template used to build containers. Images are used to store and ship applications.
A Docker service allows containers to be scaled across multiple Docker daemons. The result is known as a "swarm", a set of cooperating daemons that communicate through the Docker API.
Registries: A Docker registry is a repository for Docker images. Docker clients connect to registries to download ("pull") images for use or upload ("push") images that they have built. Registries can be public or private. Two main public registries are Docker Hub and Docker Cloud. Docker Hub is the default registry where Docker looks for images


<h2>Tools</h2>
Docker Compose is a tool for defining and running multi-container Docker applications.It uses YAML files to configure the application's services and performs the creation and start-up process of all the containers with a single command. The docker-compose CLI utility allows users to run commands on multiple containers at once, for example, building images, scaling containers, running containers that were stopped, and more. Commands related to image manipulation, or user-interactive options, are not relevant in Docker Compose because they address one container.The docker-compose.yml file is used to define an application's services and includes various configuration options. For example, the build option defines configuration options such as the Dockerfile path, the command option allows one to override default Docker commands, and more.The first public version of Docker Compose (version 0.0.1) was released on December 21, 2013 The first production-ready version (1.0) was made available on October 16, 2014
Docker Swarm provides native clustering functionality for Docker containers, which turns a group of Docker engines into a single virtual Docker engine. In Docker 1.12 and higher, Swarm mode is integrated with Docker Engine. The swarm CLI utility allows users to run Swarm containers, create discovery tokens, list nodes in the cluster, and more. The docker node CLI utility allows users to run various commands to manage nodes in a swarm, for example, listing the nodes in a swarm, updating nodes, and removing nodes from the swarm. Docker manages swarms using the Raft Consensus Algorithm. According to Raft, for an update to be performed, the majority of Swarm nodes need to agree on the update.
Operation
Docker implements a high-level API to provide lightweight containers that run processes in isolation.

According to a Linux.com article,

Docker is a tool that can package an application and its dependencies in a virtual container that can run on any Linux server. This helps enable flexibility and portability on where the application can run, whether on premises, public cloud, private cloud, bare metal, etc.

Because Docker containers are lightweight, a single server or virtual machine can run several containers simultaneously. A 2016 analysis found that a typical Docker use case involves running five containers per host, but that many organizations run 10 or more.

Using containers may simplify the creation of highly distributed systems by allowing multiple applications, worker tasks and other processes to run autonomously on a single physical machine or across multiple virtual machines. This allows the deployment of nodes to be performed as the resources become available or when more nodes are needed, allowing a platform as a service (PaaS)-style of deployment and scaling for systems such as Apache Cassandra, MongoDB and Riak.

<h2>Integration</h2>
Docker can be integrated into various infrastructure tools, including Amazon Web Services, Ansible, CFEngine, Chef,Google Cloud Platform,IBM Bluemix, HPE Helion Stackato, Jelastic, Jenkins, KubernetesMicrosoft Azure,OpenStack Nova,OpenSVC,Oracle Container Cloud Service,Puppet ProGet, Salt, Vagrant, and VMware vSphere Integrated Containers.

The Cloud Foundry Diego project integrates Docker into the Cloud Foundry PaaS.

Nanobox uses Docker (natively and with VirtualBox) containers as a core part of its software development platform

Red Hat's OpenShift PaaS integrates Docker with related projects (Kubernetes, Geard, Project Atomic and others) since v3 (June 2015).

The Apprenda PaaS integrates Docker containers in version 6.0 of its product.

Jelastic PaaS provides managed multi-tenant Docker containers with full compatibility to the native ecosystem.

The Tsuru PaaS integrates Docker containers in its product in 2013, the first PaaS to use Docker in a production environment.

For Windows
On October 15, 2014, Microsoft announced integration of the Docker engine into the next Windows Server release, and native support for the Docker client role in Windows. On June 8, 2016, Microsoft announced that Docker now could be used natively on Windows 10 with Hyper-V Containers, to build, ship and run containers utilizing the Windows Server 2016 Technical Preview 5 Nano Server container OS image.

Since then, a feature known as Windows Containers was made available for Windows 10 and Windows Server 2016. There are two types of Windows Containers: "Windows Server Containers" and "Hyper-V Isolation". The former has nothing to do with Docker. The latter, however, is a form of hardware virtualization (as opposed to OS-level virtualization) and uses Docker to deliver the guest OS image. The guest OS image is a Windows Nano Server image, which is 652 MB in size and has the same limitations of Nano Server, as well as a separate end-user license agreement.


<h2>Reference site<h2>
https://www.wikipedia.org/
