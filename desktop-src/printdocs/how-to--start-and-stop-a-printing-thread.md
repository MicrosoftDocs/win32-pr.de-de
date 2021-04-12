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
# <a name="how-to-start-and-stop-a-printing-thread"></a><span data-ttu-id="a252a-103">Vorgehensweise: starten und Abbrechen eines Druck Threads</span><span class="sxs-lookup"><span data-stu-id="a252a-103">How To: Start and Stop a Printing Thread</span></span>

<span data-ttu-id="a252a-104">In diesem Thema wird beschrieben, wie der Druckauftrags Verarbeitungs Thread gestartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-104">This topic describes how to start and stop the print job processing thread.</span></span>

## <a name="overview"></a><span data-ttu-id="a252a-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a252a-105">Overview</span></span>

<span data-ttu-id="a252a-106">Um zu verhindern, dass Druckaktivitäten die Benutzeroberflächen Antwort blockieren, erstellen Sie einen separaten Thread, um den Druckauftrag zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a252a-106">To prevent printing activities from blocking the user interface response, create a separate thread to process the print job.</span></span> <span data-ttu-id="a252a-107">Der Thread, der gestartet wird, wenn das Programm gestartet wird, ist der Thread, der die Fenster Meldungen behandelt, die sich aus der Benutzerinteraktion ergeben, und ist daher der UI-Thread.</span><span class="sxs-lookup"><span data-stu-id="a252a-107">The thread that is started when the program is started, is the thread that handles the window messages that result from user interaction, and is therefore the UI thread.</span></span> <span data-ttu-id="a252a-108">Das Programm muss diese Nachrichten ohne Verzögerung verarbeiten, damit die Benutzeroberfläche rechtzeitig auf die Maus-und Tastatureingaben des Benutzers antwortet.</span><span class="sxs-lookup"><span data-stu-id="a252a-108">The program must process these messages without delay for the user interface to respond to the user's mouse and keyboard input in a timely manner.</span></span> <span data-ttu-id="a252a-109">Damit das Programm in der Lage ist, schnell auf diese Meldungen zu reagieren, ist die Verarbeitungs Menge, die bei einer beliebigen Nachricht durchgeführt werden kann, begrenzt.</span><span class="sxs-lookup"><span data-stu-id="a252a-109">For the program to be able to respond to these messages quickly, the amount of processing that can be performed during any one message is limited.</span></span> <span data-ttu-id="a252a-110">Wenn eine Benutzer Anforderung eine umfangreiche Verarbeitung erfordert, muss ein anderer Thread diese Verarbeitung durchführen, damit die nachfolgende Benutzerinteraktion vom Programm verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a252a-110">When a user request requires extensive processing, a different thread must perform that processing to allow subsequent user interaction to be handled by the program.</span></span>

<span data-ttu-id="a252a-111">Zum Verarbeiten von Daten in einem separaten Thread muss das Programm den Vorgang des Benutzeroberflächen Threads und des Verarbeitungs Threads koordinieren.</span><span class="sxs-lookup"><span data-stu-id="a252a-111">Processing data in a separate thread requires the program to coordinate the operation of user interface thread and the processing thread.</span></span> <span data-ttu-id="a252a-112">Wenn z. b. der Verarbeitungs Thread die Daten verarbeitet, darf der Haupt Thread diese Daten nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="a252a-112">For example, while the processing thread is processing the data, the main thread must not alter that data.</span></span> <span data-ttu-id="a252a-113">Eine Möglichkeit, dies zu verwalten, ist durch Thread sichere Synchronisierungs Objekte wie Semaphore, Ereignisse und Mutexen.</span><span class="sxs-lookup"><span data-stu-id="a252a-113">One way to manage this is through thread-safe synchronization objects such as semaphores, events, and mutexes.</span></span>

<span data-ttu-id="a252a-114">Gleichzeitig müssen einige Benutzerinteraktionen verhindert werden, während der Verarbeitungs Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-114">At the same time, some user interaction must be prevented while the processing thread is running.</span></span> <span data-ttu-id="a252a-115">Im Beispielprogramm werden die Anwendungsdaten geschützt und die Benutzerinteraktion beschränkt, indem die Verarbeitung des Druckauftrags durch das Dialogfeld modales Fortschreiten verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-115">In the sample program, the application data is protected and the user interaction is limited by having the print job processing be managed by the modal progress dialog box.</span></span> <span data-ttu-id="a252a-116">In einem modalen Dialogfeld wird verhindert, dass der Benutzer mit dem Hauptfenster des Programms interagiert, wodurch verhindert wird, dass der Benutzer die Anwendungsprogramm Daten ändert, während die Daten gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="a252a-116">A modal dialog box prevents the user from interacting with the program's main window, which prevents the user from altering the application program data while the data is printed.</span></span>

