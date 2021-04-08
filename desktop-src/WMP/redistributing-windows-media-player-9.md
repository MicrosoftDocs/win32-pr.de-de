---
title: Neuverteilen der Windows Media Player 9-Serie
description: Neuverteilen der Windows Media Player 9-Serie
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037505"
---
# <a name="redistributing-windows-media-player-9-series"></a>Neuverteilen der Windows Media Player 9-Serie

Sie können Windows Media Player 9-Serie unter Windows XP installieren, indem Sie eines der folgenden Setup Programme verwenden.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe ist eine übergeordnete Gruppe des MPSetupXP.exe Setup Programms. Sie enthält Dateien, die von Betriebssystemen benötigt werden, die vor Windows XP veröffentlicht wurden. MPSetup.exe ist bei der Installation unter Windows XP funktionell äquivalent zu MPSetupXP.exe, aber die Dateigröße des Setup Programms ist größer, da Sie nicht für die Installation unter Windows XP-Betriebssystemen optimiert wurde.

 

Sie können Windows Media Player 9-Serie unter Windows 98 Second Edition, Windows Millennium Edition oder Windows 2000 mit dem folgenden Setup Programm installieren.

-   MPSetup.exe

Hier ist ein Beispiel für eine Befehlszeile für die Installation ohne Benutzeroberfläche und ohne Neustart oder Neustart Aufforderung.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> Der Parameter/P: \# e gibt an, dass das Windows Media Player-Installationspaket während der Einrichtung von Windows Media Player zwischengespeichert werden soll. Dieser Befehl wird verwendet, um zukünftige Upgrades des Betriebssystems zu verarbeiten. Dieser Befehl sollte nur von IT-Administratoren des Unternehmens ausgelassen werden. Der einzige Fall, in dem/P: \# e nicht in der Befehlszeile enthalten sein sollte, ist, wenn Sie das Zielsystem besitzen und wissen, dass das Zielsystem nie auf ein späteres Betriebssystem aktualisiert wird. Wenn Sie z. b. Windows Media Player 9-Serie unter Windows 2000 installieren, und der Computer kann an einem Tag ein Upgrade auf Windows XP durchführen, müssen Sie/P: \# e in der Befehlszeile verwenden. Andernfalls werden die Windows-Media Player Dateien nach der Installation von Windows XP mit den Dateien für Windows Media Player für Windows XP überschrieben.

 

In der folgenden Tabelle sind zusätzliche Parameter aufgeführt, die Sie mit dem Setup Programm der Windows Media Player 9-Serie verwenden können.



| Parameter              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Verhindern der Bibliothek Migration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Erstellen Sie einen genetzten Systemwiederherstellungspunkt. Verwenden Sie diese Anwendung, wenn Ihre Anwendung einen Systemwiederherstellungspunkt erstellt, um den Windows Media Player Wiederherstellungspunkt innerhalb des Anwendungs Wiederherstellungs Punkts zu schachteln.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Hiermit wird die Erstellung eines System Wiederherstellungs Punkts nicht zugelassen. Mit diesem Flag wird die Erstellung eines System Wiederherstellungs Punkts deaktiviert. In den meisten Fällen sollte dieses Flag nicht für die allgemeine Software Verteilung verwendet werden. Dies sollte nur verwendet werden, wenn Sie im Namen des Endbenutzers eine explizite Auswahl treffen können, ohne das Rollback der Windows Media Player-Dateien auf eine frühere Version des Players zu unterstützen. Dieses Flag sollte nur für die Unternehmens Bereitstellung oder die Installation des Originalgeräte Herstellers (OEM) verwendet werden. |



 

## <a name="notes"></a>Notizen

-   Bei den Befehlszeilen Parametern wird die Groß-/Kleinschreibung beachtet.
-   Wenn Sie die Aufforderung zum erneuten Starten unterdrücken, müssen Sie den Registrierungsschlüssel installresult überprüfen und die Neustart Benachrichtigung in der aufrufenden Setup Anwendung behandeln.
-   Mit der Windows Media Player 9-Serie wird auch die Windows Media-Laufzeitumgebung installiert, sodass es nicht erforderlich ist, das Windows Media Player Verteilungs Paket und das Windows Media-Lauf Zeit Verteilungs Paket in dasselbe Software Weitergabepaket einzubeziehen. Wenn Sie MPSetup.exe oder MPSetupXP.exe in die Installation einschließen, müssen Sie daher nicht WMFdist.exe einschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Neuverteilen von Windows Media Player-Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




