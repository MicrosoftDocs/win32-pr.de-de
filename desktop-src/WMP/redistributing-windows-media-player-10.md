---
title: Neuverteilen von Windows Media Player 10
description: Neuverteilen von Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707908"
---
# <a name="redistributing-windows-media-player-10"></a>Neuverteilen von Windows Media Player 10

Sie können Windows Media Player 10 unter Windows XP mit dem folgenden Setup Programm installieren.

-   MP10Setup.exe

Hier ist ein Beispiel für eine Befehlszeile für die Installation ohne Benutzeroberfläche und ohne Neustart oder Neustart Aufforderung.


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



In der folgenden Tabelle sind zusätzliche Parameter aufgeführt, die Sie mit dem Setup Programm von Windows Media Player 10 verwenden können.



| Parameter              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Verhindern der Bibliothek Migration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Erstellen Sie einen genetzten Systemwiederherstellungspunkt. Verwenden Sie diese Anwendung, wenn Ihre Anwendung einen Systemwiederherstellungspunkt erstellt, um den Windows Media Player Wiederherstellungspunkt innerhalb des Anwendungs Wiederherstellungs Punkts zu schachteln.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Hiermit wird die Erstellung eines System Wiederherstellungs Punkts nicht zugelassen. Mit diesem Flag wird die Erstellung eines System Wiederherstellungs Punkts deaktiviert. In den meisten Fällen sollte dieses Flag nicht für die allgemeine Software Verteilung verwendet werden. Dies sollte nur verwendet werden, wenn Sie im Namen des Endbenutzers eine explizite Auswahl treffen können, ohne das Rollback der Windows Media Player-Dateien auf eine frühere Version des Players zu unterstützen. Dieses Flag sollte nur für die Unternehmens Bereitstellung oder die Installation des Originalgeräte Herstellers (OEM) verwendet werden. |
| /DefaultService        | Legen Sie den anfänglichen Online Store fest. Weitere Informationen finden Sie unter [Setup Command-Line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Neuverteilen von Windows Media Player-Software**](redistributing-windows-media-player-software.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 




