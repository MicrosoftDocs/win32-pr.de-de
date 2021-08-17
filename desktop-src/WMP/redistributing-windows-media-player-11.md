---
title: Redistributing Windows Media Player 11 (Neuverteilung Windows Media Player 11)
description: Redistributing Windows Media Player 11 (Neuverteilung Windows Media Player 11)
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec17042165ed891370d1543fad303150c4b21d1f1db7f9da38de9f75d02876a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746559"
---
# <a name="redistributing-windows-media-player-11"></a>Redistributing Windows Media Player 11 (Neuverteilung Windows Media Player 11)

Sie können Windows Media Player 11 auf Windows XP installieren, indem Sie eines der folgenden Setupprogramme verwenden, wobei *localeId* ein Gebietsschemabezeichner ist.

-   wmp11-windowsxp-x86-*localeId*.exe
-   wmp11-windowsxp-x64-*localeId*.exe

Hier ist ein Beispiel für eine Befehlszeile für die Installation ohne Benutzeroberfläche und ohne Neustart- oder Neustartaufforderung.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



Die folgende Tabelle zeigt zusätzliche Parameter, die Sie mit dem Setupprogramm Windows Media Player 11 verwenden können.



| Parameter              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Verhindern der Bibliotheksmigration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Erstellen Sie einen geschachtelten Systemwiederherstellungspunkt. Verwenden Sie dies, wenn Ihre Anwendung einen Systemwiederherstellungspunkt erstellt, um den Windows Media Player Wiederherstellungspunkt innerhalb des Anwendungswiederherstellungspunkts zu schachteln.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Das Erstellen eines Systemwiederherstellungspunkts ist nicht zu flüssigen. Dieses Flag deaktiviert die Erstellung eines Systemwiederherstellungspunkts. In den meisten Fällen sollte dieses Flag nicht für die allgemeine Softwareverteilung verwendet werden. Dies sollte nur verwendet werden, wenn Sie eine explizite Entscheidung im Namen des Endbenutzers treffen können, um das Rollback der Windows Media Player-Dateien auf eine frühere Version des Players nicht zu unterstützen. Dieses Flag sollte nur für die Unternehmensbereitstellung oder oem-Installation (Original Equipment Manufacturer) verwendet werden. |
| /DefaultService        | Legen Sie den anfänglichen Onlineshop fest. Weitere Informationen finden Sie unter [Einrichten von Befehlszeilenparametern für Onlineshops.](setup-command-line-parameters-for-online-stores.md)                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verteilen von Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




