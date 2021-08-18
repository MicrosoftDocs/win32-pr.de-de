---
description: Das Codebeispiel zeigt einen Pipeclient, der eine Named Pipe öffnet, das Pipehandle auf den Nachrichtenlesemodus festlegt, die WriteFile-Funktion verwendet, um eine Anforderung an den Server zu senden, und die ReadFile-Funktion verwendet, um die Antwort des Servers zu lesen.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Named Pipe-Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d00a3fec3e3d7df80468822d2e147cbae38f440e39fd55dafc9ed3ea2442cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695173"
---
# <a name="named-pipe-client"></a>Named Pipe-Client

Ein Named Pipe-Client verwendet die [**CreateFile-Funktion,**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) um ein Handle für eine Named Pipe zu öffnen. Wenn die Pipe vorhanden ist, aber alle zugehörigen Instanzen ausgelastet sind, gibt **CreateFile** **INVALID HANDLE \_ \_ VALUE** zurück, und die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ PIPE BUSY \_ zurück. In diesem Fall verwendet der Named Pipe-Client die [**WaitNamedPipe-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) um zu warten, bis eine Instanz der Named Pipe verfügbar wird.

Die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) schlägt fehl, wenn der angegebene Zugriff nicht mit dem Zugriff kompatibel ist, der beim Erstellen der Pipe durch den Server angegeben wurde (Duplex, ausgehend oder eingehend). Bei einer Duplexpipe kann der Client Lese-, Schreib- oder Lese-/Schreibzugriff angeben. Für eine ausgehende Pipe (schreibgeschützter Server) muss der Client schreibgeschützten Zugriff angeben. und für eine eingehende Pipe (schreibgeschützter Server) muss der Client schreibgeschützten Zugriff angeben.

Das von [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zurückgegebene Handle ist standardmäßig auf den Bytelesemodus, den Blockierungswartemodus, den überlappenden Modus deaktiviert und den Schreibmodus deaktiviert. Der Pipeclient kann **CreateFile** verwenden, um den überlappenden Modus durch Angabe von FILE \_ FLAG \_ OVERLAPPED zu aktivieren, oder um den Schreibmodus durch Angabe von FILE FLAG WRITE THROUGH zu \_ \_ \_ aktivieren. Der Client kann die [**SetNamedPipeHandleState-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) verwenden, um den Nichtblockierungsmodus durch Angabe von PIPE \_ NOWAIT zu aktivieren, oder um den Nachrichtenlesemodus durch Angabe von PIPE READMODE MESSAGE zu \_ \_ aktivieren.

Das folgende Beispiel zeigt einen Pipeclient, der eine benannte Pipe öffnet, das Pipehandle auf den Nachrichtenlesemodus festlegt, die [**WriteFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-writefile) verwendet, um eine Anforderung an den Server zu senden, und die [**ReadFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-readfile) verwendet, um die Antwort des Servers zu lesen. Dieser Pipeclient kann mit einem beliebigen Nachrichtentypserver verwendet werden, der unten in diesem Thema aufgeführt ist. Bei einem Bytetypserver schlägt dieser Pipeclient jedoch fehl, wenn [**er SetNamedPipeHandleState aufruft,**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) um in den Nachrichtenlesemodus zu wechseln. Da der Client im Nachrichtenlesemodus aus der Pipe liest, ist es möglich, dass der **ReadFile-Vorgang** nach dem Lesen einer Teilnachricht 0 (null) zurückgibt. Dies geschieht, wenn die Nachricht größer als der Lesepuffer ist. In diesem Fall gibt [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ERROR \_ MORE DATA \_ zurück, und der Client kann den Rest der Nachricht mithilfe zusätzlicher Aufrufe von **ReadFile** lesen.

Dieser Pipeclient kann mit jedem der unter Siehe auch aufgeführten Pipeserver verwendet werden.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpvMessage=TEXT("Default message from client."); 
   TCHAR  chBuf[BUFSIZE]; 
   BOOL   fSuccess = FALSE; 
   DWORD  cbRead, cbToWrite, cbWritten, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1 )
      lpvMessage = argv[1];
 
// Try to open a named pipe; wait for it, if necessary. 
 
   while (1) 
   { 
      hPipe = CreateFile( 
         lpszPipename,   // pipe name 
         GENERIC_READ |  // read and write access 
         GENERIC_WRITE, 
         0,              // no sharing 
         NULL,           // default security attributes
         OPEN_EXISTING,  // opens existing pipe 
         0,              // default attributes 
         NULL);          // no template file 
 
   // Break if the pipe handle is valid. 
 
      if (hPipe != INVALID_HANDLE_VALUE) 
         break; 
 
      // Exit if an error other than ERROR_PIPE_BUSY occurs. 
 
      if (GetLastError() != ERROR_PIPE_BUSY) 
      {
         _tprintf( TEXT("Could not open pipe. GLE=%d\n"), GetLastError() ); 
         return -1;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
 
      if ( ! WaitNamedPipe(lpszPipename, 20000)) 
      { 
         printf("Could not open pipe: 20 second wait timed out."); 
         return -1;
      } 
   } 
 
// The pipe connected; change to message-read mode. 
 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if ( ! fSuccess) 
   {
      _tprintf( TEXT("SetNamedPipeHandleState failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }
 
// Send a message to the pipe server. 
 
   cbToWrite = (lstrlen(lpvMessage)+1)*sizeof(TCHAR);
   _tprintf( TEXT("Sending %d byte message: \"%s\"\n"), cbToWrite, lpvMessage); 

   fSuccess = WriteFile( 
      hPipe,                  // pipe handle 
      lpvMessage,             // message 
      cbToWrite,              // message length 
      &cbWritten,             // bytes written 
      NULL);                  // not overlapped 

   if ( ! fSuccess) 
   {
      _tprintf( TEXT("WriteFile to pipe failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }

   printf("\nMessage sent to server, receiving reply as follows:\n");
 
   do 
   { 
   // Read from the pipe. 
 
      fSuccess = ReadFile( 
         hPipe,    // pipe handle 
         chBuf,    // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 
 
      if ( ! fSuccess && GetLastError() != ERROR_MORE_DATA )
         break; 
 
      _tprintf( TEXT("\"%s\"\n"), chBuf ); 
   } while ( ! fSuccess);  // repeat loop if ERROR_MORE_DATA 

   if ( ! fSuccess)
   {
      _tprintf( TEXT("ReadFile from pipe failed. GLE=%d\n"), GetLastError() );
      return -1;
   }

   printf("\n<End of message, press ENTER to terminate connection and exit>");
   _getch();
 
   CloseHandle(hPipe); 
 
   return 0; 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multithreadpipeserver](multithreaded-pipe-server.md)
</dt> <dt>

[Named Pipe-Server mit überlappender E/A](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Named Pipe-Server mit Vervollständigungsroutinen](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
