---
description: Die get \_ sourceWidth-Methode ruft die Breite des aktuellen Quell Rechtecks ab.
ms.assetid: e8e27f8f-57e5-489c-aae7-86493677b380
title: CBaseControlVideo.get_SourceWidth-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60a78fe647ebf488a47907c058962f13790f2538
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369508"
---
# <a name="cbasecontrolvideoget_sourcewidth-method"></a><span data-ttu-id="b498a-103">Cbasecontrolvideo. get \_ sourceWidth-Methode</span><span class="sxs-lookup"><span data-stu-id="b498a-103">CBaseControlVideo.get\_SourceWidth method</span></span>

<span data-ttu-id="b498a-104">Die- `get_SourceWidth` Methode ruft die Breite des aktuellen Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="b498a-104">The `get_SourceWidth` method retrieves the width of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b498a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b498a-105">Syntax</span></span>


```C++
HRESULT get_SourceWidth(
   long *pSourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="b498a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b498a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b498a-107">*psourcewidth*</span><span class="sxs-lookup"><span data-stu-id="b498a-107">*pSourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="b498a-108">Ein Zeiger auf die Breite des aktuellen Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="b498a-108">Pointer to the width of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b498a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b498a-109">Return value</span></span>

<span data-ttu-id="b498a-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b498a-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="b498a-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b498a-111">Return code</span></span>                                                                                           | <span data-ttu-id="b498a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b498a-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b498a-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="b498a-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="b498a-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="b498a-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b498a-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b498a-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="b498a-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="b498a-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b498a-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="b498a-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b498a-118">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="b498a-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="b498a-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="b498a-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="b498a-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b498a-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b498a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b498a-121">Remarks</span></span>

<span data-ttu-id="b498a-122">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ sourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b498a-122">This member function implements the [**IBasicVideo::get\_SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) method.</span></span>

<span data-ttu-id="b498a-123">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="b498a-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="b498a-124">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b498a-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="b498a-125">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="b498a-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="b498a-126">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="b498a-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b498a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b498a-127">Requirements</span></span>



| <span data-ttu-id="b498a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b498a-128">Requirement</span></span> | <span data-ttu-id="b498a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b498a-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b498a-130">Header</span><span class="sxs-lookup"><span data-stu-id="b498a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b498a-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b498a-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b498a-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b498a-132">Library</span></span><br/> | <dl> <span data-ttu-id="b498a-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b498a-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b498a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b498a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b498a-135">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b498a-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




