---
description: In diesem Thema wird beschrieben, wie der Druckauftrags Verarbeitungs Thread gestartet und beendet wird.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Vorgehensweise: starten und Abbrechen eines Druck Threads'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218223"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a>Vorgehensweise: starten und Abbrechen eines Druck Threads

In diesem Thema wird beschrieben, wie der Druckauftrags Verarbeitungs Thread gestartet und beendet wird.

## <a name="overview"></a>Übersicht

Um zu verhindern, dass Druckaktivitäten die Benutzeroberflächen Antwort blockieren, erstellen Sie einen separaten Thread, um den Druckauftrag zu verarbeiten. Der Thread, der gestartet wird, wenn das Programm gestartet wird, ist der Thread, der die Fenster Meldungen behandelt, die sich aus der Benutzerinteraktion ergeben, und ist daher der UI-Thread. Das Programm muss diese Nachrichten ohne Verzögerung verarbeiten, damit die Benutzeroberfläche rechtzeitig auf die Maus-und Tastatureingaben des Benutzers antwortet. Damit das Programm in der Lage ist, schnell auf diese Meldungen zu reagieren, ist die Verarbeitungs Menge, die bei einer beliebigen Nachricht durchgeführt werden kann, begrenzt. Wenn eine Benutzer Anforderung eine umfangreiche Verarbeitung erfordert, muss ein anderer Thread diese Verarbeitung durchführen, damit die nachfolgende Benutzerinteraktion vom Programm verarbeitet werden kann.

Zum Verarbeiten von Daten in einem separaten Thread muss das Programm den Vorgang des Benutzeroberflächen Threads und des Verarbeitungs Threads koordinieren. Wenn z. b. der Verarbeitungs Thread die Daten verarbeitet, darf der Haupt Thread diese Daten nicht ändern. Eine Möglichkeit, dies zu verwalten, ist durch Thread sichere Synchronisierungs Objekte wie Semaphore, Ereignisse und Mutexen.

Gleichzeitig müssen einige Benutzerinteraktionen verhindert werden, während der Verarbeitungs Thread ausgeführt wird. Im Beispielprogramm werden die Anwendungsdaten geschützt und die Benutzerinteraktion beschränkt, indem die Verarbeitung des Druckauftrags durch das Dialogfeld modales Fortschreiten verwaltet wird. In einem modalen Dialogfeld wird verhindert, dass der Benutzer mit dem Hauptfenster des Programms interagiert, wodurch verhindert wird, dass der Benutzer die Anwendungsprogramm Daten ändert, während die Daten gedruckt werden.

Die einzige Aktion, die der Benutzer ausführen kann, während ein Druckauftrag verarbeitet wird, besteht darin, den Druckauftrag abzubrechen. Diese Einschränkung wird dem Benutzer durch die Form "Cursor" signalisiert. Wenn sich der Cursor über der Schaltfläche **Abbrechen** befindet, wird ein Pfeilcursor angezeigt, der anzeigt, dass der Benutzer auf diese Schaltfläche klicken kann. Wenn sich der Cursor über einem anderen Teil des Fenster Bereichs des Programms befindet, wird ein warte Cursor angezeigt, der anzeigt, dass das Programm ausgelastet ist und nicht auf Benutzereingaben reagieren kann.

## <a name="creating-the-printing-thread-procedure"></a>Erstellen der Druck Thread Prozedur

Es wird empfohlen, diese Features während der Druck Verarbeitung einzubeziehen.

