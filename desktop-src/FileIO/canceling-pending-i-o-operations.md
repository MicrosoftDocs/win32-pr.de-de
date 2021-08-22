---
description: Wenn Benutzer E/A-Anforderungen abbrechen können, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Abbrechen ausstehender E/A-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ca0f938420888934dccb28c9837bdff5dd8515bbdeeb1b3acf4078ae558ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534120"
---
# <a name="canceling-pending-io-operations"></a>Abbrechen ausstehender E/A-Vorgänge

Wenn Benutzer E/A-Anforderungen abbrechen können, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden. Wenn z. B. ein Aufruf der [**OpenFile-Funktion**](/windows/desktop/api/WinBase/nf-winbase-openfile) blockiert wird, weil der Aufruf an ein sehr langsames Gerät erfolgt, ermöglicht das Abbrechen den erneuten Aufruf mit neuen Parametern, ohne die Anwendung zu beenden.

Windows Vista erweitert die Abbruchfunktionen und bietet Unterstützung für das Abbrechen synchroner Vorgänge.

**Hinweis:**  Das Aufrufen [**der CancelIoEx-Funktion**](cancelioex-func.md) garantiert nicht, dass ein E/A-Vorgang abgebrochen wird. Der Treiber, der den Vorgang behandeln soll, muss einen Abbruch unterstützen, und der Vorgang muss sich in einem Zustand befindet, der abgebrochen werden kann.

## <a name="cancellation-considerations"></a>Abbruchüberlegungen

Beachten Sie beim Programmieren von Abbruchaufrufen die folgenden Überlegungen:

-   Es gibt keine Garantie dafür, dass zugrunde liegende Treiber den Abbruch ordnungsgemäß unterstützen.
-   Wenn beim Abbrechen der asynchronen E/A keine überlappende Struktur für die [**CancelIoEx-Funktion**](cancelioex-func.md) bereitgestellt wird, versucht die Funktion, alle ausstehenden E/A-Vorgänge für die Datei in allen Threads im Prozess abzubricht. Jeder Thread wird einzeln verarbeitet, sodass nach der Verarbeitung eines Threads möglicherweise eine weitere E/A für die Datei gestartet wird, bevor alle anderen Threads ihre E/A für die Datei abgebrochen haben, was zu Synchronisierungsproblemen führt.
-   Wenn Sie asynchrone E/A abbrechen, sollten Sie überlappende Strukturen nicht mit einem gezielten Abbruch wiederverwenden. Sobald der E/A-Vorgang abgeschlossen ist (entweder erfolgreich oder mit einem abgebrochenen Status), wird die überlappende Struktur nicht mehr vom System verwendet und kann wiederverwendet werden.
-   Beim Abbrechen synchroner E/A versucht der Aufruf der [**CancelSynchronousIo-Funktion,**](cancelsynchronousio-func.md) jeden aktuellen synchronen Aufruf des Threads abzubricht. Sie müssen darauf achten, dass die Synchronisierung der Aufrufe korrekt ist. Der falsche Aufruf in einer Reihe von Aufrufen könnte abgebrochen werden. Wenn beispielsweise die **CancelSynchronousIo-Funktion** für einen synchronen Vorgang X aufgerufen wird, wird Vorgang Y erst gestartet, nachdem dieser Vorgang X abgeschlossen wurde (normalerweise oder mit einem Fehler). Wenn der Thread, der Vorgang X aufgerufen hat, dann einen weiteren synchronen Aufruf von X startet, kann der Abbruchaufruf diese neue E/A-Anforderung unterbrechen.
-   Beachten Sie beim Abbrechen synchroner E/A-Ereignisse, dass immer dann eine Racebedingung vorhanden sein kann, wenn ein Thread von verschiedenen Teilen einer Anwendung gemeinsam genutzt wird, z. B. mit einem Threadpoolthread.

## <a name="operations-that-cannot-be-canceled"></a>Vorgänge, die nicht abgebrochen werden können

Einige Funktionen können nicht mithilfe der [**CancelIo-,**](cancelio.md) [**CancelIoEx-**](cancelioex-func.md)oder [**CancelSynchronousIo-Funktion abgebrochen**](cancelsynchronousio-func.md) werden. Einige dieser Funktionen wurden erweitert, um einen Abbruch zu ermöglichen (z. B. die [**CopyFileEx-Funktion),**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) und Sie sollten diese stattdessen verwenden. Zusätzlich zur Unterstützung des Abbruchs verfügen diese Funktionen auch über integrierte Rückrufe, die Sie beim Nachverfolgen des Vorgangsfortschritts unterstützen. Die folgenden Funktionen unterstützen keinen Abbruch:

