# Установка и настройка Minikube

Этот документ содержит краткую инструкцию по установке и базовой настройке Minikube.

---

## Установка Minikube

1. **Скачивание Minikube**  
   Скачайте последнюю версию Minikube:
   ```bash
   curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
     && chmod +x minikube
   ```
   > Делает файл исполняемым.

2. **Установка Minikube**  
   Переместите Minikube в `/usr/local/bin` для глобального доступа:
   ```bash
   sudo mkdir -p /usr/local/bin/
   sudo install minikube /usr/local/bin/
   ```

3. **Настройка псевдонима для kubectl**  
   Создайте псевдоним для удобного использования команды `kubectl` через Minikube:
   ```bash
   alias k="minikube kubectl --"
   ```
   > Позволяет использовать `k` вместо полной команды.

4. **Получение IP кластера**  
   Для доступа к сервисам получите IP-адрес Minikube:
   ```bash
   minikube ip
   ```
   > Возвращает IP-адрес вашего кластера.

---
