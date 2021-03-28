---
description: In diesem Thema wird das Debuggen von Shell-und Namespace Erweiterungs-DLLs erläutert.
title: Debuggen mit der Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525379"
---
# <a name="debugging-with-the-shell"></a>Debuggen mit der Shell

In diesem Thema wird das Debuggen von Shell-und Namespace Erweiterungs-DLLs erläutert.

-   [Ausführen der Shell unter einem Debugger](#running-the-shell-under-a-debugger)
-   [Ausführen und Testen von Shellerweiterungen](#running-and-testing-shell-extensions)
-   [Entladen der dll](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Ausführen der Shell unter einem Debugger

Zum Debuggen der Erweiterung müssen Sie die Shell über den Debugger ausführen. Folgen Sie diesen Schritten:

1.  Laden Sie das Projekt der Erweiterung in den Debugger, führen Sie es jedoch nicht aus.
2.  Beenden Sie die Shell.

    -   Für Windows Vista und höher:
        1.  Zeigen Sie das **Startmenü** an.
        2.  Drücken Sie STRG + UMSCHALT und klicken Sie mit der rechten Maustaste auf den Hintergrund der rechten Hälfte des **Startmenü** .
        3.  Wählen Sie im angezeigten Menü die Option **Exit Explorer** aus.
    -   Für Windows XP:
        1.  Wählen Sie im Menü **Start** die Option **herunter** fahren aus.
        2.  Drücken Sie Strg + Alt + Umschalttaste, und klicken Sie im Dialogfeld **Windows herunter** fahren auf **Nein** .

    Die Shell ist nun heruntergefahren, aber alle anderen Anwendungen werden weiterhin ausgeführt, einschließlich des Debuggers.

3.  Legen Sie den Debugger so fest, dass die Erweiterungs-DLL mit Explorer.exe aus dem **Windows** -Verzeichnis ausgeführt wird.
4.  Führen Sie das Projekt aus dem Debugger aus. Die Shell wird wie üblich gestartet, aber der Debugger wird an den Shellprozess angefügt.

## <a name="running-and-testing-shell-extensions"></a>Ausführen und Testen von Shellerweiterungen

Sie können Ihre Erweiterungen in einem separaten Windows Explorer-Prozess ausführen und testen, um das Beenden und Neustarten des Desktops und der Taskleiste zu vermeiden. Der Desktop und die Taskleiste können weiterhin verwendet werden, während Sie die Erweiterungen ausführen und testen.

Fügen Sie der Registrierung den folgenden reg DWORD-Eintrag hinzu, um dieses Feature zu aktivieren \_ .

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Damit dieser Eintrag wirksam wird, müssen Sie sich ab-und wieder anmelden. Diese Einstellung bewirkt, dass die Fenster Desktop und Taskleiste in einem Explorer.exe Prozess erstellt werden und alle anderen Explorer-und Ordner Fenster in einem anderen Explorer.exe Prozess geöffnet werden.

Mit dieser Einstellung können Sie nicht nur die Ausführung und das Testen der Erweiterungen vereinfachen, sondern auch den Desktop stabiler machen, da er sich auf Shellerweiterungen bezieht. Viele solche Erweiterungen (z. b. Kontextmenü Erweiterungen) werden in den nicht-Desktop Explorer.exe Prozess geladen. Wenn dieser Prozess beendet wird, sind der Desktop und die Taskleiste nicht betroffen, und im nächsten Explorer oder Ordner Fenster wird der beendete Prozess neu erstellt.

## <a name="unloading-the-dll"></a>Entladen der dll

Die Shell entlädt automatisch jede DLL, wenn Ihre Verwendungs Anzahl 0 (null) ist, aber erst, nachdem die DLL für einen bestimmten Zeitraum verwendet wurde. Dieser inaktive Zeitraum ist ggf. nicht akzeptabel, insbesondere dann, wenn eine Shellerweiterungs-dll gedeppt wird. Sie können den inaktiven Zeitraum verkürzen, indem Sie der Registrierung die folgenden Informationen hinzufügen.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



