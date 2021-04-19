---
description: Benutzern das Abbrechen von e/a-Anforderungen, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Abbrechen von ausstehenden e/a-Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d108409eea32cf18a94f83bf7aacd282c60d3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359513"
---
# <a name="canceling-pending-io-operations"></a><span data-ttu-id="b0390-103">Abbrechen von ausstehenden e/a-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="b0390-103">Canceling Pending I/O Operations</span></span>

<span data-ttu-id="b0390-104">Benutzern das Abbrechen von e/a-Anforderungen, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="b0390-104">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span> <span data-ttu-id="b0390-105">Wenn z. b. ein aufrufungs Vorgang der [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) -Funktion blockiert ist, weil der-Vorgang an ein sehr langsames Gerät gerichtet ist, wird durch Abbrechen des Aufrufes wiederholt, mit neuen Parametern, ohne die Anwendung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="b0390-105">For example, if a call to the [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) function is blocked because the call is to a very slow device, canceling it enables the call to be made again, with new parameters, without terminating the application.</span></span>

<span data-ttu-id="b0390-106">Windows Vista erweitert die Abbruch Funktionen und bietet Unterstützung für das Abbrechen synchroner Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="b0390-106">Windows Vista extends the cancellation capabilities and includes support for canceling synchronous operations.</span></span>

<span data-ttu-id="b0390-107">**Hinweis**  Durch Aufrufen der [**CancelIoEx**](cancelioex-func.md) -Funktion wird nicht garantiert, dass ein e/a-Vorgang abgebrochen wird. der Treiber, der den Vorgang verarbeitet, muss den Abbruch unterstützen, und der Vorgang muss sich in einem Zustand befinden, der abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0390-107">**Note**  Calling the [**CancelIoEx**](cancelioex-func.md) function does not guarantee that an I/O operation will be canceled; the driver which is handling the operation must support cancellation and the operation must be in a state that can be canceled.</span></span>

## <a name="cancellation-considerations"></a><span data-ttu-id="b0390-108">Überlegungen zum Abbruch</span><span class="sxs-lookup"><span data-stu-id="b0390-108">Cancellation Considerations</span></span>

<span data-ttu-id="b0390-109">Beachten Sie beim Programmieren von Abbruch aufrufen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b0390-109">When programming cancellation calls, keep in mind the following considerations:</span></span>

