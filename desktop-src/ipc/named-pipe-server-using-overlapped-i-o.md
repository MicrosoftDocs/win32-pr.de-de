---
description: Code Beispiel für einen Single Thread-Pipe-Server, der überlappende Vorgänge verwendet, um gleichzeitige Verbindungen mit mehreren Pipe-Clients zu bedienen.
ms.assetid: c0ac70cc-4ab9-47e5-b0e6-c0b373d16b25
title: Named Pipe-Server mit überlappenden e/a-Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f9134582a50c2053893cf6ee4908e447e3cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959889"
---
# <a name="named-pipe-server-using-overlapped-io"></a>Named Pipe-Server mit überlappenden e/a-Vorgängen

Im folgenden finden Sie ein Beispiel für einen Single Thread-Pipe-Server, der überlappende Vorgänge verwendet, um gleichzeitige Verbindungen mit mehreren Pipe-Clients zu bedienen. Der Pipeserver erstellt eine Fixed-Anzahl von Pipe-Instanzen. Jede Pipeinstanz kann mit einem separaten Pipe-Client verbunden werden. Wenn ein Pipe-Client seine Pipe-Instanz nicht mehr verwendet, trennt der Server die Verbindung mit dem Client und verwendet die Pipe-Instanz erneut, um eine Verbindung mit einem neuen Client herzustellen. Dieser Pipeserver kann mit dem in [Named Pipe-Client](named-pipe-client.md)beschriebenen Pipe-Client verwendet werden.

Die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur wird in jedem [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)-, [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)-und [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) -Vorgang auf der Pipe-Instanz als Parameter angegeben. Obwohl das Beispiel gleichzeitige Vorgänge für verschiedene Pipe-Instanzen anzeigt, werden gleichzeitige Vorgänge für eine einzelne Pipe-Instanz vermieden, indem das Ereignis Objekt in der **über** Lapp enden Struktur verwendet wird. Da dasselbe Ereignis Objekt für Lese-, Schreib-und Verbindungs Vorgänge für jede Instanz verwendet wird, gibt es keine Möglichkeit, zu ermitteln, welcher Vorgang abgeschlossen hat, dass das Ereignis auf den signalisierten Zustand für gleichzeitige Vorgänge mit derselben Pipe-Instanz festgelegt wurde.

