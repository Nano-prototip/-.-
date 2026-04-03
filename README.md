# Домашнее задание к занятию «Вычислительные мощности. Балансировщики нагрузки»  

## Задание. Yandex Cloud 

1. Создать бакет Object Storage и разместить в нём файл с картинкой:

 - Создать бакет в Object Storage с произвольным именем (например, _имя_студента_дата_).
 - Положить в бакет файл с картинкой.
 - Сделать файл доступным из интернета.
 
2. Создать группу ВМ в public подсети фиксированного размера с шаблоном LAMP и веб-страницей, содержащей ссылку на картинку из бакета:

 - Создать Instance Group с тремя ВМ и шаблоном LAMP. Для LAMP рекомендуется использовать `image_id = fd827b91d99psvq5fjit`.
 - Для создания стартовой веб-страницы рекомендуется использовать раздел `user_data` в [meta_data](https://cloud.yandex.ru/docs/compute/concepts/vm-metadata).
 - Разместить в стартовой веб-странице шаблонной ВМ ссылку на картинку из бакета.
 - Настроить проверку состояния ВМ.
 
3. Подключить группу к сетевому балансировщику:

 - Создать сетевой балансировщик.
 - Проверить работоспособность, удалив одну или несколько ВМ.

---

## Решение.

1. [Бакет](https://github.com/Nano-prototip/-.-/blob/main/bucket.tf)

<img width="711" height="188" alt="01" src="https://github.com/user-attachments/assets/a4d919f6-e4d9-4f1c-a863-1e08028acd50" />

2. [Instance Group](https://github.com/Nano-prototip/-.-/blob/main/instance-group.tf)

Скриншот Instance Group

<img width="1108" height="262" alt="02" src="https://github.com/user-attachments/assets/001f7baa-f7cb-4231-8188-a6293207e044" />

Скриншот Target Group

<img width="539" height="162" alt="03" src="https://github.com/user-attachments/assets/61b14b2f-303d-4916-a3e8-b7c85034f649" />

Скриншот картинки на инстансах из Instance Group

<img width="819" height="254" alt="04" src="https://github.com/user-attachments/assets/561f0563-5313-4992-b41f-f49d1677dbe2" />

3. [load-balancer](https://github.com/Nano-prototip/-.-/blob/main/lb.tf)
Проверка работоспособности

<img width="575" height="221" alt="05" src="https://github.com/user-attachments/assets/be01bebd-a832-42ed-a4c9-a5421c227fa7" />

