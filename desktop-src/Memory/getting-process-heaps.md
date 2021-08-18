---
description: Dieses Beispiel veranschaulicht die Verwendung der GetProcessHeaps-Funktion zum Abrufen von Handles für den Standardprozessheap und alle privaten Heaps, die für den aktuellen Prozess aktiv sind.
ms.assetid: 00f69593-f03b-4f30-aeec-db3fda0ac356
title: Abrufen von Prozesshaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b055bd558d12506d5a900c369365cb497e3817dbfa1fd53dd6506f6a919eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067840"
---
# <a name="getting-process-heaps"></a>Abrufen von Prozesshaps

Dieses Beispiel veranschaulicht die Verwendung der [**GetProcessHeaps-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) zum Abrufen von Handles für den Standardprozessheap und alle privaten Heaps, die für den aktuellen Prozess aktiv sind.

Im Beispiel wird [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) zweimal aufgerufen, um zuerst die Größe des Puffers zu berechnen, der zum Abrufen von Handles im Puffer benötigt wird. Der Puffer wird mithilfe des von [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap)zurückgegebenen Handles aus dem Standardprozessheap zugeordnet. Im Beispiel wird die Startadresse jedes Heaps in der Konsole ausgegeben. Anschließend wird die [**HeapFree-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) verwendet, um den für den Puffer zugeordneten Arbeitsspeicher frei zu geben.

Die Anzahl der Heaps in einem Prozess kann variieren. Ein Prozess verfügt immer über mindestens einen Heap – den Standardprozesshap – und kann einen oder mehrere private Heaps haben, die von der Anwendung oder von DLLs erstellt werden, die in den Adressraum des Prozesses geladen werden.

Beachten Sie, dass eine Anwendung Heapfunktionen nur auf dem Standardprozesshap oder auf privaten Heaps aufrufen sollte, die von der Anwendung erstellt wurden. Das Aufrufen von Heapfunktionen auf einem privaten Heap, der sich im Besitz einer anderen Komponente befindet, kann zu nicht definiertem Verhalten führen.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <intsafe.h>

int __cdecl _tmain()
{
    DWORD NumberOfHeaps;
    DWORD HeapsIndex;
    DWORD HeapsLength;
    HANDLE hDefaultProcessHeap;
    HRESULT Result;
    PHANDLE aHeaps;
    SIZE_T BytesToAllocate;

    //
    // Retrieve the number of active heaps for the current process
    // so we can calculate the buffer size needed for the heap handles.
    //
    NumberOfHeaps = GetProcessHeaps(0, NULL);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve the number of heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Calculate the buffer size.
    //
    Result = SIZETMult(NumberOfHeaps, sizeof(*aHeaps), &BytesToAllocate);
    if (Result != S_OK) {
        _tprintf(TEXT("SIZETMult failed with HR %d.\n"), Result);
        return 1;
    }

    //
    // Get a handle to the default process heap.
    //
    hDefaultProcessHeap = GetProcessHeap();
    if (hDefaultProcessHeap == NULL) {
        _tprintf(TEXT("Failed to retrieve the default process heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Allocate the buffer from the default process heap.
    //
    aHeaps = (PHANDLE)HeapAlloc(hDefaultProcessHeap, 0, BytesToAllocate);
    if (aHeaps == NULL) {
        _tprintf(TEXT("HeapAlloc failed to allocate %d bytes.\n"),
                 BytesToAllocate);
        return 1;
    }

    // 
    // Save the original number of heaps because we are going to compare it
    // to the return value of the next GetProcessHeaps call.
    //
    HeapsLength = NumberOfHeaps;

    //
    // Retrieve handles to the process heaps and print them to stdout. 
    // Note that heap functions should be called only on the default heap of the process
    // or on private heaps that your component creates by calling HeapCreate.
    //
    NumberOfHeaps = GetProcessHeaps(HeapsLength, aHeaps);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }
    else if (NumberOfHeaps > HeapsLength) {

        //
        // Compare the latest number of heaps with the original number of heaps.
        // If the latest number is larger than the original number, another
        // component has created a new heap and the buffer is too small.
        //
        _tprintf(TEXT("Another component created a heap between calls. ") \
                 TEXT("Please try again.\n"));
        return 1;
    }

    _tprintf(TEXT("Process has %d heaps.\n"), HeapsLength);
    for (HeapsIndex = 0; HeapsIndex < HeapsLength; ++HeapsIndex) {
        _tprintf(TEXT("Heap %d at address: %#p.\n"),
                 HeapsIndex,
                 aHeaps[HeapsIndex]);
    }
  
    //
    // Release memory allocated from default process heap.
    //
    if (HeapFree(hDefaultProcessHeap, 0, aHeaps) == FALSE) {
        _tprintf(TEXT("Failed to free allocation from default process heap.\n"));
    }

    return 0;
}
```



 

 



