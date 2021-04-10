---
title: Die type_to_xmit-Funktion
description: Der stubwert Ruft den Typ \_ für die \_ xmit-Funktion auf, um den Typ, der von der Anwendung dargestellt wird, in den übertragenen Typ zu konvertieren.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947934"
---
# <a name="the-type_to_xmit-function"></a>Der Typ \_ der \_ xmit-Funktion.

Der stubwert Ruft den **Typ \_ für die \_ xmit** -Funktion auf, um den Typ, der von der Anwendung dargestellt wird, in den übertragenen Typ zu konvertieren. Die-Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

Der erste Parameter ist ein Zeiger auf die Anwendungsdaten. Der zweite Parameter wird von der-Funktion festgelegt, um auf die übertragenen Daten zu verweisen. Die Funktion muss Arbeitsspeicher für den übertragenen Typ zuweisen.

Im folgenden Beispiel ruft der Client die Remote Prozedur mit einem **\[ in-, out \]** -Parameter vom Typ Double- \_ \_ Linktyp auf. Der Clientstub Ruft den **Typ \_ an die \_ xmit** -Funktion auf, die hier mit dem Namen "Double \_ \_ linktype" \_ in "xmit" benannt \_ ist, um doppelt verknüpfte Listen Daten in ein Array zu konvertieren

Die-Funktion bestimmt die Anzahl der Elemente in der Liste, weist ein Array zu, das groß genug ist, um diese Elemente aufzunehmen, und kopiert dann die Listenelemente in das Array. Vor der Rückgabe der Funktion wird der zweite Parameter ( *pziray*) so festgelegt, dass er auf die neu zugeordnete Datenstruktur verweist.


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



 

 




