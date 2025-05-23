# Дипломный практикум в Yandex.Cloud

# Создание облачной инфраструктуры

1) Создайте сервисный аккаунт
2) Подготовьте backend для Terraform:
Рекомендуемый вариант: S3 bucket в созданном ЯО аккаунте(создание бакета через TF)
3) Создайте конфигурацию Terrafrom, используя созданный бакет ранее как бекенд для хранения стейт файла. 
4) Создайте VPC с подсетями в разных зонах доступности.

# Создание Kubernetes кластера

1) При помощи Terraform подготовить как минимум 3 виртуальных машины Compute Cloud для создания Kubernetes-кластера. Тип виртуальной машины следует выбрать самостоятельно с учётом требовании к производительности и стоимости
Подготовить ansible конфигурации, можно воспользоваться, например Kubespray
Задеплоить Kubernetes на подготовленные ранее инстансы, в случае нехватки каких-либо ресурсов вы всегда можете создать их при помощи Terraform.

# Создание тестового приложения

а. Создайте отдельный git репозиторий с простым nginx конфигом, который будет отдавать статические данные.
б. Подготовьте Dockerfile для создания образа приложения.

# Подготовка cистемы мониторинга и деплой приложения

1) Задеплоить в кластер prometheus, grafana, alertmanager, экспортер основных метрик Kubernetes.
2) Задеплоить тестовое приложение, например, nginx сервер отдающий статическую страницу.

# Установка и настройка CI/CD

1) Автоматическая сборка docker образа при коммите в репозиторий с тестовым приложением.
2) Автоматический деплой нового docker образа.
Можно использовать teamcity, jenkins, GitLab CI или GitHub Actions.
