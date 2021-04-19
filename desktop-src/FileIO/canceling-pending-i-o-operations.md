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
# <a name="canceling-pending-io-operations"></a>Abbrechen von ausstehenden e/a-Vorgängen

Benutzern das Abbrechen von e/a-Anforderungen, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden. Wenn z. b. ein aufrufungs Vorgang der [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) -Funktion blockiert ist, weil der-Vorgang an ein sehr langsames Gerät gerichtet ist, wird durch Abbrechen des Aufrufes wiederholt, mit neuen Parametern, ohne die Anwendung zu beenden.

Windows Vista erweitert die Abbruch Funktionen und bietet Unterstützung für das Abbrechen synchroner Vorgänge.

**Hinweis**  Durch Aufrufen der [**CancelIoEx**](cancelioex-func.md) -Funktion wird nicht garantiert, dass ein e/a-Vorgang abgebrochen wird. der Treiber, der den Vorgang verarbeitet, muss den Abbruch unterstützen, und der Vorgang muss sich in einem Zustand befinden, der abgebrochen werden kann.

## <a name="cancellation-considerations"></a>Überlegungen zum Abbruch

Beachten Sie beim Programmieren von Abbruch aufrufen Folgendes:

-   Es gibt keine Garantie, dass zugrunde liegende Treiber den Abbruch ordnungsgemäß unterstützen.
-   Wenn beim Abbrechen der asynchronen e/a-Vorgänge keine überlappende Struktur an die [**CancelIoEx**](cancelioex-func.md) -Funktion übergeben wird, versucht die Funktion, alle ausstehenden e/a-Vorgänge für die Datei für alle Threads im Prozess abzubrechen. Jeder Thread wird einzeln verarbeitet, sodass nach der Verarbeitung eines Threads möglicherweise ein weiterer e/a-Vorgang für die Datei gestartet wird, bevor für alle anderen Threads die e/a-Vorgänge für die Datei abgebrochen wurden, was zu Synchronisierungs Problemen geführt hat.
-   Verwenden Sie beim Abbrechen von asynchronen e/a-Vorgängen keine überlappenden Strukturen mit gezielter Abbruch. Sobald die e/a-Operation abgeschlossen ist (entweder erfolgreich oder mit dem Status "abgebrochen"), wird die überlappende Struktur nicht mehr vom System verwendet und kann wieder verwendet werden.
-   Beim Abbrechen synchroner e/a versucht der Aufruf der [**CancelSynchronousIo**](cancelsynchronousio-func.md) -Funktion, jeden aktuellen synchronen Aufruf für den Thread abzubrechen. Sie müssen sicherstellen, dass die Synchronisierung der Aufrufe korrekt ist. der falsche Aufruf in einer Reihe von aufrufen könnte abgebrochen werden. Wenn beispielsweise die Funktion **CancelSynchronousIo** für einen synchronen Vorgang, x, aufgerufen wird, wird der Vorgang Y nur gestartet, nachdem der Vorgang x abgeschlossen wurde (normalerweise oder mit einem Fehler). Wenn der Thread, der Vorgang x aufgerufen hat, einen anderen synchronen Aufruf von x startet, kann der Abbruch Aufruf diese neue e/a-Anforderung unterbrechen.
-   Beachten Sie beim Abbrechen synchroner e/a, dass eine Racebedingung immer vorhanden sein kann, wenn ein Thread von verschiedenen Teilen einer Anwendung gemeinsam genutzt wird, z. b. mit einem Thread Pool Thread.

## <a name="operations-that-cannot-be-canceled"></a>Vorgänge, die nicht abgebrochen werden können

