---
title: Die type_from_xmit-Funktion
description: Die Stubs rufen den Typ \_ der \_ xmit-Funktion auf, um Daten von ihrem übertragenen Typ in den Typ zu konvertieren, der der Anwendung präsentiert wird.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a38e372467208c76111728080037c65f5dca2856304a49f06e7e33426277eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923699"
---
# <a name="the-type_from_xmit-function"></a>Der Typ \_ der \_ xmit-Funktion

Die Stubs rufen den **Typ \_ der \_ xmit-Funktion** auf, um Daten von ihrem übertragenen Typ in den Typ zu konvertieren, der der Anwendung präsentiert wird. Die Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

Der erste Parameter ist ein Zeiger auf die übertragenen Daten. Die -Funktion legt den zweiten Parameter so fest, dass er auf die dargestellten Daten zeigt.

Der **Typ \_ der \_ xmit-Funktion** muss den Arbeitsspeicher für den dargestellten Typ verwalten. Die Funktion muss Arbeitsspeicher für die gesamte Datenstruktur zuordnen, die an der durch den zweiten Parameter angegebenen Adresse beginnt, mit Ausnahme des Parameters selbst (der Stub belegt Speicher für den Stammknoten und übergibt ihn an die Funktion). Der Wert des zweiten Parameters kann während des Aufrufs nicht geändert werden. Die Funktion kann den Inhalt an dieser Adresse ändern.

In diesem Beispiel konvertiert die Funktion DOUBLE \_ LINK \_ TYPE von \_ \_ xmit das Array der Größe in eine doppelt verknüpfte Liste. Die Funktion behält den gültigen Zeiger auf den Anfang der Liste bei, gibt Arbeitsspeicher frei, der dem Rest der Liste zugeordnet ist, und erstellt dann eine neue Liste, die mit demselben Zeiger beginnt. Die Funktion verwendet die Hilfsprogrammfunktion **InsertNewNode**, um einen Listenknoten an das Ende der Liste anzufügen und die *pNext-* und *pPrevious-Zeiger* den entsprechenden Werten zuzuweisen.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