-   [**CopyFile –**](/windows/desktop/api/WinBase/nf-winbase-copyfile) [ **CopyFileEx verwenden**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)– [ **MoveFileWithProgress verwenden**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**MoveFileEx –**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) [ **MoveFileWithProgress verwenden**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Weitere Informationen finden Sie unter [E/A-Vervollständigungs-/Abbruchrichtlinien.](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)

## <a name="canceling-asynchronous-io"></a>Abbrechen von asynchronen E/A-Vorgängen

Sie können die asynchrone E/A von jedem Thread im Prozess abbrechen, der den E/A-Vorgang ausgegeben hat. Sie müssen das Handle angeben, für das die E/A ausgeführt wurde, und optional die überlappende Struktur, die zum Ausführen der E/A verwendet wurde. Sie können ermitteln, ob der Abbricht aufgetreten ist, indem Sie den Status untersuchen, der in der überlappenden Struktur oder im Abschlussrückruf zurückgegeben wird. Der Status **ERROR \_ OPERATION \_ ABORTED gibt** an, dass der Vorgang abgebrochen wurde.

Das folgende Beispiel zeigt eine Routine, die ein Timeout erfordert und einen Lesevorgang versucht und ihn mit der [**CancelIoEx-Funktion**](cancelioex-func.md) abbricht, wenn das Timeout abläuft.


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



## <a name="canceling-synchronous-io"></a>Abbrechen synchroner E/A

Sie können synchrone E/A von jedem Thread im Prozess abbrechen, der den E/A-Vorgang ausgegeben hat. Sie müssen das Handle für den Thread angeben, der derzeit den E/A-Vorgang vor sich hat.

Das folgende Beispiel zeigt zwei Routinen:

-   Die **SynchronousIoWorker-Funktion** ist ein Arbeitsthread, der synchrone Datei-E/A implementiert, beginnend mit einem Aufruf der [**CreateFile-Funktion.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Wenn die Routine erfolgreich ist, können auf die Routine zusätzliche Vorgänge folgen, die hier nicht enthalten sind. Die globale Variable *gCompletionStatus* kann verwendet werden, um zu bestimmen, ob alle Vorgänge erfolgreich waren oder ob ein Vorgang fehlgeschlagen ist oder abgebrochen wurde. Die globale Variable *dwOperationInProgress gibt* an, ob die Datei-E/A noch in Bearbeitung ist.

    **Hinweis:**  In diesem Beispiel könnte der UI-Thread auch überprüfen, ob der Arbeitsthread existiert.

    Zusätzliche manuelle Überprüfungen, die hier nicht enthalten sind, sind in der **SynchronousIoWorker-Funktion** erforderlich, um sicherzustellen, dass die restlichen Vorgänge abgebrochen werden, wenn der Abbruch während der kurzen Zeiträume zwischen Datei-E/A-Aufrufen angefordert wurde.

-   Die **MainUIThreadMessageHandler-Funktion** simuliert den Meldungshandler innerhalb der Fensterprozedur eines UI-Threads. Der Benutzer fordert einen Satz synchroner Dateivorgänge an, indem er auf ein Steuerelement klickt, das eine benutzerdefinierte Fenstermeldung generiert (in dem abschnitt, der durch **WM \_ MYSYNCOPS gekennzeichnet ist).** Dadurch wird ein neuer Thread mithilfe der **CreateFileThread-Funktion** erstellt, die dann die **SynchronousIoWorker-Funktion** startet. Der UI-Thread wird weiterhin Nachrichten verarbeiten, während der Arbeitsthread die angeforderte E/A ausführt. Wenn der Benutzer beschließt, die nicht abgeschlossenen Vorgänge abzubricht (in der Regel durch Klicken auf eine Schaltfläche zum Abbrechen), ruft die Routine (in dem von **WM \_ MYCANCEL** markierten Abschnitt) die [**CancelSynchronousIo-Funktion**](cancelsynchronousio-func.md) mithilfe des von der **CreateFileThread-Funktion** zurückgegebenen Threadhandles auf. Die **CancelSynchronousIo-Funktion** wird unmittelbar nach dem Abbruchversuch zurückgegeben. Schließlich kann der Benutzer oder die Anwendung später einen anderen Vorgang anfordern, der davon abhängt, ob die Dateivorgänge abgeschlossen wurden. In diesem Fall überprüft die Routine (in dem durch **WM \_ PROCESSDATA** markierten Abschnitt), ob die Vorgänge abgeschlossen wurden, und führt dann die Bereinigungsvorgänge aus.

    **Hinweis:**  Da der Abbruch in diesem Beispiel an einer beliebigen Stelle in der Abfolge von Vorgängen hätte ausgeführt werden können, muss der Aufrufer möglicherweise sicherstellen, dass der Zustand konsistent oder zumindest verstanden ist, bevor der Vorgang ausgeführt wird.


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

[Synchrone und asynchrone E/A](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



