# Требования к проекту
---

# Содержание
1 [Введение](#intro)  
1.1 [Назначение](#appointment)  
1.2 [Бизнес-требования](#business_requirements)  
1.2.1 [Исходные данные](#initial_data)  
1.2.2 [Возможности бизнеса](#business_opportunities)  
1.2.3 [Границы проекта](#project_boundary)  
1.3 [Обзор аналогов](#analogues)  
2 [Требования пользователя](#user_requirements)  
2.1 [Программные интерфейсы](#software_interfaces)  
2.2 [Интерфейс пользователя](#user_interface)  
2.3 [Характеристики пользователей](#user_specifications)  
2.3.1 [Классы пользователей](#user_classes)  
2.3.2 [Аудитория приложения](#application_audience)  
2.3.2.1 [Целевая аудитория](#target_audience)  
2.3.2.1 [Побочная аудитория](#collateral_audience)  
2.4 [Предположения и зависимости](#assumptions_and_dependencies)  
3 [Системные требования](#system_requirements)  
3.1 [Функциональные требования](#functional_requirements)  
3.1.1 [Основные функции](#main_functions)  
3.1.1.1 [Вход пользователя в приложение](#user_logon_to_the_application)  
3.1.1.2 [Загрузка курсов](#download_products)  
3.1.1.3 [Просмотр информации о линамике изменения курса валюты](#download_product)  
3.1.1.4 [Настройка курсов](#add_to_cart)  
3.1.2 [Ограничения и исключения](#restrictions_and_exclusions)  
3.2 [Нефункциональные требования](#non-functional_requirements)  
3.2.1 [Атрибуты качества](#quality_attributes)  
3.2.1.1 [Требования к удобству использования](#requirements_for_ease_of_use)  
3.2.2 [Внешние интерфейсы](#external_interfaces)  
3.2.3 [Ограничения](#restrictions)  

<a name="intro"/>

# 1 Введение

<a name="appointment"/>

## 1.1 Назначение
В этом документе описаны функциональные и нефункциональные требования к приложению «Сurrencies» для ОС Android. Этот документ предназначен для команды, которая будет реализовывать и проверять корректность работы приложения. 

<a name="business_requirements"/>

## 1.2 Бизнес-требования

<a name="initial_data"/>

### 1.2.1 Исходные данные
Большинство людей работают в интенсивном режиме поэтому зачастую по пути с работы забегают купить фаст-фуд. Когда они приходят, то видят десятки баннеров с ценами и непонятными названиями, даже если с этим можно разобраться, то выполнение заказа займет еще минут 20-30. Приложение будет разработано с целью упростить процесс выбора товара и ознакомлния с ценами, а также заказа еды заранее, чтобы к приходу в кафе она уже была готова.

<a name="business_opportunities"/>

### 1.2.2 Возможности бизнеса
Многие молодые люди желают иметь приложение, которое позволит просмотреть актуальный курс валют или отследить динамику их изменеия. Подобное приложение позволит им тратить меньше времени на получение желаемого. Отсутствие авторизации позволит увеличить количество людей, использующих приложение.

<a name="project_boundary"/>

### 1.2.3 Границы проекта
Приложение «Currencies» позволит всем пользователям просматривать информацию о текущих курсах волют, а так же динамику их изменения за последний 30 дней.

<a name="analogues"/>

## 1.3 Обзор аналогов
Аналогами будут являться приложения разлычных банков. Далее приведен список наиболее выделяющихся.
Myfin.by - одно из лучших приложений. Имеется выбор банка, выбор валюты, конвертер валют, а так же курсы валют на карте в реальном времени.
imbanking - приложение крупнейшего банка РБ. Имеется возможность просмотра курсов, а так же присутствует конвертер валют. 

<a name="user_requirements"/>

# 2 Требования пользователя

<a name="software_interfaces"/>

## 2.1 Программные интерфейсы
Приложение обрабатывает данные из api НБРБ. 

<a name="user_interface"/>

## 2.2 Интерфейс пользователя

<details>
<summary>Главный экран.</summary>

![Главный экран]((https://user-images.githubusercontent.com/70812017/199708821-7be5665d-fa28-4f76-8ea5-1b1cbb388e62.png))

</details>
  
 <details>
<summary>Динамика изменения курса валюты.</summary>

![Динамика]((https://user-images.githubusercontent.com/70812017/199708940-9c5c0509-0da6-4ffb-bf9f-05e99901690a.png)) 

</details>

  <details>
<summary>Экран настроек.</summary>

![Экран настройки]((https://user-images.githubusercontent.com/70812017/199709033-74017d41-7368-4b55-a2d2-1dbc27416013.png))

</details>

<a name="user_specifications"/>

## 2.3 Характеристики пользователей

<a name="user_classes"/>

### 2.3.1 Классы пользователей

| Класс пользователей | Описание |
|:---|:---|
| Анонимные пользователи | Все пользователи, приложение не требует авторизации |

<a name="application_audience"/>

### 2.3.2 Аудитория приложения

<a name="target_audience"/>

#### 2.3.2.1 Целевая аудитория
Люди средней возрастной категории со средним или выше среднего уровнем образования, обладающие минимальной технической грамотностью.

<a name="collateral_audience"/>

#### 2.3.2.2 Побочная аудитория
Люди младшей и встаршей возрастной категории, обладающие вышеперечисленными качествами.

<a name="assumptions_and_dependencies"/>

## 2.4 Предположения и зависимости
1. Приложение не работает при отсутствии подключения к Интернету;

<a name="system_requirements"/>

# 3 Системные требования

<a name="functional_requirements"/>

## 3.1 Функциональные требования

<a name="main_functions"/>

### 3.1.1 Основные функции

<a name="user_logon_to_the_application"/>

#### 3.1.1.1 Вход пользователя в приложение
**Описание.** Приложение не требует авторизации и запускается сразу на главном экране.

<a name="download_products"/>

#### 3.1.1.2 Загрузка валют
**Описание.** После входа пользователя в приложение необходимо загрузить список валют и курсы к ним.

| Функция | Требования | 
|:---|:---|
| Загрузка списка валют и курсов | Приложение должно загрузить список валют и курсов к ним. В случае ошибки или отсутствия интеренета должно быть выведено соответствующее сообщение|

<a name="download_product"/>

#### 3.1.1.3 Просмотр информации о динамике изменения курса валюты
**Описание.** Пользователь имеет возможность просмотреть информацию о данамике изменения курса отдельной валюты в течении 30 дней.

| Функция | Требования | 
|:---|:---|
| Просмотр информации | Пользователь имеет возможность выбрать курс в таблице одинарным кликом по нему. Приложение должно отобразить его динамику изменения в течении 30 дней|

<a name="add_to_cart"/>

#### 3.1.1.4 Настройки курсов
**Описание.** Пользователь имеет возможность настроить под себя курсы.

| Функция | Требования | 
|:---|:---|
| Настройка курсов | Пользователь имеет возможность настроить курсы под себя. Включить или выключить их отображение на главное странице, а так же поменять их положение.|

### 3.1.2 Ограничения и исключения
1. Приложение работает только при наличии подключения к Интернету;
2. Заказ происходит только при заполненных полях имени и номера. 

<a name="non-functional_requirements"/>

## 3.2 Нефункциональные требования

<a name="quality_attributes"/>

### 3.2.1 Атрибуты качества

<a name="requirements_for_ease_of_use"/>

#### 3.2.1.1 Требования к удобству использования
1. Доступ к основным функциям приложения не более чем за одну операции;
2. Все функциональные элементы пользовательского интерфейса имеют названия и иконки, описывающие действие, которое произойдет при выборе элемента;
3. Обновление информации о курсах валют происходит при каждом новом запуске приложения.

<a name="external_interfaces"/>

### 3.2.2 Внешние интерфейсы
Окна приложения удобны для использования пользователями с плохим зрением:
  * размер шрифта не менее 14пт;
  * функциональные элементы контрастны фону окна.

<a name="restrictions"/>

### 3.2.3 Ограничения
1. Приложение реализовано на платформе Android с использованием языка Kotlin;
2. Минимальная версия Android 6.0
