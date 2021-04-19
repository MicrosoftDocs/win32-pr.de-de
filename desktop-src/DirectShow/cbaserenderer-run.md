---
description: Die Run-Methode führt den Filter aus.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Cbaserderderer. Run-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362151"
---
# <a name="cbaserendererrun-method"></a><span data-ttu-id="a0e72-103">Cbaserderderer. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="a0e72-103">CBaseRenderer.Run method</span></span>

<span data-ttu-id="a0e72-104">Die- `Run` Methode führt den Filter aus.</span><span class="sxs-lookup"><span data-stu-id="a0e72-104">The `Run` method runs the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0e72-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="a0e72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0e72-106">Parameters</span></span>

<span data-ttu-id="a0e72-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0e72-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0e72-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0e72-108">Return value</span></span>

<span data-ttu-id="a0e72-109">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="a0e72-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e72-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0e72-110">Remarks</span></span>

<span data-ttu-id="a0e72-111">Diese Methode überschreibt die [**cbasefilter:: Run**](cbasefilter-run.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a0e72-111">This method overrides the [**CBaseFilter::Run**](cbasefilter-run.md) method.</span></span> <span data-ttu-id="a0e72-112">Es führt die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a0e72-112">It performs the following actions:</span></span>

-   <span data-ttu-id="a0e72-113">Ruft die **cbasefilter:: Run** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a0e72-113">Calls the **CBaseFilter::Run** method.</span></span>
-   <span data-ttu-id="a0e72-114">Führt einen Commit für die Zuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="a0e72-114">Commits the allocator.</span></span> <span data-ttu-id="a0e72-115">(Weitere Informationen finden Sie unter [**imemzuordcator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="a0e72-115">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="a0e72-116">Wenn der vorherige Zustand beendet wurde, gibt der Filter jedes enthaltene Beispiel frei.</span><span class="sxs-lookup"><span data-stu-id="a0e72-116">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="a0e72-117">(Das Beispiel ist nicht mehr gültig.)</span><span class="sxs-lookup"><span data-stu-id="a0e72-117">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="a0e72-118">Ruft die [**cbaserenderer:: startstreaming**](cbaserenderer-startstreaming.md) -Methode auf und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="a0e72-118">Calls the [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method and returns the result.</span></span> <span data-ttu-id="a0e72-119">Wenn eine Stichprobe aussteht, plant die **startstreaming** -Methode Sie für das Rendering.</span><span class="sxs-lookup"><span data-stu-id="a0e72-119">If a sample is pending, the **StartStreaming** method schedules it for rendering.</span></span>

<span data-ttu-id="a0e72-120">Wenn der Filter nicht verbunden ist, sendet er sofort ein [**EC \_ Complete**](ec-complete.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a0e72-120">If the filter is not connected, it posts an [**EC\_COMPLETE**](ec-complete.md) event immediately.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e72-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0e72-121">Requirements</span></span>



| <span data-ttu-id="a0e72-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0e72-122">Requirement</span></span> | <span data-ttu-id="a0e72-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a0e72-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e72-124">Header</span><span class="sxs-lookup"><span data-stu-id="a0e72-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a0e72-125"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0e72-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0e72-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0e72-126">Library</span></span><br/> | <dl> <span data-ttu-id="a0e72-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a0e72-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0e72-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0e72-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e72-129">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a0e72-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




