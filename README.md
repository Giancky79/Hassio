Per alcuni sensori esterni, andrà attivata una cartella ssh nel quale useremo le key generate per intercettare lo stato su proxmox ad esempio

#SSH

usando Home Assistant Supervised, attivando addon web&ssh, potrete interagire attraverso putty o terminale (macos e linux), nela caso di proxmox andrà bene anche terminal&ssh, ma farete tutto attraverso terminale della vm o collegandovi in ssh sulla vostra installazione di proxmox

Attivare web&ssh, configurazione base è sufficiente

*      mkdir ssh

creerà una cartella in /config, in caso di backup avrete tutto salvato

*      ssh-keygen -t ed25519 -C "your_email@example.com"

il percorso da salvare sarà

*      /config/ssh/id_rsa

una volta fatto, nel caso usiate proxmox

*      ssh-copy-id -i /config/ssh/id_rsa root@ip
 
nel caso invece volete collegarvi da putty o terminale, sarà

*      ssh hassio@ip-ha 

 hassio o utente messo nella configurazione di web&ssh
 password dovete decidere voi se averla, mettete per sicurezza maggiore
