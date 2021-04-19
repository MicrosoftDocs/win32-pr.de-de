---
description: Die Benachrichtigungs Methode erhält eine Benachrichtigung, dass eine Qualitätsänderung angefordert wird.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Cbasevideorenderer. Notify-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356402"
---
# <a name="cbasevideorenderernotify-method"></a><span data-ttu-id="aced1-103">Cbasevideorenderer. Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="aced1-103">CBaseVideoRenderer.Notify method</span></span>

<span data-ttu-id="aced1-104">Die- `Notify` Methode empfängt eine Benachrichtigung, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="aced1-104">The `Notify` method receives a notification that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="aced1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aced1-105">Syntax</span></span>


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="aced1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aced1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aced1-107">*pself* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aced1-107">*pSelf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aced1-108">Zeiger auf den Filter, der die Qualitäts Benachrichtigung sendet.</span><span class="sxs-lookup"><span data-stu-id="aced1-108">Pointer to the filter that is sending the quality notification.</span></span>

</dd> <dt>

<span data-ttu-id="aced1-109">*q* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aced1-109">*q* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aced1-110">Qualitätsbenachrichtigungs-Struktur.</span><span class="sxs-lookup"><span data-stu-id="aced1-110">Quality notification structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aced1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aced1-111">Return value</span></span>

<span data-ttu-id="aced1-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="aced1-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aced1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aced1-113">Remarks</span></span>

<span data-ttu-id="aced1-114">Diese Member-Funktion implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode für den Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="aced1-114">This member function implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method on the video renderer.</span></span> <span data-ttu-id="aced1-115">Dies wird in der Regel vom Filter Graph-Manager aufgerufen, wenn die Qualität gekürzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="aced1-115">This is called, typically by the filter graph manager, when the quality must be cut back.</span></span> <span data-ttu-id="aced1-116">Dies kann vorkommen, wenn die Qualität der Audiowiedergabe auf den Punkt angehoben wurde, an dem die Qualität der Videowiedergabe gesenkt werden muss.</span><span class="sxs-lookup"><span data-stu-id="aced1-116">This might occur when the quality of audio playback has been increased to the point that the video playback quality must be decreased.</span></span>

<span data-ttu-id="aced1-117">`Notify` Legt den **m \_ trthrottle** -Datenmember auf einen Verzögerungswert fest, der durch [**throttlewait**](cbasevideorenderer-throttlewait.md)zwischen Frames eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aced1-117">`Notify` sets the **m\_trThrottle** data member to a delay value to be inserted between frames by [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aced1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aced1-118">Requirements</span></span>



| <span data-ttu-id="aced1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aced1-119">Requirement</span></span> | <span data-ttu-id="aced1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="aced1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aced1-121">Header</span><span class="sxs-lookup"><span data-stu-id="aced1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="aced1-122"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aced1-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aced1-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aced1-123">Library</span></span><br/> | <dl> <span data-ttu-id="aced1-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aced1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aced1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aced1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aced1-126">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aced1-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




