---
description: Die reconnectpin-Methode unterbricht eine vorhandene Pin-Verbindung und verbindet Sie mit dem gleichen PIN, wobei ein angegebener Medientyp verwendet wird.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Cbasefilter. reconnectpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369525"
---
# <a name="cbasefilterreconnectpin-method"></a><span data-ttu-id="e06b3-103">Cbasefilter. reconnectpin-Methode</span><span class="sxs-lookup"><span data-stu-id="e06b3-103">CBaseFilter.ReconnectPin method</span></span>

<span data-ttu-id="e06b3-104">Die `ReconnectPin` -Methode unterbricht eine vorhandene Pin-Verbindung und verbindet Sie mit dem gleichen PIN, wobei ein angegebener Medientyp verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e06b3-104">The `ReconnectPin` method breaks an existing pin connection and reconnects it to the same pin, using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e06b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e06b3-105">Syntax</span></span>


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e06b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e06b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e06b3-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="e06b3-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="e06b3-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN.</span><span class="sxs-lookup"><span data-stu-id="e06b3-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e06b3-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="e06b3-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e06b3-110">Ein Zeiger auf eine [**am- \_ Medientyp \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e06b3-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e06b3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e06b3-111">Return value</span></span>

<span data-ttu-id="e06b3-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e06b3-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e06b3-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="e06b3-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e06b3-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e06b3-114">Return code</span></span>                                                                                   | <span data-ttu-id="e06b3-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e06b3-115">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e06b3-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e06b3-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e06b3-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e06b3-117">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="e06b3-118"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="e06b3-118"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="e06b3-119">die [**m- \_ PGraph**](cbasefilter-m-pgraph.md) -Element Variable ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e06b3-119">[**m\_pGraph**](cbasefilter-m-pgraph.md) member variable is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e06b3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e06b3-120">Remarks</span></span>

<span data-ttu-id="e06b3-121">Diese Methode ruft die [**IFilterGraph2:: reconnectex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) -Methode für den Filter Graph-Manager auf.</span><span class="sxs-lookup"><span data-stu-id="e06b3-121">This method calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span> <span data-ttu-id="e06b3-122">Wenn die [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) -Schnittstelle nicht verfügbar ist, ruft die-Methode [**ifiltergraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect)auf.</span><span class="sxs-lookup"><span data-stu-id="e06b3-122">If the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface is not available, the method calls [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span></span>

## <a name="requirements"></a><span data-ttu-id="e06b3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e06b3-123">Requirements</span></span>



| <span data-ttu-id="e06b3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e06b3-124">Requirement</span></span> | <span data-ttu-id="e06b3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e06b3-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e06b3-126">Header</span><span class="sxs-lookup"><span data-stu-id="e06b3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e06b3-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e06b3-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e06b3-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e06b3-128">Library</span></span><br/> | <dl> <span data-ttu-id="e06b3-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e06b3-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e06b3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e06b3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e06b3-131">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e06b3-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




