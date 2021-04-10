---
title: Die type_from_xmit-Funktion
description: Die Stubdateien nennen den Typ \_ von der \_ xmit-Funktion, um Daten aus dem übertragenen Typ in den Typ zu konvertieren, der der Anwendung angezeigt wird.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037405"
---
# <a name="the-type_from_xmit-function"></a>Der Typ \_ aus der \_ xmit-Funktion

Die Stubdateien nennen den **Typ \_ von der \_ xmit** -Funktion, um Daten aus dem übertragenen Typ in den Typ zu konvertieren, der der Anwendung angezeigt wird. Die-Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

Der erste Parameter ist ein Zeiger auf die übertragenen Daten. Die-Funktion legt den zweiten Parameter fest, um auf die dargestellten Daten zu verweisen.

Der **Typ \_ aus der \_ xmit** -Funktion muss den Arbeitsspeicher für den dargestellten Typ verwalten. Die-Funktion muss für die gesamte Datenstruktur, die bei der durch den zweiten Parameter angegebenen Adresse beginnt, Arbeitsspeicher zuweisen, mit Ausnahme des-Parameters selbst (der Stub weist Speicher für den Stamm Knoten zu und übergibt ihn an die-Funktion). Der Wert des zweiten Parameters kann während des Aufrufes nicht geändert werden. Die Funktion kann den Inhalt an dieser Adresse ändern.

In diesem Beispiel konvertiert der Double \_ \_ -Linktyp der Funktion \_ von \_ xmit das Array der Größenangabe in eine doppelt verknüpfte Liste. Die Funktion behält den gültigen Zeiger am Anfang der Liste bei, gibt den dem Rest der Liste zugeordneten Arbeitsspeicher frei und erstellt dann eine neue Liste, die mit dem gleichen Zeiger beginnt. Die Funktion verwendet die Utility-Funktion **insertnewnode**, um einen Listen Knoten an das Ende der Liste anzufügen und die *pNext* -und *pprevious* -Zeiger den entsprechenden Werten zuzuweisen.


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



 

 




