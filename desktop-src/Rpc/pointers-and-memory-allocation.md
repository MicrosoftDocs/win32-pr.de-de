---
title: Zeiger und Speicherbelegung
description: Die Möglichkeit zum Ändern des Arbeitsspeichers durch Zeiger erfordert häufig, dass der Server und der Client genügend Arbeitsspeicher für die Elemente im Array zuordnen.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d634b209c1f6369429c432d5fad5d4e64b47aeae16778efd8916c00e65911e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927360"
---
# <a name="pointers-and-memory-allocation"></a>Zeiger und Speicherbelegung

Die Möglichkeit zum Ändern des Arbeitsspeichers durch Zeiger erfordert häufig, dass der Server und der Client genügend Arbeitsspeicher für die Elemente im Array zuordnen.

Wenn ein Stub Arbeitsspeicher zuordnen oder freigeben muss, ruft er Laufzeitbibliotheksfunktionen auf, die wiederum die Funktionen [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) und [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1)aufrufen. Diese Funktionen sind nicht als Teil der Laufzeitbibliothek enthalten. Sie müssen Ihre eigenen Versionen dieser Funktionen schreiben und sie mit Ihrer Anwendung verknüpfen. Auf diese Weise können Sie entscheiden, wie Der Arbeitsspeicher verwaltet werden soll. Wenn Sie Ihre IDL-Datei im OSF-Kompatibilitätsmodus **(/osf)** kompilieren, müssen Sie diese Funktionen nicht implementieren. Sie müssen diese Funktionen in die folgenden Prototypen schreiben:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Beispielsweise können die Versionen dieser Funktionen für eine Anwendung einfach Standardbibliotheksfunktionen aufrufen:


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 