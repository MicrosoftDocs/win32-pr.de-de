---
title: Die type_to_xmit-Funktion
description: Die Stubs rufen den Typ der xmit-Funktion auf, um den von der Anwendung dargestellten Typ in den \_ \_ übertragenen Typ zu konvertieren.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970d4a0de9675ac7a5f1b1c1449521177ecb661a1a80fd9ef609a6dc630605a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016500"
---
# <a name="the-type_to_xmit-function"></a>Der Typ \_ der \_ xmit-Funktion

Die Stubs rufen den Typ **der \_ \_ xmit-Funktion** auf, um den von der Anwendung dargestellten Typ in den übertragenen Typ zu konvertieren. Die Funktion ist wie die folgenden definiert:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

Der erste Parameter ist ein Zeiger auf die Anwendungsdaten. Der zweite Parameter wird von der Funktion festgelegt, um auf die übertragenen Daten zu verweisen. Die Funktion muss Arbeitsspeicher für den übertragenen Typ zuordnen.

Im folgenden Beispiel ruft der Client die Remoteprozedur auf, die über einen **\[ in, \] out-Parameter** vom Typ DOUBLE \_ LINK TYPE \_ verfügt. Der Clientstub ruft den Typ der **\_ \_ xmit-Funktion** auf, hier mit dem Namen DOUBLE \_ LINK TYPE in \_ \_ xmit, um doppelt verknüpfte Listendaten in ein Array mit \_ einer Größe zu konvertieren.

Die Funktion bestimmt die Anzahl der Elemente in der Liste, ordnet ein Array zu, das groß genug ist, um diese Elemente zu speichern, und kopiert dann die Listenelemente in das Array. Bevor die Funktion zurückgegeben wird, wird der zweite Parameter *ppArray* so festgelegt, dass er auf die neu zugeordnete Datenstruktur zeigen kann.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




