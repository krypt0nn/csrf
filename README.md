<h1 align="center">🚀 CSRF</h1>

**CSRF** - небольшая функция для реализации [CSRF токенов](https://ru.wikipedia.org/wiki/Межсайтовая_подделка_запроса)

## Установка
```cmd
php qero.phar i KRypt0nn/csrf
```

```php
<?php

require 'qero-packages/autoload.php';
```

[Что такое Qero?](https://github.com/KRypt0nn/Qero)

<p align="center">или</p>

Скачайте файл `csrf.php` и подключите его к проекту с помощью *require*

```php
<?php

require 'csrf.php';
```

## Пример работы

```html
<?php

require 'qero-packages/autoload.php';

if (isset ($_POST['csrf']))
    echo 'csrf token status: '. (
        csrf($_POST['csrf']) ? 'working' : 'not working');

?>

<form method="post">
    <input type="hidden" name="csrf" value="<?= csrf() ?>">

    <button type="submit">
</form>
```

Автор: [Подвирный Никита](https://vk.com/technomindlp). Специально для [Enfesto Studio Group](https://vk.com/hphp_convertation)