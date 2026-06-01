# Rover-Card

<p align="center">
  <img src="brand/icon.png" alt="Rover" width="180" />
</p>

**Lovelace-карточка для системы [Rover](https://github.com/BotoVed/Rover)** — дистанционное управление умным домом через LoRa, когда интернет недоступен.

🧩 Это один из трёх компонентов экосистемы Rover. Полная картина и документация — в [главном репозитории](https://github.com/BotoVed/Rover).

---

## Что это

Карточка для дашборда Home Assistant, показывающая, что происходит в Rover-радиосети:

- Имя дома и количество подключённых телефонов (онлайн / всего).
- Живой поток пакетов — последние 200 входящих и исходящих, с раскрытием подробностей по клику.
- Админ-панель с QR-онбордингом новых клиентов (под паролем).

Управление самими устройствами в карточке нет — для этого есть нативные карточки HA. Rover-Card отвечает за то, **чего не видно стандартными средствами** — состояние самой радиосети.

## Установка

### Через HACS
1. HACS → Frontend → ⋮ → Custom repositories.
2. Добавить `https://github.com/BotoVed/Rover-Card` как **Dashboard**.
3. Установить **Rover Card**, перезагрузить страницу.

Добавить на дашборд:
```yaml
type: custom:rover-card
```

### Вручную
Скачать `rover-card.js` из [последнего релиза](https://github.com/BotoVed/Rover-Card/releases), положить в `<HA_config>/www/community/rover-card/`, добавить в resources Lovelace.

## Связанные репозитории

- **[Rover](https://github.com/BotoVed/Rover)** — плагин Home Assistant (бэк) + общая документация
- **[Rover-App](https://github.com/BotoVed/Rover-App)** — мобильное приложение Android

## Лицензия

[GPL v3](https://github.com/BotoVed/Rover/blob/main/LICENSE)
