---
description: Code Beispiel zeigt einen Pipe-Client, der eine Named Pipe öffnet, das Pipehandle auf den Nachrichten Lese Modus festlegt, die Funktion "Write file" verwendet, um eine Anforderung an den Server zu senden, und die Funktion "Read File" zum Lesen der Serverantwort verwendet.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Named Pipe-Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6318edd7d5b41c701e3112188a896c0529338805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861923"
---
# <a name="named-pipe-client"></a>Named Pipe-Client

Ein Named Pipe Client [**verwendet die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion", um ein Handle für eine Named Pipe zu öffnen. Wenn die Pipe vorhanden ist, aber alle Ihre Instanzen ausgelastet sind, gibt " **kreatefile** " **einen ungültigen \_ handle- \_ Wert** zurück, und die Funktion " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt die \_ fehlerpipe \_ ausgelastet In diesem Fall verwendet der Named Pipe Client die [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) -Funktion, um zu warten, bis eine Instanz des Named Pipe verfügbar wird.

Die Funktion " [**deatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " schlägt fehl, wenn der angegebene Zugriff mit dem angegebenen Zugriff (Duplex, ausgehend oder eingehend) nicht kompatibel ist, als der Server die Pipe erstellt hat. Bei einer Duplex Pipe kann der Client Lese-, Schreib-oder Lese-/Schreibzugriff angeben. bei einer ausgehenden Pipe (Server mit Leseberechtigung) muss der Client schreibgeschützten Zugriff angeben. für eine eingehende Pipe (Schreib geschützter Server) muss der Client nur Lesezugriff angeben.

Das von " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " zurückgegebene Handle ist standardmäßig auf den Byte-/Lesemodus, den blockierenden Wartemodus, den überlappenden Modus deaktiviert und den Schreibmodus deaktiviert. Der Pipe-Client kann den überlappenden Modus mithilfe von " **kreatefile** " aktivieren, indem er das überlappende \_ Dateiflag angibt oder den \_ Schreibmodus aktiviert, indem das \_ Dateiflag " \_ Write \_ through" angegeben wird Der Client kann die [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) -Funktion verwenden, um den Modus für die nicht Blockierung zu aktivieren, indem Pipe \_ nowait angegeben wird, oder um den Nachrichten Lese Modus durch Angeben der Pipe-lesemodusnachricht \_ \_

Das folgende Beispiel zeigt einen Pipe-Client, der eine Named Pipe öffnet, das Pipehandle auf den Nachrichten Lese Modus festlegt, die Funktion " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " verwendet, um eine Anforderung an den Server zu senden, und die Funktion " [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " verwendet, um die Antwort des Servers zu lesen. Dieser Pipeclient kann mit jedem der Nachrichten Typen Server verwendet werden, die am Ende dieses Themas aufgelistet sind. Bei einem Bytetyp Server schlägt dieser Pipe-Client jedoch fehl, wenn [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) aufgerufen wird, um in den Nachrichten Lese Modus zu wechseln. Da der Client aus der Pipe im Nachrichten Lese Modus liest, ist es möglich, dass der **ReadFile** -Vorgang nach dem Lesen einer partiellen Nachricht 0 (null) zurückgibt. Dies geschieht, wenn die Nachricht größer als der Lese Puffer ist. In dieser Situation gibt [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fehlerhafte \_ \_ Daten zurück, und der Client kann den Rest der Nachricht mit zusätzlichen Aufrufen von " **Infofile**" lesen.

Dieser pipenclient kann mit einem der unter "Siehe auch" aufgeführten Pipeserver verwendet werden.


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

[Multithreaded Pipe-Server](multithreaded-pipe-server.md)
</dt> <dt>

[Named Pipe-Server mit überlappenden e/a-Vorgängen](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Named Pipe-Server mithilfe von Vervollständigungs Routinen](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
