# Описание playbook

## Общее описание
Playbook предназначен для установки Java, ElasticSearch и Kibana на соответствующих хостах.

## Переменные групп (group_vars).

1) Java.

* java_jdk_version - версия jdk.
* java_oracle_jdk_package - название установочного архива.
* java_home - переменная окружения, указывающая на директорию с установленным JDK.

2) Elasticsearch.

* elastic_version - версия Elasticsearch.
* elastic_home - переменная окружения, указывающая на директорию с установленным Elasticsearch.

3) Kibana.

* kibana_version - версия Kibana.
* kibana_home - переменная окружения, указывающая на директорию с установленным Kibana.

## Теги

Используются теги java, elastic, kibana для запусков play соответственно java, elasticsearch и kibana.

## Описание Play

1) Install Java

* установка переменных (facts)
* загрузка установочного пакета из локальной директории
* создание рабочей директории
* распаковка пакета в java_home
* создание по шаблону переменных окружений (templates)

2) Install Elasticsearch

* загрузка установочного пакета
* создание рабочей директории
* распаковка пакета в elastic_home
* создание по шаблону переменных окружений (templates)

3) Install Kibana

* загрузка установочного пакета
* создание рабочей директории
* распаковка пакета в kibana_home
* создание по шаблону переменных окружений (templates)