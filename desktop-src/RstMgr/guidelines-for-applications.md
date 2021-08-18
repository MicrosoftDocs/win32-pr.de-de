---
title: Richtlinien für Anwendungen
description: Anwendungen, die unter Windows Vista und Windows Server 2008 ausgeführt werden, sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Anwendungen herunterfahren und bei Bedarf neu starten kann, um Updates zu installieren.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9624f578a04267b94bde41bbdf8e3312e7b8ae0f4fb84280212ea51c2db7e2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010128"
---
# <a name="guidelines-for-applications"></a>Richtlinien für Anwendungen

Anwendungen, die unter Windows Vista und Windows Server 2008 ausgeführt werden, sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Anwendungen herunterfahren und bei Bedarf neu starten kann, um Updates zu installieren. Dienste können die Richtlinien verwenden, die unter [Richtlinien für Dienste beschrieben sind.](guidelines-for-services.md)

-   Der Neustart-Manager fragt GUI-Anwendungen zum Herunterfahren ab, indem er eine [**WM \_ QUERYENDSESSION-Benachrichtigung**](/windows/desktop/Shutdown/wm-queryendsession) sendet, bei der der *Parameter lParam* auf **ENDSESSION \_ CLOSEAPP** (0x1) festgelegt ist. Anwendungen sollten nicht heruntergefahren werden, wenn sie eine **WM \_ QUERYENDSESSION-Meldung** erhalten, da eine andere Anwendung möglicherweise nicht heruntergefahren werden kann. GUI-Anwendungen sollten auf die **WM \_ QUERYENDSESSION-Meldung** lauschen und den Wert **TRUE** zurückgeben, wenn die Anwendung zum Herunterfahren und Neustarten vorbereitet ist. Wenn keine Anwendung den Wert **FALSE** zurückgibt, sendet der Neustart-Manager eine [**WM \_ ENDSESSION-Nachricht,**](/windows/desktop/Shutdown/wm-endsession) bei der der *lParam-Parameter* auf **ENDSESSION \_ CLOSEAPP** (0x1) und der *wparam-Parameter* auf TRUE festgelegt **ist.** Anwendungen sollten nur heruntergefahren werden, wenn sie die **WM \_ ENDSESSION-Nachricht** erhalten. Der Neustart-Manager sendet auch eine [**WM \_ CLOSE-Meldung**](../winmsg/wm-close.md) für GUI-Anwendungen, die beim Empfang von **WM \_ ENDSESSION nicht heruntergefahren werden.** Wenn eine GUI-Anwendung auf eine **WM \_ QUERYENDSESSION-Meldung** antwortet, indem sie den Wert **FALSE** zurücksendet, wird das Herunterfahren abgebrochen. Wenn das Herunterfahren jedoch erzwungen wird, wird die Anwendung unabhängig davon beendet.
-   Wenn eine GUI-Anwendung eine [**WM \_ ENDSESSION-Nachricht**](/windows/desktop/Shutdown/wm-endsession) empfängt, sollte die Anwendung sich darauf vorbereiten, innerhalb des angegebenen Timeoutzeitraums heruntergefahren zu werden. Anwendungen sollten mindestens durch Speichern von Benutzerdaten und Zustandsinformationen vorbereitet werden, die nach einem Neustart benötigt werden. Es wird empfohlen, dass Anwendungen die Benutzerdaten und den Zustand in regelmäßigen Abständen speichern.
-   Der Neustart-Manager sendet eine **\_ STRG-C-EREIGNISbenachrichtigung \_** an Konsolenanwendungen, die heruntergefahren und neu gestartet werden müssen. Wenn eine Konsolenanwendung eine **\_ STRG-C-EREIGNISbenachrichtigung \_** empfängt, sollte die Anwendung die erforderlichen Maßnahmen ergreifen, um das Herunterfahren innerhalb des angegebenen Timeoutzeitraums vorzubereiten. Konsolenanwendungen sollten mindestens eine [*HandlerRoutine-Funktion*](/windows/console/handlerroutine) definieren, um die **\_ STRG-C-EREIGNISbenachrichtigung \_** zu verarbeiten, und alle Benutzerdaten und Zustandsinformationen speichern, die nach einem Neustart benötigt werden. Es wird empfohlen, dass Anwendungen die Benutzerdaten und den Zustand in regelmäßigen Abständen speichern.
-   Wenn Anwendungen als Reaktion auf die Meldungen zum Herunterfahren nicht heruntergefahren werden, können Installationsprogramme die **RmForceShutdown-Option** der [**RmShutdown-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) verwenden, um das Herunterfahren der Anwendungen zu erzwingen. Wenn das Installationsprogramm ein erzwungenes Herunterfahren angibt, versucht der Neustart-Manager, die Anwendungen durch Senden der Meldungen zum Herunterfahren sauber herunterfahren, erzwingen sie jedoch, wenn dies fehlschlägt. GUI-Anwendungen und Konsolenanwendungen können zum Herunterfahren gezwungen werden, um die Installation eines kritischen Sicherheitsupdates zu ermöglichen. Da dies zu Datenverlusten führen kann, sollten Anwendungen die Meldungen zum Herunterfahren verarbeiten und bei Bedarf sauber herunterfahren.
-   Anwendungen sollten sich mithilfe der [**RegisterApplicationRestart-Funktion für einen Neustart**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) registrieren. Restart Manager kann nur Anwendungen neu starten, die für den Neustart registriert wurden. Dies ist die einzige Möglichkeit, mit der der Neustart-Manager den Befehlszeilenbefehl bestimmen kann, der beim Neustart der Anwendung verwendet werden soll. Wenn die Anwendung mit einem gespeicherten Zustand oder daten erneut geöffnet werden muss, müssen diese Informationen im Befehlszeilenbefehl enthalten sein, der für die Anwendung registriert ist.
    > [!Note]  
    > Wenn die neu gestartete Anwendung in dem Verzeichnis ausgeführt werden muss, in dem sie ausgeführt wurde, bevor sie heruntergefahren wird, muss die Anwendung die Verzeichnisinformationen speichern und dann nach dem Neustart in das Verzeichnis wechseln.

     

    > [!Note]  
    > Die [**RmRestart-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) startet keine Anwendungen neu, die nicht als der aktuell angemeldete Benutzer ausgeführt werden. Die **RmRestart-Funktion** startet beispielsweise keine Anwendungen  neu, die mit dem Befehl "Ausführen als" gestartet wurden und nicht als der aktuell angemeldete Benutzer ausgeführt werden. Diese Anwendungen müssen manuell neu gestartet werden.

     

-   Wenn restart Manager feststellt, dass ein Systemneustart erforderlich ist, um ein Update zu installieren, werden keine Anwendungen und Dienste heruntergefahren. Stattdessen wird dies dem Installationsprogramm überlässt, um zu entscheiden, wann ein Systemneustart geplant und das Update installiert werden soll. Installationsprogramme können die Unterbrechung für Benutzer reduzieren, die durch Updates verursacht werden, die einen Systemneustart erfordern, indem sie die [**ExitWindowsEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) mit dem **EWX \_ RESTARTAPPS-Flag** oder die [**InitiateShutdown-Funktion**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) mit dem **SHUTDOWN \_ RESTARTAPPS-Flag** verwenden. Durch die Verwendung dieser Flags wird sichergestellt, dass anwendungen, die für den Neustart registriert sind, nach einem Systemneustart neu gestartet werden, wodurch die Auswirkungen auf den Benutzer minimiert werden.

 

 