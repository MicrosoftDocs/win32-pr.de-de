---
title: Durchlaufen der Heap Liste
description: In den Beispielen wird gezeigt, wie eine Liste von Heaps für den aktuellen Prozess abgerufen wird.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 5cc555f9a94166fa181309985d8a49c686baf06c
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "106370973"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="c55d0-103">Durchlaufen der Heap Liste</span><span class="sxs-lookup"><span data-stu-id="c55d0-103">Traversing the Heap List</span></span>

<span data-ttu-id="c55d0-104">Im folgenden Beispiel wird eine Liste von Heaps für den aktuellen Prozess abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c55d0-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="c55d0-105">Er erstellt eine Momentaufnahme der Heaps mithilfe der [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) -Funktion und durchläuft dann die Liste mithilfe der [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) -und [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c55d0-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="c55d0-106">Für jeden Heap verwendet er die [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) -Funktion und die [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) -Funktion zum Durchlaufen der Heap Blöcke.</span><span class="sxs-lookup"><span data-stu-id="c55d0-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="c55d0-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sind ineffizient, insbesondere für große Heaps.</span><span class="sxs-lookup"><span data-stu-id="c55d0-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) are inefficient, particularly for large heaps.</span></span> <span data-ttu-id="c55d0-108">Sie sind jedoch nützlich, wenn Sie andere Prozesse Abfragen möchten, bei denen Sie in der Regel einen Thread in den anderen Prozess einfügen müssen, um die Informationen zu erfassen (diese APIs werden dies für Sie tun).</span><span class="sxs-lookup"><span data-stu-id="c55d0-108">However, they are useful for querying other processes where you'd typically have to inject a thread into the other process to gather the information (these APIs do this for you).</span></span>

<span data-ttu-id="c55d0-109">Weitere Informationen finden Sie im zweiten Beispiel für eine äquivalente, weitaus effizientere Alternative, die [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) anstelle von [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c55d0-109">See the second example for an equivalent, much more efficient, alternative that uses [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) instead of [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span></span> <span data-ttu-id="c55d0-110">Beachten Sie, dass [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) nur für denselben Prozess verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c55d0-110">Note that [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) can only be used for the same process.</span></span>

```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```

<span data-ttu-id="c55d0-111">Der folgende Code Ausschnitt verwendet die [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) -Funktion, um die Prozess Heaps zu durchlaufen und so eine identische Ausgabe für das vorherige Beispiel zu erzeugen, aber weitaus effizienter:</span><span class="sxs-lookup"><span data-stu-id="c55d0-111">The following code snippet uses the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function to walk the process heaps, producing identical output to the previous example, but much more efficiently:</span></span>

```C++
#include <windows.h>
#include <stdio.h>

int main( void )
{
    DWORD heapIndex;
    DWORD heapCount = 0;
    PHANDLE heaps = NULL;
    while (TRUE)
    {
        DWORD actualHeapCount = GetProcessHeaps(heapCount, heaps);
        if (actualHeapCount <= heapCount)
        {
            break;
        }
        heapCount = actualHeapCount;
        free(heaps);
        heaps = (HANDLE*)malloc(heapCount * sizeof(HANDLE));
        if (heaps == NULL)
        {
            printf("Unable to allocate memory for list of heaps\n");
            return 1;
        }
    }

    for (heapIndex = 0; heapIndex < heapCount; heapIndex++)
    {
        PROCESS_HEAP_ENTRY entry;

        printf("Heap ID: %d\n", (DWORD)(ULONG_PTR)heaps[heapIndex]);
        entry.lpData = NULL;
        while (HeapWalk(heaps[heapIndex], &entry))
        {
            // Heap32First and Heap32Next ignore entries
            // with the PROCESS_HEAP_REGION flag
            if (!(entry.wFlags & PROCESS_HEAP_REGION))
            {
                printf("Block size: %d\n", entry.cbData + entry.cbOverhead);
            }
        }
    }

    free(heaps);
    return 0;
}
```

<span data-ttu-id="c55d0-112">Das Durchlaufen eines [**Heaps mit der heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) -Funktion ist ungefähr linear in der Größe des Heaps, während das Durchlaufen eines Heaps mit der [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) -Funktion ungefähr quadratisch in der Größe des Heaps ist.</span><span class="sxs-lookup"><span data-stu-id="c55d0-112">Walking a heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function is roughly linear in the size of the heap, whereas walking a heap with the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function is roughly quadratic in the size of the heap.</span></span>
<span data-ttu-id="c55d0-113">Auch bei einem bescheidenen Heap mit 10.000-Zuordnungen läuft [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 10.000 mal schneller als [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , während ausführlichere Informationen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c55d0-113">Even for a modest heap with 10,000 allocations, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) runs 10,000 times faster than [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) while providing more detailed information.</span></span> <span data-ttu-id="c55d0-114">Der Unterschied in der Leistung wird mit zunehmender Heapgröße noch dramatischer.</span><span class="sxs-lookup"><span data-stu-id="c55d0-114">The difference in performance becomes even more dramatic as the heap size increases.</span></span>

<span data-ttu-id="c55d0-115">Ein ausführlicheres Beispiel für das Durchlaufen des [**Heaps mit der heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) -Funktion finden Sie unter Auflisten [eines](/windows/win32/memory/enumerating-a-heap)Heaps.</span><span class="sxs-lookup"><span data-stu-id="c55d0-115">For a more detailed example of walking the heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function, see [Enumerating a Heap](/windows/win32/memory/enumerating-a-heap).</span></span>