Einige Funktionen können mit der Funktion [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)oder [**CancelSynchronousIo**](cancelsynchronousio-func.md) nicht abgebrochen werden. Einige dieser Funktionen wurden erweitert, um einen Abbruch zuzulassen (z. b. die [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) -Funktion), und Sie sollten diese stattdessen verwenden. Zusätzlich zur Unterstützung von Abbruch verfügen diese Funktionen auch über integrierte Rückrufe, mit denen Sie den Fortschritt des Vorgangs verfolgen können. Die folgenden Funktionen unterstützen keinen Abbruch:

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)– Verwenden von [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   " [**Muvefile**](/windows/desktop/api/WinBase/nf-winbase-movefile)" – Verwenden von " [ **muvefilewithprogress** "](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   " [**Fivefileex**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)" – Verwenden von " [ **muvefilewithprogress** "](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Weitere Informationen finden Sie unter e [/a-Abschluss-/Abbruch Richtlinien](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

## <a name="canceling-asynchronous-io"></a>Abbrechen von asynchronen e/a-Vorgängen

Sie können asynchrone e/a-Vorgänge von einem beliebigen Thread im Prozess Abbrechen, der den e/a-Vorgang ausgegeben hat. Sie müssen das Handle angeben, für das die e/a-Vorgänge ausgeführt wurden, und optional die überlappende Struktur, die zum Ausführen des e/a-Vorgangs verwendet wurde. Sie können ermitteln, ob der Abbruch aufgetreten ist, indem Sie den in der überlappenden Struktur oder im Vervollständigungs Rückruf zurückgegebenen Status überprüfen. Der Status " **Fehler \_ Vorgang \_ abgebrochen** " gibt an, dass der Vorgang abgebrochen wurde.

Das folgende Beispiel zeigt eine Routine, die eine Zeitüberschreitung annimmt und einen Lesevorgang versucht, mit der [**CancelIoEx**](cancelioex-func.md) -Funktion abgebrochen wird, wenn das Timeout abläuft.


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



## <a name="canceling-synchronous-io"></a>Synchrone e/a wird abgebrochen

Sie können synchrone e/a-Vorgänge von einem beliebigen Thread im Prozess Abbrechen, der den e/a-Vorgang ausgegeben hat. Sie müssen das Handle für den Thread angeben, der gerade den e/a-Vorgang ausführt.

Das folgende Beispiel zeigt zwei Routinen:

-   Die **SynchronousIoWorker** -Funktion ist ein Arbeits Thread, der einige synchrone Datei-e/a implementiert, beginnend mit einem Aufrufen der Funktion " [**foratefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ". Wenn die Routine erfolgreich ist, kann auf die Routine zusätzliche Vorgänge folgen, die hier nicht enthalten sind. Die globale Variable *gCompletionStatus* kann verwendet werden, um zu bestimmen, ob alle Vorgänge erfolgreich waren oder ob ein Vorgang fehlgeschlagen ist oder abgebrochen wurde. Die globale Variable *dwOperationInProgress* gibt an, ob die Datei-e/a noch in Bearbeitung ist.

    **Hinweis**  In diesem Beispiel könnte der UI-Thread auch überprüfen, ob der Arbeits Thread vorhanden ist.

    Weitere manuelle Überprüfungen, die hier nicht enthalten sind, sind in der **SynchronousIoWorker** -Funktion erforderlich, um sicherzustellen, dass die restlichen Vorgänge abgebrochen werden, wenn der Abbruch während der kurzen Zeiträume zwischen Datei-e/a-Aufrufen angefordert wurde.

-   Die **MainUIThreadMessageHandler** -Funktion simuliert den Nachrichten Handler in der Fenster Prozedur eines UI-Threads. Der Benutzer fordert einen Satz synchroner Datei Vorgänge an, indem er auf ein Steuerelement klickt, das eine benutzerdefinierte Fenster Meldung generiert (in dem durch **WM \_ mysyncops** markierten Abschnitt). Dadurch wird ein neuer Thread mit der Funktion "-Funktion" erstellt, die dann die **SynchronousIoWorker** **-Funktion startet** . Der UI-Thread verarbeitet weiterhin Nachrichten, während der Arbeits Thread die angeforderte e/a-Vorgänge ausführt. Wenn sich der Benutzer entscheidet, die unerledigten Vorgänge abzubrechen (in der Regel durch Klicken auf die Schaltfläche Abbrechen), ruft die Routine (in dem durch **WM \_ mycancel** markierten Abschnitt) die Funktion [**CancelSynchronousIo**](cancelsynchronousio-func.md) mithilfe des Thread Handles auf, das von der Funktion " **deatefilethread** " ausgegeben wurde. Die Funktion **CancelSynchronousIo** gibt unmittelbar nach dem Abbruch Versuch zurück. Schließlich kann der Benutzer oder die Anwendung später einen anderen Vorgang anfordern, der davon abhängt, ob die Datei Vorgänge abgeschlossen wurden. In diesem Fall überprüft die Routine (in dem durch WM- **\_ Prozess** markierten Abschnitt) zuerst, ob die Vorgänge abgeschlossen sind, und führt dann die Bereinigungs Vorgänge aus.

    **Hinweis**  Da in diesem Beispiel der Abbruch an beliebiger Stelle in der Sequenz von Vorgängen auftreten könnte, kann es erforderlich sein, dass der Aufrufer sicherstellt, dass der Zustand konsistent oder zumindest verstanden wird, bevor er fortfahren kann.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Synchrone und asynchrone e/a](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



