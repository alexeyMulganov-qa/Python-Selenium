# Python-Selenium
### пример автотеста на Python + Selenium

#### Виртуальное окружение
Cоздаётся командой:  
`python -m venv env` (в нек-рых случаях вместо `python` нужно использовать `python3`)  
Активация виртуального окружения:  
Windows: `.\env\Scripts\Activate.ps1`  
Mac и Linux: `source env/bin/activate`  
Деактивация окружения: `deactivate`  

#### Необходимые модули
```
pip install pytest
pip install selenium
pip install webdriver_manager
pip install allure-pytest
```

#### Запуск тестов
Из командной строки: `pytest test_product_view_sku`  
*либо*  
Через VS Code. Пример файла с настройками:  
```
{
    "python.testing.pytestArgs": [
        "tests",
        "--alluredir=my_allure_results"   # настройка для сохранения отчетов
    ],
    "python.testing.unittestEnabled": false,
    "python.testing.pytestEnabled": true
}
```

#### Отчёты в Allure
Ссылка для скачивания Allure на Windows: https://clck.ru/32YkLm  
Команда для Mac: `brew install allure`  
Команда для Linux (Debian):
```
sudo apt-add-repository ppa:qameta/allure
sudo apt-get update
sudo apt-get install allure
```

На Windows в каталоге **allure\bin** нужно запустить файл **allure.bat**  
На Linux/Mac выполнить файл рядом **./allure**  

Для хранения отчётов Allure нужно создать отдельную папку  
После проведения тестов сервер отчётов запускается командой:
```
cd <путь до папке allure\bin>
.\allure.bat
.\allure serve <путь до каталога с результатами>
```
