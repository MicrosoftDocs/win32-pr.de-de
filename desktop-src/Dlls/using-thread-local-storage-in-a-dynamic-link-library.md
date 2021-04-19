---
description: In diesem Abschnitt wird die Verwendung einer DLL-Einstiegspunkt Funktion zum Einrichten eines Thread lokalen Speicher Index (TLS) zum Bereitstellen des privaten Speichers für jeden Thread eines multithreadprozesses veranschaulicht.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Verwenden des lokalen Thread Speichers in einer Dynamic-Link-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347851"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a><span data-ttu-id="f68b0-103">Verwenden des lokalen Thread Speichers in einer Dynamic-Link-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f68b0-103">Using Thread Local Storage in a Dynamic-Link Library</span></span>

<span data-ttu-id="f68b0-104">In diesem Abschnitt wird die Verwendung einer DLL-Einstiegspunkt Funktion zum Einrichten eines Thread lokalen Speicher Index (TLS) zum Bereitstellen des privaten Speichers für jeden Thread eines multithreadprozesses veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f68b0-104">This section shows the use of a DLL entry-point function to set up a thread local storage (TLS) index to provide private storage for each thread of a multithreaded process.</span></span>

<span data-ttu-id="f68b0-105">Der TLS-Index wird in einer globalen Variablen gespeichert, sodass er für alle DLL-Funktionen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f68b0-105">The TLS index is stored in a global variable, making it available to all of the DLL functions.</span></span> <span data-ttu-id="f68b0-106">In diesem Beispiel wird davon ausgegangen, dass die globalen Daten der dll nicht freigegeben werden, da der TLS-Index für jeden Prozess, der die dll lädt, nicht notwendigerweise identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f68b0-106">This example assumes that the DLL's global data is not shared, because the TLS index is not necessarily the same for each process that loads the DLL.</span></span>

<span data-ttu-id="f68b0-107">Die Einstiegspunkt Funktion verwendet die [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) -Funktion, um einen TLS-Index zuzuweisen, wenn ein Prozess die dll lädt.</span><span class="sxs-lookup"><span data-stu-id="f68b0-107">The entry-point function uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index whenever a process loads the DLL.</span></span> <span data-ttu-id="f68b0-108">Jeder Thread kann diesen Index dann verwenden, um einen Zeiger auf seinen eigenen Speicherblock zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f68b0-108">Each thread can then use this index to store a pointer to its own block of memory.</span></span>

<span data-ttu-id="f68b0-109">Wenn die Einstiegspunkt Funktion mit dem Anfüge Wert des dll-Prozesses aufgerufen wird \_ \_ , führt der Code die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="f68b0-109">When the entry-point function is called with the DLL\_PROCESS\_ATTACH value, the code performs the following actions:</span></span>

1.  <span data-ttu-id="f68b0-110">Verwendet die [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) -Funktion, um einen TLS-Index zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f68b0-110">Uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index.</span></span>
2.  <span data-ttu-id="f68b0-111">Ordnet einen Speicherblock zu, der exklusiv vom ursprünglichen Thread des Prozesses verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f68b0-111">Allocates a block of memory to be used exclusively by the initial thread of the process.</span></span>
3.  <span data-ttu-id="f68b0-112">Verwendet den TLS-Index in einem Aufrufe der [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) -Funktion, um die Adresse des Speicherblocks in dem TLS-Slot zu speichern, der dem Index zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f68b0-112">Uses the TLS index in a call to the [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function to store the address of the memory block in the TLS slot associated with the index.</span></span>

<span data-ttu-id="f68b0-113">Jedes Mal, wenn der Prozess einen neuen Thread erstellt, wird die Einstiegspunkt Funktion mit dem \_ Anfüge Wert des dll-Threads aufgerufen \_ .</span><span class="sxs-lookup"><span data-stu-id="f68b0-113">Each time the process creates a new thread, the entry-point function is called with the DLL\_THREAD\_ATTACH value.</span></span> <span data-ttu-id="f68b0-114">Die Einstiegspunkt Funktion ordnet dann einen Speicherblock für den neuen Thread zu und speichert einen Zeiger darauf mithilfe des TLS-Indexes.</span><span class="sxs-lookup"><span data-stu-id="f68b0-114">The entry-point function then allocates a block of memory for the new thread and stores a pointer to it by using the TLS index.</span></span>

