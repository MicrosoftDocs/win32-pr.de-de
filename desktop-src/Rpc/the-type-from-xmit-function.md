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
# <a name="the-type_from_xmit-function"></a><span data-ttu-id="fd6d3-104">Der Typ \_ aus der \_ xmit-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd6d3-104">The type\_from\_xmit Function</span></span>

<span data-ttu-id="fd6d3-105">Die Stubdateien nennen den **Typ \_ von der \_ xmit** -Funktion, um Daten aus dem übertragenen Typ in den Typ zu konvertieren, der der Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-105">The stubs call the **type\_from\_xmit** function to convert data from its transmitted type to the type that is presented to the application.</span></span> <span data-ttu-id="fd6d3-106">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="fd6d3-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

<span data-ttu-id="fd6d3-107">Der erste Parameter ist ein Zeiger auf die übertragenen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-107">The first parameter is a pointer to the transmitted data.</span></span> <span data-ttu-id="fd6d3-108">Die-Funktion legt den zweiten Parameter fest, um auf die dargestellten Daten zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="fd6d3-109">Der **Typ \_ aus der \_ xmit** -Funktion muss den Arbeitsspeicher für den dargestellten Typ verwalten.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-109">The **type\_from\_xmit** function must manage memory for the presented type.</span></span> <span data-ttu-id="fd6d3-110">Die-Funktion muss für die gesamte Datenstruktur, die bei der durch den zweiten Parameter angegebenen Adresse beginnt, Arbeitsspeicher zuweisen, mit Ausnahme des-Parameters selbst (der Stub weist Speicher für den Stamm Knoten zu und übergibt ihn an die-Funktion).</span><span class="sxs-lookup"><span data-stu-id="fd6d3-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="fd6d3-111">Der Wert des zweiten Parameters kann während des Aufrufes nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="fd6d3-112">Die Funktion kann den Inhalt an dieser Adresse ändern.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-112">The function can change the contents at that address.</span></span>

<span data-ttu-id="fd6d3-113">In diesem Beispiel konvertiert der Double \_ \_ -Linktyp der Funktion \_ von \_ xmit das Array der Größenangabe in eine doppelt verknüpfte Liste.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-113">In this example, the function DOUBLE\_LINK\_TYPE\_from\_xmit converts the sized array to a double-linked list.</span></span> <span data-ttu-id="fd6d3-114">Die Funktion behält den gültigen Zeiger am Anfang der Liste bei, gibt den dem Rest der Liste zugeordneten Arbeitsspeicher frei und erstellt dann eine neue Liste, die mit dem gleichen Zeiger beginnt.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-114">The function retains the valid pointer to the beginning of the list, frees memory associated with the rest of the list, then creates a new list that starts at the same pointer.</span></span> <span data-ttu-id="fd6d3-115">Die Funktion verwendet die Utility-Funktion **insertnewnode**, um einen Listen Knoten an das Ende der Liste anzufügen und die *pNext* -und *pprevious* -Zeiger den entsprechenden Werten zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="fd6d3-115">The function uses a utility function, **InsertNewNode**, to append a list node to the end of the list and to assign the *pNext* and *pPrevious* pointers to appropriate values.</span></span>


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



 

 




