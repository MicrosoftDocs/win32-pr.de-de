---
title: Die type_free_xmit-Funktion
description: Die Stubdateien nennen die Type \_ Free \_ xmit-Funktion, um Speicher freizugeben, der den übertragenen Daten zugeordnet ist.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206837"
---
# <a name="the-type_free_xmit-function"></a>Die Type \_ Free \_ xmit-Funktion

Die Stubdateien nennen die **Type \_ Free \_ xmit** -Funktion, um Speicher freizugeben, der den übertragenen Daten zugeordnet ist. Nachdem der [Typ \_ aus der \_ xmit](the-type-from-xmit-function.md) -Funktion die übertragenen Daten in den dargestellten Typ konvertiert hat, wird der Arbeitsspeicher nicht mehr benötigt. Die-Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

Der-Parameter ist ein Zeiger auf den Arbeitsspeicher, in dem der übertragene Typ enthalten ist.

In diesem Beispiel enthält der Arbeitsspeicher ein Array, das sich in einer einzelnen Struktur befindet. Die Funktion "Double \_ Link \_ Type \_ Free \_ xmit" verwendet die vom Benutzer bereitgestellte Funktion "Mittel l \_ Benutzer frei" \_ , um den Arbeitsspeicher freizugeben:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




