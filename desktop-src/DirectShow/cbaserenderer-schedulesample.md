---
description: Die schedulesample-Methode plant ein Beispiel für das Rendering.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Cbaserderderer. schedulesample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369224"
---
# <a name="cbaserendererschedulesample-method"></a><span data-ttu-id="31e80-103">Cbaserderderer. schedulesample-Methode</span><span class="sxs-lookup"><span data-stu-id="31e80-103">CBaseRenderer.ScheduleSample method</span></span>

<span data-ttu-id="31e80-104">Die- `ScheduleSample` Methode plant ein Beispiel für das Rendering.</span><span class="sxs-lookup"><span data-stu-id="31e80-104">The `ScheduleSample` method schedules a sample for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31e80-105">Syntax</span></span>


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="31e80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31e80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e80-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="31e80-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="31e80-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="31e80-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e80-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31e80-109">Return value</span></span>

<span data-ttu-id="31e80-110">Gibt " **true** " zurück, wenn das Beispiel geplant wurde, oder " **false** ", wenn das Beispiel gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="31e80-110">Returns **TRUE** if the sample was scheduled, or **FALSE** if the sample was dropped.</span></span>

## <a name="remarks"></a><span data-ttu-id="31e80-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31e80-111">Remarks</span></span>

<span data-ttu-id="31e80-112">Diese Methode bestimmt zunächst, ob das Beispiel sofort gerendert, in der Zukunft gerendert oder gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="31e80-112">This method first determines whether the sample should be rendered immediately, rendered in the future, or dropped.</span></span> <span data-ttu-id="31e80-113">(Hierzu wird die [**cbaserdenderer:: getsampletimes**](cbaserenderer-getsampletimes.md) -Methode aufgerufen.) Wenn das Beispiel sofort gerendert werden soll, signalisiert die Methode das Ereignis [**cbaserenderer:: m \_ renderevent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="31e80-113">(To do so, it calls the [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method.) If the sample should be rendered immediately, the method signals the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span> <span data-ttu-id="31e80-114">Wenn das Beispiel in Zukunft gerendert werden soll, ruft die-Methode die [**IReferenceClock:: advisettime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode für die Planung auf.</span><span class="sxs-lookup"><span data-stu-id="31e80-114">If the sample should be rendered in the future, the method calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method for scheduling.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e80-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31e80-115">Requirements</span></span>



| <span data-ttu-id="31e80-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31e80-116">Requirement</span></span> | <span data-ttu-id="31e80-117">Wert</span><span class="sxs-lookup"><span data-stu-id="31e80-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e80-118">Header</span><span class="sxs-lookup"><span data-stu-id="31e80-118">Header</span></span><br/>  | <dl> <span data-ttu-id="31e80-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31e80-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31e80-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31e80-120">Library</span></span><br/> | <dl> <span data-ttu-id="31e80-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="31e80-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e80-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31e80-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e80-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="31e80-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




