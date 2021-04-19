---
description: Die setfiltergraph-Methode gibt die Ereignis Senke für streamsteuerungsereignisse an.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Cbasestreamcontrol. setfiltergraph-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363208"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a><span data-ttu-id="44582-103">Cbasestreamcontrol. setfiltergraph-Methode</span><span class="sxs-lookup"><span data-stu-id="44582-103">CBaseStreamControl.SetFilterGraph method</span></span>

<span data-ttu-id="44582-104">Die- `SetFilterGraph` Methode gibt die Ereignis Senke für streamsteuerungsereignisse an.</span><span class="sxs-lookup"><span data-stu-id="44582-104">The `SetFilterGraph` method specifies the event sink for stream control events.</span></span>

## <a name="syntax"></a><span data-ttu-id="44582-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44582-105">Syntax</span></span>


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="44582-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44582-107">*psink*</span><span class="sxs-lookup"><span data-stu-id="44582-107">*pSink*</span></span> 
</dt> <dd>

<span data-ttu-id="44582-108">Ein Zeiger auf die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle des Filter Diagramm-Managers oder **null** , wenn der Filter das Filter Diagramm verlässt.</span><span class="sxs-lookup"><span data-stu-id="44582-108">Pointer to the Filter Graph Manager's [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, or **NULL** when the filter leaves the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44582-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44582-109">Return value</span></span>

<span data-ttu-id="44582-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="44582-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44582-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44582-111">Remarks</span></span>

<span data-ttu-id="44582-112">Diese Methode wird innerhalb der [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode des Filters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="44582-112">Call this method from inside the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="44582-113">Die **cbasestreamcontrol** -Klasse verwendet die **imediaeventsink** -Schnittstelle, um das [**gestartete EC- \_ Stream- \_ Steuer \_**](ec-stream-control-started.md) Element zu senden, und Ereignisse, die von der [**\_ \_ \_**](ec-stream-control-stopped.md)</span><span class="sxs-lookup"><span data-stu-id="44582-113">The **CBaseStreamControl** class uses the **IMediaEventSink** interface to send [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) events.</span></span>

<span data-ttu-id="44582-114">Wenn der Filter von **cbasefilter** abgeleitet ist, müssen Sie zuerst die [**cbasefilter:: joinfiltergraph**](cbasefilter-joinfiltergraph.md) -Methode aufzurufen, mit der die [**cbasefilter:: m \_ psink**](cbasefilter-m-psink.md) -Element Variable festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="44582-114">If your filter derives from **CBaseFilter**, first call the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, which sets the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="44582-115">Übergeben Sie dann **m \_ psink** an die- `SetFilterGraph` Methode.</span><span class="sxs-lookup"><span data-stu-id="44582-115">Then pass **m\_pSink** to the `SetFilterGraph` method.</span></span> <span data-ttu-id="44582-116">Beachten Sie, dass **m \_ psink** **null** ist, wenn der Filter das Diagramm verlässt, was korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="44582-116">Note that **m\_pSink** is **NULL** when the filter leaves the graph, which is correct.</span></span>

## <a name="examples"></a><span data-ttu-id="44582-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44582-117">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="44582-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44582-118">Requirements</span></span>



| <span data-ttu-id="44582-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44582-119">Requirement</span></span> | <span data-ttu-id="44582-120">Wert</span><span class="sxs-lookup"><span data-stu-id="44582-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44582-121">Header</span><span class="sxs-lookup"><span data-stu-id="44582-121">Header</span></span><br/>  | <dl> <span data-ttu-id="44582-122"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44582-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44582-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44582-123">Library</span></span><br/> | <dl> <span data-ttu-id="44582-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="44582-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44582-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44582-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44582-126">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="44582-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




