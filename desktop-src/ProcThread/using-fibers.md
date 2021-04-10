---
description: Im folgenden Beispiel wird veranschaulicht, wie Fibers erstellt, geplant und gelöscht werden.
ms.assetid: b09c00ae-a498-499b-ba2b-735028e9fd8f
title: Verwenden von Fibers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c25c8d9d258853990bd200a01c77be85c1fdfaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865047"
---
# <a name="using-fibers"></a><span data-ttu-id="3c19a-103">Verwenden von Fibers</span><span class="sxs-lookup"><span data-stu-id="3c19a-103">Using Fibers</span></span>

<span data-ttu-id="3c19a-104">Die Funktion " [**kreatefiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) " erstellt eine neue Fiber für einen Thread.</span><span class="sxs-lookup"><span data-stu-id="3c19a-104">The [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) function creates a new fiber for a thread.</span></span> <span data-ttu-id="3c19a-105">Der Erstellungs Thread muss die Startadresse des Codes angeben, der von der neuen Fiber ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c19a-105">The creating thread must specify the starting address of the code that the new fiber is to execute.</span></span> <span data-ttu-id="3c19a-106">In der Regel handelt es sich bei der Startadresse um den Namen einer vom Benutzer bereitgestellten Funktion.</span><span class="sxs-lookup"><span data-stu-id="3c19a-106">Typically, the starting address is the name of a user-supplied function.</span></span> <span data-ttu-id="3c19a-107">Mehrere Fibers können dieselbe Funktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c19a-107">Multiple fibers can execute the same function.</span></span>

<span data-ttu-id="3c19a-108">Im folgenden Beispiel wird veranschaulicht, wie Fibers erstellt, geplant und gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3c19a-108">The following example demonstrates how to create, schedule, and delete fibers.</span></span> <span data-ttu-id="3c19a-109">Die Fibers führen die lokal definierten Funktionen "leserfiberfunc" und "Write-fiberfunc" aus.</span><span class="sxs-lookup"><span data-stu-id="3c19a-109">The fibers execute the locally defined functions ReadFiberFunc and WriteFiberFunc.</span></span> <span data-ttu-id="3c19a-110">In diesem Beispiel wird ein Fiber basierter Datei Kopiervorgang implementiert.</span><span class="sxs-lookup"><span data-stu-id="3c19a-110">This example implements a fiber-based file copy operation.</span></span> <span data-ttu-id="3c19a-111">Wenn Sie das Beispiel ausführen, müssen Sie die Quell-und Zieldateien angeben.</span><span class="sxs-lookup"><span data-stu-id="3c19a-111">When running the example, you must specify the source and destination files.</span></span> <span data-ttu-id="3c19a-112">Beachten Sie, dass es viele weitere Möglichkeiten zum programmgesteuerten Kopieren der Datei gibt. Dieses Beispiel besteht hauptsächlich darin, die Verwendung der Fiber Funktionen zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="3c19a-112">Note that there are many other ways to copy file programmatically; this example exists primarily to illustrate the use of the fiber functions.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

VOID
__stdcall
ReadFiberFunc(LPVOID lpParameter);

VOID
__stdcall
WriteFiberFunc(LPVOID lpParameter);

void DisplayFiberInfo(void);

typedef struct
{
   DWORD dwParameter;          // DWORD parameter to fiber (unused)
   DWORD dwFiberResultCode;    // GetLastError() result code
   HANDLE hFile;               // handle to operate on
   DWORD dwBytesProcessed;     // number of bytes processed
} FIBERDATASTRUCT, *PFIBERDATASTRUCT, *LPFIBERDATASTRUCT;

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

#define BUFFER_SIZE 32768   // read/write buffer size
#define FIBER_COUNT 3       // max fibers (including primary)

#define PRIMARY_FIBER 0 // array index to primary fiber
#define READ_FIBER 1    // array index to read fiber
#define WRITE_FIBER 2   // array index to write fiber

LPVOID g_lpFiber[FIBER_COUNT];
LPBYTE g_lpBuffer;
DWORD g_dwBytesRead;

