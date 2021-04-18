---
description: 'Die Methode "beenden" beendet den Filter. Diese Methode implementiert die imediafilter:: stopmethode.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Cbasefilter. stoppt-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371119"
---
# <a name="cbasefilterstop-method"></a><span data-ttu-id="bfcff-104">Cbasefilter. stoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="bfcff-104">CBaseFilter.Stop method</span></span>

<span data-ttu-id="bfcff-105">Die- `Stop` Methode beendet den Filter.</span><span class="sxs-lookup"><span data-stu-id="bfcff-105">The `Stop` method stops the filter.</span></span> <span data-ttu-id="bfcff-106">Diese Methode implementiert die [**imediafilter:: stopmethode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="bfcff-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfcff-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="bfcff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfcff-108">Parameters</span></span>

<span data-ttu-id="bfcff-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bfcff-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfcff-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfcff-110">Return value</span></span>

<span data-ttu-id="bfcff-111">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="bfcff-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfcff-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfcff-112">Remarks</span></span>

<span data-ttu-id="bfcff-113">Diese Methode ruft die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode für jeden verbundenen Pins des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="bfcff-113">This method calls the [**CBasePin::Inactive**](cbasepin-inactive.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="bfcff-114">Außerdem wird der Zustand des Filters auf "beendet" festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="bfcff-114">It also sets the filter's state to State\_Stopped.</span></span>

<span data-ttu-id="bfcff-115">Wenn der Filter angehalten wird, sollte er Beispiele von Upstream ablehnen, die Bereitstellung von Beispielen nach unten beenden, Arbeitsthreads Herunterfahren und alle Ressourcen freigeben, die für das Streaming verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="bfcff-115">When the filter stops, it should reject samples from upstream, stop delivering samples downstream, shut down worker threads, and free any resources that it used for streaming.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfcff-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfcff-116">Requirements</span></span>



| <span data-ttu-id="bfcff-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfcff-117">Requirement</span></span> | <span data-ttu-id="bfcff-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bfcff-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcff-119">Header</span><span class="sxs-lookup"><span data-stu-id="bfcff-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bfcff-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfcff-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bfcff-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bfcff-121">Library</span></span><br/> | <dl> <span data-ttu-id="bfcff-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bfcff-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcff-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfcff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcff-124">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bfcff-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




