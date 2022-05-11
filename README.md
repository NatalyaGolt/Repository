# repository
### 1. На локальном репозитории сделать ветки для Postman, Jmeter, CheckLists, Bag_Reports, SQL, Charles, Mobile_testing
    git branch Postman && git branch Jmeter && git branch Checklists && git branch Bug_Reports && git branch SQL && git branch Charles && git branch Mobile_testing
### 2. Запушить все ветки на внешний репозиторий
    git push -u origin --all
### 4. В ветке Bag_Reports сделать текстовый документ со структурой баг репорта
- Перейти в ветку:

        git checkout Bug_Reports
- Создать файл:

        vim bug_reports.txt
- Перейти в режим редактирования:

        i
- Написать структуру баг-репорта:

        id:
        summary:
        environment:
        precondisions:
        steps:
        expected result:
        actual result:
        priority:
        severity:
        assign:
- Выйти из режима редактирования:

        esc
- Выйти из редактора текста:

        :wq
### 5. Запушить структуру багрепорта на внешний репозиторий

        git add bug_reports.txt && git commit -m "add bug_reports.txt on branch Bag_Reports" && git push -u origin Bag_Reports

### 6. Вмержить ветку Bag_Reports в Main
- Перейти в ветку, в которую будем мержиться (Main):
  
        git checkout main

- Слить ветки:


        git merge Bug_Reports

### 7. Запушить main на внешний репозиторий
        git push origin main
### 8. В ветке CheckLists набросать структуру чек листа
- Перейти в ветку:

        git checkout CheckLists
- Создать файл:

        vim checklists.txt
- Перейти в режим редактирования:

        i
- Написать структуру чек-листа:

        id:
        module:
        submodule:
        checking:
        status:

- Выйти из режима редактирования:

        esc
- Выйти из редактора текста:

        :wq
### 9. Запушить структуру чек-листа на внешний репозиторий
        git add checklists.txt && git commit -m "add checklists.txt on branch Checklists" && git push -u origin CheckLists
### 10. На внешнем репозитории сделать Pull Request ветки CheckLists в main
- Находясь на внешнем репозитории, открыть Pull Request:
<img src="https://s219vla.storage.yandex.net/rdisk/7b4e6c6a9d82c0872b7e6d063f26982d381ab93d3f24e3422c17a4dfbd5e6af6/627c4aed/n0TScqWseOyzBp-7ZA_dB0qbzaCGhz4C_Mc0rZ5xYxugW98bfXUZm5-YMfadcaeomvNfM9Vrfnk0B22OnQBs7g==?uid=40883143&filename=git%20compare%20and%20pull%20requests.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=40883143&fsize=16951&hid=bc72ca0dd627fe149492ff167df980ab&media_type=image&tknv=v2&etag=06330efd2af898573f44f4f51d4a111c&rtoken=tZ686ky98ZWR&force_default=yes&ycrid=na-03552780fb27661a646f82742f624e91-downloader22f&ts=5dec50e46d540&s=060563fdb28262c4c3b6048dc645f533b53e85541a98e5175edf63258dc7616a&pb=U2FsdGVkX1_zU3n_35mS4WGMc13tdOYjeZtnsMnh2Zuj2z0d_KAv4M4-nEKiLEjwCfG1JD42USHDKz-7R1QXsrPJ8B-RcfSiD5p6oJ8Wnuo" alt="git compare and pull request">

- Создать Pull Request:
  
     <img src="https://s205vla.storage.yandex.net/rdisk/84c3dca7e69a056628f04c2785c79fdd69359682cdd3e5e68be1e6f86470be4a/627c4b5d/n0TScqWseOyzBp-7ZA_dB72V5lw7Nh2rQ8TizlVVR_sYkFUJpIy7ev9FTVGFlTZnpKacxPhjSt_SxCFIzHZ4xA==?uid=40883143&filename=git%20create%20pullrequest.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=40883143&fsize=1707&hid=ffaa284b69b4203c00b9d392d535ede2&media_type=image&tknv=v2&etag=0c693fe536bc6c7a366c6de14ef60b31&rtoken=zQzO0PhW3Uy4&force_default=yes&ycrid=na-1c9e66f96f79cca89dba1af7d850eb69-downloader5e&ts=5dec514f3d140&s=e6cf1379ef2b23d8afb6424f2b200bf9baa2fa88e7bb7d6adf1fe1ec09a0aa37&pb=U2FsdGVkX1_Ze7z_AbySOZ5FTDxONPfGGLauh3FpTd_bKmVYjKD1EUaOV1C8Pc2HrSblvsCvn8-TkWoAhfTGLpsKh8zgCdeT1gRG21yNIUM" alt="git create pullrequest">

- Смержить Pull Request:

     <img src="https://s102vla.storage.yandex.net/rdisk/20af24e333f51f4eb643a47a25faef07c8185bcc4ee5865fcd276ff188ea8b37/627c4c57/n0TScqWseOyzBp-7ZA_dBzW_UmPiqdtf1xjmeZ1Z7XMXfNj0udmxPSUrcO3S_TV0JegTz-mX-_7q-pjpovfdAA==?uid=40883143&filename=git%20merge%20pull%20request.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=40883143&fsize=1698&hid=36ec4d6cd72efd44102581a4afc87183&media_type=image&tknv=v2&etag=73d5c2ec62007fb9b192fb34e75e8939&rtoken=88mQ4S8e5My2&force_default=yes&ycrid=na-edeaae2378e2969add3e5d6642d37a71-downloader6f&ts=5dec523da83c0&s=f5d4bf564801c1ce0f2990ac0c41223a2899929e9d37baee5a5de7f4eb483855&pb=U2FsdGVkX1_HFJfUOe8BbjTZLyuU9_lSe90yKnmEh_sb4Xn0bSf_KdsHCuxlmhOCbUsKvs47RfTiiY7bVuqt0mNQKlKhvdbbrNFviwoGBxI" alt="git merge pull request">

- Подтвердить слияние:

     <img src="https://s436vla.storage.yandex.net/rdisk/9750883125eb83f60cb0b55991b7386d0cfe212c450dc804a992b08af1b39677/627c4c9c/n0TScqWseOyzBp-7ZA_dB6hVt_BWf9CCoBRuxvDhpxFMzk7-MDZ61ZQI1nIF6EkMsF360enxLj245p0JIQRSFA==?uid=40883143&filename=git%20confirm%20merge.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=40883143&fsize=1392&hid=6b4d4bd0fd1d717479692527aef85e67&media_type=image&tknv=v2&etag=a736168309eb6754b2701896237cda5d&rtoken=72B10p5yj9BD&force_default=yes&ycrid=na-a65d8482b69d0520092ea3fd9c4de603-downloader6f&ts=5dec527f75f00&s=38fa949b20cc1d1ada99441b3551a00302b16991d3914cad3e21c0bb86f3096b&pb=U2FsdGVkX1_P1bHavYAOVZ55qhCiaoDJe7A4jjomXWH6VN7I_ZnflQH873qmhMdwEN0BldMxuSZ2hKE4rKVjkPh4NM0Yo2FJexGU9yhhlFw" alt="git confirm merge">

### 11. Синхронизировать Внешнюю и Локальную ветки Main
        git fetch && git pull
