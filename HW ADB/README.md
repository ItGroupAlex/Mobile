 ###  HW QA ADB

Сценарий напишите в .txt файл.
.txt сценарий и .log файл приложения todolist выгружайте на GitHub.
Ссылку на гитхаб присылайте в лс.

 1. Отобразить подключенный девайс в консоли.
- скачиваем ADB
- подключаемся к телефону кабелем или WiFi через AndroidStudio
- заходим через PowerShell из папки распакованного архива ADB

`.\adb devices`

 2. Вывести адрес приложения todolist в системе Android

- перетягиваем файл todolist.apk в окно PowerShell 

 3. Установить .apk файл приложения todolist на телефон с компьютера через  ADB

`.\adb install D:\QA\HW\Android_apk\TodoList.apk`

 4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.

[`.\adb shell screencap /sdcard/screencap.png | .\adb pull /sdcard/screencap.png`](https://github.com/ItGroupAlex/Mobile/blob/main/HW%20ADB/screencap.png "screencap.png")    

 5. Вывести в консоль логи приложения todolist

 6. Скопировать логи приложения todolist на компьютер.

[`.\adb logcat -d | findstr com.android.todolist > todolist.log`](https://github.com/ItGroupAlex/Mobile/blob/main/HW%20ADB/todolist_ADB.log "todolist_ADB.log")       

- но сбивается, поэтому лучше [через AndroidStudio](https://github.com/ItGroupAlex/Mobile/blob/main/HW%20ADB/todolist_AndroidStudio.log "todolist_AndroidStudio.log")    

 7. Удалить приложение todolist с телефона через ADB

`.\adb uninstall com.android.todolist`
