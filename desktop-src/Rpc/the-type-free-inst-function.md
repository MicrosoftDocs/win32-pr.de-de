---
title: Die type_free_inst-Funktion
description: Die stuften geben den Typ " \_ Free \_ inst" an, um dem dargestellten Typ zugeordneten Arbeitsspeicher freizugeben.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856164"
---
# <a name="the-type_free_inst-function"></a>Die \_ typfreie \_ inst-Funktion

Die stuften **geben den Typ " \_ Free \_ inst** " an, um dem dargestellten Typ zugeordneten Arbeitsspeicher freizugeben. Die-Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

Der-Parameter verweist auf die präsentierte Typinstanz. Dieses Objekt sollte nicht freigegeben werden. Eine Erläuterung dazu, wann die-Funktion aufgerufen werden muss, finden Sie unter "über [tragen \_ als](the-transmit-as-attribute.md)"-Attribut.

Im folgenden Beispiel wird die Liste mit doppelten verknüpften freigegeben, indem Sie die Liste bis zum Ende durchlaufen und dann jedes Element der Liste sichern und freigeben.


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



 

 