<span data-ttu-id="f68b0-115">Wenn eine Funktion Zugriff auf die Daten erfordert, die einem TLS-Index zugeordnet sind, geben Sie den Index in einem Aufrufen der [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="f68b0-115">When a function requires access to the data associated with a TLS index, specify the index in a call to the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function.</span></span> <span data-ttu-id="f68b0-116">Dadurch wird der Inhalt des TLS-Slots für den aufrufenden Thread abgerufen, bei dem es sich in diesem Fall um einen Zeiger auf den Speicherblock für die Daten handelt.</span><span class="sxs-lookup"><span data-stu-id="f68b0-116">This retrieves the contents of the TLS slot for the calling thread, which in this case is a pointer to the memory block for the data.</span></span> <span data-ttu-id="f68b0-117">Wenn ein Prozess Lade Zeit-Verknüpfungen mit dieser DLL verwendet, reicht die Einstiegspunkt Funktion aus, um den lokalen Thread Speicher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f68b0-117">When a process uses load-time linking with this DLL, the entry-point function is sufficient to manage the thread local storage.</span></span> <span data-ttu-id="f68b0-118">Es können Probleme bei einem Prozess auftreten, der die Laufzeit-Verknüpfung verwendet, da die Einstiegspunkt Funktion nicht für Threads aufgerufen wird, die vor dem Aufruf der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion vorhanden sind, sodass der TLS-Speicher für diese Threads nicht zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f68b0-118">Problems can occur with a process that uses run-time linking because the entry-point function is not called for threads that exist before the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is called, so TLS memory is not allocated for these threads.</span></span> <span data-ttu-id="f68b0-119">In diesem Beispiel wird dieses Problem gelöst, indem der von der [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) -Funktion zurückgegebene Wert überprüft und Arbeitsspeicher belegt wird, wenn der Wert angibt, dass der TLS-Slot für diesen Thread nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f68b0-119">This example solves this problem by checking the value returned by the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function and allocating memory if the value indicates that the TLS slot for this thread is not set.</span></span>

<span data-ttu-id="f68b0-120">Wenn jeder Thread keinen TLS-Index mehr verwenden muss, muss der Arbeitsspeicher freigegeben werden, dessen Zeiger im TLS-Slot gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f68b0-120">When each thread no longer needs to use a TLS index, it must free the memory whose pointer is stored in the TLS slot.</span></span> <span data-ttu-id="f68b0-121">Wenn alle Threads einen TLS-Index verwendet haben, verwenden Sie die [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) -Funktion, um den Index freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f68b0-121">When all threads have finished using a TLS index, use the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to release the index.</span></span>

<span data-ttu-id="f68b0-122">Wenn ein Thread beendet wird, wird die Einstiegspunkt Funktion mit dem \_ Trenn Wert des dll-Threads aufgerufen, \_ und der Speicher für diesen Thread wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f68b0-122">When a thread terminates, the entry-point function is called with the DLL\_THREAD\_DETACH value and the memory for that thread is freed.</span></span> <span data-ttu-id="f68b0-123">Wenn ein Prozess beendet wird, wird die Einstiegspunkt Funktion mit dem \_ Trenn Wert des dll-Prozesses aufgerufen, \_ und der Speicher, auf den der Zeiger im TLS-Index verweist, wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f68b0-123">When a process terminates, the entry-point function is called with the DLL\_PROCESS\_DETACH value and the memory referenced by the pointer in the TLS index is freed.</span></span>


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



<span data-ttu-id="f68b0-124">Der folgende Code veranschaulicht die Verwendung der DLL-Funktionen, die im vorherigen Beispiel definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f68b0-124">The following code demonstrates the use of the DLL functions defined in the previous example.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="f68b0-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f68b0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f68b0-126">Dynamic Link Library-Daten</span><span class="sxs-lookup"><span data-stu-id="f68b0-126">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> <dt>

[<span data-ttu-id="f68b0-127">Verwenden von TLS (threadlokaler Speicher)</span><span class="sxs-lookup"><span data-stu-id="f68b0-127">Using Thread Local Storage</span></span>](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