<span data-ttu-id="a252a-117">Die einzige Aktion, die der Benutzer ausführen kann, während ein Druckauftrag verarbeitet wird, besteht darin, den Druckauftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="a252a-117">The only action the user can perform while a print job is processing is to cancel the print job.</span></span> <span data-ttu-id="a252a-118">Diese Einschränkung wird dem Benutzer durch die Form "Cursor" signalisiert.</span><span class="sxs-lookup"><span data-stu-id="a252a-118">This restriction is signaled to the user by the cursor shape.</span></span> <span data-ttu-id="a252a-119">Wenn sich der Cursor über der Schaltfläche **Abbrechen** befindet, wird ein Pfeilcursor angezeigt, der anzeigt, dass der Benutzer auf diese Schaltfläche klicken kann.</span><span class="sxs-lookup"><span data-stu-id="a252a-119">When the cursor is over the **Cancel** button, an arrow cursor is displayed, which indicates that the user can click this button.</span></span> <span data-ttu-id="a252a-120">Wenn sich der Cursor über einem anderen Teil des Fenster Bereichs des Programms befindet, wird ein warte Cursor angezeigt, der anzeigt, dass das Programm ausgelastet ist und nicht auf Benutzereingaben reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="a252a-120">When the cursor is over any other part of the program's window area, a wait cursor is displayed, which indicates that the program is busy and cannot respond to user input.</span></span>

## <a name="creating-the-printing-thread-procedure"></a><span data-ttu-id="a252a-121">Erstellen der Druck Thread Prozedur</span><span class="sxs-lookup"><span data-stu-id="a252a-121">Creating the Printing Thread Procedure</span></span>

<span data-ttu-id="a252a-122">Es wird empfohlen, diese Features während der Druck Verarbeitung einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="a252a-122">We recommend including these features while print processing.</span></span>

-   <span data-ttu-id="a252a-123">**Die Druck Verarbeitung ist in Schritte unterteilt.**</span><span class="sxs-lookup"><span data-stu-id="a252a-123">**Print processing is divided into steps**</span></span>

    <span data-ttu-id="a252a-124">Sie können die Druck Verarbeitung in diskrete Verarbeitungsschritte aufteilen, die Sie unterbrechen können, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt.</span><span class="sxs-lookup"><span data-stu-id="a252a-124">You can divide the print processing into discrete processing steps that you can interrupt if the user clicks the **Cancel** button.</span></span> <span data-ttu-id="a252a-125">Dies ist hilfreich, da die Druck Verarbeitung prozessorintensive Vorgänge beinhalten kann.</span><span class="sxs-lookup"><span data-stu-id="a252a-125">This is useful because print processing can include processor-intensive operations.</span></span> <span data-ttu-id="a252a-126">Das Abbrechen dieser Verarbeitung in Schritte kann verhindern, dass die Druck Verarbeitung andere Threads oder Prozesse blockiert oder verzögert.</span><span class="sxs-lookup"><span data-stu-id="a252a-126">Breaking this processing into steps can prevent the print processing from blocking or delaying other threads or processes.</span></span> <span data-ttu-id="a252a-127">Wenn Sie die Verarbeitung in logische Schritte unterteilen, ist es auch möglich, die Druck Verarbeitung zu einem beliebigen Zeitpunkt ordnungsgemäß zu beenden, sodass das Beenden eines Druckauftrags vor dem Abschluss keine verwaisten Ressourcen verlässt.</span><span class="sxs-lookup"><span data-stu-id="a252a-127">Breaking the processing into logical steps also makes it possible to cleanly terminate the print processing at any point, so that ending a print job before it has finished will not leave any orphaned resources.</span></span>

    <span data-ttu-id="a252a-128">Dies ist eine Beispielliste von Druck Schritten.</span><span class="sxs-lookup"><span data-stu-id="a252a-128">This is an example list of print steps.</span></span>

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   <span data-ttu-id="a252a-129">**Nach einem Abbruch Ereignis zwischen den Schritten suchen**</span><span class="sxs-lookup"><span data-stu-id="a252a-129">**Check for a cancel event between steps**</span></span>

    <span data-ttu-id="a252a-130">Wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, signalisiert der Benutzeroberflächen Thread das Ereignis abbrechen.</span><span class="sxs-lookup"><span data-stu-id="a252a-130">When the user clicks the **Cancel** button, the user interface thread signals the cancel event.</span></span> <span data-ttu-id="a252a-131">Der Verarbeitungs Thread muss das Ereignis abbrechen regelmäßig überprüfen, um zu wissen, wann ein Benutzer auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="a252a-131">The processing thread must check the cancel event periodically to know when a user clicked the **Cancel** button.</span></span> <span data-ttu-id="a252a-132">Die [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Anweisungen führen diese Überprüfung aus und geben anderen Programmen die Möglichkeit zur Ausführung, damit die Verarbeitung von Druckaufträgen andere Threads oder Prozesse nicht blockiert oder verzögert.</span><span class="sxs-lookup"><span data-stu-id="a252a-132">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) statements perform this check and they also give other programs a chance to run so that the print job processing doesn't block or delay other threads or processes.</span></span>

    <span data-ttu-id="a252a-133">Das folgende Codebeispiel veranschaulicht einen der Tests, um festzustellen, ob das Cancel-Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a252a-133">The following code example illustrates one of the tests to see whether the cancel event has occurred.</span></span>

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   <span data-ttu-id="a252a-134">**Statusaktualisierungen an Benutzeroberflächen Thread senden**</span><span class="sxs-lookup"><span data-stu-id="a252a-134">**Send status updates to user interface thread**</span></span>

    <span data-ttu-id="a252a-135">Bei jedem Schritt der Druck Verarbeitung sendet der Druck Verarbeitungs Thread Aktualisierungs Meldungen an das Dialogfeld "Druck Status", sodass die Statusanzeige aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a252a-135">As each print processing step, the print processing thread sends update messages to the print progress dialog box so that it can update the progress bar.</span></span> <span data-ttu-id="a252a-136">Beachten Sie, dass das Dialogfeld Druck Status im UI-Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-136">Note that the print progress dialog box is running in the UI thread.</span></span>

    <span data-ttu-id="a252a-137">Im folgenden Codebeispiel wird einer der Update-Nachrichten Aufrufe veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a252a-137">The following code example illustrates one of the update message calls.</span></span>

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a><span data-ttu-id="a252a-138">Der Druck Thread wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="a252a-138">Starting the Printing Thread</span></span>

