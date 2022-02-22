# prework

Para generar una clave SSH y agregarla a Github

1.Creamos una llave SSH

    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
  
2.Copiamos la llave publica

    cat .ssh/id_rsa.pub
  
3.La pegamos en nuestra cuenta de GitHub

4.Configuramos Linux con la llave

    $ eval `ssh-agent -s`
    # Agent PID #### 
    $ ssh-add /home/user/.ssh/id_ed_25519
    
5.Creamos un repositorio vacio en GitHub

6.Lo probamos crando un README.md y subiendolo (uar la opción SSH)

    git config --global user.name YourUserName
    mkdir project-folder
    cd project-folder
    git init
    echo "# Hello World" > README.md
    git add README.md
    git commit -m "Frosty Labs Demonstration" 
    git remote add origin git@github.com:YourUserName/project-folder.git
    git push -u origin master
