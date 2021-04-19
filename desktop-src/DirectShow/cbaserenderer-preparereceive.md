---
description: Die preparereceive-Methode bereitet den Filter zum Rendering eines Beispiels vor.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Cbaserderderer. preparereceive-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367135"
---
# <a name="cbaserendererpreparereceive-method"></a><span data-ttu-id="14bf8-103">Cbaserderderer. preparereceive-Methode</span><span class="sxs-lookup"><span data-stu-id="14bf8-103">CBaseRenderer.PrepareReceive method</span></span>

<span data-ttu-id="14bf8-104">Die- `PrepareReceive` Methode bereitet den Filter zum Rendering eines Beispiels vor.</span><span class="sxs-lookup"><span data-stu-id="14bf8-104">The `PrepareReceive` method prepares the filter to render a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="14bf8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14bf8-105">Syntax</span></span>


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="14bf8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14bf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14bf8-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="14bf8-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="14bf8-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="14bf8-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14bf8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14bf8-109">Return value</span></span>

<span data-ttu-id="14bf8-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="14bf8-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="14bf8-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="14bf8-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="14bf8-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="14bf8-112">Return code</span></span>                                                                                             | <span data-ttu-id="14bf8-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14bf8-113">Description</span></span>                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="14bf8-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf8-114"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="14bf8-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="14bf8-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="14bf8-116"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf8-116"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="14bf8-117">Fehler.</span><span class="sxs-lookup"><span data-stu-id="14bf8-117">Failed.</span></span><br/>                         |
| <dl> <span data-ttu-id="14bf8-118"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf8-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="14bf8-119">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="14bf8-119">Unexpected error.</span></span><br/>               |
| <dl> <span data-ttu-id="14bf8-120"><dt>**VFW \_ E- \_ Beispiel \_ abgelehnt**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf8-120"><dt>**VFW\_E\_SAMPLE\_REJECTED**</dt></span></span> </dl> | <span data-ttu-id="14bf8-121">Das Beispiel wird vom Filter gelöscht.</span><span class="sxs-lookup"><span data-stu-id="14bf8-121">Filter is dropping this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14bf8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14bf8-122">Remarks</span></span>

<span data-ttu-id="14bf8-123">Der Filter ruft diese Methode innerhalb der [**cbaserenderer:: Receive**](cbaserenderer-receive.md) -Methode auf, bevor ein Beispiel gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="14bf8-123">The filter calls this method from inside the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, before it renders a sample.</span></span> <span data-ttu-id="14bf8-124">Wenn der Filter ausgeführt wird, plant diese Methode das Beispiel für das Rendering.</span><span class="sxs-lookup"><span data-stu-id="14bf8-124">If the filter is running, this method schedules the sample for rendering.</span></span>

<span data-ttu-id="14bf8-125">Wenn für den Filter bereits ein ausstehendes Beispiel vorhanden ist, oder wenn das Ende des Streams bereits erreicht wurde, gibt die Methode "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="14bf8-125">If the filter already has a pending sample, or if the end-of-stream was already reached, the method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="14bf8-126">Der Upstream-Filter serialisiert seine Streamingaufrufe möglicherweise nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="14bf8-126">Possibly the upstream filter is not serializing its streaming calls correctly.</span></span>

<span data-ttu-id="14bf8-127">Wenn der Zeit Planungs Algorithmus feststellt, dass das Beispiel gelöscht werden soll (siehe [**cbaserenderer:: schedulesample**](cbaserenderer-schedulesample.md)), gibt die Methode VFW \_ E \_ Sample zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="14bf8-127">If the scheduling algorithm determines that the sample should be dropped (see [**CBaseRenderer::ScheduleSample**](cbaserenderer-schedulesample.md)), the method returns VFW\_E\_SAMPLE\_REJECTED.</span></span> <span data-ttu-id="14bf8-128">Die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode der Eingabe-PIN übergibt diesen Fehlercode jedoch nicht an den upstreamfilter, da das Ablegen eines Beispiels kein Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="14bf8-128">However, the input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method does not pass this error code to the upstream filter, because dropping a sample is not an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="14bf8-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14bf8-129">Requirements</span></span>



| <span data-ttu-id="14bf8-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14bf8-130">Requirement</span></span> | <span data-ttu-id="14bf8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="14bf8-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14bf8-132">Header</span><span class="sxs-lookup"><span data-stu-id="14bf8-132">Header</span></span><br/>  | <dl> <span data-ttu-id="14bf8-133"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14bf8-133"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="14bf8-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14bf8-134">Library</span></span><br/> | <dl> <span data-ttu-id="14bf8-135">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="14bf8-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14bf8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14bf8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bf8-137">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="14bf8-137">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




