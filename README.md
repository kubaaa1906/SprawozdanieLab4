# SprawozdanieLab4

1. Należy przejść w konsoli do poziomu folderu z plikiem Dockerfile i index.html.
2. Wpisać polecenie: docker build -f Dockerfile_sprawoz -t web100 .
3. Następnie należy uruchomić nasz build poleceniem: docker run -d -p 8080:8080 web100
4. Aby zmienić port z 80 na 8080:
     1. docker exec -it <id_kontenera> sh
     2. cd etc
     3. cd apache2
     4. nano ports.conf (trzeba zainstalować pakiet nano poleceniem: apt install nano)
     5. Zmienić na Listen 8080
     6. Teraz trzeba zrestartować Apache poleceniem: service apache2 restart
5. Uruchomić kontener poleceniem: docker start <id_kontenera>.

Serwer posiada 4 warstwy, można to sprawdzić poleceniem: docker image inspect web100 i poszukać w listingu pozycji Layers.
        
