---
description: Eine Named Pipe-Transaktion ist eine Client-/Serverkommunikation, die einen Schreibvorgang und einen Lesevorgang in einem einzigen Netzwerkvorgang kombiniert. Transaktionen verbessern die Leistung der Netzwerkkommunikation zwischen einem Client und einem Remoteserver.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Transaktionen für Named Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524f9ae453eb958efd59d8ef6ee5adfda12dd2701e4c719be51299e2873913dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963900"
---
# <a name="transactions-on-named-pipes"></a>Transaktionen für Named Pipes

Eine Named Pipe-Transaktion ist eine Client-/Serverkommunikation, die einen Schreibvorgang und einen Lesevorgang in einem einzigen Netzwerkvorgang kombiniert. Eine Transaktion kann nur für eine Duplexpipe vom Typ "Message" verwendet werden. Transaktionen verbessern die Leistung der Netzwerkkommunikation zwischen einem Client und einem Remoteserver. Prozesse können die [**Funktionen TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) und [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) verwenden, um Named Pipe-Transaktionen auszuführen.

Die [**TransactNamedPipe-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) wird am häufigsten von einem Pipeclient verwendet, um eine Anforderungsnachricht auf den Named Pipe-Server zu schreiben und die Antwortnachricht des Servers zu lesen. Der Pipeclient muss GENERIC \_ READ \| GENERIC \_ WRITE-Zugriff angeben, wenn er sein Pipehandle öffnet, indem er die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aufruft. Anschließend legt der Pipeclient das Pipehandle auf den Nachrichtenlesemodus fest, indem er die [**SetNamedPipeHandleState-Funktion aufruft.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) Wenn der im Aufruf von **TransactNamedPipe** angegebene Lesepuffer nicht groß genug ist, um die gesamte vom Server geschriebene Nachricht zu speichern, gibt die Funktion 0 (null) zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ MORE DATA \_ zurück. Der Client kann den Rest der Nachricht lesen, indem er entweder die [**ReadFile-,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**ReadFileEx-**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)oder [**PeekNamedPipe-Funktion aufruft.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)

[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) wird in der Regel von Pipeclients aufgerufen, kann aber auch von einem Pipeserver verwendet werden.

Das folgende Beispiel zeigt einen Pipeclient mit [**TransactNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) Dieser Pipeclient kann mit jedem der unter Siehe auch aufgeführten Pipeserver verwendet werden.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
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
         printf("Could not open pipe\n"); 
         return 0;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
      if (! WaitNamedPipe(lpszPipename, 20000) ) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
  } 
 
   // The pipe connected; change to message-read mode. 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if (!fSuccess) 
   {
      printf("SetNamedPipeHandleState failed.\n"); 
      return 0;
   }
 
   // Send a message to the pipe server and read the response. 
   fSuccess = TransactNamedPipe( 
      hPipe,                  // pipe handle 
      lpszWrite,              // message to server
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply
      BUFSIZE*sizeof(TCHAR),  // size of read buffer
      &cbRead,                // bytes read
      NULL);                  // not overlapped 

   if (!fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
   {
      printf("TransactNamedPipe failed.\n"); 
      return 0;
   }
 
   while(1)
   { 
      _tprintf(TEXT("%s\n"), chReadBuf);

      // Break if TransactNamedPipe or ReadFile is successful
      if(fSuccess)
         break;

      // Read from the pipe if there is more data in the message.
      fSuccess = ReadFile( 
         hPipe,      // pipe handle 
         chReadBuf,  // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 

      // Exit if an error other than ERROR_MORE_DATA occurs.
      if( !fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
         break;
      else _tprintf( TEXT("%s\n"), chReadBuf); 
   }

   _getch(); 

   CloseHandle(hPipe); 
 
   return 0; 
}
```



Ein Pipeclient verwendet [**CallNamedPipe,**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) um die Funktionsaufrufe [**CreateFile,**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (falls erforderlich), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)und [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) in einem einzigen Aufruf zu kombinieren. Da das Pipehandle geschlossen wird, bevor die Funktion zurückgegeben wird, gehen alle zusätzlichen Bytes in der Nachricht verloren, wenn die Nachricht größer als die angegebene Größe des Lesepuffers ist. Das folgende Beispiel ist das vorherige Beispiel, das zur Verwendung von **CallNamedPipe** umgeschrieben wurde.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   fSuccess = CallNamedPipe( 
      lpszPipename,        // pipe name 
      lpszWrite,           // message to server 
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply 
      BUFSIZE*sizeof(TCHAR),  // size of read buffer 
      &cbRead,                // number of bytes read 
      20000);                 // waits for 20 seconds 
 
   if (fSuccess || GetLastError() == ERROR_MORE_DATA) 
   { 
      _tprintf( TEXT("%s\n"), chReadBuf ); 
    
      // The pipe is closed; no more data can be read. 
 
      if (! fSuccess) 
      {
         printf("\nExtra data in message was lost\n"); 
      }
   }
 
   _getch(); 

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

 

 
