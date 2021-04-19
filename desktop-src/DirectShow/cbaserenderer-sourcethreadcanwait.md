---
description: Die sourcethreadcanwait-Methode enthält den streamingindthread oder gibt diesen frei.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Cbaserderderer. sourcethreadcanwait-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367114"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a><span data-ttu-id="42419-103">Cbaserderderer. sourcethreadcanwait-Methode</span><span class="sxs-lookup"><span data-stu-id="42419-103">CBaseRenderer.SourceThreadCanWait method</span></span>

<span data-ttu-id="42419-104">Die- `SourceThreadCanWait` Methode enthält den streamingthread oder gibt diesen frei.</span><span class="sxs-lookup"><span data-stu-id="42419-104">The `SourceThreadCanWait` method holds or releases the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="42419-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42419-105">Syntax</span></span>


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a><span data-ttu-id="42419-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42419-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42419-107">*bcanwait*</span><span class="sxs-lookup"><span data-stu-id="42419-107">*bCanWait*</span></span> 
</dt> <dd>

<span data-ttu-id="42419-108">Boolescher Wert, der angibt, ob der streamingthread enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="42419-108">Boolean value indicating whether to hold the streaming thread.</span></span> <span data-ttu-id="42419-109">**True** gibt an, dass der streamingingthread blockiert wird, während der Filter auf das Rendering der nächsten Beispiele wartet.</span><span class="sxs-lookup"><span data-stu-id="42419-109">If **TRUE**, the streaming thread is blocked while the filter waits to render the next samples.</span></span> <span data-ttu-id="42419-110">Wenn **false**, wird der streamingingthread freigegeben.</span><span class="sxs-lookup"><span data-stu-id="42419-110">If **FALSE**, the streaming thread is released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42419-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42419-111">Return value</span></span>

<span data-ttu-id="42419-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="42419-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="42419-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42419-113">Remarks</span></span>

<span data-ttu-id="42419-114">Wenn Sie die- `SourceThreadCanWait` Methode mit dem Wert **false** aufrufen, wird der Filter gezwungen, von einem blockierten [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Aufruf zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="42419-114">Calling the `SourceThreadCanWait` method with the value **FALSE** forces the filter to return from a blocked [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call.</span></span> <span data-ttu-id="42419-115">Wenn der Filter ausgeführt wird, werden **Empfangs** Aufrufe bis zum Präsentations Zeitpunkt des aktuellen Beispiels blockiert.</span><span class="sxs-lookup"><span data-stu-id="42419-115">When the filter is running, it blocks **Receive** calls until the current sample's presentation time.</span></span> <span data-ttu-id="42419-116">Wenn der Filter angehalten wird, werden **Empfangs** Aufrufe unbegrenzt blockiert.</span><span class="sxs-lookup"><span data-stu-id="42419-116">When the filter is paused, it blocks **Receive** calls indefinitely.</span></span> <span data-ttu-id="42419-117">Dieses Verhalten regelt den Datenfluss im Stream.</span><span class="sxs-lookup"><span data-stu-id="42419-117">This behavior regulates the flow of data in the stream.</span></span> <span data-ttu-id="42419-118">Wenn der Filter beendet oder geleert wird, sollte er jedoch nicht blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="42419-118">When the filter is stopped or flushing, however, it should not block.</span></span>

<span data-ttu-id="42419-119">Die Blockierung wird von der [**cbaserdenderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md) -Methode gesteuert, die auf zwei Ereignisse wartet: [**cbaserdenderer:: m \_ renderevent**](cbaserenderer-m-renderevent.md) und [**cbasererderer:: m \_ threadsignal**](cbaserenderer-m-threadsignal.md).</span><span class="sxs-lookup"><span data-stu-id="42419-119">The blocking is controlled by the [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method, which waits on two events: [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) and [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md).</span></span> <span data-ttu-id="42419-120">Das **m \_ renderevent** -Ereignis wird signalisiert, wenn die Präsentationszeit erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="42419-120">The **m\_RenderEvent** event is signaled when the presentation time arrives.</span></span> <span data-ttu-id="42419-121">Das **m \_ threadsignal** -Ereignis wird signalisiert, wenn `SourceThreadCanWait` mit dem Wert **false** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="42419-121">The **m\_ThreadSignal** event is signaled when `SourceThreadCanWait` is called with the value **FALSE**.</span></span> <span data-ttu-id="42419-122">`SourceThreadCanWait`Wenn Sie mit dem Wert **true** aufrufen, wird das-Ereignis zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="42419-122">Calling `SourceThreadCanWait` with the value **TRUE** resets the event.</span></span>

<span data-ttu-id="42419-123">Die [**cbaserenderer:: Ende**](cbaserenderer-stop.md) -und [**cbaserenderer:: beginflush**](cbaserenderer-beginflush.md) -Methoden aufrufen `SourceThreadCanWait` mit dem Wert **false** (Freigabe des streaminginthreads).</span><span class="sxs-lookup"><span data-stu-id="42419-123">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call `SourceThreadCanWait` with the value **FALSE** (releasing the streaming thread).</span></span> <span data-ttu-id="42419-124">Der [**cbaserenumderer::P ause**](cbaserenderer-pause.md), [**cbasererderderer:: Run**](cbaserenderer-run.md)-Methode und der [**cbaserderderer:: endflush**](cbaserenderer-endflush.md) -Methodenaufrufe `SourceThreadCanWait` mit dem Wert " **true**".</span><span class="sxs-lookup"><span data-stu-id="42419-124">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md), and [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) methods call `SourceThreadCanWait` with the value **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="42419-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42419-125">Requirements</span></span>



| <span data-ttu-id="42419-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42419-126">Requirement</span></span> | <span data-ttu-id="42419-127">Wert</span><span class="sxs-lookup"><span data-stu-id="42419-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42419-128">Header</span><span class="sxs-lookup"><span data-stu-id="42419-128">Header</span></span><br/>  | <dl> <span data-ttu-id="42419-129"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42419-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42419-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="42419-130">Library</span></span><br/> | <dl> <span data-ttu-id="42419-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="42419-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42419-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42419-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42419-133">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="42419-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