-   <span data-ttu-id="b0390-110">Es gibt keine Garantie, dass zugrunde liegende Treiber den Abbruch ordnungsgemäß unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b0390-110">There is no guarantee that underlying drivers correctly support cancellation.</span></span>
-   <span data-ttu-id="b0390-111">Wenn beim Abbrechen der asynchronen e/a-Vorgänge keine überlappende Struktur an die [**CancelIoEx**](cancelioex-func.md) -Funktion übergeben wird, versucht die Funktion, alle ausstehenden e/a-Vorgänge für die Datei für alle Threads im Prozess abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="b0390-111">When canceling asynchronous I/O, when no overlapped structure is supplied to the [**CancelIoEx**](cancelioex-func.md) function, the function attempts to cancel all outstanding I/O on the file on all threads in the process.</span></span> <span data-ttu-id="b0390-112">Jeder Thread wird einzeln verarbeitet, sodass nach der Verarbeitung eines Threads möglicherweise ein weiterer e/a-Vorgang für die Datei gestartet wird, bevor für alle anderen Threads die e/a-Vorgänge für die Datei abgebrochen wurden, was zu Synchronisierungs Problemen geführt hat.</span><span class="sxs-lookup"><span data-stu-id="b0390-112">Each thread is processed individually, so after a thread has been processed it may start another I/O on the file before all the other threads have had their I/O for the file canceled, causing synchronization issues.</span></span>
-   <span data-ttu-id="b0390-113">Verwenden Sie beim Abbrechen von asynchronen e/a-Vorgängen keine überlappenden Strukturen mit gezielter Abbruch.</span><span class="sxs-lookup"><span data-stu-id="b0390-113">When canceling asynchronous I/O, do not reuse overlapped structures with targeted cancellation.</span></span> <span data-ttu-id="b0390-114">Sobald die e/a-Operation abgeschlossen ist (entweder erfolgreich oder mit dem Status "abgebrochen"), wird die überlappende Struktur nicht mehr vom System verwendet und kann wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0390-114">Once the I/O operation completes (either successfully or with a canceled status) then the overlapped structure is no longer in use by the system and can be reused.</span></span>
-   <span data-ttu-id="b0390-115">Beim Abbrechen synchroner e/a versucht der Aufruf der [**CancelSynchronousIo**](cancelsynchronousio-func.md) -Funktion, jeden aktuellen synchronen Aufruf für den Thread abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="b0390-115">When canceling synchronous I/O, calling the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function attempts to cancel any current synchronous call on the thread.</span></span> <span data-ttu-id="b0390-116">Sie müssen sicherstellen, dass die Synchronisierung der Aufrufe korrekt ist. der falsche Aufruf in einer Reihe von aufrufen könnte abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="b0390-116">You must take care to ensure the synchronization of the calls is correct; the wrong call in a series of calls could get canceled.</span></span> <span data-ttu-id="b0390-117">Wenn beispielsweise die Funktion **CancelSynchronousIo** für einen synchronen Vorgang, x, aufgerufen wird, wird der Vorgang Y nur gestartet, nachdem der Vorgang x abgeschlossen wurde (normalerweise oder mit einem Fehler).</span><span class="sxs-lookup"><span data-stu-id="b0390-117">For example, if the **CancelSynchronousIo** function is called for a synchronous operation, X, operation Y only starts after that operation X is completed (normally or with an error).</span></span> <span data-ttu-id="b0390-118">Wenn der Thread, der Vorgang x aufgerufen hat, einen anderen synchronen Aufruf von x startet, kann der Abbruch Aufruf diese neue e/a-Anforderung unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="b0390-118">If the thread that called operation X then starts another synchronous call to X, the cancel call could interrupt this new I/O request.</span></span>
-   <span data-ttu-id="b0390-119">Beachten Sie beim Abbrechen synchroner e/a, dass eine Racebedingung immer vorhanden sein kann, wenn ein Thread von verschiedenen Teilen einer Anwendung gemeinsam genutzt wird, z. b. mit einem Thread Pool Thread.</span><span class="sxs-lookup"><span data-stu-id="b0390-119">When canceling synchronous I/O, be aware that a race condition can exist whenever a thread is shared between different parts of an application, for example, with a thread-pool thread.</span></span>

## <a name="operations-that-cannot-be-canceled"></a><span data-ttu-id="b0390-120">Vorgänge, die nicht abgebrochen werden können</span><span class="sxs-lookup"><span data-stu-id="b0390-120">Operations That Cannot Be Canceled</span></span>

<span data-ttu-id="b0390-121">Einige Funktionen können mit der Funktion [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)oder [**CancelSynchronousIo**](cancelsynchronousio-func.md) nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="b0390-121">Some functions cannot be canceled using the [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md), or [**CancelSynchronousIo**](cancelsynchronousio-func.md) function.</span></span> <span data-ttu-id="b0390-122">Einige dieser Funktionen wurden erweitert, um einen Abbruch zuzulassen (z. b. die [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) -Funktion), und Sie sollten diese stattdessen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0390-122">Some of these functions have been extended to allow cancellation (for example, the [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function) and you should use these instead.</span></span> <span data-ttu-id="b0390-123">Zusätzlich zur Unterstützung von Abbruch verfügen diese Funktionen auch über integrierte Rückrufe, mit denen Sie den Fortschritt des Vorgangs verfolgen können.</span><span class="sxs-lookup"><span data-stu-id="b0390-123">In addition to supporting cancellation, these functions also have built-in callbacks to support you when tracking the progress of the operation.</span></span> <span data-ttu-id="b0390-124">Die folgenden Funktionen unterstützen keinen Abbruch:</span><span class="sxs-lookup"><span data-stu-id="b0390-124">The following functions do not support cancellation:</span></span>

