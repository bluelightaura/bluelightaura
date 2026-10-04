![bluelightaura — tests network gear, writes the tools that do the testing](assets/banner.png)

[English version](README.md)

<div align="center">

# Максим Степанов

### Сетевой инженер · Python AQA · SDET

Автоматизация сетей, тестовая инфраструктура и инструменты
для проверки оборудования L2/L3.

[![GitHub](https://img.shields.io/badge/GitHub-bluelightaura-181717?style=for-the-badge&logo=github)](https://github.com/bluelightaura)
![Location](https://img.shields.io/badge/Location-Russia-1261A0?style=for-the-badge)
![Focus](https://img.shields.io/badge/Focus-SDET%20%7C%20SRE%20%7C%20DevOps-0077B5?style=for-the-badge)

</div>

---

## Обо мне

Автоматизирую тестирование сетевого оборудования, собираю лабораторные
стенды L2/L3 и пишу инструменты для анализа сетевой инфраструктуры.

- Тестирование и автоматизация ПО сетевого оборудования
- Разработка тестовых фреймворков на Python и Pytest
- Коммутаторы L2/L3, Ethernet, VLAN, STP/RSTP, маршрутизация
- Генерация и анализ трафика: TRex, DPDK, Scapy
- Виртуальные стенды на containerlab и FRRouting, отчётность через Allure
- Тестовые окружения на Linux и CI/CD
- Мониторинг инфраструктуры на Prometheus и Grafana
- Расту в сторону SDET, SRE и DevOps

## Стек

<p align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Fedora](https://img.shields.io/badge/Fedora-51A2DA?style=for-the-badge&logo=fedora&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=for-the-badge&logo=gitlab&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![TRex](https://img.shields.io/badge/TRex%20%C2%B7%20DPDK-005073?style=for-the-badge)
![Allure](https://img.shields.io/badge/Allure-2EB67D?style=for-the-badge)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)

</p>

## Проекты

<table>
<tr>
<td width="50%" valign="top">

### [CLIRadar](https://github.com/bluelightaura/CLIRadar)

Вендоронезависимый сканер CLI сетевых устройств.

Обходит дерево команд через контекстную справку, сверяет CLI железки
с вендорской документацией и собирает YAML-каталог и HTML-отчёт.

**Стек:** Python, SSH, Telnet, YAML, Pytest, Ruff, Bandit

</td>
<td width="50%" valign="top">

### [TRaphy](https://github.com/bluelightaura/traphy)

Терминальный генератор трафика для тестирования оборудования L2-L4.

Собираешь кадр руками, а дальше выбираешь, чем он уйдёт в провод:
Scapy-скриптом через ядро или TRex на карте — DPDK на линейной скорости
либо AF_PACKET, когда карту нельзя забирать у ядра. Сам готовит генератор:
привязывает карты, пишет `trex_cfg.yaml`, поднимает демона — назвав до
того, что именно сломает. Потери показываются только тогда, когда их
действительно мерили, и прогон говорит, какому счётчику поверил.

**Стек:** Python, Scapy, TRex, DPDK, Paramiko, SSH, Pytest, Ruff

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [NetBench](https://github.com/bluelightaura/netbench)

Стенд, который поднимает себя сам, и набор, который по нему гоняют.

Топология встаёт контейнерами из одного файла, живёт ровно прогон и
гасится даже если тесты упали. Четыре слоя, каждый проверяется отдельно:
Terraform, Ansible и containerlab, pytest по SSH, три пайплайна CI, отчёт
Allure. Написан образцом архитектуры — склонировать и положить свои
топологии.

**Стек:** Pytest, containerlab, FRRouting, Ansible, Terraform, Allure

</td>
<td width="50%" valign="top">

### [RestPilot](https://github.com/bluelightaura/restpilot)

Консольный клиент для REST API, которые писал не ты.

Импортирует контракт OpenAPI, держит окружения и токены вне истории
шелла и превращает спецификацию в готовый к запуску набор pytest.

**Стек:** Python, Typer, httpx, Pydantic, Jinja2, OpenAPI, Pytest

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [DevOps Monitoring Stack](https://github.com/bluelightaura/devops-monitoring-stack)

Автоматическое развёртывание Nginx, Prometheus, Grafana и экспортеров.

Сделан в менторской программе под руководством сеньорного DevOps-инженера
из бигтеха. Всё, что смотрит внутрь, слушает loopback и достаётся через
SSH-туннель; наружу опубликован только Nginx.

**Стек:** Docker, Ansible, Prometheus, Grafana, Nginx

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

## Опыт

- Тестирование и автоматизация тестирования ПО сетевого оборудования
- Ранее — инженер по планированию и оптимизации сетей
- Магистр физики с отличием
- Опыт с сетевым оборудованием, оптической и медной инфраструктурой
- Научные интересы: волоконно-оптические системы связи, управление
  поляризацией и устойчивость сетей

## Чем занят сейчас

- Архитектура автоматизации тестирования
- Наблюдаемость сетевых устройств
- CI/CD для тестирования железа и прошивок
- Сетевая автоматизация
- SDET, SRE и DevOps

## Статистика GitHub

<div align="center">

<img height="165"
src="https://github-readme-stats.vercel.app/api?username=bluelightaura&show_icons=true&theme=github_dark&hide_border=true&rank_icon=github"
alt="Статистика GitHub" />

<img height="165"
src="https://github-readme-stats.vercel.app/api/top-langs/?username=bluelightaura&layout=compact&theme=github_dark&hide_border=true"
alt="Используемые языки" />

</div>

---

<div align="center">

### Сетевая инженерия встречается с программной

</div>
