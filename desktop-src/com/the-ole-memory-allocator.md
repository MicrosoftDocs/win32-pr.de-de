---
title: Die OLE-Speicherzuweisung
description: Die OLE-Speicherzuweisung
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102398"
---
# <a name="the-ole-memory-allocator"></a><span data-ttu-id="36477-103">Die OLE-Speicherzuweisung</span><span class="sxs-lookup"><span data-stu-id="36477-103">The OLE Memory Allocator</span></span>

<span data-ttu-id="36477-104">Die com-Bibliothek stellt eine Implementierung eines Speicher belegers bereit, der Thread sicher ist.</span><span class="sxs-lookup"><span data-stu-id="36477-104">The COM library provides an implementation of a memory allocator that is thread-safe.</span></span> <span data-ttu-id="36477-105">(Das heißt, es können keine Probleme in Multithread-Situationen verursacht werden.) Wenn der Besitz eines zugeordneten Arbeitsspeichers über eine COM-Schnittstelle oder zwischen einem Client und der com-Bibliothek übermittelt wird, müssen Sie diesen com-Allocator verwenden, um den Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="36477-105">(That is, it cannot cause problems in multithreaded situations.) Whenever ownership of an allocated chunk of memory is passed through a COM interface or between a client and the COM library, you must use this COM allocator to allocate the memory.</span></span> <span data-ttu-id="36477-106">Bei der internen Zuordnung zu einem Objekt können alle gewünschten Zuordnungs Schemas verwendet werden, aber die com-Speicher Belegung ist eine praktische, effiziente und Thread sichere Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="36477-106">Allocation internal to an object can use any allocation scheme desired, but the COM memory allocator is a handy, efficient, and thread-safe allocator.</span></span>

<span data-ttu-id="36477-107">Ein Aufrufen der API-Funktion [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) stellt einen Zeiger auf die OLE-Zuweisung bereit, bei der es sich um eine Implementierung der [**imzuzuordnungsschnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) handelt.</span><span class="sxs-lookup"><span data-stu-id="36477-107">A call to the API function [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) provides a pointer to the OLE allocator, which is an implementation of the [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) interface.</span></span> <span data-ttu-id="36477-108">Es ist jedoch effizienter, die Hilfsfunktionen [**cotaskmemzuzugsc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**cotaskmemrebelegc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)und [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)aufzurufen, die einen Zeiger auf die Arbeitsspeicher Zuweisung einbinden, die entsprechende **imzuzuordnungsmethode** aufrufen und dann den Zeiger auf die Zuweisung freigeben.</span><span class="sxs-lookup"><span data-stu-id="36477-108">However, it is more efficient to call the helper functions [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc), and [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), which wrap getting a pointer to the task memory allocator, calling the corresponding **IMalloc** method, and then releasing the pointer to the allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36477-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36477-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36477-110">Verwalten der Speicher Belegung</span><span class="sxs-lookup"><span data-stu-id="36477-110">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> <dt>

[<span data-ttu-id="36477-111">Die com-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="36477-111">The COM Library</span></span>](the-com-library.md)
</dt> </dl>

 

 