Die Ereignis Handles für jede Pipe-Instanz werden in einem Array gespeichert, das an die [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) -Funktion übergeben wird. Diese Funktion wartet auf die Signalisierung eines der Ereignisse und gibt den Array Index des Ereignisses zurück, das bewirkt hat, dass der Warte Vorgang beendet wurde. Im Beispiel in diesem Thema wird dieser Array Index verwendet, um eine Struktur abzurufen, die Informationen für die Pipe-Instanz enthält. Der Server verwendet das **fpdingio** -Member der-Struktur, um nachzuverfolgen, ob der letzte e/a-Vorgang für die Instanz aussteht. hierfür ist ein Aufrufen der [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion erforderlich. Der Server verwendet den **dwstate** -Member der-Struktur, um den nächsten Vorgang zu bestimmen, der für die Pipe-Instanz ausgeführt werden muss.

Überlappende [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)-, [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)-und [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) -Vorgänge können bis zum Zeitpunkt der Rückgabe der Funktion abgeschlossen werden. Andernfalls, wenn der Vorgang aussteht, wird das Ereignis Objekt in der angegebenen [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur auf den nicht signalisierten Zustand festgelegt, bevor die Funktion zurückgegeben wird. Wenn der ausstehende Vorgang abgeschlossen ist, legt das System den Status des Ereignis Objekts auf "signalisiert" fest. Der Status des Ereignis Objekts wird nicht geändert, wenn der Vorgang abgeschlossen ist, bevor die Funktion zurückgegeben wird.

Da im Beispiel Ereignis Objekte mit manuellem Zurücksetzen verwendet werden, wird der Status eines Ereignis Objekts von der [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) -Funktion nicht in "nicht signalisiert" geändert. Dies ist wichtig, da das Beispiel von den Ereignis Objekten abhängig ist, die im signalisierten Zustand verbleiben, außer wenn es einen ausstehenden Vorgang gibt.

Wenn der Vorgang bereits abgeschlossen ist, wenn " [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)", " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)" oder " [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) " zurückgegeben wird, gibt der Rückgabewert der Funktion das Ergebnis an. Für Lese-und Schreibvorgänge wird auch die Anzahl der übertragenen Bytes zurückgegeben. Wenn der Vorgang noch aussteht, gibt die Funktion **ReadFile**, **Write File** oder **connectnamedpipe** den Wert 0 (null) zurück, und die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt die Fehler-e/a steht \_ \_ aus. Verwenden Sie in diesem Fall die [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion, um die Ergebnisse abzurufen, nachdem der Vorgang abgeschlossen wurde. **Gedeverlappedresult** gibt nur die Ergebnisse von ausstehenden Vorgängen zurück. Die Ergebnisse von Vorgängen, die abgeschlossen wurden, bevor die überlappende **ReadFile**-, **Write File**-oder **connectnamedpipe** -Funktion zurückgegeben wurde, werden nicht gemeldet.

Vor dem Trennen der Verbindung mit einem Client müssen Sie auf ein Signal warten, das angibt, dass der Client beendet wurde. (Das Leeren der Datei Puffer würde den Zweck der überlappenden e/a-Vorgänge zunichte machen, da der Löschvorgang die Ausführung des Server Threads blockieren würde, während er darauf wartet, dass der Client die Pipe leert.) In diesem Beispiel ist das Signal der Fehler, der ausgelöst wird, wenn versucht wird, aus der Pipe zu lesen, nachdem der Pipe-Client das Handle geschlossen hat.


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
 
#define CONNECTING_STATE 0 
#define READING_STATE 1 
#define WRITING_STATE 2 
#define INSTANCES 4 
#define PIPE_TIMEOUT 5000
#define BUFSIZE 4096
 
typedef struct 
{ 
   OVERLAPPED oOverlap; 
   HANDLE hPipeInst; 
   TCHAR chRequest[BUFSIZE]; 
   DWORD cbRead;
   TCHAR chReply[BUFSIZE];
   DWORD cbToWrite; 
   DWORD dwState; 
   BOOL fPendingIO; 
} PIPEINST, *LPPIPEINST; 
 
 
VOID DisconnectAndReconnect(DWORD); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 
 
PIPEINST Pipe[INSTANCES]; 
HANDLE hEvents[INSTANCES]; 
 
int _tmain(VOID) 
{ 
   DWORD i, dwWait, cbRet, dwErr; 
   BOOL fSuccess; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
// The initial loop creates several instances of a named pipe 
// along with an event object for each instance.  An 
// overlapped ConnectNamedPipe operation is started for 
// each instance. 
 
   for (i = 0; i < INSTANCES; i++) 
   { 
 
   // Create an event object for this instance. 
 
      hEvents[i] = CreateEvent( 
         NULL,    // default security attribute 
         TRUE,    // manual-reset event 
         TRUE,    // initial state = signaled 
         NULL);   // unnamed event object 

      if (hEvents[i] == NULL) 
      {
         printf("CreateEvent failed with %d.\n", GetLastError()); 
         return 0;
      }
 
      Pipe[i].oOverlap.hEvent = hEvents[i]; 
 
      Pipe[i].hPipeInst = CreateNamedPipe( 
         lpszPipename,            // pipe name 
         PIPE_ACCESS_DUPLEX |     // read/write access 
         FILE_FLAG_OVERLAPPED,    // overlapped mode 
         PIPE_TYPE_MESSAGE |      // message-type pipe 
         PIPE_READMODE_MESSAGE |  // message-read mode 
         PIPE_WAIT,               // blocking mode 
         INSTANCES,               // number of instances 
         BUFSIZE*sizeof(TCHAR),   // output buffer size 
         BUFSIZE*sizeof(TCHAR),   // input buffer size 
         PIPE_TIMEOUT,            // client time-out 
         NULL);                   // default security attributes 

      if (Pipe[i].hPipeInst == INVALID_HANDLE_VALUE) 
      {
         printf("CreateNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
 
   // Call the subroutine to connect to the new client
 
      Pipe[i].fPendingIO = ConnectToNewClient( 
         Pipe[i].hPipeInst, 
         &Pipe[i].oOverlap); 
 
      Pipe[i].dwState = Pipe[i].fPendingIO ? 
         CONNECTING_STATE : // still connecting 
         READING_STATE;     // ready to read 
   } 
 
   while (1) 
   { 
   // Wait for the event object to be signaled, indicating 
   // completion of an overlapped read, write, or 
   // connect operation. 
 
      dwWait = WaitForMultipleObjects( 
         INSTANCES,    // number of event objects 
         hEvents,      // array of event objects 
         FALSE,        // does not wait for all 
         INFINITE);    // waits indefinitely 
 
   // dwWait shows which pipe completed the operation. 
 
      i = dwWait - WAIT_OBJECT_0;  // determines which pipe 
      if (i < 0 || i > (INSTANCES - 1)) 
      {
         printf("Index out of range.\n"); 
         return 0;
      }
 
   // Get the result if the operation was pending. 
 
      if (Pipe[i].fPendingIO) 
      { 
         fSuccess = GetOverlappedResult( 
            Pipe[i].hPipeInst, // handle to pipe 
            &Pipe[i].oOverlap, // OVERLAPPED structure 
            &cbRet,            // bytes transferred 
            FALSE);            // do not wait 
 
         switch (Pipe[i].dwState) 
         { 
         // Pending connect operation 
            case CONNECTING_STATE: 
               if (! fSuccess) 
               {
                   printf("Error %d.\n", GetLastError()); 
                   return 0;
               }
               Pipe[i].dwState = READING_STATE; 
               break; 
 
         // Pending read operation 
            case READING_STATE: 
               if (! fSuccess || cbRet == 0) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               }
               Pipe[i].cbRead = cbRet;
               Pipe[i].dwState = WRITING_STATE; 
               break; 
 
         // Pending write operation 
            case WRITING_STATE: 
               if (! fSuccess || cbRet != Pipe[i].cbToWrite) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               } 
               Pipe[i].dwState = READING_STATE; 
               break; 
 
            default: 
            {
               printf("Invalid pipe state.\n"); 
               return 0;
            }
         }  
      } 
 
   // The pipe state determines which operation to do next. 
 
      switch (Pipe[i].dwState) 
      { 
      // READING_STATE: 
      // The pipe instance is connected to the client 
      // and is ready to read a request from the client. 
 
         case READING_STATE: 
            fSuccess = ReadFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chRequest, 
               BUFSIZE*sizeof(TCHAR), 
               &Pipe[i].cbRead, 
               &Pipe[i].oOverlap); 
 
         // The read operation completed successfully. 
 
            if (fSuccess && Pipe[i].cbRead != 0) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = WRITING_STATE; 
               continue; 
            } 
 
         // The read operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
      // WRITING_STATE: 
      // The request was successfully read from the client. 
      // Get the reply data and write it to the client. 
 
         case WRITING_STATE: 
            GetAnswerToRequest(&Pipe[i]); 
 
            fSuccess = WriteFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chReply, 
               Pipe[i].cbToWrite, 
               &cbRet, 
               &Pipe[i].oOverlap); 
 
         // The write operation completed successfully. 
 
            if (fSuccess && cbRet == Pipe[i].cbToWrite) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = READING_STATE; 
               continue; 
            } 
 
         // The write operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
         default: 
         {
            printf("Invalid pipe state.\n"); 
            return 0;
         }
      } 
  } 
 
  return 0; 
} 
 
 
// DisconnectAndReconnect(DWORD) 
// This function is called when an error occurs or when the client 
// closes its handle to the pipe. Disconnect from this client, then 
// call ConnectNamedPipe to wait for another client to connect. 
 
