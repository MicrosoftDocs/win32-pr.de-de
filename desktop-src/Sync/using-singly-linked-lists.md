---
description: Im folgenden Beispiel wird die InitializeSListHead-Funktion verwendet, um eine singly verknüpfte Liste zu initialisieren, und die InterlockedPushEntrySList-Funktion zum Einfügen von 10 Elementen.
ms.assetid: 5608f84f-9211-4043-bb53-60339191ee29
title: Verwenden von einfach verknüpften Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa3a99202637e7d7b0b64f964ca1452244d72f02d99770bcdc6cbe368d960be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765011"
---
# <a name="using-singly-linked-lists"></a>Verwenden von einfach verknüpften Listen

Im folgenden Beispiel wird die [**InitializeSListHead-Funktion**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) verwendet, um eine [singly](interlocked-singly-linked-lists.md) verknüpfte Liste zu initialisieren, und die [**InterlockedPushEntrySList-Funktion**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) zum Einfügen von 10 Elementen. Im Beispiel wird die [**InterlockedPopEntrySList-Funktion**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) verwendet, um 10 Elemente zu entfernen, und die [**InterlockedFlushSList-Funktion,**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist) um zu überprüfen, ob die Liste leer ist.


```C++
#include <windows.h>
#include <malloc.h>
#include <stdio.h>

// Structure to be used for a list item; the first member is the 
// SLIST_ENTRY structure, and additional members are used for data.
// Here, the data is simply a signature for testing purposes. 


typedef struct _PROGRAM_ITEM {
    SLIST_ENTRY ItemEntry;
    ULONG Signature; 
} PROGRAM_ITEM, *PPROGRAM_ITEM;

int main( )
{
    ULONG Count;
    PSLIST_ENTRY pFirstEntry, pListEntry;
    PSLIST_HEADER pListHead;
    PPROGRAM_ITEM pProgramItem;

    // Initialize the list header to a MEMORY_ALLOCATION_ALIGNMENT boundary.
    pListHead = (PSLIST_HEADER)_aligned_malloc(sizeof(SLIST_HEADER),
       MEMORY_ALLOCATION_ALIGNMENT);
    if( NULL == pListHead )
    {
        printf("Memory allocation failed.\n");
        return -1;
    }
    InitializeSListHead(pListHead);

    // Insert 10 items into the list.
    for( Count = 1; Count <= 10; Count += 1 )
    {
        pProgramItem = (PPROGRAM_ITEM)_aligned_malloc(sizeof(PROGRAM_ITEM),
            MEMORY_ALLOCATION_ALIGNMENT);
        if( NULL == pProgramItem )
        {
            printf("Memory allocation failed.\n");
            return -1;
        }
        pProgramItem->Signature = Count;
        pFirstEntry = InterlockedPushEntrySList(pListHead, 
                       &(pProgramItem->ItemEntry)); 
    }

    // Remove 10 items from the list and display the signature.
    for( Count = 10; Count >= 1; Count -= 1 )
    {
        pListEntry = InterlockedPopEntrySList(pListHead);

        if( NULL == pListEntry )
        {
            printf("List is empty.\n");
            return -1;
        }
  
        pProgramItem = (PPROGRAM_ITEM)pListEntry;
        printf("Signature is %d\n", pProgramItem->Signature);

    // This example assumes that the SLIST_ENTRY structure is the 
    // first member of the structure. If your structure does not 
    // follow this convention, you must compute the starting address 
    // of the structure before calling the free function.

        _aligned_free(pListEntry);
    }

    // Flush the list and verify that the items are gone.
    pListEntry = InterlockedFlushSList(pListHead);
    pFirstEntry = InterlockedPopEntrySList(pListHead);
    if (pFirstEntry != NULL)
    {
        printf("Error: List is not empty.\n");
        return -1;
    }

    _aligned_free(pListHead);

    return 1;
}

```



 

 
