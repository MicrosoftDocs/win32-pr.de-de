---
description: Die resetstreamingtimes-Methode setzt alle Zeiten zurück, die das Streaming steuern.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Cbasevideorenderer. resetstreamingtimes-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373640"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a><span data-ttu-id="024d7-103">Cbasevideorenderer. resetstreamingtimes-Methode</span><span class="sxs-lookup"><span data-stu-id="024d7-103">CBaseVideoRenderer.ResetStreamingTimes method</span></span>

<span data-ttu-id="024d7-104">Die- `ResetStreamingTimes` Methode setzt alle Zeiten zurück, die das Streaming steuern.</span><span class="sxs-lookup"><span data-stu-id="024d7-104">The `ResetStreamingTimes` method resets all times that control the streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="024d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="024d7-105">Syntax</span></span>


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a><span data-ttu-id="024d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="024d7-106">Parameters</span></span>

<span data-ttu-id="024d7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="024d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="024d7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="024d7-108">Return value</span></span>

<span data-ttu-id="024d7-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="024d7-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="024d7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="024d7-110">Remarks</span></span>

<span data-ttu-id="024d7-111">Die Uhrzeiten werden so festgelegt, dass Frames nicht anfänglich abgelegt werden und dass der erste Frame gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="024d7-111">The times are set so that frames will not be initially dropped and so that the first frame will be drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="024d7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="024d7-112">Requirements</span></span>



| <span data-ttu-id="024d7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="024d7-113">Requirement</span></span> | <span data-ttu-id="024d7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="024d7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024d7-115">Header</span><span class="sxs-lookup"><span data-stu-id="024d7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="024d7-116"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="024d7-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="024d7-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="024d7-117">Library</span></span><br/> | <dl> <span data-ttu-id="024d7-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="024d7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024d7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="024d7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024d7-120">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="024d7-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




