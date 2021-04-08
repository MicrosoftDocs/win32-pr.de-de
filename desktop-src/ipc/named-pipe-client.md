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
# <a name="named-pipe-client"></a><span data-ttu-id="32182-103">Named Pipe-Client</span><span class="sxs-lookup"><span data-stu-id="32182-103">Named Pipe Client</span></span>

<span data-ttu-id="32182-104">Ein Named Pipe Client [**verwendet die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion", um ein Handle für eine Named Pipe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="32182-104">A named pipe client uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a named pipe.</span></span> <span data-ttu-id="32182-105">Wenn die Pipe vorhanden ist, aber alle Ihre Instanzen ausgelastet sind, gibt " **kreatefile** " **einen ungültigen \_ handle- \_ Wert** zurück, und die Funktion " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt die \_ fehlerpipe \_ ausgelastet</span><span class="sxs-lookup"><span data-stu-id="32182-105">If the pipe exists but all of its instances are busy, **CreateFile** returns **INVALID\_HANDLE\_VALUE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_PIPE\_BUSY.</span></span> <span data-ttu-id="32182-106">In diesem Fall verwendet der Named Pipe Client die [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) -Funktion, um zu warten, bis eine Instanz des Named Pipe verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="32182-106">When this happens, the named pipe client uses the [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) function to wait for an instance of the named pipe to become available.</span></span>

<span data-ttu-id="32182-107">Die Funktion " [**deatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " schlägt fehl, wenn der angegebene Zugriff mit dem angegebenen Zugriff (Duplex, ausgehend oder eingehend) nicht kompatibel ist, als der Server die Pipe erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="32182-107">The [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function fails if the access specified is incompatible with the access specified (duplex, outbound, or inbound) when the server created the pipe.</span></span> <span data-ttu-id="32182-108">Bei einer Duplex Pipe kann der Client Lese-, Schreib-oder Lese-/Schreibzugriff angeben. bei einer ausgehenden Pipe (Server mit Leseberechtigung) muss der Client schreibgeschützten Zugriff angeben. für eine eingehende Pipe (Schreib geschützter Server) muss der Client nur Lesezugriff angeben.</span><span class="sxs-lookup"><span data-stu-id="32182-108">For a duplex pipe, the client can specify read, write, or read/write access; for an outbound pipe (write-only server), the client must specify read-only access; and for an inbound pipe (read-only server), the client must specify write-only access.</span></span>

<span data-ttu-id="32182-109">Das von " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " zurückgegebene Handle ist standardmäßig auf den Byte-/Lesemodus, den blockierenden Wartemodus, den überlappenden Modus deaktiviert und den Schreibmodus deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="32182-109">The handle returned by [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) defaults to byte-read mode, blocking-wait mode, overlapped mode disabled, and write-through mode disabled.</span></span> <span data-ttu-id="32182-110">Der Pipe-Client kann den überlappenden Modus mithilfe von " **kreatefile** " aktivieren, indem er das überlappende \_ Dateiflag angibt oder den \_ Schreibmodus aktiviert, indem das \_ Dateiflag " \_ Write \_ through" angegeben wird</span><span class="sxs-lookup"><span data-stu-id="32182-110">The pipe client can use **CreateFile** to enable overlapped mode by specifying FILE\_FLAG\_OVERLAPPED or to enable write-through mode by specifying FILE\_FLAG\_WRITE\_THROUGH.</span></span> <span data-ttu-id="32182-111">Der Client kann die [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) -Funktion verwenden, um den Modus für die nicht Blockierung zu aktivieren, indem Pipe \_ nowait angegeben wird, oder um den Nachrichten Lese Modus durch Angeben der Pipe-lesemodusnachricht \_ \_</span><span class="sxs-lookup"><span data-stu-id="32182-111">The client can use the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function to enable nonblocking mode by specifying PIPE\_NOWAIT or to enable message-read mode by specifying PIPE\_READMODE\_MESSAGE.</span></span>

<span data-ttu-id="32182-112">Das folgende Beispiel zeigt einen Pipe-Client, der eine Named Pipe öffnet, das Pipehandle auf den Nachrichten Lese Modus festlegt, die Funktion " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " verwendet, um eine Anforderung an den Server zu senden, und die Funktion " [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " verwendet, um die Antwort des Servers zu lesen.</span><span class="sxs-lookup"><span data-stu-id="32182-112">The following example shows a pipe client that opens a named pipe, sets the pipe handle to message-read mode, uses the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to send a request to the server, and uses the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function to read the server's reply.</span></span> <span data-ttu-id="32182-113">Dieser Pipeclient kann mit jedem der Nachrichten Typen Server verwendet werden, die am Ende dieses Themas aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="32182-113">This pipe client can be used with any of the message-type servers listed at the bottom of this topic.</span></span> <span data-ttu-id="32182-114">Bei einem Bytetyp Server schlägt dieser Pipe-Client jedoch fehl, wenn [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) aufgerufen wird, um in den Nachrichten Lese Modus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="32182-114">With a byte-type server, however, this pipe client fails when it calls [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) to change to message-read mode.</span></span> <span data-ttu-id="32182-115">Da der Client aus der Pipe im Nachrichten Lese Modus liest, ist es möglich, dass der **ReadFile** -Vorgang nach dem Lesen einer partiellen Nachricht 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="32182-115">Because the client is reading from the pipe in message-read mode, it is possible for the **ReadFile** operation to return zero after reading a partial message.</span></span> <span data-ttu-id="32182-116">Dies geschieht, wenn die Nachricht größer als der Lese Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="32182-116">This happens when the message is larger than the read buffer.</span></span> <span data-ttu-id="32182-117">In dieser Situation gibt [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fehlerhafte \_ \_ Daten zurück, und der Client kann den Rest der Nachricht mit zusätzlichen Aufrufen von " **Infofile**" lesen.</span><span class="sxs-lookup"><span data-stu-id="32182-117">In this situation, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA, and the client can read the remainder of the message using additional calls to **ReadFile**.</span></span>

<span data-ttu-id="32182-118">Dieser pipenclient kann mit einem der unter "Siehe auch" aufgeführten Pipeserver verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32182-118">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="32182-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32182-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32182-120">Multithreaded Pipe-Server</span><span class="sxs-lookup"><span data-stu-id="32182-120">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="32182-121">Named Pipe-Server mit überlappenden e/a-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="32182-121">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="32182-122">Named Pipe-Server mithilfe von Vervollständigungs Routinen</span><span class="sxs-lookup"><span data-stu-id="32182-122">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
