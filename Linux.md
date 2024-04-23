# Linux
```
Используя команду cat в терминале операционной системы Linux,
создать два файла Домашние животные (заполнив файл собаками, кошками, хомяками) и Вьючные животными заполнив файл Лошадьми, верблюдами и ослы), а затем объединить их. Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя (Друзья человека).
```

## Создаём файл с Домашними животными
```
db@karasev-linux:~$ cat > Pets << EOF > Dog > Cat > Hamsters > EOF
```

## Cоздаём файл с Вьючными животными
```
db@karasev-linux:~$ cat > Pack_animals << EOF > Horse > Camel > Donkey > EOF
```

## Перенаправляем из стандартного потока ввывода информация в файл
```
db@karasev-linux:~$ cat Pets Pack_animals > file_animals
file_animals
```
## вывод содержимого файла
```
db@karasev-linux:~$ cat file_animals

Dog
Cat
Hamsters
Horse
Camel
Donkey
```
## переименовываем файл

```
db@karasev-linux:~$ mv file_animals Human_Friends

```

# Создать директорию, переместить файл туда.
## создаём директорию
```
db@karasev-linux:~$ mkdir Human_Friends_dir
```
## перемещаем файл Human_Friends
```
db@karasev-linux:~$ mv Human_Friends Human_Friends_dir

db@karasev-linux:~/Human_Friends_dir$ tree

. └── Human_Friends

0 directories, 1 file
```

# Подключить дополнительный репозиторий MySQL. Установить любой пакет из этого репозитория.
```
загружаем репозиторий
db@karasev-linuxx:~$ wget https://dev.mysql.com/get/mysql-apt-config_0.8.12-1_all.deb

устанавливаем через утилиту apt
db@karasev-linux:~$ sudo apt install ./mysql-apt-config_0.8.12-1_all.deb –y

устанавливаем версию 5.7
sudo apt install -f mysql-client=5.7* mysql-community-server=5.7* mysql-server=5.7* sudo mysql_secure_installation
```
# Установить и удалить deb-пакет с помощью dpkg.
```
загрузка пакета deb
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

установка пакета
sudo dpkg -i --force-depends google-chrome-stable_current_amd64.deb

поиск пакета
sudo dpkg -S /usr/bin/google-chrome-stable

удаления пакета
sudo dpkg --purge google-chrome-stable
```
