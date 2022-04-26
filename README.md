# Removendo Samsung Bloatwares sem root
**Android Samsung Remove Bloatware (rootless)**

É possível remover aplicativos bloqueados (bloatwares) sem acesso root via adb (shell)

<br>
<br>

### Ferramenta para descobrir o id_package dos pacotes:
**App Inspector**

<br>

### Comando para remover um pacote:
```sh
pm uninstall -k --user 0 <id_package>
```

<br>

### Comando para reinstalar um pacote:
```sh
pm install-existing <id_package>
```

<br>
<br>

### Samsung Bloatwares:
**Facebook**<br>
`com.facebook.appmanager`<br>
`com.facebook.katana`<br>
`com.facebook.services`<br>
`com.facebook.system`<br>
**Galaxy Themes** <br> 
`com.samsung.android.themestore`<br>
**Google Duo**<br>
`com.google.android.apps.tachyon`<br>
**User Manual**<br>
`com.sec.android.usermanual`<br>
**Microsoft OneDrive**<br>
`com.microsoft.skydrive`<br>
**Netflix**<br>
`com.netflix.mediaclient`<br>
**Samsung AR Emoji Editor**<br>
`com.samsung.android.aremojieditor`<br>
**Samsung AR Emoji Stickers**<br>
`com.sec.android.mimage.avatarstickers`<br>
**Samsung AR Zone**<br>
`com.samsung.android.arzone`<br>
**Samsung Calculator**<br>
`com.sec.android.app.popupcalculator`<br>
**Samsung Calendar**<br>
`com.samsung.android.calendar`<br>
**Samsung Clock**<br>
`com.sec.android.app.clockpackage`<br>
**Samsung Contacts**<br>
`com.samsung.android.app.contacts`<br>
**Samsung DECO PIC**<br>
`com.samsung.android.livestickers`<br>
**Samsung Emoji AR**<br>
`com.samsung.android.aremoji`<br>
**Samsung Free**<br>
`com.samsung.android.app.spage`<br>
**Samsung Galaxy Store**<br>
`com.sec.android.app.samsungapps`<br>
**Samsung Gallery \***<br>
**OBS:** *O aplicativo de câmera da Samsung não consegue visualizar as fotos pois utiliza o Samsung Gallery*<br>
`com.sec.android.gallery3d `<br>
**Samsung Game Launcher**<br>
`com.samsung.android.game.gamehome`<br>
**Samsung Kids**<br>
`com.sec.android.app.kidshome`<br>
**Samsung Kids Installer**<br>
`com.samsung.android.kidsinstaller`<br>
**Samsung Messages**<br>
`com.samsung.android.messaging`<br>
**Samsung My Files**<br>
`com.sec.android.app.myfiles`<br>
**Samsung Phone**<br>
`com.samsung.android.dialer`<br>
**Samsung Smart Switch \***<br>
`com.sec.android.easyMover`<br>
`com.sec.android.easyMover.agent`<br>

<br>

**OBS:** Marquei com asterístico (*) os pacotes que são interessantes serem mantidos.

<br>
<br>

### Remoção dos pacotes em Lote
```sh
for pkg in { \
        com.facebook.appmanager, \
        com.facebook.katana, \
        com.facebook.services, \
        com.facebook.system, \
        com.samsung.android.themestore, \
        com.google.android.apps.tachyon, \
        com.sec.android.usermanual, \
        com.microsoft.skydrive, \
        com.netflix.mediaclient, \
        com.samsung.android.aremojieditor, \
        com.sec.android.mimage.avatarstickers, \
        com.samsung.android.arzone, \
        com.sec.android.app.popupcalculator, \
        com.samsung.android.calendar, \
        com.sec.android.app.clockpackage, \
        com.samsung.android.app.contacts, \
        com.samsung.android.livestickers, \
        com.samsung.android.aremoji, \
        com.samsung.android.app.spage, \
        com.sec.android.app.samsungapps, \
        com.samsung.android.game.gamehome, \
        com.sec.android.app.kidshome, \
        com.samsung.android.kidsinstaller, \
        com.samsung.android.messaging, \
        com.sec.android.app.myfiles, \
        com.samsung.android.dialer \
    }; \
    
    do pm uninstall -k --user 0 $pkg ; \

done
```