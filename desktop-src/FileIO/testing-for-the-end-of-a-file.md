---
description: Beispielcode, der zeigt, wie während eines synchronen Lesevorgang und während eines asynchronen Lesevorganges auf das Dateiende testt wird.
ms.assetid: 93fa9e29-1ff1-496d-9551-99ae88ba7253
title: Testen auf das Ende einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b345a0b908e88cfbb98129bc05350c2e265db8bc943d10151a89a17a10fc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950999"
---
# <a name="testing-for-the-end-of-a-file"></a>Testen auf das Ende einer Datei

Die [**ReadFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) überprüft auf synchrone und asynchrone Lesevorgänge anders auf die End-of-File-Bedingung (End-of-File Condition, EOF). Wenn ein synchroner Lesevorgang an das Ende einer Datei geht, gibt **ReadFile** **TRUE** zurück und legt die Variable, auf die der *lpNumberOfBytesRead-Parameter* zeigt, auf 0 (null) fest. Bei einem asynchronen Lesevorgang kann das Ende einer Datei während des initiierenden Aufrufs von **ReadFile** oder bei nachfolgenden asynchronen Vorgängen auftreten, wenn der Dateizeiger programmgesteuert über das Ende der Datei hinaus erweitert wird.

Das folgende C++-Beispiel zeigt, wie sie während eines synchronen Lesevorganges auf das Ende einer Datei testen.


```C++
  // Attempt a synchronous read operation.
  bResult = ReadFile(hFile, &inBuffer, nBytesToRead, &nBytesRead, NULL);

  // Check for eof.
  if (bResult &&  nBytesRead == 0) 
   {
    // at the end of the file
   }
```



Der Test für das Dateiende während eines asynchronen Lesevorgang ist etwas schwieriger als bei einem ähnlichen synchronen Lesevorgang. Der End-of-File-Indikator für asynchrone Lesevorgänge ist, wenn [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) **FALSE** und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **ERROR HANDLE \_ \_ EOF zurückgibt.**

Das folgende C++-Beispiel zeigt, wie sie während eines asynchronen Lesevorganges auf das Dateiende testen.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUF_SIZE (61)

LPCTSTR ErrorMessage( DWORD error ) 

// Routine Description:
//      Retrieve the system error message for the last-error code
{ 

    LPVOID lpMsgBuf;

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        error,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    return((LPCTSTR)lpMsgBuf);
}

void GoDoSomethingElse(void)

// Routine Description:
//     Placeholder to demo when async I/O might want to do
//     other processing.
{
    printf("Inside GoDoSomethingElse()\n");
}

DWORD AsyncTestForEnd( HANDLE hEvent, HANDLE hFile )

// Routine Description:
//      Demonstrate async ReadFile operations that can catch
//      End-of-file conditions. Unless the operation completes
//      synchronously or the file size happens to be an exact
//      multiple of BUF_SIZE, this routine will eventually force
//      an EOF condition on any file.

// Parameters:
//      hEvent - pre-made manual-reset event.
//
//      hFile - pre-opened file handle, overlapped.
//
//      inBuffer - the buffer to read in the data to.
//
//      nBytesToRead - how much to read (usually the buffer size).