-   **Die Druck Verarbeitung ist in Schritte unterteilt.**

    Sie können die Druck Verarbeitung in diskrete Verarbeitungsschritte aufteilen, die Sie unterbrechen können, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt. Dies ist hilfreich, da die Druck Verarbeitung prozessorintensive Vorgänge beinhalten kann. Das Abbrechen dieser Verarbeitung in Schritte kann verhindern, dass die Druck Verarbeitung andere Threads oder Prozesse blockiert oder verzögert. Wenn Sie die Verarbeitung in logische Schritte unterteilen, ist es auch möglich, die Druck Verarbeitung zu einem beliebigen Zeitpunkt ordnungsgemäß zu beenden, sodass das Beenden eines Druckauftrags vor dem Abschluss keine verwaisten Ressourcen verlässt.

    Dies ist eine Beispielliste von Druck Schritten.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Nach einem Abbruch Ereignis zwischen den Schritten suchen**

    Wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, signalisiert der Benutzeroberflächen Thread das Ereignis abbrechen. Der Verarbeitungs Thread muss das Ereignis abbrechen regelmäßig überprüfen, um zu wissen, wann ein Benutzer auf die Schaltfläche **Abbrechen** geklickt hat. Die [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Anweisungen führen diese Überprüfung aus und geben anderen Programmen die Möglichkeit zur Ausführung, damit die Verarbeitung von Druckaufträgen andere Threads oder Prozesse nicht blockiert oder verzögert.

    Das folgende Codebeispiel veranschaulicht einen der Tests, um festzustellen, ob das Cancel-Ereignis aufgetreten ist.

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **Statusaktualisierungen an Benutzeroberflächen Thread senden**

    Bei jedem Schritt der Druck Verarbeitung sendet der Druck Verarbeitungs Thread Aktualisierungs Meldungen an das Dialogfeld "Druck Status", sodass die Statusanzeige aktualisiert werden kann. Beachten Sie, dass das Dialogfeld Druck Status im UI-Thread ausgeführt wird.

    Im folgenden Codebeispiel wird einer der Update-Nachrichten Aufrufe veranschaulicht.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Der Druck Thread wird gestartet.

Der Druck Verarbeitungs Thread wird ausgeführt, bis die printthreadproc-Funktion zurückgibt. Mit den folgenden Schritten wird der Druck Thread gestartet.

1.  **Bereiten Sie die Daten und die Benutzeroberflächen Elemente für das Drucken vor.**

    Bevor Sie den druckverarbeitungs Thread starten, müssen Sie die Datenelemente initialisieren, die den Druckauftrag und die Benutzeroberflächen Elemente beschreiben. Diese Elemente enthalten den Cursor Zustand, sodass der Warte Cursor entsprechend angezeigt wird. Außerdem müssen Sie die Statusanzeige so konfigurieren, dass Sie die Größe des Druckauftrags widerspiegelt. Diese Vorbereitungsschritte werden im Abschnitt Gewusst [wie: Sammeln von Druckauftrags Informationen des Benutzers](preparing-to-print.md)ausführlich beschrieben.

    Im folgenden Codebeispiel wird gezeigt, wie Sie die Statusanzeige so konfigurieren, dass Sie die Größe des vom Benutzer angeforderten Druckauftrags widerspiegelt.

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

    

2.  **Starten Sie den druckverarbeitungs Thread.**

    Aufrufen von " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ", um den Verarbeitungs Thread zu starten.

    Im folgenden Codebeispiel wird der Verarbeitungs Thread gestartet.

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

    

3.  **Überprüfen Sie, ob bei der Druck Verarbeitung beim Start Fehler**

    " [**Kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " gibt ein Handle für den erstellten Thread zurück, wenn der Thread erfolgreich erstellt wurde. Die printthreadproc-Funktion, die im neuen Thread gestartet wurde, prüft einige Bedingungen, bevor die tatsächliche Druckauftrags Verarbeitung gestartet wird. Wenn Fehler in diesen Überprüfungen erkannt werden, könnte printthreadproc zurückgeben, ohne Druckauftrags Daten verarbeiten zu müssen. Der UI-Thread kann überprüfen, ob der Verarbeitungs Thread erfolgreich gestartet wurde, indem er auf das Thread Handle für einen Zeitraum wartet, der länger ist als für die Durchführung der anfänglichen Tests, jedoch nicht länger als erforderlich. Wenn der Thread beendet wird, wird das Handle für den Thread signalisiert. Der Code überprüft den Zustand des Threads für eine kurze Zeitspanne, nachdem der Verarbeitungs Thread gestartet wurde. Die [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion gibt zurück, wenn entweder das Timeout auftritt oder das Thread Handle signalisiert wird. Wenn die Funktion " **WaitForSingleObject** " den Status " **Wait \_ Object \_ 0** " zurückgibt, wurde der Thread frühzeitig beendet. Daher sollten Sie das Dialogfeld "Druckfortschritt" schließen, wie im folgenden Codebeispiel gezeigt.

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

    

## <a name="stopping-the-printing-thread"></a>Der Druck Thread wird angehalten.

Wenn der Benutzer im Dialogfeld Druck Status auf die Schaltfläche **Abbrechen** klickt, wird der Druck Thread benachrichtigt, sodass er die Verarbeitung des Druckauftrags ordnungsgemäß beenden kann. Während die Schaltfläche **Abbrechen** und das Ereignis **quitevent** wichtige Aspekte dieser Verarbeitung sind, müssen Sie die gesamte Verarbeitungssequenz so entwerfen, dass Sie erfolgreich unterbrochen wird. Dies bedeutet, dass die Schritte in der Sequenz keine zugeordneten Ressourcen belassen dürfen, die nicht freigegeben werden, wenn ein Benutzer die Sequenz abbricht, bevor er abgeschlossen wurde.

Im folgenden Codebeispiel wird gezeigt, wie das Beispielprogramm das " **quitevent** " überprüft, bevor es die einzelnen Seiten im gedruckten Dokument verarbeitet. Wenn das " **quitevent** " signalisiert wird oder ein Fehler erkannt wurde, wird die Druck Verarbeitung angehalten.


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



 

 