int __cdecl _tmain(int argc, TCHAR *argv[])
{
   LPFIBERDATASTRUCT fs;

   if (argc != 3)
   {
      printf("Usage: %s <SourceFile> <DestinationFile>\n", argv[0]);
      return RTN_USAGE;
   }

   //
   // Allocate storage for our fiber data structures
   //
   fs = (LPFIBERDATASTRUCT) HeapAlloc(
                              GetProcessHeap(), 0,
                              sizeof(FIBERDATASTRUCT) * FIBER_COUNT);

   if (fs == NULL)
   {
      printf("HeapAlloc error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Allocate storage for the read/write buffer
   //
   g_lpBuffer = (LPBYTE)HeapAlloc(GetProcessHeap(), 0, BUFFER_SIZE);
   if (g_lpBuffer == NULL)
   {
      printf("HeapAlloc error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Open the source file
   //
   fs[READ_FIBER].hFile = CreateFile(
                                    argv[1],
                                    GENERIC_READ,
                                    FILE_SHARE_READ,
                                    NULL,
                                    OPEN_EXISTING,
                                    FILE_FLAG_SEQUENTIAL_SCAN,
                                    NULL
                                    );

   if (fs[READ_FIBER].hFile == INVALID_HANDLE_VALUE)
   {
      printf("CreateFile error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Open the destination file
   //
   fs[WRITE_FIBER].hFile = CreateFile(
                                     argv[2],
                                     GENERIC_WRITE,
                                     0,
                                     NULL,
                                     CREATE_NEW,
                                     FILE_FLAG_SEQUENTIAL_SCAN,
                                     NULL
                                     );

   if (fs[WRITE_FIBER].hFile == INVALID_HANDLE_VALUE)
   {
      printf("CreateFile error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Convert thread to a fiber, to allow scheduling other fibers
   //
   g_lpFiber[PRIMARY_FIBER]=ConvertThreadToFiber(&fs[PRIMARY_FIBER]);

   if (g_lpFiber[PRIMARY_FIBER] == NULL)
   {
      printf("ConvertThreadToFiber error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Initialize the primary fiber data structure.  We don't use
   // the primary fiber data structure for anything in this sample.
   //
   fs[PRIMARY_FIBER].dwParameter = 0;
   fs[PRIMARY_FIBER].dwFiberResultCode = 0;
   fs[PRIMARY_FIBER].hFile = INVALID_HANDLE_VALUE;

   //
   // Create the Read fiber
   //
   g_lpFiber[READ_FIBER]=CreateFiber(0,ReadFiberFunc,&fs[READ_FIBER]);

   if (g_lpFiber[READ_FIBER] == NULL)
   {
      printf("CreateFiber error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   fs[READ_FIBER].dwParameter = 0x12345678;

   //
   // Create the Write fiber
   //
   g_lpFiber[WRITE_FIBER]=CreateFiber(0,WriteFiberFunc,&fs[WRITE_FIBER]);

   if (g_lpFiber[WRITE_FIBER] == NULL)
   {
      printf("CreateFiber error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   fs[WRITE_FIBER].dwParameter = 0x54545454;

   //
   // Switch to the read fiber
   //
   SwitchToFiber(g_lpFiber[READ_FIBER]);

   //
   // We have been scheduled again. Display results from the 
   // read/write fibers
   //
   printf("ReadFiber: result code is %lu, %lu bytes processed\n",
   fs[READ_FIBER].dwFiberResultCode, fs[READ_FIBER].dwBytesProcessed);

   printf("WriteFiber: result code is %lu, %lu bytes processed\n",
   fs[WRITE_FIBER].dwFiberResultCode, fs[WRITE_FIBER].dwBytesProcessed);

   //
   // Delete the fibers
   //
   DeleteFiber(g_lpFiber[READ_FIBER]);
   DeleteFiber(g_lpFiber[WRITE_FIBER]);

   //
   // Close handles
   //
   CloseHandle(fs[READ_FIBER].hFile);
   CloseHandle(fs[WRITE_FIBER].hFile);

   //
   // Free allocated memory
   //
   HeapFree(GetProcessHeap(), 0, g_lpBuffer);
   HeapFree(GetProcessHeap(), 0, fs);

   return RTN_OK;
}

VOID
__stdcall
ReadFiberFunc(
             LPVOID lpParameter
             )
{
   LPFIBERDATASTRUCT fds = (LPFIBERDATASTRUCT)lpParameter;

   //
   // If this fiber was passed NULL for fiber data, just return,
   // causing the current thread to exit
   //
   if (fds == NULL)
   {
      printf("Passed NULL fiber data; exiting current thread.\n");
      return;
   }

   //
   // Display some information pertaining to the current fiber
   //
   DisplayFiberInfo();

   fds->dwBytesProcessed = 0;

   while (1)
   {
      //
      // Read data from file specified in the READ_FIBER structure
      //
      if (!ReadFile(fds->hFile, g_lpBuffer, BUFFER_SIZE, 
         &g_dwBytesRead, NULL))
      {
         break;
      }

      //
      // if we reached EOF, break
      //
      if (g_dwBytesRead == 0) break;

      //
      // Update number of bytes processed in the fiber data structure
      //
      fds->dwBytesProcessed += g_dwBytesRead;

      //
      // Switch to the write fiber
      //
      SwitchToFiber(g_lpFiber[WRITE_FIBER]);
   } // while

   //
   // Update the fiber result code
   //
   fds->dwFiberResultCode = GetLastError();

   //
   // Switch back to the primary fiber
   //
   SwitchToFiber(g_lpFiber[PRIMARY_FIBER]);
}

VOID
__stdcall
WriteFiberFunc(
              LPVOID lpParameter
              )
{
   LPFIBERDATASTRUCT fds = (LPFIBERDATASTRUCT)lpParameter;
   DWORD dwBytesWritten;

   //
   // If this fiber was passed NULL for fiber data, just return,
   // causing the current thread to exit
   //
   if (fds == NULL)
   {
      printf("Passed NULL fiber data; exiting current thread.\n");
      return;
   }

   //
   // Display some information pertaining to the current fiber
   //
   DisplayFiberInfo();

   //
   // Assume all writes succeeded.  If a write fails, the fiber
   // result code will be updated to reflect the reason for failure
   //
   fds->dwBytesProcessed = 0;
   fds->dwFiberResultCode = ERROR_SUCCESS;

   while (1)
   {
      //
      // Write data to the file specified in the WRITE_FIBER structure
      //
      if (!WriteFile(fds->hFile, g_lpBuffer, g_dwBytesRead, 
         &dwBytesWritten, NULL))
      {
         //
         // If an error occurred writing, break
         //
         break;
      }

      //
      // Update number of bytes processed in the fiber data structure
      //
      fds->dwBytesProcessed += dwBytesWritten;

      //
      // Switch back to the read fiber
      //
      SwitchToFiber(g_lpFiber[READ_FIBER]);
   }  // while

   //
   // If an error occurred, update the fiber result code...
   //
   fds->dwFiberResultCode = GetLastError();

   //
   // ...and switch to the primary fiber
   //
   SwitchToFiber(g_lpFiber[PRIMARY_FIBER]);
}

void
DisplayFiberInfo(
                void
                )
{
   LPFIBERDATASTRUCT fds = (LPFIBERDATASTRUCT)GetFiberData();
   LPVOID lpCurrentFiber = GetCurrentFiber();

   //
   // Determine which fiber is executing, based on the fiber address
   //
   if (lpCurrentFiber == g_lpFiber[READ_FIBER])
      printf("Read fiber entered");
   else
   {
      if (lpCurrentFiber == g_lpFiber[WRITE_FIBER])
         printf("Write fiber entered");
      else
      {
         if (lpCurrentFiber == g_lpFiber[PRIMARY_FIBER])
            printf("Primary fiber entered");
         else
            printf("Unknown fiber entered");
      }
   }

   //
   // Display dwParameter from the current fiber data structure
   //
   printf(" (dwParameter is 0x%lx)\n", fds->dwParameter);
}
```



<span data-ttu-id="3c19a-113">In diesem Beispiel wird eine Fiber Datenstruktur verwendet, mit der das Verhalten und der Zustand der Fiber bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="3c19a-113">This example makes use of a fiber data structure which is used to determine the behavior and state of the fiber.</span></span> <span data-ttu-id="3c19a-114">Eine Datenstruktur ist für jede Fiber vorhanden. der Zeiger auf die Datenstruktur wird mithilfe des-Parameters der [*fiberproc*](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine) -Funktion zur Fiber-Erstellungszeit an die Fiber übergeben.</span><span class="sxs-lookup"><span data-stu-id="3c19a-114">One data structure exists for each fiber; the pointer to the data structure is passed to the fiber at fiber creation time using the parameter of the [*FiberProc*](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine) function.</span></span>

<span data-ttu-id="3c19a-115">Der aufrufende Thread ruft die [**convertthreadtofiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) -Funktion auf, mit der Fibers von dem Aufrufer geplant werden kann.</span><span class="sxs-lookup"><span data-stu-id="3c19a-115">The calling thread calls the [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) function, which enables fibers to be scheduled by the caller.</span></span> <span data-ttu-id="3c19a-116">Dadurch kann die Fiber auch durch eine andere Fiber geplant werden.</span><span class="sxs-lookup"><span data-stu-id="3c19a-116">This also allows the fiber to be scheduled by another fiber.</span></span> <span data-ttu-id="3c19a-117">Als Nächstes erstellt der Thread zwei zusätzliche Fibers, eine, die Lesevorgänge für eine angegebene Datei ausführt, und eine andere, die Schreibvorgänge für eine angegebene Datei ausführt.</span><span class="sxs-lookup"><span data-stu-id="3c19a-117">Next, the thread creates two additional fibers, one that performs read operations against a specified file, and another that performs the write operations against a specified file.</span></span>

<span data-ttu-id="3c19a-118">Die primäre Fiber Ruft die [**switchdefiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) -Funktion auf, um die gelesene Fiber zu planen.</span><span class="sxs-lookup"><span data-stu-id="3c19a-118">The primary fiber calls the [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) function to schedule the read fiber.</span></span> <span data-ttu-id="3c19a-119">Nach einem erfolgreichen Lesevorgang plant die Lese Fiber die Schreib Fiber.</span><span class="sxs-lookup"><span data-stu-id="3c19a-119">After a successful read, the read fiber schedules the write fiber.</span></span> <span data-ttu-id="3c19a-120">Nach einem erfolgreichen Schreibvorgang in die Schreib Fiber plant die Schreib Fiber die gelesene Fiber.</span><span class="sxs-lookup"><span data-stu-id="3c19a-120">After a successful write in the write fiber, the write fiber schedules the read fiber.</span></span> <span data-ttu-id="3c19a-121">Wenn der Lese-/Schreib-Cycle abgeschlossen ist, wird die primäre Fiber geplant, was zur Anzeige des Lese-/Schreibstatus führt.</span><span class="sxs-lookup"><span data-stu-id="3c19a-121">When the read/write cycle has completed, the primary fiber is scheduled, which results in the display of the read/write status.</span></span> <span data-ttu-id="3c19a-122">Wenn während der Lese-oder Schreibvorgänge ein Fehler auftritt, wird die primäre Fiber geplant und zeigt den Status des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="3c19a-122">If an error occurs during the read or write operations, the primary fiber is scheduled and example displays the status of the operation.</span></span>

<span data-ttu-id="3c19a-123">Vor der Beendigung des Prozesses gibt der Prozess die Fibers mithilfe der [**deletefiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) -Funktion frei, schließt die Datei Handles und gibt den zugewiesenen Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="3c19a-123">Prior to process termination, the process frees the fibers using the [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) function, closes the file handles, and frees the allocated memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c19a-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c19a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c19a-125">STAP</span><span class="sxs-lookup"><span data-stu-id="3c19a-125">Fibers</span></span>](fibers.md)
</dt> </dl>

 

 
