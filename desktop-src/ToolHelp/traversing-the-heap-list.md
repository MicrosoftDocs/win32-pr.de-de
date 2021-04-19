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
# <a name="traversing-the-heap-list"></a>Durchlaufen der Heap Liste

Im folgenden Beispiel wird eine Liste von Heaps für den aktuellen Prozess abgerufen. Er erstellt eine Momentaufnahme der Heaps mithilfe der [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) -Funktion und durchläuft dann die Liste mithilfe der [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) -und [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) -Funktionen. Für jeden Heap verwendet er die [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) -Funktion und die [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) -Funktion zum Durchlaufen der Heap Blöcke.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sind ineffizient, insbesondere für große Heaps. Sie sind jedoch nützlich, wenn Sie andere Prozesse Abfragen möchten, bei denen Sie in der Regel einen Thread in den anderen Prozess einfügen müssen, um die Informationen zu erfassen (diese APIs werden dies für Sie tun).

Weitere Informationen finden Sie im zweiten Beispiel für eine äquivalente, weitaus effizientere Alternative, die [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) anstelle von [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)verwendet. Beachten Sie, dass [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) nur für denselben Prozess verwendet werden kann.

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

Der folgende Code Ausschnitt verwendet die [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) -Funktion, um die Prozess Heaps zu durchlaufen und so eine identische Ausgabe für das vorherige Beispiel zu erzeugen, aber weitaus effizienter:

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

Das Durchlaufen eines [**Heaps mit der heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) -Funktion ist ungefähr linear in der Größe des Heaps, während das Durchlaufen eines Heaps mit der [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) -Funktion ungefähr quadratisch in der Größe des Heaps ist.
Auch bei einem bescheidenen Heap mit 10.000-Zuordnungen läuft [**heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 10.000 mal schneller als [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , während ausführlichere Informationen bereitgestellt werden. Der Unterschied in der Leistung wird mit zunehmender Heapgröße noch dramatischer.

Ein ausführlicheres Beispiel für das Durchlaufen des [**Heaps mit der heapwalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) -Funktion finden Sie unter Auflisten [eines](/windows/win32/memory/enumerating-a-heap)Heaps.