// Return Value:
//      Number of bytes read.
{
    char inBuffer[BUF_SIZE];
    DWORD nBytesToRead      = BUF_SIZE;
    DWORD dwBytesRead       = 0;
    DWORD dwFileSize        = GetFileSize(hFile, NULL);
    OVERLAPPED stOverlapped = {0};

    DWORD dwError  = 0;
    LPCTSTR errMsg = NULL;

    BOOL bResult   = FALSE;
    BOOL bContinue = TRUE;

    // Set up overlapped structure event. Other members are already 
    // initialized to zero.
    stOverlapped.hEvent = hEvent; 

    // This is an intentionally brute-force loop to force the EOF trigger.
    // A properly designed loop for this simple file read would use the
    // GetFileSize API to regulate execution. However, the purpose here
    // is to demonstrate how to trigger the EOF error and handle it.

    while(bContinue)
    {
        // Default to ending the loop.
        bContinue = FALSE;
        
        // Attempt an asynchronous read operation.
        bResult = ReadFile(hFile,
                           inBuffer,
                           nBytesToRead,
                           &dwBytesRead,
                           &stOverlapped); 
     
        dwError = GetLastError();

        // Check for a problem or pending operation. 
        if (!bResult) 
        { 
            switch (dwError) 
            { 
                 
                case ERROR_HANDLE_EOF:
                {
                    printf("\nReadFile returned FALSE and EOF condition, async EOF not triggered.\n");
                    break;
                }
                case ERROR_IO_PENDING: 
                { 
                    BOOL bPending=TRUE;

                    // Loop until the I/O is complete, that is: the overlapped 
                    // event is signaled.

                    while( bPending )
                    {
                        bPending = FALSE;
                        
                        // Pending asynchronous I/O, do something else
                        // and re-check overlapped structure.
                        printf("\nReadFile operation is pending\n");
     
                        // Do something else then come back to check. 
                        GoDoSomethingElse(); 
     
                        // Check the result of the asynchronous read
                        // without waiting (forth parameter FALSE). 
                        bResult = GetOverlappedResult(hFile,
                                                      &stOverlapped,
                                                      &dwBytesRead,
                                                      FALSE) ; 
     
                        if (!bResult) 
                        { 
                            switch (dwError = GetLastError()) 
                            { 
                                case ERROR_HANDLE_EOF: 
                                { 
                                    // Handle an end of file
                                    printf("GetOverlappedResult found EOF\n");
                                    break;
                                } 

                                case ERROR_IO_INCOMPLETE:
                                {
                                    // Operation is still pending, allow while loop
                                    // to loop again after printing a little progress.
                                    printf("GetOverlappedResult I/O Incomplete\n");
                                    bPending = TRUE;
                                    bContinue = TRUE;
                                    break;
                                }

                                default:
                                {
                                    // Decode any other errors codes.
                                    errMsg = ErrorMessage(dwError);
                                    _tprintf(TEXT("GetOverlappedResult failed (%d): %s\n"), 
                                        dwError, errMsg);
                                    LocalFree((LPVOID)errMsg);
                                }
                            }
                        } 
                        else
                        {
                            printf("ReadFile operation completed\n");

                            // Manual-reset event should be reset since it is now signaled.
                            ResetEvent(stOverlapped.hEvent);
                        }
                    }
                    break;
                }

                default:
                {
                    // Decode any other errors codes.
                    errMsg = ErrorMessage(dwError);
                    printf("ReadFile GLE unhandled (%d): %s\n", dwError, errMsg); 
                    LocalFree((LPVOID)errMsg);
                    break;
                }
            }
        }
        else
        {
            // EOF demo did not trigger for the given file.
            // Note that system caching may cause this condition on most files
            // after the first read. CreateFile can be called using the
            // FILE_FLAG_NOBUFFERING parameter but it would require reads are
            // always aligned to the volume's sector boundary. This is beyond
            // the scope of this example. See comments in the main() function.

            printf("ReadFile completed synchronously\n");
        }

        // The following operation assumes the file is not extremely large, otherwise 
        // logic would need to be included to adequately account for very large
        // files and manipulate the OffsetHigh member of the OVERLAPPED structure.

        stOverlapped.Offset += dwBytesRead;
        if ( stOverlapped.Offset < dwFileSize )             
            bContinue = TRUE;
    }

    return stOverlapped.Offset;
}

int __cdecl _tmain(int argc, TCHAR *argv[])

// To force an EOF condition, execute this application specifying a
// zero-length file. This is because the offset (file pointer) must be
// at or beyond the end-of-file marker when ReadFile is called. For
// more information, see the comments for the AsyncTestForEnd routine.

{
    HANDLE hEvent;
    HANDLE hFile;
    DWORD dwReturnValue;

    printf("\n");
    if( argc != 2 )
    {
        printf("ERROR:\tIncorrect number of arguments\n\n");
        printf("%s <file_name>\n", argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],                // file to open
                       GENERIC_READ,           // open for reading
                       FILE_SHARE_READ,        // share for reading
                       NULL,                   // default security
                       OPEN_EXISTING,          // existing file only
                       FILE_FLAG_OVERLAPPED,   // overlapped operation
                       NULL);                  // no attr. template
 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DWORD dwError = GetLastError();
        LPCTSTR errMsg = ErrorMessage(dwError);
        printf("Could not open file (%d): %s\n", dwError, errMsg); 
        LocalFree((LPVOID)errMsg);
        return; 
    }

    hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

    if (hEvent == NULL) 
    { 
        DWORD dwError = GetLastError();
        LPCTSTR errMsg = ErrorMessage(dwError);
        printf("Could not CreateEvent: %d %s\n", dwError, errMsg); 
        LocalFree((LPVOID)errMsg);
        return; 
    }

    dwReturnValue = AsyncTestForEnd(hEvent, hFile);

    printf( "\nRead complete. Bytes read: %d\n", dwReturnValue);

    CloseHandle(hFile);
    CloseHandle(hEvent);
}
```



Die Ausgabe dieses Beispielcodes lautet wie folgt.

``` syntax
ReadFile operation is pending
Inside GoDoSomethingElse()
GetOverlappedResult I/O Incomplete

ReadFile operation is pending
Inside GoDoSomethingElse()
ReadFile operation completed

Complete. Bytes read: 541
```

 

 
