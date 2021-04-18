---
description: Die signaltimerfired-Methode löscht den Zeit Geber Bezeichner, der zum Planen des Rendering verwendet wurde.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Cbaserderderer. signaltimerfired-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364528"
---
# <a name="cbaserenderersignaltimerfired-method"></a><span data-ttu-id="f9406-103">Cbaserderderer. signaltimerfired-Methode</span><span class="sxs-lookup"><span data-stu-id="f9406-103">CBaseRenderer.SignalTimerFired method</span></span>

<span data-ttu-id="f9406-104">Die- `SignalTimerFired` Methode löscht den Zeit Geber Bezeichner, der für die Zeit Plan Rendering</span><span class="sxs-lookup"><span data-stu-id="f9406-104">The `SignalTimerFired` method clears the timer identifier used to schedule rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9406-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9406-105">Syntax</span></span>


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a><span data-ttu-id="f9406-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9406-106">Parameters</span></span>

<span data-ttu-id="f9406-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9406-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9406-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9406-108">Return value</span></span>

<span data-ttu-id="f9406-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f9406-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9406-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9406-110">Remarks</span></span>

<span data-ttu-id="f9406-111">Der Filter ruft diese Methode auf, wenn der rendertimer aktiviert wird (siehe [**cbaserenderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md)) oder wenn der Timer abgebrochen wird (siehe [**cbaserenderer:: cancelnotification**](cbaserenderer-cancelnotification.md)).</span><span class="sxs-lookup"><span data-stu-id="f9406-111">The filter calls this method when the rendering timer activates (see [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) or when the timer is canceled (see [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)).</span></span> <span data-ttu-id="f9406-112">Die-Methode setzt die Element Variable [**cbaserenderer:: m \_ DW-**](cbaserenderer-m-dwadvise.md) Member auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="f9406-112">The method resets the [**CBaseRenderer::m\_dwAdvise**](cbaserenderer-m-dwadvise.md) member variable to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9406-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9406-113">Requirements</span></span>



| <span data-ttu-id="f9406-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9406-114">Requirement</span></span> | <span data-ttu-id="f9406-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f9406-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9406-116">Header</span><span class="sxs-lookup"><span data-stu-id="f9406-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f9406-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9406-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9406-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9406-118">Library</span></span><br/> | <dl> <span data-ttu-id="f9406-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f9406-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9406-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9406-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9406-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f9406-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




