---
description: In diesem Thema wird beschrieben, wie der Druckauftragsverarbeitungsthread gestartet und beendet wird.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Vorgehensweise: Starten und Beenden eines Druckthreads'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393f1f95efbb52c7cdd81316db000de22d45ca9e5dda0eadebb82ebaa3942350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686712"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a>Vorgehensweise: Starten und Beenden eines Druckthreads

In diesem Thema wird beschrieben, wie der Druckauftragsverarbeitungsthread gestartet und beendet wird.

## <a name="overview"></a>Übersicht

Um zu verhindern, dass Druckaktivitäten die Antwort auf die Benutzeroberfläche blockieren, erstellen Sie einen separaten Thread zum Verarbeiten des Druckauftrags. Der Thread, der beim Starten des Programms gestartet wird, ist der Thread, der die Fenstermeldungen verarbeitet, die sich aus der Benutzerinteraktion ergeben, und ist daher der UI-Thread. Das Programm muss diese Nachrichten ohne Verzögerung verarbeiten, damit die Benutzeroberfläche rechtzeitig auf die Maus- und Tastatureingabe des Benutzers reagiert. Damit das Programm schnell auf diese Nachrichten reagieren kann, ist die Verarbeitungsmenge, die während einer Nachricht ausgeführt werden kann, begrenzt. Wenn eine Benutzeranforderung eine umfangreiche Verarbeitung erfordert, muss diese Verarbeitung von einem anderen Thread ausgeführt werden, damit nachfolgende Benutzerinteraktionen vom Programm verarbeitet werden können.

Das Verarbeiten von Daten in einem separaten Thread erfordert, dass das Programm den Betrieb des Benutzeroberflächenthreads und des Verarbeitungsthreads koordiniert. Während der Verarbeitungsthread beispielsweise die Daten verarbeitet, darf der Hauptthread diese Daten nicht ändern. Eine Möglichkeit, dies zu verwalten, sind threadsichere Synchronisierungsobjekte wie Semaphore, Ereignisse und Mutexe.

Gleichzeitig muss eine Benutzerinteraktion verhindert werden, während der Verarbeitungsthread ausgeführt wird. Im Beispielprogramm werden die Anwendungsdaten geschützt, und die Benutzerinteraktion wird eingeschränkt, indem die Druckauftragsverarbeitung über das Modale Statusdialogfeld verwaltet wird. Ein modales Dialogfeld verhindert, dass der Benutzer mit dem Hauptfenster des Programms interagiert, wodurch verhindert wird, dass der Benutzer die Anwendungsprogrammdaten ändert, während die Daten gedruckt werden.

Die einzige Aktion, die der Benutzer ausführen kann, während ein Druckauftrag verarbeitet wird, besteht darin, den Druckauftrag abzubrechen. Diese Einschränkung wird dem Benutzer durch die Cursorform signalisiert. Wenn sich der Cursor über der Schaltfläche **Abbrechen** befindet, wird ein Pfeilcursor angezeigt, der angibt, dass der Benutzer auf diese Schaltfläche klicken kann. Wenn sich der Cursor über einem anderen Teil des Fensterbereichs des Programms befindet, wird ein Wartecursor angezeigt, der angibt, dass das Programm ausgelastet ist und nicht auf Benutzereingaben reagieren kann.

## <a name="creating-the-printing-thread-procedure"></a>Erstellen der Druckthreadprozedur

Es wird empfohlen, diese Features während der Druckverarbeitung zu nutzen.

