
1. https://stackoverflow.com/questions/3127388/including-bash-autocompletion-with-setuptools
   ![alt text](https://github.com/AndrewNikoala/clibash/blob/main/Pasted%20image%2020240720212834.png?raw=true)   
2. https://stackoverflow.com/questions/15440115/how-would-i-run-a-script-file-as-part-of-the-python-setup-py-install 
   ![alt text](https://github.com/AndrewNikoala/clibash/blob/main/Pasted%20image%2020240720213121.png?raw=true)
3. Библиотека для генерации bash_complete файлов из питона. Удобно, если не хочешь страдать на bash
   https://github.com/joaquincasares/python-bashcomplete/blob/master/README.md
4. setup.py умеет собирать питоновский пакет, который не нужно будет запускать через python myscript.py
   https://stackoverflow.com/questions/56534678/how-to-create-a-cli-in-python-that-can-be-installed-with-pip
   ![alt text](https://github.com/AndrewNikoala/clibash/blob/main/Pasted%20image%2020240720215811.png?raw=true)
   

Варианты решения:
1. Написать скрипт дополнения через bash и положить в /etc/bash_completion.d/ (п.1 выше)
2. Написать скрипт дополнения через библиотеку python-bashcomplete и исполнить в конце setup.py (п.2, п.3 выше)

Дополнительно:
1. Динамическое дополнение делается, если вызвать скрипт из bash_completion
   ![alt text](https://github.com/AndrewNikoala/clibash/blob/main/Pasted%20image%2020240720213617.png?raw=true)
   Такой подход может, например: вернуть значения из конфига или вызвать скрипт деплоя и получить список стендов текущего пользователя
2. Поддержать конфиг для utms-deploy
   1. Хранить префикс
   2. Дефолтное количество дней
   3. Алиасы
