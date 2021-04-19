---
description: Die sendquality-Methode sendet eine Qualitäts Meldung, um anzugeben, was der Lieferant mit der Qualität tun soll.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Cbasevideorenderer. sendquality-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369418"
---
# <a name="cbasevideorenderersendquality-method"></a><span data-ttu-id="5dd66-103">Cbasevideorenderer. sendquality-Methode</span><span class="sxs-lookup"><span data-stu-id="5dd66-103">CBaseVideoRenderer.SendQuality method</span></span>

<span data-ttu-id="5dd66-104">Die- `SendQuality` Methode sendet eine Qualitäts Meldung, um anzugeben, was der Lieferant mit der Qualität tun soll.</span><span class="sxs-lookup"><span data-stu-id="5dd66-104">The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dd66-105">Syntax</span></span>


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a><span data-ttu-id="5dd66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dd66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd66-107">*trlate*</span><span class="sxs-lookup"><span data-stu-id="5dd66-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="5dd66-108">Die Zeitspanne, nach der der Rahmen spät ist.</span><span class="sxs-lookup"><span data-stu-id="5dd66-108">Amount of time by which the frame is late.</span></span>

</dd> <dt>

<span data-ttu-id="5dd66-109">*trrealstream*</span><span class="sxs-lookup"><span data-stu-id="5dd66-109">*trRealStream*</span></span> 
</dt> <dd>

<span data-ttu-id="5dd66-110">Currentstream-Zeit.</span><span class="sxs-lookup"><span data-stu-id="5dd66-110">Currentstream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd66-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5dd66-111">Return value</span></span>

<span data-ttu-id="5dd66-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5dd66-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd66-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dd66-113">Remarks</span></span>

<span data-ttu-id="5dd66-114">Diese Member-Funktion sendet eine Qualitäts Steuerungs Nachricht zum Steuern der Qualitäts Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="5dd66-114">This member function sends a quality control message upstream to control quality management.</span></span> <span data-ttu-id="5dd66-115">Die Art der Qualitäts Meldung (d. h., ob die Anzahl der Stichproben reduziert oder erhöht werden soll) wird in der Quality Management-Implementierung in dieser abgeleiteten Klasse festgelegt (siehe [**cbasevideorenderer:: schulddrawsamplenow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span><span class="sxs-lookup"><span data-stu-id="5dd66-115">The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd66-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5dd66-116">Requirements</span></span>



| <span data-ttu-id="5dd66-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5dd66-117">Requirement</span></span> | <span data-ttu-id="5dd66-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5dd66-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd66-119">Header</span><span class="sxs-lookup"><span data-stu-id="5dd66-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5dd66-120"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dd66-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5dd66-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5dd66-121">Library</span></span><br/> | <dl> <span data-ttu-id="5dd66-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5dd66-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dd66-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd66-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd66-124">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5dd66-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




