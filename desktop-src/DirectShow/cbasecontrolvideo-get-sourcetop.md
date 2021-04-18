---
description: Die get \_ sourceTop-Methode ruft die obere Koordinate des aktuellen Quell Rechtecks ab.
ms.assetid: 78dbd1e6-f591-487e-b9fe-fcbda55f5338
title: CBaseControlVideo.get_SourceTop-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1c2a2a90b441571a23bfa4210002b352e388a98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358070"
---
# <a name="cbasecontrolvideoget_sourcetop-method"></a><span data-ttu-id="d9f16-103">Cbasecontrolvideo. get \_ sourceTop-Methode</span><span class="sxs-lookup"><span data-stu-id="d9f16-103">CBaseControlVideo.get\_SourceTop method</span></span>

<span data-ttu-id="d9f16-104">Die- `get_SourceTop` Methode ruft die obere Koordinate des aktuellen Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="d9f16-104">The `get_SourceTop` method retrieves the top coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9f16-105">Syntax</span></span>


```C++
HRESULT get_SourceTop(
   long *pSourceTop
);
```



## <a name="parameters"></a><span data-ttu-id="d9f16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f16-107">*psourcetop*</span><span class="sxs-lookup"><span data-stu-id="d9f16-107">*pSourceTop*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f16-108">Ein Zeiger auf die obere Koordinate des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="d9f16-108">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9f16-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9f16-109">Return value</span></span>

<span data-ttu-id="d9f16-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d9f16-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="d9f16-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d9f16-111">Return code</span></span>                                                                                           | <span data-ttu-id="d9f16-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9f16-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9f16-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f16-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="d9f16-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="d9f16-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="d9f16-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f16-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="d9f16-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="d9f16-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d9f16-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f16-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d9f16-118">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="d9f16-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d9f16-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f16-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="d9f16-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d9f16-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d9f16-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9f16-121">Remarks</span></span>

<span data-ttu-id="d9f16-122">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ sourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d9f16-122">This member function implements the [**IBasicVideo::get\_SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) method.</span></span>

<span data-ttu-id="d9f16-123">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="d9f16-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="d9f16-124">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d9f16-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="d9f16-125">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="d9f16-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="d9f16-126">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="d9f16-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f16-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9f16-127">Requirements</span></span>



| <span data-ttu-id="d9f16-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9f16-128">Requirement</span></span> | <span data-ttu-id="d9f16-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d9f16-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f16-130">Header</span><span class="sxs-lookup"><span data-stu-id="d9f16-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d9f16-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f16-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d9f16-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9f16-132">Library</span></span><br/> | <dl> <span data-ttu-id="d9f16-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f16-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f16-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9f16-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f16-135">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d9f16-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




