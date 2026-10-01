## ☁️ Containerized WebLogic Environment

![GitHub top language](https://img.shields.io/github/languages/top/zappee/weblogic-box)
![GitHub Issues](https://img.shields.io/github/issues/zappee/weblogic-box)
![GitHub Release](https://img.shields.io/github/v/release/zappee/weblogic-box)

### 1) Overview

**WebLogic Box** is a pre-configured, isolated runtime environment designed to simplify Java EE application deployment on Oracle WebLogic Server without requiring complex local installations.
It eliminates manual configuration bottlenecks by packaging the server environment inside a reproducible container blueprint.


### 2) A note on timeless architecture

In today’s software development landscape, teams heavily favor lightweight, cloud-native frameworks like **Spring Boot** over traditional Java EE application servers.
However, large enterprise environments (especially within the financial, governmental, and corporate sectors) still rely extensively on **Oracle WebLogic Server** to run core, business-critical applications.

The primary objective of **WebLogic Box** is not merely to build a legacy runtime environment, but to serve as a reference architecture.
While the framework itself belongs to an older generation of technology, the containerization mechanisms engineered into these images are entirely **timeless and framework-agnostic**.

The architectural design and automation scripting can be directly applied to modern stacks (including Spring Boot) to solve complex container orchestration challenges.

By analyzing the source code, you can discover enterprise-grade patterns for:
* **Determining first-time Initialization:** Intelligent state checking that detects whether a container is booting up for the very first time or performing a routine restart, executing completely different execution paths dynamically.
* **Orchestrating multi-container startups:** Fail-safe sequencing techniques that force dependent containers to wait gracefully until prerequisites are verified, resuming the container boot sequence only when the environment is fully ready.
* **Decoupled inter-container configuration sharing:** Designing secure workflows to safely download and inject configuration files directly between running containers on the fly, eliminating configuration duplication and hardcoded values.
* **Dynamic script execution:** A clean mechanism to scan a directory and execute shell scripts sequentially without ever hardcoding individual file names, maximizing script extensibility.
* **Secured inter-container communication:** A robust solution to establish secure SSH and SFTP communication channels directly between the running containers.

Whether you are modernizing a legacy system or designing a complex architecture from scratch, this repository serves as a practical, reusable guide for bulletproof container design.

### 3) Image hierarchy

The project provides the following Docker images:
* Java 8
* Apache Tomcat 10.0
* Oracle Database Enterprise 12.2.0.1
* Oracle WebLogic 12.2.1.4 dmin and managed servers
* Splunk 8.2 server

![docker image hierarchy](docker-images.png)

### 4) Source core

[https://github.com/zappee/weblogic-box](https://github.com/zappee/weblogic-box)

### 🤝 Contributing

Contributions, feature requests, optimization, and bug reports are always welcome!
For more information, please visit my [homepage](https://zappee.github.io).
