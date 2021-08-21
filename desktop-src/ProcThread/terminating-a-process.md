---
description: 'Das Beenden eines Prozesses hat die folgenden Ergebnisse: Alle verbleibenden Threads im Prozess werden zum Beenden markiert. Alle vom Prozess zugeordneten Ressourcen werden frei. Alle Kernelobjekte werden geschlossen. Der Prozesscode wird aus dem Arbeitsspeicher entfernt. Der Prozessendcode ist festgelegt. Das Prozessobjekt wird signalisiert.'
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Beenden eines Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d1a97b2b7342b67eaab72cae244b188df4cfeafbf2875d3bd62136ab6139748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081300"
---
# <a name="terminating-a-process"></a>Beenden eines Prozesses

Das Beenden eines Prozesses hat die folgenden Ergebnisse:

-   Alle verbleibenden Threads im Prozess werden zur Beendigung markiert.
-   Alle vom Prozess zugeordneten Ressourcen werden frei.
-   Alle Kernelobjekte werden geschlossen.
-   Der Prozesscode wird aus dem Arbeitsspeicher entfernt.
-   Der Prozessendcode ist festgelegt.
-   Das Prozessobjekt wird signalisiert.

Während geöffnete Handles für Kernelobjekte automatisch geschlossen werden, wenn ein Prozess beendet wird, sind die Objekte selbst vorhanden, bis alle geöffneten Handles für sie geschlossen sind. Daher bleibt ein Objekt gültig, nachdem ein Prozess, der es verwendet, beendet wird, wenn ein anderer Prozess über ein offenes Handle verfügt.

Die [**GetExitCodeProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) gibt den Beendigungsstatus eines Prozesses zurück. Während ein Prozess ausgeführt wird, ist sein Beendigungsstatus STILL \_ ACTIVE. Wenn ein Prozess beendet wird, ändert sich sein Beendigungsstatus von STILL \_ ACTIVE in den Exitcode des Prozesses.

Wenn ein Prozess beendet wird, wird der Zustand des Prozessobjekts signalisiert und gibt alle Threads frei, die auf das Beenden des Prozesses gewartet haben. Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads.](synchronizing-execution-of-multiple-threads.md)

Wenn das System einen Prozess beendet, werden keine untergeordneten Prozesse beendet, die der Prozess erstellt hat. Durch das Beenden eines Prozesses werden keine Benachrichtigungen für \_ WH-CBT-Hookverfahren generiert.

Verwenden Sie [**die Funktion SetProcessShutdownParameters,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) um bestimmte Aspekte der Prozessbeendigung beim Herunterfahren des Systems anzugeben, z. B. wann ein Prozess relativ zu den anderen Prozessen im System beendet werden soll.

## <a name="how-processes-are-terminated"></a>Beenden von Prozessen

Ein Prozess wird ausgeführt, bis eines der folgenden Ereignisse eintritt:

-   Jeder Thread des Prozesses ruft die [**ExitProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) auf. Beachten Sie, dass einige Implementierungen der C-Laufzeitbibliothek (CRT) **ExitProcess** aufrufen, wenn der primäre Thread des Prozesses zurückgegeben wird.
-   Der letzte Thread des Prozesses wird beendet.
-   Jeder Thread ruft die [**TerminateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) mit einem Handle für den Prozess auf.
-   Bei Konsolenprozessen ruft der [Standardmäßige](/windows/console/console-control-handlers) Konsolensteuerungshandler [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) auf, wenn die Konsole ein STRG+C- oder STRG+BREAK-Signal empfängt.
-   Der Benutzer fährt das System herunter oder meldet sich ab.

Beenden Sie einen Prozess nur, wenn sich seine Threads in bekannten Zuzuständen befinden. Wenn ein Thread auf ein Kernelobjekt wartet, wird er erst beendet, wenn der Wartemodus abgeschlossen ist. Dies kann dazu führen, dass die Anwendung nicht mehr reagiert.

Der primäre Thread kann das Beenden anderer Threads vermeiden, indem er sie zum Aufrufen von [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) leitet, bevor der Prozess beendet wird (weitere Informationen finden Sie unter [Beenden eines Threads](terminating-a-thread.md)). Der primäre Thread kann auch danach [**ExitProcess aufrufen,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) um sicherzustellen, dass alle Threads beendet werden.

Der Exitcode für einen Prozess ist entweder der im Aufruf von [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) oder [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)angegebene Wert oder der Wert, der von der main- oder [**WinMain-Funktion**](/windows/win32/api/winbase/nf-winbase-winmain) des Prozesses zurückgegeben wird. Wenn ein Prozess aufgrund einer schwerwiegenden Ausnahme beendet wird, ist der Exitcode der Wert der Ausnahme, die die Beendigung verursacht hat. Darüber hinaus wird dieser Wert als Exitcode für alle Threads verwendet, die ausgeführt wurden, als die Ausnahme aufgetreten ist.

Wenn ein Prozess durch [**ExitProcess beendet**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)wird, ruft das System die Einstiegspunktfunktion jeder angefügten DLL mit einem Wert auf, der angibt, dass der Prozess von der DLL getrennt wird. DLLs werden nicht benachrichtigt, wenn ein Prozess durch [**TerminateProcess beendet wird.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) Weitere Informationen zu DLLs finden Sie unter [Dynamic Link Libraries](../dlls/dynamic-link-libraries.md).

Wenn ein Prozess durch [**TerminateProcess beendet**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)wird, werden alle Threads des Prozesses sofort beendet, ohne dass zusätzlichen Code ausgeführt werden kann. Dies bedeutet, dass der Thread keinen Code in Beendigungshandlerblöcken ausricht. Darüber hinaus werden keine angefügten DLLs benachrichtigt, dass der Prozess getrennt wird. Wenn ein Prozess einen anderen Prozess beenden muss, bieten die folgenden Schritte eine bessere Lösung:

-   Lassen Sie beide Prozesse die [**RegisterWindowMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) aufrufen, um eine private Nachricht zu erstellen.
-   Ein Prozess kann den anderen Prozess beenden, indem er eine private Nachricht wie folgt mithilfe der [**BroadcastSystemMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) sendet:

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

-   Der Prozess, der die private Nachricht empfängt, ruft [**ExitProcess auf,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) um die Ausführung zu beenden.

Die Ausführung der [**Funktionen ExitProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) [**ExitThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)und [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) wird in einem Adressraum serialisiert. Es gelten folgende Einschränkungen:

-   Während des Prozessstarts und der DLL-Initialisierungsroutinen können neue Threads erstellt werden, aber sie beginnen erst, wenn die DLL-Initialisierung für den Prozess abgeschlossen ist.
-   Es kann immer nur ein Thread gleichzeitig in einer DLL-Initialisierungs- oder -Trennungsroutine enthalten sein.
-   Die [**ExitProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) gibt erst dann zurück, wenn in ihren DLL-Initialisierungs- oder Trennungsroutinen keine Threads enthalten sind.

 

 
