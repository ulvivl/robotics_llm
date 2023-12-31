# robotics_llm

Данный репозиторий создан в рамках хакатона "Цифровой прорыв". 

## Поставленная задача:
Создать программный модуль для планирования поведения робота с использованием языковых моделей. 

## Описание файлов:
В данном репозитории содержатся файлы, необходимые для запуска предложенных решений. Перед запуском необходимо также будет скачать датасет.

## Процесс запуска:
### Первый метод
1. Скачать проект с репозитория на GitHub
      ```
      git clone https://github.com/ulvivl/robotics_llm.git
      ```
2. Скачать файлы из репозитория с моделью LLava
      ```
      git clone https://github.com/haotian-liu/LLaVA.git
      cd LLaVA
      ```
3. Установить необходимые для запуска библиотеки
      ```
      conda create -n llava python=3.10 -y
      conda activate llava
      pip install --upgrade pip  # enable PEP 660 support
      pip install -e .
      ```                   
4. Запустить ноутбука llava_pipeline.ipynb

### Второй метод
1. Выполнить шаги, необходимые для запуска Первого метода.
2. Запустить ячейки ноутбука zephyr_llava_dual_multithread_dataframe.ipynb
3. Результат выполнения будет в ячейке `parsed_cmd`

### Подходы
1. Использование модели Llava (llava_pipeline.ipynb)
2. Использование модели Llava совместно с моделью на базе мистраль (zephyr_llava_dual_multithread_dataframe.ipynb)
3. Попытка обучить модель на задачу VQA на обучающем датасете (fine-tune-BLIP.ipynb)
