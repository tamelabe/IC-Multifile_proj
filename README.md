# Multifile projects

В рамках данного проекта я ознакомился с медодами сборки многофайловых проектов.

## Quest 1. Modules.

Доработан модуль src/data_module таким образом, чтобы src/data_module/data_module_entry.c запускался и работал корректно. Переиспользованы имеющиеся файлы и функции, путем применения соответствующих директив препроцессора.

## Quest 2. Modules II.

Доработан модуль src/yet_another_decision_module таким образом, чтобы src/yet_another_decision_module/yet_another_decision_module_entry.c запускался и работал корректно. Переиспользованы имеющиеся файлы и функции, путем применения соответствующих директив препроцессора.

## Quest 3. Makefile.

Доработан модуль src/main_executable_module таким образом, чтобы src/main_executable_module/main_executable_module.c запускался и работал корректно. Разработан Makefile для сборки решения и помещен в директорию src/main_executable_module. В Makefile предусмотрены стандартные цели: clean, all, rebuild. Скомпилированный файл будет располагаться в папке build, в корне репозитория и иметь имя Quest_3. Сам результат компиляции не загружен в репозиторий.

## Quest 4. Static Lib.

В Makefile добавлена цель data_stat.a, собирающая модуль data_stat как статическую библиотеку data_stat.a. В Makefile добавлена цель build_with_static, собирающая main_executable_module с подключением модуля data_stat как статической библиотеки. Скомпилированный файл будет располагается в папке build, в корне репозитория и иметь имя Quest_5.

## Quest 5. Dynamic Lib.

В Makefile добавлена цель data_process.so, собирающая модуль data_process как динамическую библиотеку data_process.so. Также, в Makefile добавлена цель build_with_dynamic, собирающая main_executable_module с подключением модуля data_process как динамической библиотеки. Внесены необходимые изменения в код main_executable_module, конфигурировав использование динамической библиотеки с помощью макросов. Скомпилированный файл будет располагаться в папке build, в корне репозитория и иметь имя Quest_6.