<span data-ttu-id="a252a-139">Der Druck Verarbeitungs Thread wird ausgeführt, bis die printthreadproc-Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a252a-139">The print processing thread runs until the PrintThreadProc function returns.</span></span> <span data-ttu-id="a252a-140">Mit den folgenden Schritten wird der Druck Thread gestartet.</span><span class="sxs-lookup"><span data-stu-id="a252a-140">The following steps start the printing thread.</span></span>

1.  <span data-ttu-id="a252a-141">**Bereiten Sie die Daten und die Benutzeroberflächen Elemente für das Drucken vor.**</span><span class="sxs-lookup"><span data-stu-id="a252a-141">**Prepare the data and user interface elements for printing.**</span></span>

    <span data-ttu-id="a252a-142">Bevor Sie den druckverarbeitungs Thread starten, müssen Sie die Datenelemente initialisieren, die den Druckauftrag und die Benutzeroberflächen Elemente beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a252a-142">Before starting the print processing thread, you must initialize the data elements that describe the print job and the user interface elements.</span></span> <span data-ttu-id="a252a-143">Diese Elemente enthalten den Cursor Zustand, sodass der Warte Cursor entsprechend angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-143">These elements include the cursor state, so that the wait cursor will be displayed appropriately.</span></span> <span data-ttu-id="a252a-144">Außerdem müssen Sie die Statusanzeige so konfigurieren, dass Sie die Größe des Druckauftrags widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="a252a-144">You must also configure the progress bar to reflect the size of the print job.</span></span> <span data-ttu-id="a252a-145">Diese Vorbereitungsschritte werden im Abschnitt Gewusst [wie: Sammeln von Druckauftrags Informationen des Benutzers](preparing-to-print.md)ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a252a-145">These preparation steps are described in detail in [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

    <span data-ttu-id="a252a-146">Im folgenden Codebeispiel wird gezeigt, wie Sie die Statusanzeige so konfigurieren, dass Sie die Größe des vom Benutzer angeforderten Druckauftrags widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="a252a-146">The following code example shows how to configure the progress bar to reflect the size of the print job that the user requested.</span></span>

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

    

