В текущий момент работает с ubuntu от 16.04 до 24.04+
1) Копируем репозиторий: git clone https://github.com/Dustlex/xray_ansible_0.1.git
2) Заходим в загруженную директорию: cd xray_ansible_0.1/
3) Устанавливаем pip командой: apt install python3-pip
4) Им в свою очередь ставим ансибл: pip install ansible
5) Затем подготавливаем сервер командой:
```
ansible-playbook -i host.yml all.yml -e "role=preconfig"
```
6) После чего запускаем установку xray-xtls-rprx-vision:
```
ansible-playbook -i host.yml all.yml -e "role=xray-xtls-real"
```
Выведенные в параграфе TASK [xray-xtls-real : Connection data for clients] данные, использовать для клиентов по типу Nekoray и т.д.
