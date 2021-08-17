---
description: Anwendungen, Prozesse und Fenster können sich dafür entscheiden, sich selbst für das Anheften an die Taskleiste oder die Aufnahme in die MFU-Liste (Most Frequently Used) von Startmenü nicht verfügbar zu machen.
title: Ausschließen von Elementen aus Taskleisten-Pinning und zuletzt verwendeten/häufigen Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3adb60353836e436f4327837c30448c7628a435048cc2a41b0464d56341f410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223564"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Ausschließen von Elementen aus Taskleisten-Pinning und zuletzt verwendeten/häufigen Listen

Anwendungen, Prozesse und Fenster können sich selbst für das Anheften an die  Taskleiste oder für die Aufnahme in die Liste Am häufigsten verwendet (Most frequently Used, MFU) des Startmenüs nicht verfügbar machen.

## <a name="instructions"></a>Anweisungen


Es gibt drei Mechanismen, um den Ausschluss von Elementen aus der Taskleisten-Pinning und den aktuellen/häufigen Listen zu erreichen:

-   Fügen Sie der Registrierung der Anwendung den Eintrag NoStartPage hinzu, wie im folgenden Beispiel gezeigt:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Die dem NoStartPage-Eintrag zugeordneten Daten werden ignoriert. Nur das Vorhandensein des Eintrags ist erforderlich. Daher ist der ideale Typ für NoStartPage **REG \_ NONE.**

    Beachten Sie, dass die Verwendung einer expliziten Anwendungsbenutzermodell-ID (AppUserModelID) den Eintrag NoStartPage überschreibt. Wenn eine explizite AppUserModelID auf eine Verknüpfung, einen Prozess oder ein Fenster angewendet wird, wird sie anheftbar und für die MFU-Liste **im Startmenü** geeignet.

-   Legen Sie [die System.AppUserModel.PreventPinning-Eigenschaft für](../properties/props-system-appusermodel-preventpinning.md) Fenster und Verknüpfungen fest. Diese Eigenschaft muss in einem Fenster festgelegt werden, bevor die [Eigenschaft PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) festgelegt wird.
-   Fügen Sie eine explizite AppUserModelID als Wert unter dem folgenden Registrierungsunterschlüssel hinzu, wie in diesem Beispiel gezeigt:

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

    Jeder Eintrag ist ein **REG \_ NULL-Wert** mit dem Namen der AppUserModelID. Jede AppUserModelID, die in dieser Liste enthalten ist, ist nicht anheftbar und kann nicht in die MFU-Liste des **Startmenüs** aufgenommen werden.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass bestimmte ausführbare Dateien sowie Verknüpfungen, die bestimmte Zeichenfolgen in ihren Namen enthalten, automatisch vom Anheften und Einschluss in die MFU-Liste ausgeschlossen werden.

> [!Note]  
> Dieser automatische Ausschluss kann durch Anwenden einer expliziten AppUserModelID überschrieben werden.

 

Wenn eine der folgenden Zeichenfolgen unabhängig von der Fall im Verknüpfungsnamen enthalten ist, ist das Programm nicht anheftbar und wird nicht in der Liste der am häufigsten verwendeten Zeichenfolgen angezeigt (gilt nicht für Windows 10):

-   Dokumentation
-   Hilfe
-   Installieren
-   Weitere Informationen
-   Read me (Lesen)
-   Zuerst lesen
-   Infodatei
-   Entfernen
-   Einrichten
-   Support
-   Neuerungen

Die folgende Liste der Programme ist nicht anheftbar und wird aus der Liste der am häufigsten verwendeten Programme ausgeschlossen:

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

Die obigen Listen werden in den folgenden Registrierungswerten gespeichert.

> [!Note]  
> Diese Listen sollten nicht von Anwendungen geändert werden. Verwenden Sie eine der oben in diesem Thema beschriebenen Ausschlusslistenmethoden für die gleiche Erfahrung.

 

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

[Taskleiste](taskbar.md)
</dt> <dt>

[Taskleistenerweiterungen](taskbar-extensions.md)
</dt> </dl>

 

 