2.  <span data-ttu-id="a252a-147">**Starten Sie den druckverarbeitungs Thread.**</span><span class="sxs-lookup"><span data-stu-id="a252a-147">**Start the print processing thread.**</span></span>

    <span data-ttu-id="a252a-148">Aufrufen von " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ", um den Verarbeitungs Thread zu starten.</span><span class="sxs-lookup"><span data-stu-id="a252a-148">Call [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to start the processing thread.</span></span>

    <span data-ttu-id="a252a-149">Im folgenden Codebeispiel wird der Verarbeitungs Thread gestartet.</span><span class="sxs-lookup"><span data-stu-id="a252a-149">The following code example starts the processing thread.</span></span>

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

    

3.  <span data-ttu-id="a252a-150">**Überprüfen Sie, ob bei der Druck Verarbeitung beim Start Fehler**</span><span class="sxs-lookup"><span data-stu-id="a252a-150">**Check whether print processing failed on start.**</span></span>

    <span data-ttu-id="a252a-151">" [**Kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " gibt ein Handle für den erstellten Thread zurück, wenn der Thread erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a252a-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) returns a handle to the created thread if the thread was created successfully.</span></span> <span data-ttu-id="a252a-152">Die printthreadproc-Funktion, die im neuen Thread gestartet wurde, prüft einige Bedingungen, bevor die tatsächliche Druckauftrags Verarbeitung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-152">The PrintThreadProc function that was started in the new thread checks some conditions before it starts the actual print job processing.</span></span> <span data-ttu-id="a252a-153">Wenn Fehler in diesen Überprüfungen erkannt werden, könnte printthreadproc zurückgeben, ohne Druckauftrags Daten verarbeiten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a252a-153">If it detects any errors in these checks, PrintThreadProc could return without processing any print job data.</span></span> <span data-ttu-id="a252a-154">Der UI-Thread kann überprüfen, ob der Verarbeitungs Thread erfolgreich gestartet wurde, indem er auf das Thread Handle für einen Zeitraum wartet, der länger ist als für die Durchführung der anfänglichen Tests, jedoch nicht länger als erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a252a-154">The UI thread can check whether the processing thread started successfully by waiting on the thread handle for a period of time that is longer than it takes to perform the initial tests but no longer than necessary.</span></span> <span data-ttu-id="a252a-155">Wenn der Thread beendet wird, wird das Handle für den Thread signalisiert.</span><span class="sxs-lookup"><span data-stu-id="a252a-155">When the thread exits, the handle to the thread becomes signaled.</span></span> <span data-ttu-id="a252a-156">Der Code überprüft den Zustand des Threads für eine kurze Zeitspanne, nachdem der Verarbeitungs Thread gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a252a-156">The code checks the thread's state for a short period of time after it starts the processing thread.</span></span> <span data-ttu-id="a252a-157">Die [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion gibt zurück, wenn entweder das Timeout auftritt oder das Thread Handle signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-157">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function returns when either the timeout occurs or the thread handle is signaled.</span></span> <span data-ttu-id="a252a-158">Wenn die Funktion " **WaitForSingleObject** " den Status " **Wait \_ Object \_ 0** " zurückgibt, wurde der Thread frühzeitig beendet. Daher sollten Sie das Dialogfeld "Druckfortschritt" schließen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a252a-158">If the **WaitForSingleObject** function returns a **WAIT\_OBJECT\_0** status, the thread exited early and so you should close the print progress dialog, as the following code example shows.</span></span>

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

    

## <a name="stopping-the-printing-thread"></a><span data-ttu-id="a252a-159">Der Druck Thread wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="a252a-159">Stopping the Printing Thread</span></span>

<span data-ttu-id="a252a-160">Wenn der Benutzer im Dialogfeld Druck Status auf die Schaltfläche **Abbrechen** klickt, wird der Druck Thread benachrichtigt, sodass er die Verarbeitung des Druckauftrags ordnungsgemäß beenden kann.</span><span class="sxs-lookup"><span data-stu-id="a252a-160">When the user clicks the **Cancel** button in the print progress dialog box, the printing thread is notified so that it can stop processing the print job in an orderly manner.</span></span> <span data-ttu-id="a252a-161">Während die Schaltfläche **Abbrechen** und das Ereignis **quitevent** wichtige Aspekte dieser Verarbeitung sind, müssen Sie die gesamte Verarbeitungssequenz so entwerfen, dass Sie erfolgreich unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="a252a-161">While the **Cancel** button and the **quitEvent** event are important aspects of this processing, you must design the entire processing sequence to be interrupted successfully.</span></span> <span data-ttu-id="a252a-162">Dies bedeutet, dass die Schritte in der Sequenz keine zugeordneten Ressourcen belassen dürfen, die nicht freigegeben werden, wenn ein Benutzer die Sequenz abbricht, bevor er abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a252a-162">This means that the steps in the sequence must not leave any allocated resources that are not freed if a user cancels the sequence before it had completed.</span></span>

<span data-ttu-id="a252a-163">Im folgenden Codebeispiel wird gezeigt, wie das Beispielprogramm das " **quitevent** " überprüft, bevor es die einzelnen Seiten im gedruckten Dokument verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a252a-163">The following code example shows how the sample program checks the **quitEvent** before it processes each page in the document being printed.</span></span> <span data-ttu-id="a252a-164">Wenn das " **quitevent** " signalisiert wird oder ein Fehler erkannt wurde, wird die Druck Verarbeitung angehalten.</span><span class="sxs-lookup"><span data-stu-id="a252a-164">If the **quitEvent** is signaled or an error was detected, print processing stops.</span></span>


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



 

 
