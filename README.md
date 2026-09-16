# Егор Кузнецов

### Linux Engineer / System Administrator / Junior DevOps

Системный администратор Linux с коммерческим опытом автоматизации рабочих мест, мониторинга, сопровождения Linux/Windows-инфраструктуры и интеграции Linux с Active Directory.

Развиваюсь в сторону Linux Engineering и Junior DevOps: изучаю Docker, Kubernetes, Ansible, CI/CD, Prometheus и Grafana. В репозиториях собраны **реальные рабочие кейсы** и **учебные лабораторные стенды** — они помечены явно.

📄 **Резюме:** [hh.ru](https://hh.ru/resume/3035d41cff10607a400039ed1f32467a416956)

---

## Основные навыки

- **Linux:** ALT Linux, Ubuntu, Astra Linux
- **Скрипты и автоматизация:** Bash, Python, Ansible (Jinja2, Vault)
- **Мониторинг:** Zabbix, UserParameter, OVAL/ScanOval, Prometheus, Grafana, Alertmanager
- **Интеграция с AD:** SSSD, Kerberos, SMB/CIFS
- **Контейнеры:** Docker, Docker Compose, containerd
- **CI/CD:** GitHub Actions, Jenkins
- **Базы данных:** PostgreSQL, Redis
- **Kubernetes:** kubeadm, kubectl, манифесты *(базовый уровень)*

---

## 💼 Commercial cases

Реальные задачи из Законодательного Собрания Кировской области и Ростелекома.

### Enterprise Automation & Security

**Задача:** сократить время подготовки рабочих мест ALT Linux и внедрить аудит по ФСТЭК.

**Решение:**
- Bash-скрипт автоматизированного развёртывания: установка ПО, настройка Zabbix Agent, GLPI, UrBackup, OVAL-сканирования.
- Мониторинг в Zabbix 7.0: UserParameter, авторегистрация, OVAL-метрики, триггеры.
- Интеграция с Active Directory через SSSD/Kerberos, автомонтирование SMB.
- Диагностический Bash-инструмент для AD/SSSD.

**Результат:** время подготовки рабочего места сокращено **с 2–3 часов до 20–30 минут**.

---

### Immich Infrastructure Rescue

**Задача:** стабилизировать сервис Immich, который падал из-за OOM Killer, заполнения диска и schema drift PostgreSQL.

**Решение:**
- Перенос PostgreSQL и медиабиблиотеки на отдельный раздел.
- Перенос **390 ГБ** данных без изменения путей в БД.
- Устранение schema drift, восстановление первичных ключей.
- Добавление 4 ГБ swap, снижение параллелизма задач.
- Автоматизация резервного копирования PostgreSQL.

**Результат:** заполнение корневого раздела снижено **с 88% до 21%**, сервис стабилен.

---

## 🧪 Lab projects

Учебные стенды. Не являются production-опытом — это практика технологий.

### 🐍 [myflask](https://github.com/hagegata/myflask) — Docker + CI/CD

Flask + Redis. Dockerfile с multi-stage build, Compose, healthcheck.
CI в GitHub Actions: matrix-тесты (Python 3.10–3.12), cache, Trivy, Cosign, публикация в GHCR.

---

### 📊 [monitoring](https://github.com/hagegata/monitoring) — стек наблюдаемости

Prometheus + Node Exporter + Grafana + Alertmanager. Правило `NodeDown`, полный цикл алерта (Firing → Inactive). Дашборд Node Metrics.

---

### ⚙️ [ansible-lab](https://github.com/hagegata/ansible-lab) — IaC на Ansible

Inventory, роли, Jinja2-шаблоны, handlers, Vault. Подтверждена идемпотентность (`changed=0` при повторном запуске).

---

### ⚙️ [jenkins-lab](https://github.com/hagegata/jenkins-lab) — Jenkins pipeline

Jenkins в Docker, pipeline из 4 стадий. Docker-команды через docker.sock.

---

### ☸️ [k8s-basics](https://github.com/hagegata/k8s-basics) — учебный Kubernetes-стенд

Одноузловой кластер на ALT Linux (kubeadm + containerd). Манифесты Pod/Deployment/Service/ConfigMap/Secret/StatefulSet/PV-PVC. Разбор проблем CNI.

---

### 🛠️ [linux-automation](https://github.com/hagegata/linux-automation) — Bash-скрипты

autoinstall, cifs-mount, k8s-install, ad-fix — с документацией и траблшутингом.

---

## 📚 Сейчас изучаю

- **Kubernetes:** Helm, Ingress, рабочий CNI
- **Terraform:** IaC для облаков
- **DevSecOps:** безопасность контейнеров и CI/CD
- **Loki:** логи в стеке мониторинга

---

## 📬 Контакты

- GitHub: [github.com/hagegata](https://github.com/hagegata)
- Telegram: @Kuznetsov_E_R
- Email: fradik.kuznezov@mail.ru
- Резюме: [hh.ru](https://hh.ru/resume/3035d41cff10607a400039ed1f32467a416956)
