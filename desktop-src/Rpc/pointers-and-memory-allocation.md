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
# <a name="pointers-and-memory-allocation"></a><span data-ttu-id="2965b-103">Zeiger und Speicher Belegung</span><span class="sxs-lookup"><span data-stu-id="2965b-103">Pointers and Memory Allocation</span></span>

<span data-ttu-id="2965b-104">Die Möglichkeit, Arbeitsspeicher über Zeiger zu ändern, erfordert häufig, dass der Server und der Client ausreichend Arbeitsspeicher für die Elemente im Array zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2965b-104">The ability to change memory through pointers often requires that the server and the client allocate enough memory for the elements in the array.</span></span>

<span data-ttu-id="2965b-105">Wenn ein Stub Arbeitsspeicher zuordnen oder freigeben muss, werden Lauf Zeit Bibliotheksfunktionen aufgerufen, die wiederum die Funktionen " [**mittlere \_ Benutzer \_**](/windows/desktop/Midl/midl-user-allocate-1) Zuordnungen" und " [**mittlere \_ Benutzer \_ kostenfrei**](/windows/desktop/Midl/midl-user-free-1)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2965b-105">When a stub must allocate or free memory, it calls run-time library functions that in turn call the functions [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1).</span></span> <span data-ttu-id="2965b-106">Diese Funktionen sind nicht als Teil der Lauf Zeit Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="2965b-106">These functions are not included as part of the run-time library.</span></span> <span data-ttu-id="2965b-107">Sie müssen ihre eigenen Versionen dieser Funktionen schreiben und Sie mit Ihrer Anwendung verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="2965b-107">You need to write your own versions of these functions and link them with your application.</span></span> <span data-ttu-id="2965b-108">Auf diese Weise können Sie entscheiden, wie Sie Arbeitsspeicher verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="2965b-108">In this way, you can decide how to manage memory.</span></span> <span data-ttu-id="2965b-109">Beim Kompilieren der IDL-Datei im OSF-Kompatibilitätsmodus (**/OSF**) müssen diese Funktionen nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2965b-109">When compiling your IDL file in OSF-compatibility (**/osf**) mode, you do not need to implement these functions.</span></span> <span data-ttu-id="2965b-110">Sie müssen diese Funktionen in die folgenden Prototypen schreiben:</span><span class="sxs-lookup"><span data-stu-id="2965b-110">You must write these functions to the following prototypes:</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

<span data-ttu-id="2965b-111">Beispielsweise können die Versionen dieser Funktionen für eine Anwendung einfach die Standard Bibliotheksfunktionen aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="2965b-111">For example, the versions of these functions for an application can simply call standard library functions:</span></span>


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



 

 