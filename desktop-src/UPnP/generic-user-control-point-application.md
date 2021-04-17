---
title: Generische Benutzer Steuerungspunkt-Anwendung
description: Mit der generischen benutzersteuerungs Punkt-Anwendung (UCP) können Sie Geräte ermitteln, diese ermittelten Geräte steuern und die zugehörigen Informationen über eine grafische Benutzeroberfläche anzeigen.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566997"
---
# <a name="generic-user-control-point-application"></a>Generische Benutzer Steuerungspunkt-Anwendung

Mit der generischen benutzersteuerungs Punkt-Anwendung (UCP) können Sie Geräte ermitteln, diese ermittelten Geräte steuern und die zugehörigen Informationen über eine grafische Benutzeroberfläche anzeigen.

**So starten Sie die generische UCP-Anwendung**

1.  Erstellen und konfigurieren Sie die Beispiele \\ netds \\ UPnP \\ genericucp \\ cpp \\devtype.txt Datei (oder die \\devtype.txt Datei VisualBasic \\ ) mit Geräteinformationen. Mit dieser Datei können Sie den generischen UCP für die Suchvorgänge "Suchen nach Typ" und "Async Find" konfigurieren. Jede Zeile der Datei muss einen Gerätetyp und die zugehörige Beschreibung enthalten. Beispiel:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Dieses Beispiel gilt für ein fiktives Media Player-Gerät. Das "Media Player" am Ende der zweiten Zeile ist nicht Teil des Gerätetyps, sondern dient zu Informationszwecken in der generischen UCP-Anwendung. Das gleiche gilt für "alle Stamm Geräte" in der ersten Zeile.

    Fügen Sie eine Zeile hinzu, die den jeweiligen Gerätetyp und die Beschreibung für jedes Gerät enthält.

2.  Erstellen und konfigurieren Sie die Beispiele \\ netds \\ UPnP \\ genericucp \\ cpp \\udn.txt Datei (oder die \\udn.txt Datei VisualBasic \\ ) mit udn-Informationen für Ihre Geräte. Mit dieser Datei können Sie den generischen UCP für die Suche nach udn suchen konfigurieren. Jede Zeile verwendet die folgende Form:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Fügen Sie eine Zeile hinzu, die ihren spezifischen udn für jedes Gerät enthält.

3.  Führen Sie GenericUCP.exe aus. Das Fenster **generisches UCP** wird angezeigt.

    ![Generisches UCP-Fenster](images/generic-ucp.png)

> [!Note]  
> Die **Ansichts Darstellung** und der **Ansichts Dienst DESC.** -Funktionalität ist nicht im C++-Beispielcode implementiert.

 

 

 




