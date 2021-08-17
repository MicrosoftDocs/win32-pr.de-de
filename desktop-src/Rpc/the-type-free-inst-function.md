---
title: Die type_free_inst-Funktion
description: Die Stubs rufen den Typ \_ free \_ inst function auf, um Arbeitsspeicher frei zu geben, der dem dargestellten Typ zugeordnet ist.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc71c8d3557c62eec39fe9a90855ef3ed057d29c21ec60a82ddc7fe04207f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923709"
---
# <a name="the-type_free_inst-function"></a>Der \_ typfreie \_ inst-Funktion

Die Stubs rufen den Typ **\_ free \_ inst** function auf, um Arbeitsspeicher frei zu geben, der dem dargestellten Typ zugeordnet ist. Die Funktion ist wie die folgenden definiert:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

Der -Parameter verweist auf die dargestellte Typinstanz. Dieses Objekt sollte nicht frei werden. Eine Diskussion darüber, wann die Funktion aufruft werden soll, finden Sie unter [Die Übertragung \_ als Attribut](the-transmit-as-attribute.md).

Im folgenden Beispiel wird die doppelt verknüpfte Liste durch das Durchgehen der Liste bis zum Ende des Listenendes und anschließendes Sichern und Frei geben der einzelnen Elemente der Liste frei.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




