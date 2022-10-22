# FullStack-Lab1
#W Git Bash:  
#ssh-keygen -t rsa -b 4096 -C "Email przypisany do konta" <- Generowanie klucza RSA, ponieważ Ed25519 nie współpracował z dockerem na moim komputerze  
eval "$(ssh-agent -s)"   <- Sprawdzanie czy agent ssh działa  
ssh-add ~/.ssh/id_rsa   <-Dodawanie ssh do ssh agent  
Następnie dodałem ssh do konta.  
  
  
W VS Code:  
Uzywałem pliku DockerfileSSH  
docker build --ssh default="scieżka do klucza ssh" -f DockerfileSSH -t lab2.v1 . <-Komenda do zbudowania Obrazu lab2.v1  
