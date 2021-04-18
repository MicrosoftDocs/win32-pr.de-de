---
description: 'Das Beenden eines Prozesses hat die folgenden Ergebnisse: alle verbleibenden Threads im Prozess werden für die Beendigung markiert. Alle vom Prozess zugewiesenen Ressourcen werden freigegeben. Alle Kernel Objekte werden geschlossen. Der Prozess Code wird aus dem Arbeitsspeicher entfernt. Der Prozessexitcode wird festgelegt. Das Prozess Objekt wird signalisiert.'
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Beenden eines Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010f1d4332a575c8ee94cf1b0f196e00ba7fb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347582"
---
# <a name="terminating-a-process"></a>Beenden eines Prozesses

Das Beenden eines Prozesses hat die folgenden Ergebnisse:

-   Alle verbleibenden Threads im Prozess werden für die Beendigung gekennzeichnet.
-   Alle vom Prozess zugewiesenen Ressourcen werden freigegeben.
-   Alle Kernel Objekte werden geschlossen.
-   Der Prozess Code wird aus dem Arbeitsspeicher entfernt.
-   Der Prozessexitcode wird festgelegt.
-   Das Prozess Objekt wird signalisiert.

Während geöffnete Handles für Kernel Objekte automatisch geschlossen werden, wenn ein Prozess beendet wird, sind die Objekte selbst so lange vorhanden, bis alle geöffneten Handles geschlossen sind. Daher bleibt ein Objekt gültig, nachdem ein Prozess, von dem es verwendet wird, beendet wird, wenn ein anderer Prozess über ein geöffnetes Handle verfügt.

Die [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) -Funktion gibt den Beendigungs Status eines Prozesses zurück. Während der Ausführung eines Prozesses ist der Beendigungs Status immer noch \_ aktiv. Wenn ein Prozess beendet wird, ändert sich der Beendigungs Status von noch \_ aktiv in den Exitcode des Prozesses.

Wenn ein Prozess beendet wird, wird der Status des Prozess Objekts signalisiert und alle Threads freigegeben, die auf das Beenden des Prozesses gewartet haben. Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads](synchronizing-execution-of-multiple-threads.md).

Wenn das System einen Prozess beendet, werden keine untergeordneten Prozesse beendet, die vom Prozess erstellt wurden. Beim Beenden eines Prozesses werden keine Benachrichtigungen für die \_ CBT-Hook-Prozeduren von WH generiert

Verwenden Sie die Funktion [**setprocessshutdownparameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) , um bestimmte Aspekte der Prozess Beendigung beim Herunterfahren des Systems anzugeben, z. b. Wenn ein Prozess relativ zu den anderen Prozessen im System beendet werden soll.

## <a name="how-processes-are-terminated"></a>Beenden von Prozessen

Ein Prozess wird ausgeführt, bis eines der folgenden Ereignisse eintritt:

-   Jeder Thread des Prozesses Ruft die [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion auf. Beachten Sie, dass bei einer Implementierung der C-Lauf Zeit Bibliothek (CRT) **ExitProcess** aufgerufen wird, wenn der primäre Thread des Prozesses zurückgibt.
-   Der letzte Thread des Prozesses wird beendet.
-   Jeder Thread ruft die Funktion [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) mit einem Handle für den Prozess auf.
-   Für Konsolen Prozesse ruft der [standardkonsolen-Steuerelement Handler](/windows/console/console-control-handlers) [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) auf, wenn die Konsole das Signal STRG + C oder STRG + UNTBR empfängt.
-   Der Benutzer fährt das System herunter oder meldet sich ab.

Beenden Sie keinen Prozess, es sei denn, seine Threads befinden sich in einem bekannten Zustand. Wenn ein Thread auf ein Kernel Objekt wartet, wird es erst beendet, wenn der Warte Vorgang abgeschlossen ist. Dies kann dazu führen, dass die Anwendung nicht mehr reagiert.

Der primäre Thread kann das Beenden anderer Threads vermeiden, indem er Sie an den [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) -Befehl weiterleitet, bevor der Prozess beendet wird (Weitere Informationen finden Sie unter [Beenden eines Threads](terminating-a-thread.md)). Der primäre Thread kann später weiterhin [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) aufzurufen, um sicherzustellen, dass alle Threads beendet werden.

Der [**Exitcode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) für einen Prozess ist entweder der Wert, der im ExitProcess-oder [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)-Befehl angegeben ist, oder der von der Main-oder [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion des Prozesses zurückgegebene Wert. Wenn ein Prozess aufgrund einer schwerwiegenden Ausnahme beendet wird, ist der Exitcode der Wert der Ausnahme, die die Beendigung verursacht hat. Außerdem wird dieser Wert als Exitcode für alle Threads verwendet, die ausgeführt wurden, als die Ausnahme aufgetreten ist.

Wenn ein Prozess von [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)beendet wird, ruft das System die Einstiegspunkt Funktion der einzelnen angefügten dll mit einem Wert auf, der angibt, dass der Prozess von der DLL getrennt wird. DLLs werden nicht benachrichtigt, wenn ein Prozess von [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet wird. Weitere Informationen zu DLLs finden Sie unter [Dynamic Link Libraries (Dynamic Link Libraries](../dlls/dynamic-link-libraries.md)).

Wenn ein Prozess von [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet wird, werden alle Threads des Prozesses sofort beendet, ohne dass zusätzlicher Code ausgeführt werden kann. Dies bedeutet, dass der Thread Code in Beendigungs handlerblöcken nicht ausführt. Außerdem werden keine angefügten DLLs benachrichtigt, wenn der Prozess getrennt wird. Wenn ein Prozess einen anderen Prozess beenden muss, bieten die folgenden Schritte eine bessere Lösung:

-   Lassen Sie beide Prozesse die [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufrufen, um eine private Nachricht zu erstellen.
-   Ein Prozess kann den anderen Prozess beenden, indem er eine private Nachricht mithilfe der [**broadcastsystemmessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) -Funktion wie folgt sendet:

    ``` syntax
     DWORD dwRecipients = BSM_APPLICATIONS;
        UINT uMessage = PM_MYMSG;
        WPARAM wParam = 0;
        LPARAM lParam = 0;

        BroadcastSystemMessage( 
            BSF_IGNORECURRENTTASK, // do not send message to this process
            &dwRecipients,         // broadcast only to applications
            uMessage,              // registered private message
            wParam,                // message-specific value
            lParam );              // message-specific value
    ```

-   Der Prozess, der die private Nachricht empfängt, ruft [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) auf, um die Ausführung zu beenden.

Die Ausführung der Funktionen " [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)", " [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)", " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)", " [**forateremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)" und " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " wird innerhalb eines Adressraums serialisiert. Es gelten folgende Einschränkungen:

-   Während der Prozessstart-und dll-Initialisierungs Routinen können neue Threads erstellt werden. Sie beginnen jedoch erst mit der Ausführung, wenn die Initialisierung der DLL für den Prozess abgeschlossen ist.
-   Nur ein Thread kann sich in einer DLL-Initialisierungs-oder-Trenn Routine befinden.
-   Die [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion wird erst zurückgegeben, wenn die dll-Initialisierungs-oder Trenn Routinen vorhanden sind.

 

 
