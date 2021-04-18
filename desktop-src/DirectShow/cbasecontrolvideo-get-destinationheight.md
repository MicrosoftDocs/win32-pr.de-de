---
description: Die get \_ destinationheight-Methode ruft die aktuelle Höhe des Ziel Rechtecks ab.
ms.assetid: 0001d98a-3a5c-47f1-8f5e-ce464d64131a
title: CBaseControlVideo.get_DestinationHeight-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc4fc63e63adbc42b75ae9a24d1c47e7d985c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358383"
---
# <a name="cbasecontrolvideoget_destinationheight-method"></a><span data-ttu-id="c6c59-103">Cbasecontrolvideo. get \_ destinationheight-Methode</span><span class="sxs-lookup"><span data-stu-id="c6c59-103">CBaseControlVideo.get\_DestinationHeight method</span></span>

<span data-ttu-id="c6c59-104">Die- `get_DestinationHeight` Methode ruft die aktuelle Höhe des Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="c6c59-104">The `get_DestinationHeight` method retrieves the current destination rectangle height.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6c59-105">Syntax</span></span>


```C++
HRESULT get_DestinationHeight(
   long *pDestinationHeight
);
```



## <a name="parameters"></a><span data-ttu-id="c6c59-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6c59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c59-107">*pdestinationheight*</span><span class="sxs-lookup"><span data-stu-id="c6c59-107">*pDestinationHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c59-108">Ein Zeiger auf die Zielhöhe.</span><span class="sxs-lookup"><span data-stu-id="c6c59-108">Pointer to the destination height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c59-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6c59-109">Return value</span></span>

<span data-ttu-id="c6c59-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c6c59-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="c6c59-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c6c59-111">Return code</span></span>                                                                                           | <span data-ttu-id="c6c59-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6c59-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6c59-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="c6c59-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="c6c59-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="c6c59-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="c6c59-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c6c59-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c6c59-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="c6c59-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c6c59-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="c6c59-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c6c59-118">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="c6c59-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="c6c59-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="c6c59-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="c6c59-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c6c59-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="c6c59-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6c59-121">Remarks</span></span>

<span data-ttu-id="c6c59-122">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ destinationheight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c6c59-122">This member function implements the [**IBasicVideo::get\_DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) method.</span></span>

<span data-ttu-id="c6c59-123">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="c6c59-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="c6c59-124">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo es wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c6c59-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where it will be played.</span></span> <span data-ttu-id="c6c59-125">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="c6c59-125">The destination rectangle is relative to the client area of the window that it is playing in.</span></span> <span data-ttu-id="c6c59-126">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="c6c59-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c59-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6c59-127">Requirements</span></span>



| <span data-ttu-id="c6c59-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6c59-128">Requirement</span></span> | <span data-ttu-id="c6c59-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c6c59-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c59-130">Header</span><span class="sxs-lookup"><span data-stu-id="c6c59-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c6c59-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c59-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6c59-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6c59-132">Library</span></span><br/> | <dl> <span data-ttu-id="c6c59-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c59-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c59-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6c59-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c59-135">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c6c59-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




