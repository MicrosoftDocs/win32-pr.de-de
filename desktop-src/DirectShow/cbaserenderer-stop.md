---
description: Die Methode "beenden" beendet den Filter.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Cbaserenderer. stoppt-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367113"
---
# <a name="cbaserendererstop-method"></a><span data-ttu-id="85b00-103">Cbaserenderer. stoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="85b00-103">CBaseRenderer.Stop method</span></span>

<span data-ttu-id="85b00-104">Die- `Stop` Methode beendet den Filter.</span><span class="sxs-lookup"><span data-stu-id="85b00-104">The `Stop` method stops the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="85b00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85b00-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="85b00-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85b00-106">Parameters</span></span>

<span data-ttu-id="85b00-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="85b00-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85b00-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85b00-108">Return value</span></span>

<span data-ttu-id="85b00-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="85b00-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="85b00-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85b00-110">Remarks</span></span>

<span data-ttu-id="85b00-111">Diese Methode überschreibt die [**cbasefilter:: stopmethode**](cbasefilter-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="85b00-111">This method overrides the [**CBaseFilter::Stop**](cbasefilter-stop.md) method.</span></span> <span data-ttu-id="85b00-112">Es führt die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="85b00-112">It performs the following actions:</span></span>

-   <span data-ttu-id="85b00-113">Ruft [**cbasefilter:: Beendigung**](cbasefilter-stop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="85b00-113">Calls [**CBaseFilter::Stop**](cbasefilter-stop.md).</span></span>
-   <span data-ttu-id="85b00-114">Führt einen Commit für die Zuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="85b00-114">Decommits the allocator.</span></span> <span data-ttu-id="85b00-115">(Weitere Informationen finden Sie unter [**imemzuzukator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span><span class="sxs-lookup"><span data-stu-id="85b00-115">(See [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span></span>
-   <span data-ttu-id="85b00-116">Bricht das geplante Rendering ab und gibt den streamingingthread frei.</span><span class="sxs-lookup"><span data-stu-id="85b00-116">Cancels any scheduled rendering and releases the streaming thread.</span></span>
-   <span data-ttu-id="85b00-117">Wartet, bis alle ausstehenden **Empfangs** Aufrufe abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="85b00-117">Waits for any pending **Receive** call to complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="85b00-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85b00-118">Requirements</span></span>



| <span data-ttu-id="85b00-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85b00-119">Requirement</span></span> | <span data-ttu-id="85b00-120">Wert</span><span class="sxs-lookup"><span data-stu-id="85b00-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85b00-121">Header</span><span class="sxs-lookup"><span data-stu-id="85b00-121">Header</span></span><br/>  | <dl> <span data-ttu-id="85b00-122"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85b00-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85b00-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85b00-123">Library</span></span><br/> | <dl> <span data-ttu-id="85b00-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="85b00-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85b00-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85b00-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85b00-126">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="85b00-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




