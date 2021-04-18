---
description: Die get \_ destinationtop-Methode ruft die obere Koordinate des aktuellen Ziel Rechtecks ab.
ms.assetid: 8d5c1361-18db-4ea1-a507-781397189630
title: CBaseControlVideo.get_DestinationTop-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2c7d450c50b11186546a25ceebd317a308dd805
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371093"
---
# <a name="cbasecontrolvideoget_destinationtop-method"></a><span data-ttu-id="0f08e-103">Cbasecontrolvideo. get \_ destinationtop-Methode</span><span class="sxs-lookup"><span data-stu-id="0f08e-103">CBaseControlVideo.get\_DestinationTop method</span></span>

<span data-ttu-id="0f08e-104">Die- `get_DestinationTop` Methode ruft die obere Koordinate des aktuellen Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="0f08e-104">The `get_DestinationTop` method retrieves the top coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f08e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f08e-105">Syntax</span></span>


```C++
HRESULT get_DestinationTop(
   long *pDestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="0f08e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f08e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f08e-107">*pdestinationtop*</span><span class="sxs-lookup"><span data-stu-id="0f08e-107">*pDestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="0f08e-108">Ein Zeiger auf die obere Koordinate des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="0f08e-108">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f08e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f08e-109">Return value</span></span>

<span data-ttu-id="0f08e-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0f08e-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="0f08e-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0f08e-111">Return code</span></span>                                                                                           | <span data-ttu-id="0f08e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f08e-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f08e-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="0f08e-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="0f08e-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="0f08e-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="0f08e-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0f08e-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="0f08e-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="0f08e-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0f08e-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="0f08e-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0f08e-118">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="0f08e-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="0f08e-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="0f08e-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="0f08e-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0f08e-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="0f08e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f08e-121">Remarks</span></span>

<span data-ttu-id="0f08e-122">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ destinationtop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0f08e-122">This member function implements the [**IBasicVideo::get\_DestinationTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) method.</span></span>

<span data-ttu-id="0f08e-123">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="0f08e-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="0f08e-124">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0f08e-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="0f08e-125">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="0f08e-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="0f08e-126">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="0f08e-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f08e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f08e-127">Requirements</span></span>



| <span data-ttu-id="0f08e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f08e-128">Requirement</span></span> | <span data-ttu-id="0f08e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0f08e-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f08e-130">Header</span><span class="sxs-lookup"><span data-stu-id="0f08e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0f08e-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f08e-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f08e-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f08e-132">Library</span></span><br/> | <dl> <span data-ttu-id="0f08e-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f08e-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f08e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f08e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f08e-135">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f08e-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




