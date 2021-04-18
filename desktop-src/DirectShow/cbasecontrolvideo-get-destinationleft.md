---
description: Die get \_ destinationleft-Methode ruft die linke Koordinate des aktuellen Ziel Rechtecks ab.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: CBaseControlVideo.get_DestinationLeft-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f433d880fd7f568a173a91c533e0d07bf97e6443
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364681"
---
# <a name="cbasecontrolvideoget_destinationleft-method"></a><span data-ttu-id="5d11b-103">Cbasecontrolvideo. get \_ destinationleft-Methode</span><span class="sxs-lookup"><span data-stu-id="5d11b-103">CBaseControlVideo.get\_DestinationLeft method</span></span>

<span data-ttu-id="5d11b-104">Die- `get_DestinationLeft` Methode ruft die linke Koordinate des aktuellen Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="5d11b-104">The `get_DestinationLeft` method retrieves the left coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d11b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d11b-105">Syntax</span></span>


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## <a name="parameters"></a><span data-ttu-id="5d11b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d11b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d11b-107">*pdestinationleft*</span><span class="sxs-lookup"><span data-stu-id="5d11b-107">*pDestinationLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="5d11b-108">Ein Zeiger auf die linke Koordinate des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="5d11b-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d11b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d11b-109">Return value</span></span>

<span data-ttu-id="5d11b-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5d11b-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="5d11b-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5d11b-111">Return code</span></span>                                                                                           | <span data-ttu-id="5d11b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d11b-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d11b-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="5d11b-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="5d11b-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="5d11b-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="5d11b-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="5d11b-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5d11b-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="5d11b-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5d11b-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="5d11b-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5d11b-118">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="5d11b-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="5d11b-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="5d11b-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="5d11b-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5d11b-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="5d11b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d11b-121">Remarks</span></span>

<span data-ttu-id="5d11b-122">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ destinationleft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5d11b-122">This member function implements the [**IBasicVideo::get\_DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) method.</span></span>

<span data-ttu-id="5d11b-123">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="5d11b-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="5d11b-124">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5d11b-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="5d11b-125">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="5d11b-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="5d11b-126">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="5d11b-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d11b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d11b-127">Requirements</span></span>



| <span data-ttu-id="5d11b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d11b-128">Requirement</span></span> | <span data-ttu-id="5d11b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5d11b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d11b-130">Header</span><span class="sxs-lookup"><span data-stu-id="5d11b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5d11b-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d11b-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d11b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d11b-132">Library</span></span><br/> | <dl> <span data-ttu-id="5d11b-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5d11b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d11b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d11b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d11b-135">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5d11b-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




