---
description: Anwendungen, Prozesse und Windows können sich dazu entscheiden, sich selbst nicht für das Anheften an die Taskleiste oder für die Aufnahme in die Liste der am häufigsten verwendeten (MFU-) Startmenüs zu entscheiden.
title: Ausschließen von Elementen aus der Taskleiste anheften und zuletzt auftretenden Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979561"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Ausschließen von Elementen aus der Taskleiste anheften und zuletzt auftretenden Listen

Anwendungen, Prozesse und Windows können sich dazu entscheiden, sich selbst nicht für das Anheften an die Taskleiste oder für die Aufnahme in die Liste der am häufigsten verwendeten (MFU-) **Startmenüs** zu entscheiden.

## <a name="instructions"></a>Instructions


Es gibt drei Mechanismen, um den Ausschluss von Elementen aus dem anheften der Taskleiste und der aktuellen bzw. häufigen Listen zu erreichen:

-   Fügen Sie den NoStartPage-Eintrag zur Registrierung der Anwendung hinzu, wie im folgenden Beispiel gezeigt:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Die dem NoStartPage-Eintrag zugeordneten Daten werden ignoriert. Nur das vorhanden sein des Eintrags ist erforderlich. Daher ist der ideale Typ für NoStartPage " **reg \_ None**".

    Beachten Sie, dass jede Verwendung einer expliziten App-Benutzer Modell-ID (appusermodelid) den NoStartPage-Eintrag überschreibt. Wenn eine explizite appusermodelid auf eine Verknüpfung, einen Prozess oder ein Fenster angewendet wird, wird Sie gepinckbar und ist für die MFU-Liste des **Start** Menüs geeignet.

-   Legen Sie die [System. appusermodel. preventpinning](../properties/props-system-appusermodel-preventpinning.md) -Eigenschaft unter Windows und Verknüpfungen fest. Diese Eigenschaft muss für ein Fenster festgelegt werden, bevor die [pkey- \_ appusermodel- \_ ID](../properties/props-system-appusermodel-id.md) -Eigenschaft festgelegt wird.
-   Fügen Sie eine explizite appusermodelid als Wert unter dem folgenden Registrierungs Unterschlüssel hinzu, wie im folgenden Beispiel gezeigt:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Jeder Eintrag ist ein **reg- \_ null** -Wert mit dem Namen der appusermodelid. Alle in dieser Liste gefundenen appusermodelid-Werte können nicht in die MFU-Liste des **Start** Menüs eingefügt werden.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass bestimmte ausführbare Dateien und Verknüpfungen, die bestimmte Zeichen folgen in ihren Namen enthalten, automatisch vom anhechern und einschließen in die MFU-Liste ausgeschlossen werden.

> [!Note]  
> Dieser automatische Ausschluss kann überschrieben werden, indem eine explizite appusermodelid angewendet wird.

 

Wenn eine der folgenden Zeichen folgen, unabhängig von der Groß-/Kleinschreibung, im Verknüpfungs Namen enthalten ist, kann das Programm nicht festgelegt werden und wird nicht in der am häufigsten verwendeten Liste angezeigt (gilt nicht für Windows 10):

-   Dokumentation
-   Hilfe
-   Installieren
-   Weitere Informationen
-   Lesezugriff
-   Zuerst lesen
-   Infodatei
-   Remove (Entfernen)
-   Einrichten
-   Support
-   Neuerungen

Die folgende Liste der Programme ist nicht pinckbar und wird aus der Liste der am häufigsten verwendeten Programme ausgeschlossen:

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Die vorangehenden Listen werden in den folgenden Registrierungs Werten gespeichert.

> [!Note]  
> Diese Listen sollten nicht von Anwendungen geändert werden. Verwenden Sie eine der Methoden der Ausschlussliste, die weiter oben in diesem Thema beschrieben wurden.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Die Taskleiste](taskbar.md)
</dt> <dt>

[Task leisten Erweiterungen](taskbar-extensions.md)
</dt> </dl>

 

 