-   **Die Druckverarbeitung ist in Schritte unterteilt.**

    Sie können die Druckverarbeitung in diskrete Verarbeitungsschritte unterteilen, die Sie unterbrechen können, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt. Dies ist nützlich, da die Druckverarbeitung prozessorintensive Vorgänge umfassen kann. Das Aufbrechen dieser Verarbeitung in Schritte kann verhindern, dass die Druckverarbeitung andere Threads oder Prozesse blockiert oder verzögert. Wenn die Verarbeitung in logische Schritte unterteilt wird, ist es auch möglich, die Druckverarbeitung zu einem beliebigen Zeitpunkt sauber zu beenden, sodass das Beenden eines Druckauftrags, bevor er abgeschlossen wurde, keine verwaisten Ressourcen verlässt.

    Dies ist eine Beispielliste der Druckschritte.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Überprüfen auf ein Abbruchereignis zwischen den Schritten**

    Wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, signalisiert der Benutzeroberflächenthread das Abbruchereignis. Der Verarbeitungsthread muss das Abbruchereignis regelmäßig überprüfen, um zu wissen, wann ein Benutzer auf die Schaltfläche **Abbrechen** geklickt hat. Die [**WaitForSingleObject-Anweisungen**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) führen diese Überprüfung durch und ermöglichen auch anderen Programmen die Ausführung, sodass die Druckauftragsverarbeitung andere Threads oder Prozesse nicht blockiert oder verzögert.

    Im folgenden Codebeispiel wird einer der Tests veranschaulicht, um festzustellen, ob das Abbruchereignis aufgetreten ist.

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **Senden von Statusupdates an den Benutzeroberflächenthread**

    Bei jedem Druckverarbeitungsschritt sendet der Druckverarbeitungsthread Aktualisierungsmeldungen an das Dialogfeld "Druckfortschritt", damit die Statusanzeige aktualisiert werden kann. Beachten Sie, dass das Dialogfeld "Druckfortschritt" im UI-Thread ausgeführt wird.

    Das folgende Codebeispiel veranschaulicht einen der Updatemeldungsaufrufe.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Starten des Druckthreads

Der Druckverarbeitungsthread wird ausgeführt, bis die PrintThreadProc-Funktion zurückgegeben wird. Mit den folgenden Schritten wird der Druckthread gestartet.

1.  **Bereiten Sie die Daten- und Benutzeroberflächenelemente für das Drucken vor.**

    Bevor Sie den Druckverarbeitungsthread starten, müssen Sie die Datenelemente initialisieren, die den Druckauftrag und die Benutzeroberflächenelemente beschreiben. Diese Elemente enthalten den Cursorzustand, sodass der Wartecursor entsprechend angezeigt wird. Sie müssen auch die Statusanzeige konfigurieren, um die Größe des Druckauftrags widerzuspiegeln. Diese Vorbereitungsschritte werden unter [Vorgehensweise: Sammeln von Druckauftragsinformationen vom Benutzer](preparing-to-print.md)ausführlich beschrieben.

    Das folgende Codebeispiel zeigt, wie Sie die Statusanzeige so konfigurieren, dass sie die Größe des druckauftrags widerspiegelt, den der Benutzer angefordert hat.

    ```C++
    // Compute the number of steps in this job.
    stepCount = (((
                // One copy of a document contains
                //  one step for each page +
                //  one step for the document
                ((threadInfo->documentContent)->pages + 1) * 
                // Each copy of the document includes
                //  two steps to open and close the document
                threadInfo->copies) + 2) * 
                // Each job includes one step to start the job
                threadInfo->packages) + 1;
    // Send the total number of steps to the progress bar control.
    SendMessage (
        dlgInfo->progressBarWindow, 
        PBM_SETRANGE32, 
        0L, 
        (stepCount));
    ```

    

2.  **Starten Sie den Druckverarbeitungsthread.**

    Rufen [**Sie CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) auf, um den Verarbeitungsthread zu starten.

    Im folgenden Codebeispiel wird der Verarbeitungsthread gestartet.

    ```C++
    // Start the printing thread
    threadInfo->printThreadHandle = CreateThread (
                    NULL, 
                    0L, 
                    (LPTHREAD_START_ROUTINE)PrintThreadProc,
                    (LPVOID)threadInfo, 
                    0L, 
                    &threadInfo->printThreadId);
    ```

    

