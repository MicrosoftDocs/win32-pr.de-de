---
title: midl_user_free-Attribut
description: Die Funktion "mittlere \_ Benutzer \_ Kosten" wird von Client-und Server Anwendungen bereitgestellt, um die Zuordnung dynamisch zugeordneten Speichers aufzuheben.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free Attribut-Mittel l
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314901"
---
# <a name="midl_user_free-attribute"></a><span data-ttu-id="f6d3c-104">\_ \_ Kostenloses Attribut für mittlere Benutzer</span><span class="sxs-lookup"><span data-stu-id="f6d3c-104">midl\_user\_free attribute</span></span>

<span data-ttu-id="f6d3c-105">Die Funktion " **mittlere \_ Benutzer \_ Kosten** " wird von Client-und Server Anwendungen bereitgestellt, um die Zuordnung dynamisch zugeordneten Speichers aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="f6d3c-105">The **midl\_user\_free** function is provided by client and server applications to deallocate dynamically allocated memory.</span></span>

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a><span data-ttu-id="f6d3c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6d3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d3c-107">*cker*</span><span class="sxs-lookup"><span data-stu-id="f6d3c-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="f6d3c-108">Ein Zeiger auf den Speicherblock, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6d3c-108">A pointer to the memory block to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6d3c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6d3c-109">Remarks</span></span>

<span data-ttu-id="f6d3c-110">Sowohl die Client Anwendung als auch die Serveranwendung müssen die Free-Funktion der **mittleren \_ \_ Benutzer** implementieren, es sei denn, Sie kompilieren ihn im OSF-Kompatibilitätsmodus ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="f6d3c-110">Both client application and server application must implement the **midl\_user\_free** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="f6d3c-111">Die **mittlere \_ Benutzer \_ freie** Funktion muss in der Lage sein, den gesamten Speicher freizugeben, der von der [**\_ Benutzer \_ Zuordnung**](/windows/desktop/Rpc/the-midl-user-allocate-function)für den Benutzer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f6d3c-111">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span>

<span data-ttu-id="f6d3c-112">Anwendungen und stufstufs wenden den **\_ Benutzer \_ kostenlos** an, wenn Sie mit Objekten arbeiten, auf die durch Zeiger verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="f6d3c-112">Applications and stubs call **midl\_user\_free** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="f6d3c-113">Die Serveranwendung sollte den **\_ Benutzer freien Benutzer \_ Free** anrufen, um Speicher freizugeben, der von der application\\z. b. beim Löschen eines bestimmten Knotens zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f6d3c-113">The server application should call **midl\_user\_free** to free memory allocated by the applicationâ€”for example, when deleting a specified node.</span></span>
-   <span data-ttu-id="f6d3c-114">Der Serverstub Ruft den **\_ Benutzer \_ kostenlos** auf, um Arbeitsspeicher auf dem Server freizugeben, nachdem alle **\[** [](out-idl.md) **\]** Argumente, **\[** [**in**](in.md), **out \]** -Argumente und der Rückgabewert gemarshallert wurden.</span><span class="sxs-lookup"><span data-stu-id="f6d3c-114">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all **\[**[**out**](out-idl.md)**\]** arguments, **\[**[**in**](in.md), **out\]** arguments, and the return value.</span></span>

## <a name="examples"></a><span data-ttu-id="f6d3c-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6d3c-115">Examples</span></span>


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a><span data-ttu-id="f6d3c-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f6d3c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d3c-117">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="f6d3c-117">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="f6d3c-118">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="f6d3c-118">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="f6d3c-119">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="f6d3c-119">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6d3c-120">**in**</span><span class="sxs-lookup"><span data-stu-id="f6d3c-120">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="f6d3c-121">**mittlere Benutzer Zuordnungen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f6d3c-121">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="f6d3c-122">**/osf**</span><span class="sxs-lookup"><span data-stu-id="f6d3c-122">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="f6d3c-123">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="f6d3c-123">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f6d3c-124">**gem**</span><span class="sxs-lookup"><span data-stu-id="f6d3c-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 