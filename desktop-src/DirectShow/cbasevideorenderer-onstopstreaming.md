---
description: Die onstopstreaming-Methode wird am Ende des Streamings aufgerufen, um die Zeit für den Bericht der Eigenschaften Seite zu korrigieren.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Cbasevideorenderer. onstopstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368312"
---
# <a name="cbasevideorendereronstopstreaming-method"></a><span data-ttu-id="85eac-103">Cbasevideorenderer. onstopstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="85eac-103">CBaseVideoRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="85eac-104">Die- `OnStopStreaming` Methode wird am Ende des Streamings aufgerufen, um die Zeit für den Bericht der Eigenschaften Seite zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="85eac-104">The `OnStopStreaming` method is called at the end of streaming to fix times for the property page report.</span></span>

## <a name="syntax"></a><span data-ttu-id="85eac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85eac-105">Syntax</span></span>


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="85eac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85eac-106">Parameters</span></span>

<span data-ttu-id="85eac-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="85eac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85eac-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85eac-108">Return value</span></span>

<span data-ttu-id="85eac-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="85eac-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85eac-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85eac-110">Remarks</span></span>

<span data-ttu-id="85eac-111">Diese Member-Funktion wird zweimal aufgerufen, einmal beim Anhalten und wiederholen, wenn der Stream tatsächlich angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="85eac-111">This member function is called twice, once when pausing and again when the stream is actually stopped.</span></span>

<span data-ttu-id="85eac-112">Diese Member-Funktion überschreibt [**cbaserenderer:: onstopstreaming**](cbaserenderer-onstopstreaming.md).</span><span class="sxs-lookup"><span data-stu-id="85eac-112">This member function overrides [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85eac-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85eac-113">Requirements</span></span>



| <span data-ttu-id="85eac-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85eac-114">Requirement</span></span> | <span data-ttu-id="85eac-115">Wert</span><span class="sxs-lookup"><span data-stu-id="85eac-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85eac-116">Header</span><span class="sxs-lookup"><span data-stu-id="85eac-116">Header</span></span><br/>  | <dl> <span data-ttu-id="85eac-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85eac-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85eac-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85eac-118">Library</span></span><br/> | <dl> <span data-ttu-id="85eac-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="85eac-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85eac-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85eac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85eac-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="85eac-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




