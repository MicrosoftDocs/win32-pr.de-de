---
description: Die onreceivefirstsample-Methode wird aufgerufen, wenn der Filter eine Stichprobe empfängt, während Sie angehalten wird.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Cbaserderderer. onreceivefirstsample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371788"
---
# <a name="cbaserendereronreceivefirstsample-method"></a><span data-ttu-id="c2b22-103">Cbaserderderer. onreceivefirstsample-Methode</span><span class="sxs-lookup"><span data-stu-id="c2b22-103">CBaseRenderer.OnReceiveFirstSample method</span></span>

<span data-ttu-id="c2b22-104">Die- `OnReceiveFirstSample` Methode wird aufgerufen, wenn der Filter eine Stichprobe empfängt, während Sie angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c2b22-104">The `OnReceiveFirstSample` method is called when the filter receives a sample while paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2b22-105">Syntax</span></span>


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c2b22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2b22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2b22-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="c2b22-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c2b22-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="c2b22-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2b22-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2b22-109">Return value</span></span>

<span data-ttu-id="c2b22-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c2b22-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2b22-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2b22-111">Remarks</span></span>

<span data-ttu-id="c2b22-112">Die [**cbaserdenderer:: Receive**](cbaserenderer-receive.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="c2b22-112">The [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method calls this method.</span></span> <span data-ttu-id="c2b22-113">Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c2b22-113">It does nothing in the base class, but the derived class can override it.</span></span> <span data-ttu-id="c2b22-114">Diese Methode ist hauptsächlich für Videorenderer vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c2b22-114">This method is intended primarily for video renderers.</span></span> <span data-ttu-id="c2b22-115">Wenn ein Videorenderer angehalten wird, wird das erste Beispiel in der Regel als Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c2b22-115">When a video renderer is paused, it typically displays the first sample as a still image.</span></span>

<span data-ttu-id="c2b22-116">Wenn Sie das Diagramm im angehaltenen Zustand suchen, wird auch diese Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c2b22-116">Seeking the graph while paused also causes this method to be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b22-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2b22-117">Requirements</span></span>



| <span data-ttu-id="c2b22-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2b22-118">Requirement</span></span> | <span data-ttu-id="c2b22-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c2b22-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b22-120">Header</span><span class="sxs-lookup"><span data-stu-id="c2b22-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c2b22-121"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2b22-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2b22-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2b22-122">Library</span></span><br/> | <dl> <span data-ttu-id="c2b22-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c2b22-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2b22-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2b22-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b22-125">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c2b22-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




