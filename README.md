<br/>
<p align="center">
  <h3 align="center">Parallele Systeme – NVIDIA in Docker</h3>

</p>

![Downloads](https://img.shields.io/github/downloads/derOtto/parallel-computing/total) ![Issues](https://img.shields.io/github/issues/derOtto/parallel-computing) ![License](https://img.shields.io/github/license/derOtto/parallel-computing)

## Table Of Contents

* [About the Project](#about-the-project)
* [Getting Started](#getting-started)
    * [Prerequisites](#prerequisites)
    * [Installation](#installation)
* [License](#license)
* [Authors](#authors)
* [Acknowledgements](#acknowledgements)

## About The Project

Im Ordner [tensorflow](./tensorflow) befindet sich eine Beispiel docker-compose.yml Datei, welche zwei Instanzen (eine mit und eine ohne GPU) startet.

Im Ordner [dockprom](./dockprom) befindet sich ein Beispiel, um ein Monitoring mit Prometheus zu starten.

Die Folien können unter folgendem Link gefunden werden: https://slides.com/jotto/parallele-systeme-nvidia-docker

<iframe src="https://slides.com/jotto/parallele-systeme-nvidia-docker/embed" width="576" height="420" title="Parallele Systeme – Nvidia & Docker" scrolling="no" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

## Getting Started

Hier wird beschrieben, wie man die Beispiele laufen lassen kann.

### Prerequisites

Folgendes wird benötigt:

* NVIDIA-GPU
* installiert
    * Docker
    * Docker Compose
    * NVIDA-Treiber
    * nvida-docker

### Installation

1. Repo klonen

```sh
git clone --recurse-submodules https://github.com/derOtto/parallel-computing.git
```

2. In geklonten Ordner wechseln:

```sh
cd parallel-computing
```

3. Changes aus dockprom-mods kopieren

```sh
cp -R dockprom-mods/* dockprom/
```

4. Monitoring starten

```sh
cd dockprom && docker-compose up -d
```

5. Tensorflow-Jupyter starten

```sh
cd ../tensorflow && docker-compose up
```

6. Im Browser über die entsprechenden Ports auf die Dienste zugreifen.

## License

Distributed under the MIT License. See [LICENSE](https://github.com/derOtto/parallel-computing/blob/main/LICENSE.md) for more information.

## Authors

* **Jan Otto** - *(otja1011)*

## Acknowledgements

* [ShaanCoding](https://github.com/ShaanCoding/)
* [Othneil Drew](https://github.com/othneildrew/Best-README-Template)
* [ImgShields](https://shields.io/)
* [Dockprom](https://github.com/stefanprodan/dockprom)
