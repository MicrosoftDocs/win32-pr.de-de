---
description: Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Cbasefilter:: m_pLock Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351290"
---
# <a name="cbasefilterm_plock-member"></a><span data-ttu-id="a3041-103">Cbasefilter:: m \_ Plock-Member</span><span class="sxs-lookup"><span data-stu-id="a3041-103">CBaseFilter::m\_pLock member</span></span>

<span data-ttu-id="a3041-104">Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3041-104">Pointer to a critical section that is used to serialize state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3041-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3041-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="a3041-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3041-106">Remarks</span></span>

<span data-ttu-id="a3041-107">Diese Variable wird im-Klassenkonstruktor initialisiert. Weitere Informationen finden Sie unter [**cbasefilter:: cbasefilter**](cbasefilter-cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="a3041-107">This variable is initialized in the class constructor; see [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).</span></span>

<span data-ttu-id="a3041-108">Halten Sie diesen kritischen Abschnitt während der Zustandsübergänge oder wenn eine Methode über mehrere Vorgänge auf den Zustand zugreift.</span><span class="sxs-lookup"><span data-stu-id="a3041-108">Hold this critical section during state transitions, or when a method accesses the state over several operations.</span></span> <span data-ttu-id="a3041-109">Die Basisklasse enthält den kritischen Abschnitt der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="a3041-109">The base class holds the critical section in the following methods:</span></span>

-   [<span data-ttu-id="a3041-110">**Cbasefilter:: findpin**</span><span class="sxs-lookup"><span data-stu-id="a3041-110">**CBaseFilter::FindPin**</span></span>](cbasefilter-findpin.md)
-   [<span data-ttu-id="a3041-111">**Cbasefilter:: getsyncsource**</span><span class="sxs-lookup"><span data-stu-id="a3041-111">**CBaseFilter::GetSyncSource**</span></span>](cbasefilter-getsyncsource.md)
-   [<span data-ttu-id="a3041-112">**Cbasefilter:: joinfiltergraph**</span><span class="sxs-lookup"><span data-stu-id="a3041-112">**CBaseFilter::JoinFilterGraph**</span></span>](cbasefilter-joinfiltergraph.md)
-   [<span data-ttu-id="a3041-113">**Cbasefilter:: IsActive**</span><span class="sxs-lookup"><span data-stu-id="a3041-113">**CBaseFilter::IsActive**</span></span>](cbasefilter-isactive.md)
-   [<span data-ttu-id="a3041-114">**Cbasefilter:: setsyncsource**</span><span class="sxs-lookup"><span data-stu-id="a3041-114">**CBaseFilter::SetSyncSource**</span></span>](cbasefilter-setsyncsource.md)
-   [<span data-ttu-id="a3041-115">**Cbasefilter::P ause**</span><span class="sxs-lookup"><span data-stu-id="a3041-115">**CBaseFilter::Pause**</span></span>](cbasefilter-pause.md)
-   [<span data-ttu-id="a3041-116">**Cbasefilter:: Run**</span><span class="sxs-lookup"><span data-stu-id="a3041-116">**CBaseFilter::Run**</span></span>](cbasefilter-run.md)
-   [<span data-ttu-id="a3041-117">**Cbasefilter:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="a3041-117">**CBaseFilter::Stop**</span></span>](cbasefilter-stop.md)

<span data-ttu-id="a3041-118">Behalten Sie diesen kritischen Abschnitt nicht bei Streamingvorgängen bei (d. h. beim Bereitstellen von Beispielen für einen downstreamfilter).</span><span class="sxs-lookup"><span data-stu-id="a3041-118">Do not hold this critical section during streaming operations (that is, when delivering samples to a downstream filter).</span></span> <span data-ttu-id="a3041-119">Serialisieren von Streamingvorgängen mithilfe eines anderen kritischen Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="a3041-119">Serialize streaming operations using a different critical section.</span></span> <span data-ttu-id="a3041-120">Andernfalls kann dies zu einem Deadlock führen.</span><span class="sxs-lookup"><span data-stu-id="a3041-120">Otherwise, it can cause deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3041-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3041-121">Requirements</span></span>



| <span data-ttu-id="a3041-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3041-122">Requirement</span></span> | <span data-ttu-id="a3041-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a3041-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3041-124">Header</span><span class="sxs-lookup"><span data-stu-id="a3041-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a3041-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3041-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3041-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3041-126">Library</span></span><br/> | <dl> <span data-ttu-id="a3041-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a3041-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3041-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3041-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3041-129">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a3041-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="a3041-130">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="a3041-130">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