-   <span data-ttu-id="b0390-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)– Verwenden von [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span><span class="sxs-lookup"><span data-stu-id="b0390-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)—use [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span></span>
-   <span data-ttu-id="b0390-126">" [**Muvefile**](/windows/desktop/api/WinBase/nf-winbase-movefile)" – Verwenden von " [ **muvefilewithprogress** "](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="b0390-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   <span data-ttu-id="b0390-127">" [**Fivefileex**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)" – Verwenden von " [ **muvefilewithprogress** "](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="b0390-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   [<span data-ttu-id="b0390-128">**ReplaceFile**</span><span class="sxs-lookup"><span data-stu-id="b0390-128">**ReplaceFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

<span data-ttu-id="b0390-129">Weitere Informationen finden Sie unter e [/a-Abschluss-/Abbruch Richtlinien](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="b0390-129">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

## <a name="canceling-asynchronous-io"></a><span data-ttu-id="b0390-130">Abbrechen von asynchronen e/a-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="b0390-130">Canceling Asynchronous I/O</span></span>

<span data-ttu-id="b0390-131">Sie können asynchrone e/a-Vorgänge von einem beliebigen Thread im Prozess Abbrechen, der den e/a-Vorgang ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b0390-131">You can cancel asynchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="b0390-132">Sie müssen das Handle angeben, für das die e/a-Vorgänge ausgeführt wurden, und optional die überlappende Struktur, die zum Ausführen des e/a-Vorgangs verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b0390-132">You must specify the handle which the I/O was performed on and, optionally, the overlapped structure that was used to perform the I/O.</span></span> <span data-ttu-id="b0390-133">Sie können ermitteln, ob der Abbruch aufgetreten ist, indem Sie den in der überlappenden Struktur oder im Vervollständigungs Rückruf zurückgegebenen Status überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b0390-133">You can determine if the cancel occurred by examining the status returned in the overlapped structure or in the completion callback.</span></span> <span data-ttu-id="b0390-134">Der Status " **Fehler \_ Vorgang \_ abgebrochen** " gibt an, dass der Vorgang abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="b0390-134">A status of **ERROR\_OPERATION\_ABORTED** indicates that the operation was canceled.</span></span>

<span data-ttu-id="b0390-135">Das folgende Beispiel zeigt eine Routine, die eine Zeitüberschreitung annimmt und einen Lesevorgang versucht, mit der [**CancelIoEx**](cancelioex-func.md) -Funktion abgebrochen wird, wenn das Timeout abläuft.</span><span class="sxs-lookup"><span data-stu-id="b0390-135">The following example shows a routine that takes a timeout and attempts a read operation, canceling it with the [**CancelIoEx**](cancelioex-func.md) function if the timeout expires.</span></span>


```C++
#include <windows.h>

BOOL DoCancelableRead(HANDLE hFile,
                 LPVOID lpBuffer,
                 DWORD nNumberOfBytesToRead,
                 LPDWORD lpNumberOfBytesRead,
                 LPOVERLAPPED lpOverlapped,
                 DWORD dwTimeout,
                 LPBOOL pbCancelCalled)
//
// Parameters:
//
//      hFile - An open handle to a readable file or device.
//
//      lpBuffer - A pointer to the buffer to store the data being read.
//
//      nNumberOfBytesToRead - The number of bytes to read from the file or 
//          device. Must be less than or equal to the actual size of
//          the buffer referenced by lpBuffer.
//
//      lpNumberOfBytesRead - A pointer to a DWORD to receive the number 
//          of bytes read after all I/O is complete or canceled.
//
//      lpOverlapped - A pointer to a preconfigured OVERLAPPED structure that
//          has a valid hEvent.
//          If the caller does not properly initialize this structure, this
//          routine will fail.
//
//      dwTimeout - The desired time-out, in milliseconds, for the I/O read.
//          After this time expires, the I/O is canceled.
// 
//      pbCancelCalled - A pointer to a Boolean to notify the caller if this
//          routine attempted to perform an I/O cancel.
//
// Return Value:
//
//      TRUE on success, FALSE on failure.
//
{
    BOOL result;
    DWORD waitTimer;
    BOOL bIoComplete = FALSE;
    const DWORD PollInterval = 100; // milliseconds

    // Initialize "out" parameters
    *pbCancelCalled = FALSE;
    *lpNumberOfBytesRead = 0;

    // Perform the I/O, in this case a read operation.
    result = ReadFile(hFile,
                  lpBuffer,
                  nNumberOfBytesToRead,
                  lpNumberOfBytesRead,
                  lpOverlapped );

    if (result == FALSE) 
    {
        if (GetLastError() != ERROR_IO_PENDING) 
        {
            // The function call failed. ToDo: Error logging and recovery.
            return FALSE; 
        }
    } 
    else 
    {
        // The I/O completed, done.
        return TRUE;
    }
        
    // The I/O is pending, so wait and see if the call times out.
    // If so, cancel the I/O using the CancelIoEx function.

    for (waitTimer = 0; waitTimer < dwTimeout; waitTimer += PollInterval)
    {
        result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, FALSE );
        if (result == FALSE)
        {
            if (GetLastError() != ERROR_IO_PENDING)
            {
                // The function call failed. ToDo: Error logging and recovery.
                return FALSE;
            }
            Sleep(PollInterval);
        }
        else
        {
            bIoComplete = TRUE;
            break;
        }
    }

    if (bIoComplete == FALSE) 
    {
        result = CancelIoEx( hFile, lpOverlapped );
        
        *pbCancelCalled = TRUE;

        if (result == TRUE || GetLastError() != ERROR_NOT_FOUND) 
        {
            // Wait for the I/O subsystem to acknowledge our cancellation.
            // Depending on the timing of the calls, the I/O might complete with a
            // cancellation status, or it might complete normally (if the ReadFile was
            // in the process of completing at the time CancelIoEx was called, or if
            // the device does not support cancellation).
            // This call specifies TRUE for the bWait parameter, which will block
            // until the I/O either completes or is canceled, thus resuming execution, 
            // provided the underlying device driver and associated hardware are functioning 
            // properly. If there is a problem with the driver it is better to stop 
            // responding here than to try to continue while masking the problem.

            result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, TRUE );

            // ToDo: check result and log errors. 
        }
    }

    return result;
}
```



## <a name="canceling-synchronous-io"></a><span data-ttu-id="b0390-136">Synchrone e/a wird abgebrochen</span><span class="sxs-lookup"><span data-stu-id="b0390-136">Canceling Synchronous I/O</span></span>

<span data-ttu-id="b0390-137">Sie können synchrone e/a-Vorgänge von einem beliebigen Thread im Prozess Abbrechen, der den e/a-Vorgang ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b0390-137">You can cancel synchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="b0390-138">Sie müssen das Handle für den Thread angeben, der gerade den e/a-Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="b0390-138">You must specify the handle to the thread which is currently performing the I/O operation.</span></span>

<span data-ttu-id="b0390-139">Das folgende Beispiel zeigt zwei Routinen:</span><span class="sxs-lookup"><span data-stu-id="b0390-139">The following example shows two routines:</span></span>

-   <span data-ttu-id="b0390-140">Die **SynchronousIoWorker** -Funktion ist ein Arbeits Thread, der einige synchrone Datei-e/a implementiert, beginnend mit einem Aufrufen der Funktion " [**foratefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ".</span><span class="sxs-lookup"><span data-stu-id="b0390-140">The **SynchronousIoWorker** function is a worker thread that implements some synchronous file I/O, starting with a call to the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="b0390-141">Wenn die Routine erfolgreich ist, kann auf die Routine zusätzliche Vorgänge folgen, die hier nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b0390-141">If the routine is successful, the routine can be followed by additional operations, which are not included here.</span></span> <span data-ttu-id="b0390-142">Die globale Variable *gCompletionStatus* kann verwendet werden, um zu bestimmen, ob alle Vorgänge erfolgreich waren oder ob ein Vorgang fehlgeschlagen ist oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="b0390-142">The global variable *gCompletionStatus* can be used to determine whether all operations succeeded or whether an operation failed or was canceled.</span></span> <span data-ttu-id="b0390-143">Die globale Variable *dwOperationInProgress* gibt an, ob die Datei-e/a noch in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="b0390-143">The global variable *dwOperationInProgress* indicates whether file I/O is still in progress.</span></span>

    <span data-ttu-id="b0390-144">**Hinweis**  In diesem Beispiel könnte der UI-Thread auch überprüfen, ob der Arbeits Thread vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b0390-144">**Note**  In this example, the UI thread could also check for the existence of the worker thread.</span></span>

    <span data-ttu-id="b0390-145">Weitere manuelle Überprüfungen, die hier nicht enthalten sind, sind in der **SynchronousIoWorker** -Funktion erforderlich, um sicherzustellen, dass die restlichen Vorgänge abgebrochen werden, wenn der Abbruch während der kurzen Zeiträume zwischen Datei-e/a-Aufrufen angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="b0390-145">Additional manual checks, which are not included here, are required in the **SynchronousIoWorker** function is to ensure that if the cancellation was requested during the brief periods between file I/O calls, the rest of the operations will be canceled.</span></span>

-   <span data-ttu-id="b0390-146">Die **MainUIThreadMessageHandler** -Funktion simuliert den Nachrichten Handler in der Fenster Prozedur eines UI-Threads.</span><span class="sxs-lookup"><span data-stu-id="b0390-146">The **MainUIThreadMessageHandler** function simulates the message handler within a UI thread's window procedure.</span></span> <span data-ttu-id="b0390-147">Der Benutzer fordert einen Satz synchroner Datei Vorgänge an, indem er auf ein Steuerelement klickt, das eine benutzerdefinierte Fenster Meldung generiert (in dem durch **WM \_ mysyncops** markierten Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="b0390-147">The user requests a set of synchronous file operations by clicking a control, which generates a user-defined window message, (in the section marked by **WM\_MYSYNCOPS**).</span></span> <span data-ttu-id="b0390-148">Dadurch wird ein neuer Thread mit der Funktion "-Funktion" erstellt, die dann die **SynchronousIoWorker** **-Funktion startet** .</span><span class="sxs-lookup"><span data-stu-id="b0390-148">This creates a new thread using the **CreateFileThread** function, which then starts the **SynchronousIoWorker** function is.</span></span> <span data-ttu-id="b0390-149">Der UI-Thread verarbeitet weiterhin Nachrichten, während der Arbeits Thread die angeforderte e/a-Vorgänge ausführt.</span><span class="sxs-lookup"><span data-stu-id="b0390-149">The UI thread continues to process messages while the worker thread performs the requested I/O.</span></span> <span data-ttu-id="b0390-150">Wenn sich der Benutzer entscheidet, die unerledigten Vorgänge abzubrechen (in der Regel durch Klicken auf die Schaltfläche Abbrechen), ruft die Routine (in dem durch **WM \_ mycancel** markierten Abschnitt) die Funktion [**CancelSynchronousIo**](cancelsynchronousio-func.md) mithilfe des Thread Handles auf, das von der Funktion " **deatefilethread** " ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b0390-150">If the user decides to cancel the unfinished operations (typically by clicking a cancel button), the routine (in the section marked by **WM\_MYCANCEL**) calls the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function using the thread handle returned by the **CreateFileThread** function.</span></span> <span data-ttu-id="b0390-151">Die Funktion **CancelSynchronousIo** gibt unmittelbar nach dem Abbruch Versuch zurück.</span><span class="sxs-lookup"><span data-stu-id="b0390-151">The **CancelSynchronousIo** function returns immediately after the cancellation attempt.</span></span> <span data-ttu-id="b0390-152">Schließlich kann der Benutzer oder die Anwendung später einen anderen Vorgang anfordern, der davon abhängt, ob die Datei Vorgänge abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="b0390-152">Finally, the user or application may later request some other operation that depends on whether the file operations have completed.</span></span> <span data-ttu-id="b0390-153">In diesem Fall überprüft die Routine (in dem durch WM- **\_ Prozess** markierten Abschnitt) zuerst, ob die Vorgänge abgeschlossen sind, und führt dann die Bereinigungs Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="b0390-153">In this case, the routine (in the section marked by **WM\_PROCESSDATA**) first verifies that the operations have completed and then executes the clean-up operations.</span></span>

    <span data-ttu-id="b0390-154">**Hinweis**  Da in diesem Beispiel der Abbruch an beliebiger Stelle in der Sequenz von Vorgängen auftreten könnte, kann es erforderlich sein, dass der Aufrufer sicherstellt, dass der Zustand konsistent oder zumindest verstanden wird, bevor er fortfahren kann.</span><span class="sxs-lookup"><span data-stu-id="b0390-154">**Note**  In this example, since the cancellation could have occurred anywhere in the sequence of operations, it may be necessary for the caller to ensure that the state is consistent, or at least understood, before proceeding.</span></span>


```C++
// User-defined codes for the message-pump, which is outside the scope 
// of this sample. Windows messaging and message pumps are well-documented
// elsewhere.
#define WM_MYSYNCOPS    1
#define WM_MYCANCEL     2
#define WM_PROCESSDATA  3

VOID SynchronousIoWorker( VOID *pv )
{
    LPCSTR lpFileName = (LPCSTR)pv;
    HANDLE hFile;
    g_dwOperationInProgress = TRUE;    
    g_CompletionStatus = ERROR_SUCCESS;
     
    hFile = CreateFileA(lpFileName,
                        GENERIC_READ,
                        0,
                        NULL,
                        OPEN_EXISTING,
                        0,
                        NULL);


    if (hFile != INVALID_HANDLE_VALUE) 
    {
        BOOL result = TRUE;
        // TODO: CreateFile succeeded. 
        // Insert your code to make more synchronous calls with hFile.
        // The result variable is assumed to act as the error flag here,
        // but can be whatever your code needs.
        
        if (result == FALSE) 
        {
            // An operation failed or was canceled. If it was canceled,
            // GetLastError() returns ERROR_OPERATION_ABORTED.

            g_CompletionStatus = GetLastError();            
        }
             
        CloseHandle(hFile);
    } 
    else 
    {
        // CreateFile failed or was canceled. If it was canceled,
        // GetLastError() returns ERROR_OPERATION_ABORTED.
        g_CompletionStatus = GetLastError();
    }

    g_dwOperationInProgress = FALSE;
}  


LRESULT
CALLBACK
MainUIThreadMessageHandler(HWND hwnd,
                           UINT uMsg,
                           WPARAM wParam,
                           LPARAM lParam)
{
    UNREFERENCED_PARAMETER(hwnd);
    UNREFERENCED_PARAMETER(wParam);
    UNREFERENCED_PARAMETER(lParam);
    HANDLE syncThread = INVALID_HANDLE_VALUE;

    //  Insert your initializations here.

    switch (uMsg) 
    {
        // User requested an operation on a file.  Insert your code to 
        // retrieve filename from parameters.
        case WM_MYSYNCOPS:    
            syncThread = CreateThread(
                          NULL,
                          0,
                          (LPTHREAD_START_ROUTINE)SynchronousIoWorker,
                          &g_lpFileName,
                          0,
                          NULL);

            if (syncThread == INVALID_HANDLE_VALUE) 
            {
                // Insert your code to handle the failure.
            }
        break;
    
        // User clicked a cancel button.
        case WM_MYCANCEL:
            if (syncThread != INVALID_HANDLE_VALUE) 
            {
                CancelSynchronousIo(syncThread);
            }
        break;

        // User requested other operations.
        case WM_PROCESSDATA:
            if (!g_dwOperationInProgress) 
            {
                if (g_CompletionStatus == ERROR_OPERATION_ABORTED) 
                {
                    // Insert your cleanup code here.
                } 
                else
                {
                    // Insert code to handle other cases.
                }
            }
        break;
    } 

    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="b0390-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0390-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0390-156">Synchrone und asynchrone e/a</span><span class="sxs-lookup"><span data-stu-id="b0390-156">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



