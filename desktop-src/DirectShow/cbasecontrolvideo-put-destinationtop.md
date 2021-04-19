---
description: Mit der Put \_ destinationtop-Methode wird die obere Koordinate des Ziel Rechtecks festgelegt.
ms.assetid: d18996ac-85f2-4778-b0aa-1bc0c4d5f7d9
title: CBaseControlVideo.put_DestinationTop-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c89e4693d424412a43869509e046a5023e76341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369130"
---
# <a name="cbasecontrolvideoput_destinationtop-method"></a><span data-ttu-id="eafa2-103">Cbasecontrolvideo. Put \_ destinationtop-Methode</span><span class="sxs-lookup"><span data-stu-id="eafa2-103">CBaseControlVideo.put\_DestinationTop method</span></span>

<span data-ttu-id="eafa2-104">Die- `put_DestinationTop` Methode legt die obere Koordinate des Ziel Rechtecks fest.</span><span class="sxs-lookup"><span data-stu-id="eafa2-104">The `put_DestinationTop` method sets the top coordinate of the destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="eafa2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eafa2-105">Syntax</span></span>


```C++
HRESULT put_DestinationTop(
   long DestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="eafa2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eafa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafa2-107">*Destinationtop*</span><span class="sxs-lookup"><span data-stu-id="eafa2-107">*DestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="eafa2-108">Neue obere Koordinate des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="eafa2-108">New top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eafa2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eafa2-109">Return value</span></span>

<span data-ttu-id="eafa2-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="eafa2-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="eafa2-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eafa2-111">Return code</span></span>                                                                                           | <span data-ttu-id="eafa2-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eafa2-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eafa2-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="eafa2-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="eafa2-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="eafa2-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="eafa2-115"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="eafa2-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="eafa2-116">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="eafa2-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="eafa2-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="eafa2-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="eafa2-118">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="eafa2-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="eafa2-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="eafa2-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="eafa2-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="eafa2-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="eafa2-121"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="eafa2-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="eafa2-122">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="eafa2-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eafa2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eafa2-123">Remarks</span></span>

<span data-ttu-id="eafa2-124">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="eafa2-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="eafa2-125">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eafa2-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="eafa2-126">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="eafa2-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="eafa2-127">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="eafa2-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="eafa2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eafa2-128">Requirements</span></span>



| <span data-ttu-id="eafa2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eafa2-129">Requirement</span></span> | <span data-ttu-id="eafa2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="eafa2-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eafa2-131">Header</span><span class="sxs-lookup"><span data-stu-id="eafa2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="eafa2-132"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eafa2-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eafa2-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eafa2-133">Library</span></span><br/> | <dl> <span data-ttu-id="eafa2-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eafa2-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eafa2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eafa2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eafa2-136">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eafa2-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




