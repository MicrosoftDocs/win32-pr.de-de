---
description: Bei einer Named Pipe Transaktion handelt es sich um eine Client/Server-Kommunikation, in der ein Schreibvorgang und ein Lesevorgang in einem einzelnen Netzwerk Vorgang kombiniert werden. Transaktionen verbessern die Leistung der Netzwerkkommunikation zwischen einem Client und einem Remote Server.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Transaktionen auf Named Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489039b92b65f57cefc71c5d78a01b1824b1418a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530110"
---
# <a name="transactions-on-named-pipes"></a><span data-ttu-id="9d275-104">Transaktionen auf Named Pipes</span><span class="sxs-lookup"><span data-stu-id="9d275-104">Transactions on Named Pipes</span></span>

<span data-ttu-id="9d275-105">Bei einer Named Pipe Transaktion handelt es sich um eine Client/Server-Kommunikation, in der ein Schreibvorgang und ein Lesevorgang in einem einzelnen Netzwerk Vorgang kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9d275-105">A named pipe transaction is a client/server communication that combines a write operation and a read operation into a single network operation.</span></span> <span data-ttu-id="9d275-106">Eine Transaktion kann nur für eine Duplex-und Nachrichtentyp Pipe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d275-106">A transaction can be used only on a duplex, message-type pipe.</span></span> <span data-ttu-id="9d275-107">Transaktionen verbessern die Leistung der Netzwerkkommunikation zwischen einem Client und einem Remote Server.</span><span class="sxs-lookup"><span data-stu-id="9d275-107">Transactions improve the performance of network communications between a client and a remote server.</span></span> <span data-ttu-id="9d275-108">Prozesse können die Funktionen [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) und [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) verwenden, um Named Pipe Transaktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9d275-108">Processes can use the [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) and [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) functions to perform named pipe transactions.</span></span>

<span data-ttu-id="9d275-109">Die [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) -Funktion wird am häufigsten von einem Pipe-Client verwendet, um eine Anforderungs Nachricht an den Named Pipe Server zu schreiben und die Antwortnachricht des Servers zu lesen.</span><span class="sxs-lookup"><span data-stu-id="9d275-109">The [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) function is most commonly used by a pipe client to write a request message to the named pipe server and read the server's response message.</span></span> <span data-ttu-id="9d275-110">Der Pipe-Client muss generischen \_ Lesezugriff auf den generischen \| Schreibzugriff angeben, \_ Wenn er das Pipehandle durch Aufrufen der [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -Funktion öffnet.</span><span class="sxs-lookup"><span data-stu-id="9d275-110">The pipe client must specify GENERIC\_READ \| GENERIC\_WRITE access when it opens its pipe handle by calling the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="9d275-111">Anschließend legt der Pipe-Client das Pipehandle auf den Nachrichten Lese Modus fest, indem er die [**setnamedpipegsstate**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="9d275-111">Then, the pipe client sets the pipe handle to message-read mode by calling the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function.</span></span> <span data-ttu-id="9d275-112">Wenn der im Aufrufe von **transactnamedpipe** angegebene Lese Puffer nicht groß genug ist, um die gesamte vom Server geschriebene Nachricht aufzunehmen, gibt die Funktion 0 (null) zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt Fehler \_ Weitere \_ Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="9d275-112">If the read buffer specified in the call to **TransactNamedPipe** is not large enough to hold the entire message written by the server, the function returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="9d275-113">Der Client kann den Rest der Nachricht lesen, indem er entweder die Funktion " [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)", " [**infofileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)" oder " [**Peer-NamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) " anruft.</span><span class="sxs-lookup"><span data-stu-id="9d275-113">The client can read the remainder of the message by calling either the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), or [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) function.</span></span>

<span data-ttu-id="9d275-114">[**Transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) wird in der Regel von Pipe-Clients aufgerufen, kann aber auch von einem Pipeserver verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d275-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) is typically called by pipe clients, but can also be used by a pipe server.</span></span>

<span data-ttu-id="9d275-115">Das folgende Beispiel zeigt einen Pipe-Client mithilfe von [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="9d275-115">The following example shows a pipe client using [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span></span> <span data-ttu-id="9d275-116">Dieser pipenclient kann mit einem der unter "Siehe auch" aufgeführten Pipeserver verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d275-116">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


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



<span data-ttu-id="9d275-117">Ein Pipe-Client [**verwendet callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) [**, um die Funktions**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)Aufrufe "anfügen", " [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) " (falls erforderlich), " [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)" und " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) " in einem einzigen Aufruf zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="9d275-117">A pipe client uses [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) to combine the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (if necessary), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function calls into a single call.</span></span> <span data-ttu-id="9d275-118">Da das Pipehandle vor der Rückgabe der Funktion geschlossen wird, gehen alle zusätzlichen Bytes in der Nachricht verloren, wenn die Nachricht größer als die angegebene Größe des Lese Puffers ist.</span><span class="sxs-lookup"><span data-stu-id="9d275-118">Because the pipe handle is closed before the function returns, any additional bytes in the message are lost if the message is larger than the specified size of the read buffer.</span></span> <span data-ttu-id="9d275-119">Im folgenden Beispiel wird das vorherige Beispiel so umgeschrieben, dass **callnamedpipe** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d275-119">The following example is the previous example rewritten to use **CallNamedPipe**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9d275-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d275-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d275-121">Multithreaded Pipe-Server</span><span class="sxs-lookup"><span data-stu-id="9d275-121">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="9d275-122">Named Pipe-Server mit überlappenden e/a-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="9d275-122">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="9d275-123">Named Pipe-Server mithilfe von Vervollständigungs Routinen</span><span class="sxs-lookup"><span data-stu-id="9d275-123">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
