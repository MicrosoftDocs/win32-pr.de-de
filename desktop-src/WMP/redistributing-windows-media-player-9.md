---
title: Redistributing Windows Media Player 9 Series
description: Redistributing Windows Media Player 9 Series
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418a780836c0a64a1b31b0d3c01a69841b695803f5db61b049915ec0d981f9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861680"
---
# <a name="redistributing-windows-media-player-9-series"></a>Redistributing Windows Media Player 9 Series

Sie können Windows Media Player 9-Serie auf Windows XP installieren, indem Sie eines der folgenden Setupprogramme verwenden.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe ist eine Obermenge des setup-Programms für MPSetupXP.exe. Sie enthält Dateien, die von Betriebssystemen benötigt werden, die vor Windows XP veröffentlicht wurden. MPSetup.exe entspricht funktional MPSetupXP.exe, wenn sie auf Windows XP ausgeführt wird, aber die Dateigröße des Setupprogramms ist größer, da sie nicht für die Installation auf Windows XP-Betriebssystemen optimiert wurde.

 

Sie können Windows Media Player 9-Serie mithilfe des folgenden Setupprogramms auf Windows 98 Second Edition, Windows Edition Oder Windows 2000 installieren.

-   MPSetup.exe

Hier ist ein Beispiel für eine Befehlszeile für die Installation ohne Benutzeroberfläche und ohne Neustart- oder Neustartaufforderung.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> Der Parameter /P: \# e gibt an, dass das Windows Media Player Installationspaket während Windows Media Player Setups zwischengespeichert werden soll. Dieser Befehl wird verwendet, um zukünftige Upgrades des Betriebssystems zu verarbeiten. Dieser Befehl sollte nur von IT-Unternehmensadministratoren ausgelassen werden. Der einzige Fall, in dem /P: \# e nicht in der Befehlszeile enthalten sein sollte, ist, wenn Sie das Zielsystem besitzen und wissen, dass das Zielsystem nie auf ein späteres Betriebssystem aktualisiert wird. Wenn Sie beispielsweise Windows Media Player 9-Serie auf Windows 2000 installieren und der Computer eines Tages auf Windows XP aktualisiert werden kann, müssen Sie /P: \# e in der Befehlszeile verwenden. Andernfalls werden die Windows Media Player Dateien nach der installation Windows XP mit den Dateien für Windows Media Player für Windows XP überschrieben.

 

Die folgende Tabelle zeigt zusätzliche Parameter, die Sie mit dem Setupprogramm der Windows Media Player 9-Serie verwenden können.



| Parameter              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Verhindern der Bibliotheksmigration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Erstellen Sie einen geschachtelten Systemwiederherstellungspunkt. Verwenden Sie dies, wenn Ihre Anwendung einen Systemwiederherstellungspunkt erstellt, um den Windows Media Player Wiederherstellungspunkt innerhalb des Wiederherstellungspunkts der Anwendung zu schachteln.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Das Erstellen eines Systemwiederherstellungspunkts ist nicht zu flüssigen. Dieses Flag deaktiviert die Erstellung eines Systemwiederherstellungspunkts. In den meisten Fällen sollte dieses Flag nicht für die allgemeine Softwareverteilung verwendet werden. Dies sollte nur verwendet werden, wenn Sie eine explizite Entscheidung im Namen des Endbenutzers treffen können, das Rollback der Windows Media Player-Dateien auf eine frühere Version des Players nicht zu unterstützen. Dieses Flag sollte nur für die Unternehmensbereitstellung oder oem-Installation (Original Equipment Manufacturer) verwendet werden. |



 

## <a name="notes"></a>Hinweise

-   Bei den Befehlszeilenparametern wird die Groß-/Kleinschreibung beachtet.
-   Wenn Sie die Neustartaufforderung unterdrücken, müssen Sie den Registrierungsschlüssel InstallResult überprüfen und die Neustartbenachrichtigung in der aufrufenden Setupanwendung behandeln.
-   Windows Media Player 9-Serie installiert auch die Windows Media Format Runtime, sodass das Windows Media Player Verteilungspaket und das Windows Media Format Runtime-Verteilungspaket nicht in dasselbe Softwareverteilungspaket eingeschlossen werden müssen. Wenn Sie daher MPSetup.exe oder MPSetupXP.exe in die Installation einschließen, müssen Sie WMFdist.exe nicht einschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verteilen von Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




