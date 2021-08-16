---
title: Anwendung für generische Benutzerkontrollpunkt
description: Mit der anwendung für den generischen Benutzersteuerungspunkt (UCP) können Sie Geräte entdecken, diese gefundenen Geräte steuern und die zugehörigen Ereignisinformationen mithilfe einer grafischen Benutzeroberfläche anzeigen.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0bbf454da2bf36becb3c8b0aff2babc87925df7ac658fc9dc7963ba9182fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655734"
---
# <a name="generic-user-control-point-application"></a>Anwendung für generische Benutzerkontrollpunkt

Mit der anwendung für den generischen Benutzersteuerungspunkt (UCP) können Sie Geräte entdecken, diese gefundenen Geräte steuern und die zugehörigen Ereignisinformationen mithilfe einer grafischen Benutzeroberfläche anzeigen.

**So starten Sie die generische UCP-Anwendung**

1.  Erstellen und konfigurieren Sie die Beispiele \\ netds upnp GenericUCP CPPdevtype.txt -Datei (oder die \\ \\ \\ \\ \\ VisualBasic \\devtype.txt-Datei) mit Geräteinformationen. Mit dieser Datei können Sie den generischen UCP für die Suchvorgänge "Nach Typ suchen" und "asynchrone Suche" konfigurieren. Jede Zeile der Datei muss einen Gerätetyp und die zugehörige Beschreibung enthalten. Beispiel:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Dieses Beispiel gilt für ein fiktives Medienplayergerät. Der "Media Player" am Ende der zweiten Zeile ist kein Teil des Gerätetyps, sondern dient zu Informationszwecken in der generischen UCP-Anwendung. Dasselbe gilt für "Alle Stammgeräte" in der ersten Zeile.

    Fügen Sie eine Zeile hinzu, die Ihren spezifischen Gerätetyp und die Beschreibung für jedes Gerät enthält.

2.  Erstellen und konfigurieren Sie die Beispiele \\ netds \\ upnp \\ GenericUCP \\ CPP \\udn.txt-Datei (oder die \\ VisualBasic \\udn.txt-Datei) mit UDN-Informationen für Ihre Geräte. Mit dieser Datei können Sie den generischen UCP für die Suche nach "Nach UDN suchen" konfigurieren. Jede Zeile verwendet das folgende Formular:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Fügen Sie eine Zeile hinzu, die Ihre spezifische UDN für jedes Gerät enthält.

3.  Führen Sie GenericUCP.exe. Das **Fenster Generischer UCP** wird angezeigt.

    ![Generisches Fenster "ucp"](images/generic-ucp.png)

> [!Note]  
> Der **Ansichtspräsentations-** **und Ansichtsdienst-Desc.** -Funktionalität ist im C++-Beispielcode nicht implementiert.

 

 

 




