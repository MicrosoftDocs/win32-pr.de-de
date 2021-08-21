---
description: In diesem Thema wird erläutert, wie Sie Shell- und Namespaceerweiterungs-DLLs debuggen.
title: Debuggen mit der Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 276023e5628ab7390398fd7bd367be32e45c13825fcf96625104be1ded8735de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032828"
---
# <a name="debugging-with-the-shell"></a>Debuggen mit der Shell

In diesem Thema wird erläutert, wie Sie Shell- und Namespaceerweiterungs-DLLs debuggen.

-   [Ausführen der Shell unter einem Debugger](#running-the-shell-under-a-debugger)
-   [Ausführen und Testen von Shellerweiterungen](#running-and-testing-shell-extensions)
-   [Entladen der DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Ausführen der Shell unter einem Debugger

Zum Debuggen der Erweiterung müssen Sie die Shell über den Debugger ausführen. Führen Sie die folgenden Schritte aus:

1.  Laden Sie das Projekt der Erweiterung in den Debugger, führen Sie es jedoch nicht aus.
2.  Fahren Sie die Shell herunter.

    -   Für Windows Vista und höher:
        1.  Zeigen Sie das **Menü Start** an.
        2.  Drücken Sie STRG+UMSCHALT, und klicken Sie mit  der rechten Maustaste auf den Hintergrund der rechten Hälfte des Startmenüs.
        3.  Wählen Sie im daraufhin angezeigten Menü **Exit Explorer (Explorer beenden)** aus.
    -   Für Windows XP:
        1.  Wählen Sie im **Menü Start** die Option **Herunterfahren** aus.
        2.  Drücken Sie STRG+ALT+UMSCHALT, und klicken Sie im Dialogfeld **Herunterfahren Windows** auf **Nein.**

    Die Shell ist jetzt heruntergefahren, aber alle anderen Anwendungen werden weiterhin ausgeführt, einschließlich des Debuggers.

3.  Legen Sie den Debugger so fest, dass die Erweiterungs-DLL mit Explorer.exe aus dem **verzeichnis Windows** ausgeführt wird.
4.  Führen Sie das Projekt über den Debugger aus. Die Shell wird wie gewohnt gestartet, aber der Debugger wird an den Shellprozess angefügt.

## <a name="running-and-testing-shell-extensions"></a>Ausführen und Testen von Shellerweiterungen

Sie können Ihre Erweiterungen in einem separaten Windows Explorer-Prozess ausführen und testen, um das Beenden und Neustarten des Desktops und der Taskleiste zu vermeiden. Der Desktop und die Taskleiste können weiterhin verwendet werden, während Sie die Erweiterungen ausführen und testen.

Um dieses Feature zu aktivieren, fügen Sie der Registrierung den folgenden REG \_ DWORD-Eintrag hinzu.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Damit dieser Eintrag wirksam wird, müssen Sie sich abmelden und erneut anmelden. Diese Einstellung bewirkt, dass die Desktop- und Taskleistenfenster in einem Explorer.exe Prozess erstellt werden und alle anderen Explorer- und Ordnerfenster in einem anderen Explorer.exe Prozess geöffnet werden.

Diese Einstellung vereinfacht nicht nur das Ausführen und Testen Ihrer Erweiterungen, sondern macht auch den Desktop stabiler, da er sich auf Shell-Erweiterungen bezieht. Viele erweiterungen dieser Art (z.B. Kontextmenüerweiterungen) werden in den Nichtdesktop-Explorer.exe Prozess geladen. Wenn dieser Prozess beendet wird, sind der Desktop und die Taskleiste nicht betroffen, und im nächsten Explorer- oder Ordnerfenster wird der beendete Prozess neu erstellt.

## <a name="unloading-the-dll"></a>Entladen der DLL

Die Shell entlädt automatisch alle DLL-Dateien, wenn die Nutzungsanzahl 0 beträgt, aber erst, nachdem die DLL für einen bestimmten Zeitraum nicht verwendet wurde. Dieser inaktive Zeitraum kann manchmal unzumutbar lang sein, insbesondere wenn eine Shellerweiterungs-DLL gedebuggt wird. Sie können den inaktiven Zeitraum verkürzen, indem Sie der Registrierung die folgenden Informationen hinzufügen.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



