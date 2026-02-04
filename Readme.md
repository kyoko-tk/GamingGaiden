<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/kulvind3r/gaminggaiden)](https://github.com/kulvind3r/gaminggaiden/stargazers)
[![GitHub Downloads (latest)](https://img.shields.io/github/downloads/kulvind3r/gaminggaiden/latest/total?label=Downloads%20-%20Latest&color=%23FFD166)](https://github.com/kulvind3r/GamingGaiden/releases/latest)
![GitHub Downloads (all)](https://img.shields.io/github/downloads/kulvind3r/gaminggaiden/total?label=Downloads%20-%20Total&color=%23FFD166)

[![Codacy Quality](https://app.codacy.com/project/badge/Grade/c4a01f22c3864d8c80b8c6891a6feb5f)](https://app.codacy.com/gh/kulvind3r/GamingGaiden/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/kulvind3r/gaminggaiden?label=Commit%20Activity&color=%23073B4C)](https://github.com/kulvind3r/gaminggaiden/graphs/commit-activity)
[![GitHub issues](https://img.shields.io/github/issues/kulvind3r/gaminggaiden?label=Issues&color=%23118AB2)](https://github.com/kulvind3r/gaminggaiden/issues)

![Gaming Gaiden](./readme-files/GamingGaidenBanner.png)

</div>

### 外伝 (Gaiden)

Японский

существительное (общее)

История; Побочная история;

Небольшое приложение в трее на PowerShell для Windows для отслеживания игрового времени. Помогает вам записывать вашу игровую историю на протяжении многих лет.

https://github.com/user-attachments/assets/4837b88c-e403-4069-a3f5-3f0147e9328a

## Возможности
- #### Отслеживание времени и поддержка эмуляторов
    - Отслеживает время игры и историю сессий для ПК или эмулированных игр.
    - Автоматически отслеживает новые ромы после однократной регистрации эмулятора.
    - Поддерживает ядра Retroarch.
    - Обнаруживает и удаляет время простоя из игровых сессий.
    - Готовая интеграция с HWiNFO64 с метриками времени сессии и статуса отслеживания.
    - Установка на несколько игровых ПК и совместное использование базы данных для отслеживания игр и часов игры для каждого ПК отдельно.
- #### Интерфейс и статистика
    - Быстрый браузерный интерфейс с поиском и сортировкой. Всплывающее окно быстрого просмотра для последних игр.
    - Множество подробной статистики по играм. Сводка за всё время, ежемесячный/ежегодный анализ времени, самые популярные игры, игры на эмулятор и т.д.
    - Анализ соотношения цены и качества для игрового ПК путем расчета стоимости игр в час или в месяц.
    - Встроенный поиск изображений Google для значков игр / обложек.
    - Отмечайте игры как Играю / Пройдено / Отложено / Брошено для отслеживания завершения бэклога.
- #### Функции качества жизни
    - Малый размер (~7 МБ). Высокая производительность (обнаружение игры менее 5 сек). Не нагружает CPU и RAM.
    - Полностью автономный и портативный, все данные хранятся в локальной базе данных.
    - Автоматическое резервное копирование данных после каждой игровой сессии.

> [!WARNING]  
> Gaming Gaiden доступен для загрузки только на этом Github репозитории. Любая копия, доступная в другом месте, может быть вредоносной.

## Как установить / обновить / использовать
1. Откройте окно Powershell от имени администратора и выполните следующую команду, чтобы разрешить загрузку модулей powershell в вашей системе. Выберите `Yes` при появлении запроса.
    - `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

2. Загрузите ***GamingGaiden.zip*** из [последнего релиза](https://github.com/kyoko-tk/GamingGaiden-ru/releases/latest).
3. Распакуйте папку ***GamingGaiden*** и запустите `Install.bat`. Выберите Да/Нет для автозапуска при загрузке.
4. Используйте ярлык на рабочем столе / в меню «Пуск» для запуска приложения.
5. Регулярно создавайте резервные копии `GamingGaiden.db` и папки `backups`, чтобы избежать потери данных. Нажмите ***Настройки => Открыть каталог установки*** в меню приложения, чтобы найти их.

## Как удалить
Запустите `Uninstall Gaming Gaiden` из папки меню «Пуск» `Gaming Gaiden`. `GamingGaiden.db` и `backups` не удаляются для сохранения данных.

## Неизвестный издатель
Windows SmartScreen может предупредить, что приложение от ***Неизвестного издателя***, поскольку у него нет подписи от публичного центра сертификации. 
Стоимость подписи для приложений составляет сотни долларов в год. Не могу себе это позволить.

## Ложные срабатывания антивируса
> :hearts:
> С ложными срабатываниями антивируса трудно бороться.
> Если вы нашли приложение полезным и безопасным. Пожалуйста, поставьте звезду на github, чтобы повысить доверие.

GamingGaiden выполняет следующие задачи, которые похожи на обычное поведение вредоносного ПО, что приводит к тому, что антивирусное программное обеспечение помечает его как вредоносное.

- Сканирование запущенных программ для обнаружения и отслеживания игр.
- Добавление записей реестра для интеграции с HWinfo64.
- Периодический переход в спящий режим для экономии ресурсов.
- Мониторинг активности пользователя для обнаружения времени простоя.
- Упаковка в виде исполняемого файла с помощью ps12exe.

Его реализация на основе PowerShell также вызывает флаги, поскольку скрипты powershell могут использоваться злонамеренно и имеют низкое доверие в техническом сообществе.

Антивирус помечает такое поведение, чтобы обезопасить пользователей, не проводя фактической проверки на вредоносную активность. Для исправления ложных срабатываний требуется вручную запрашивать у поставщиков антивируса снятие флагов с GamingGaiden или переписать его на компилируемый язык, например C#. Даже в этом случае нет гарантии исправления из-за его функциональности сканирования процессов.

Учитывая, что я написал его для личного использования, вышеперечисленное - это не то, над чем я могу работать, по крайней мере, какое-то время. Исходный код открыт и доступен для всех, чтобы проверить и убедиться, что ничего плохого не происходит. Пользователи несут ответственность за свою собственную безопасность и действия при использовании программы.

Пожалуйста, помните, что программное обеспечение с открытым исходным кодом поставляется без какой-либо поддержки или гарантий.

## Благодарности
Сделано с любовью, используя 

- [PSSQLite](https://www.powershellgallery.com/packages/PSSQLite) от [Warren Frame](https://github.com/RamblingCookieMonster)
- [ps12exe](https://github.com/steve02081504/ps12exe) от [Steve Green](https://github.com/steve02081504)
- [DOMPurify](https://github.com/cure53/DOMPurify) от [Cure53](https://github.com/cure53)
- [DataTables](https://datatables.net/)
- [Jquery](https://jquery.com/)
- [ChartJs](https://www.chartjs.org/)
- Различные иконки от [Icons8](https://icons8.com)
- Иконка игрового картриджа от [FreePik на Flaticon](https://www.flaticon.com/free-icons/game-cartridge)
- Милый [Ниндзя Вектор от Catalyststuff на Freepik](https://www.freepik.com/free-vector/cute-ninja-gaming-cartoon-vector-icon-illustration-people-technology-icon-concept-isolated-flat_42903434.htm)
- [Ninja Garden Font](https://www.fontspace.com/ninja-garden-font-f32923) от [Iconian Fonts](https://www.fontspace.com/iconian-fonts)


