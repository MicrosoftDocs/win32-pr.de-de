---
title: Die type_free_xmit-Funktion
description: Die Stubs rufen die xmit-Funktion vom Typ \_ "Free" \_ auf, um Arbeitsspeicher freizugeben, der den übertragenen Daten zugeordnet ist.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c192e30ec4f18d70d6e694e6097cb77ee7a2338230868730dc37c1c3207010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016580"
---
# <a name="the-type_free_xmit-function"></a>Die \_ xmit-Funktion vom Typ \_ "free"

Die Stubs rufen die **\_ \_ xmit-Funktion vom Typ "Free"** auf, um Arbeitsspeicher freizugeben, der den übertragenen Daten zugeordnet ist. Nachdem der [Typ \_ der \_ xmit-Funktion](the-type-from-xmit-function.md) die übertragenen Daten in den dargestellten Typ konvertiert hat, wird der Arbeitsspeicher nicht mehr benötigt. Die Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

Der -Parameter ist ein Zeiger auf den Arbeitsspeicher, der den übertragenen Typ enthält.

In diesem Beispiel enthält der Arbeitsspeicher ein Array, das sich in einer einzelnen Struktur befindet. Die Funktion DOUBLE \_ LINK \_ TYPE free \_ \_ xmit verwendet die vom Benutzer bereitgestellte Funktion midl \_ user \_ free, um den Arbeitsspeicher freizugeben:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