3.  **Überprüfen Sie, ob beim Starten der Druckverarbeitung ein Fehler aufgetreten ist.**

    [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) gibt ein Handle an den erstellten Thread zurück, wenn der Thread erfolgreich erstellt wurde. Die PrintThreadProc-Funktion, die im neuen Thread gestartet wurde, überprüft einige Bedingungen, bevor die eigentliche Druckauftragsverarbeitung gestartet wird. Wenn bei diesen Überprüfungen Fehler erkannt werden, kann PrintThreadProc zurückgeben, ohne Druckauftragsdaten zu verarbeiten. Der UI-Thread kann überprüfen, ob der Verarbeitungsthread erfolgreich gestartet wurde, indem er für einen längeren Zeitraum auf das Threadhandle wartet, als zum Ausführen der ersten Tests erforderlich ist. Wenn der Thread beendet wird, wird das Handle für den Thread signalisiert. Der Code überprüft den Zustand des Threads für einen kurzen Zeitraum, nachdem er den Verarbeitungsthread gestartet hat. Die [**WaitForSingleObject-Funktion**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) gibt zurück, wenn entweder das Timeout auftritt oder das Threadhandle signalisiert wird. Wenn die **WaitForSingleObject-Funktion** den Status **WAIT OBJECT \_ \_ 0** zurückgibt, wurde der Thread früh beendet. Daher sollten Sie das Dialogfeld "Druckstatus" schließen, wie im folgenden Codebeispiel gezeigt.

    ```C++
    // Make sure the printing thread started OK
    //  by waiting to see if it is still running after
    //  a short period of time. This time delay should be
    //  long enough to know that it's running but shorter
    //  than the shortest possible print job.
    waitStatus = WaitForSingleObject (
        threadInfo->printThreadHandle, 
        THREAD_START_WAIT);

    // If the object is signaled, that means that the
    //  thread terminated before the timeout period elapsed.
    if (WAIT_OBJECT_0 == waitStatus)
    {
        // The thread exited, so post close messages.
        PostMessage (hDlg, USER_PRINT_CLOSING, 0L, (LPARAM)E_FAIL);
        PostMessage (hDlg, USER_PRINT_COMPLETE, 0L, (LPARAM)E_FAIL);
    }
    ```

    

## <a name="stopping-the-printing-thread"></a>Beenden des Druckthreads

Wenn der Benutzer im Dialogfeld "Druckfortschritt" auf die Schaltfläche **Abbrechen** klickt, wird der Druckthread benachrichtigt, damit er die Verarbeitung des Druckauftrags in der richtigen Reihenfolge beenden kann. Während die Schaltfläche **Abbrechen** und das **Ereignis quitEvent** wichtige Aspekte dieser Verarbeitung sind, müssen Sie die gesamte Verarbeitungssequenz so entwerfen, dass sie erfolgreich unterbrochen wird. Dies bedeutet, dass die Schritte in der Sequenz keine zugeordneten Ressourcen belassen dürfen, die nicht freigegeben werden, wenn ein Benutzer die Sequenz abbricht, bevor sie abgeschlossen wurde.

Das folgende Codebeispiel zeigt, wie das Beispielprogramm das **quitEvent** überprüft, bevor es jede Seite im gedruckten Dokument verarbeitet. Wenn das **quitEvent** signalisiert oder ein Fehler erkannt wurde, wird die Druckverarbeitung beendet.


```C++
// While no errors and the user hasn't clicked cancel...
while (((waitStatus = WaitForSingleObject (
                        threadInfo->quitEvent, 
                        stepDelay)) == WAIT_TIMEOUT) &&
        SUCCEEDED(hr))
{
    // ...print one page
    hr = PrintStep_4_DoOnePage (threadInfo);

    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    

    if (threadInfo->currentPage < (threadInfo->documentContent)->pages)
    {
        // More pages, so continue to the next one
        threadInfo->currentPage++;
    }
    else
    {
        // Last page printed so exit loop and close
        break;
    }
}
```



 

 
