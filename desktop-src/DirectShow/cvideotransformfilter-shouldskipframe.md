---
description: Die Methode "schuldskipframe" bestimmt, ob der Filter eine angegebene Stichprobe löschen soll.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Cvideotransformfilter. schuldskipframe-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357561"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a><span data-ttu-id="59547-103">Cvideotransformfilter. schuldskipframe-Methode</span><span class="sxs-lookup"><span data-stu-id="59547-103">CVideoTransformFilter.ShouldSkipFrame method</span></span>

<span data-ttu-id="59547-104">Die- `ShouldSkipFrame` Methode bestimmt, ob der Filter eine angegebene Stichprobe löschen soll.</span><span class="sxs-lookup"><span data-stu-id="59547-104">The `ShouldSkipFrame` method determines whether the filter should drop a specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="59547-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59547-105">Syntax</span></span>


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="59547-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59547-107">*kehren*</span><span class="sxs-lookup"><span data-stu-id="59547-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="59547-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="59547-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59547-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59547-109">Return value</span></span>

<span data-ttu-id="59547-110">Gibt " **true** " zurück, wenn der Filter dieses Beispiel löschen soll, oder " **false** ", wenn der Filter dieses Beispiel verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="59547-110">Returns **TRUE** if the filter should drop this sample, or **FALSE** if the filter should process this sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="59547-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59547-111">Remarks</span></span>

<span data-ttu-id="59547-112">Diese Methode gibt " **true** " zurück, wenn die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="59547-112">This method returns **TRUE** if the following conditions are met:</span></span>

-   <span data-ttu-id="59547-113">Das Beispiel enthält Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="59547-113">The sample has time stamps.</span></span>
-   <span data-ttu-id="59547-114">Die durchschnittliche Decodierungs Zeit beträgt mindestens 25% der Rahmen Dauer.</span><span class="sxs-lookup"><span data-stu-id="59547-114">The average decoding time is at least 25% of the frame duration.</span></span>
-   <span data-ttu-id="59547-115">Der Renderer ist zurzeit mindestens ein Frame spät, wie er über Qualitäts Meldungen gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="59547-115">The renderer is currently at least one frame late, as reported through quality messages.</span></span>
-   <span data-ttu-id="59547-116">Das überspringen zum nächsten Keyframe bewirkt nicht, dass der Frame frühzeitig mehr als einen Frame antrifft.</span><span class="sxs-lookup"><span data-stu-id="59547-116">Skipping to the next key frame would not cause the frame to arrive more than one frame early.</span></span>

<span data-ttu-id="59547-117">Im Rahmen dieser Berechnung zeichnet der Filter bei der Verarbeitung von Daten die folgenden Informationen auf:</span><span class="sxs-lookup"><span data-stu-id="59547-117">For purposes of this calculation, the filter records the following information as it processes data:</span></span>

-   <span data-ttu-id="59547-118">Die durchschnittliche Decodierungs Zeit in den letzten 20 Frames (**m \_ itravgdecode**)</span><span class="sxs-lookup"><span data-stu-id="59547-118">The average decoding time over the past 20 frames (**m\_itrAvgDecode**)</span></span>
-   <span data-ttu-id="59547-119">Die Anzahl der Frames seit dem letzten **Keyframe (m \_ nframessincekeyframe**).</span><span class="sxs-lookup"><span data-stu-id="59547-119">The number of frames since the last key frame (**m\_nFramesSinceKeyFrame**)</span></span>
-   <span data-ttu-id="59547-120">Eine Schätzung der Anzahl von Frames zwischen **\_ Keyframes (m nkeyframeperiod**)</span><span class="sxs-lookup"><span data-stu-id="59547-120">An estimate of how many frames there are between key frames (**m\_nKeyFramePeriod**)</span></span>

<span data-ttu-id="59547-121">Nachdem der Filter einen Frame gelöscht hat, wird er fortgesetzt, bis er den nächsten Keyframe erreicht.</span><span class="sxs-lookup"><span data-stu-id="59547-121">Once the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="59547-122">Wenn diese Methode **true** zurückgibt, sendet Sie auch ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="59547-122">If this method returns **TRUE**, it also sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the Filter Graph Manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="59547-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59547-123">Requirements</span></span>



| <span data-ttu-id="59547-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59547-124">Requirement</span></span> | <span data-ttu-id="59547-125">Wert</span><span class="sxs-lookup"><span data-stu-id="59547-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59547-126">Header</span><span class="sxs-lookup"><span data-stu-id="59547-126">Header</span></span><br/>  | <dl> <span data-ttu-id="59547-127"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59547-127"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="59547-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59547-128">Library</span></span><br/> | <dl> <span data-ttu-id="59547-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="59547-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59547-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59547-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59547-131">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="59547-131">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




