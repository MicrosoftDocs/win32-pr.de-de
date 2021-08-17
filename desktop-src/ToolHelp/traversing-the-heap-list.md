---
title: Durchlaufen der Heapliste
description: Beispiele zum Abrufen einer Liste von Heaps für den aktuellen Prozess.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 868526c76ee85095f5b52cc9238e9e16015bfb3a81c9888da148f1d5ecc644aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419250"
---
# <a name="traversing-the-heap-list"></a>Durchlaufen der Heapliste

Im folgenden Beispiel wird eine Liste von Heaps für den aktuellen Prozess erhalten. Er erstellt mithilfe der [**CreateToolhelp32Snapshot-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) eine Momentaufnahme der Heaps und führt dann mithilfe der [**Funktionen Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) und [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) durch die Liste. Für jeden Heap werden die Funktionen [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) verwendet, um die Heapblöcke zu durchgehen.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sind ineffizient, insbesondere bei großen Heaps. Sie sind jedoch nützlich, um andere Prozesse abzufragen, bei denen Sie in der Regel einen Thread in den anderen Prozess einfügen müssten, um die Informationen zu sammeln (diese APIs tun dies für Sie).

Im zweiten Beispiel finden Sie eine entsprechende, viel effizientere Alternative, die [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) anstelle von [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)verwendet. Beachten Sie, dass [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) nur für denselben Prozess verwendet werden kann.

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

Der folgende Codeausschnitt verwendet die [**HeapWalk-Funktion,**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) um die Prozessheaps zu durchgehen, wodurch eine identische Ausgabe wie im vorherigen Beispiel erzeugt wird, aber viel effizienter:

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

Das Gehen eines Heaps mit der [**HeapWalk-Funktion**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) ist ungefähr linear in der Größe des Heaps, während das Gehen eines Heaps mit der [**Heap32Next-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) ungefähr quadratisch in der Größe des Heaps ist.
Selbst bei einem kleinen Heap mit 10.000 Zuordnungen wird [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 10.000-mal schneller als [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) ausgeführt, während detailliertere Informationen bereitgestellt werden. Der Unterschied in der Leistung wird noch deutlicher, wenn die Heapgröße zunimmt.

Ein ausführlicheres Beispiel für das Gehen des Heaps mit der [**HeapWalk-Funktion**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) finden Sie unter [Aufzählen eines Heaps.](/windows/win32/memory/enumerating-a-heap)
