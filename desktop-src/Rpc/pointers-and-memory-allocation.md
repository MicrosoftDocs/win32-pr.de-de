---
title: Zeiger und Speicher Belegung
description: Die Möglichkeit, Arbeitsspeicher über Zeiger zu ändern, erfordert häufig, dass der Server und der Client ausreichend Arbeitsspeicher für die Elemente im Array zuweisen.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102122"
---
# <a name="pointers-and-memory-allocation"></a>Zeiger und Speicher Belegung

Die Möglichkeit, Arbeitsspeicher über Zeiger zu ändern, erfordert häufig, dass der Server und der Client ausreichend Arbeitsspeicher für die Elemente im Array zuweisen.

Wenn ein Stub Arbeitsspeicher zuordnen oder freigeben muss, werden Lauf Zeit Bibliotheksfunktionen aufgerufen, die wiederum die Funktionen " [**mittlere \_ Benutzer \_**](/windows/desktop/Midl/midl-user-allocate-1) Zuordnungen" und " [**mittlere \_ Benutzer \_ kostenfrei**](/windows/desktop/Midl/midl-user-free-1)" aufrufen. Diese Funktionen sind nicht als Teil der Lauf Zeit Bibliothek enthalten. Sie müssen ihre eigenen Versionen dieser Funktionen schreiben und Sie mit Ihrer Anwendung verknüpfen. Auf diese Weise können Sie entscheiden, wie Sie Arbeitsspeicher verwalten möchten. Beim Kompilieren der IDL-Datei im OSF-Kompatibilitätsmodus (**/OSF**) müssen diese Funktionen nicht implementiert werden. Sie müssen diese Funktionen in die folgenden Prototypen schreiben:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Beispielsweise können die Versionen dieser Funktionen für eine Anwendung einfach die Standard Bibliotheksfunktionen aufzurufen:


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



 

 