VOID DisconnectAndReconnect(DWORD i) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(Pipe[i].hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Call a subroutine to connect to the new client. 
 
   Pipe[i].fPendingIO = ConnectToNewClient( 
      Pipe[i].hPipeInst, 
      &Pipe[i].oOverlap); 
 
   Pipe[i].dwState = Pipe[i].fPendingIO ? 
      CONNECTING_STATE : // still connecting 
      READING_STATE;     // ready to read 
} 
 
// ConnectToNewClient(HANDLE, LPOVERLAPPED) 
// This function is called to start an overlapped connect operation. 
// It returns TRUE if an operation is pending or FALSE if the 
// connection has been completed. 
 
BOOL ConnectToNewClient(HANDLE hPipe, LPOVERLAPPED lpo) 
{ 
   BOOL fConnected, fPendingIO = FALSE; 
 
// Start an overlapped connection for this pipe instance. 
   fConnected = ConnectNamedPipe(hPipe, lpo); 
 
// Overlapped ConnectNamedPipe should return zero. 
   if (fConnected) 
   {
      printf("ConnectNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   switch (GetLastError()) 
   { 
   // The overlapped connection in progress. 
      case ERROR_IO_PENDING: 
         fPendingIO = TRUE; 
         break; 
 
   // Client is already connected, so signal an event. 
 
      case ERROR_PIPE_CONNECTED: 
         if (SetEvent(lpo->hEvent)) 
            break; 
 
   // If an error occurs during the connect operation... 
      default: 
      {
         printf("ConnectNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
   } 
 
   return fPendingIO; 
}

VOID GetAnswerToRequest(LPPIPEINST pipe)
{
   _tprintf( TEXT("[%d] %s\n"), pipe->hPipeInst, pipe->chRequest);
   StringCchCopy( pipe->chReply, BUFSIZE, TEXT("Default answer from server") );
   pipe->cbToWrite = (lstrlen(pipe->chReply)+1)*sizeof(TCHAR);
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Named Pipe-Client](named-pipe-client.md)
</dt> </dl>

 

 
