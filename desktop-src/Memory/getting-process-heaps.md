---
description: Dieses Beispiel veranschaulicht die Verwendung der GetProcessHeaps-Funktion zum Abrufen von Handles für den Standardprozess Heap und alle privaten Heaps, die für den aktuellen Prozess aktiv sind.
ms.assetid: 00f69593-f03b-4f30-aeec-db3fda0ac356
title: Prozess Heaps werden erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caffc8dcc69b02ab671b379dbb5e133e65f8d448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959668"
---
# <a name="getting-process-heaps"></a>Prozess Heaps werden erhalten.

Dieses Beispiel veranschaulicht die Verwendung der [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) -Funktion zum Abrufen von Handles für den Standardprozess Heap und alle privaten Heaps, die für den aktuellen Prozess aktiv sind.

Im Beispiel wird [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) zweimal aufgerufen, zuerst, um die Größe des benötigten Puffers zu berechnen, und erneut, um Handles in den Puffer abzurufen. Der Puffer wird mithilfe des von [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap)zurückgegebenen Handles aus dem Standardprozess Heap zugeordnet. Im Beispiel wird die Startadresse der einzelnen Heap in der Konsole ausgegeben. Anschließend wird die [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) -Funktion verwendet, um den für den Puffer zugeordneten Arbeitsspeicher freizugeben.

Die Anzahl von Heaps in einem Prozess kann variieren. Ein Prozess verfügt immer über mindestens einen Heap – den Standardprozess Heap –, und er kann über eine oder mehrere private Heaps verfügen, die von der Anwendung oder durch DLLs erstellt werden, die in den Adressraum des Prozesses geladen werden.

Beachten Sie, dass eine Anwendung Heap Funktionen nur auf Ihrem Standardprozess Heap oder auf privaten Heaps, die die Anwendung erstellt hat, aufruft. das Aufrufen von Heap Funktionen für einen privaten Heap einer anderen Komponente kann zu undefiniertem Verhalten führen.


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



 

 



