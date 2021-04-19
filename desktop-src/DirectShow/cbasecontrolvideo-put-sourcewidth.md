---
description: Mit der Put \_ sourceWidth-Methode wird die Breite des Quell Rechtecks festgelegt.
ms.assetid: 0becea4f-e47e-4f64-ab95-0ee333ad48f3
title: CBaseControlVideo.put_SourceWidth-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1576389a90db71ee6d371f6e68c44ea39117c05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366907"
---
# <a name="cbasecontrolvideoput_sourcewidth-method"></a><span data-ttu-id="e274a-103">Cbasecontrolvideo. Put \_ sourceWidth-Methode</span><span class="sxs-lookup"><span data-stu-id="e274a-103">CBaseControlVideo.put\_SourceWidth method</span></span>

<span data-ttu-id="e274a-104">Die- `put_SourceWidth` Methode legt die Breite des Quell Rechtecks fest.</span><span class="sxs-lookup"><span data-stu-id="e274a-104">The `put_SourceWidth` method sets the width of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e274a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e274a-105">Syntax</span></span>


```C++
HRESULT put_SourceWidth(
   long SourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="e274a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e274a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e274a-107">*SourceWidth*</span><span class="sxs-lookup"><span data-stu-id="e274a-107">*SourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="e274a-108">Die neue Breite des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="e274a-108">New width of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e274a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e274a-109">Return value</span></span>

<span data-ttu-id="e274a-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e274a-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="e274a-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e274a-111">Return code</span></span>                                                                                           | <span data-ttu-id="e274a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e274a-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e274a-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="e274a-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="e274a-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="e274a-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="e274a-115"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e274a-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="e274a-116">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="e274a-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="e274a-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e274a-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="e274a-118">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="e274a-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="e274a-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="e274a-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="e274a-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e274a-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="e274a-121"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="e274a-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e274a-122">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="e274a-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e274a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e274a-123">Remarks</span></span>

<span data-ttu-id="e274a-124">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="e274a-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="e274a-125">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e274a-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="e274a-126">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="e274a-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="e274a-127">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="e274a-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="e274a-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e274a-128">Requirements</span></span>



| <span data-ttu-id="e274a-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e274a-129">Requirement</span></span> | <span data-ttu-id="e274a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e274a-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e274a-131">Header</span><span class="sxs-lookup"><span data-stu-id="e274a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="e274a-132"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e274a-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e274a-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e274a-133">Library</span></span><br/> | <dl> <span data-ttu-id="e274a-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e274a-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e274a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e274a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e274a-136">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e274a-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




