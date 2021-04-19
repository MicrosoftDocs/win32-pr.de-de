---
description: Die get \_ sourceLeft-Methode ruft die linke Koordinate des aktuellen Quell Rechtecks ab.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: CBaseControlVideo.get_SourceLeft-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364937"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a><span data-ttu-id="568a2-103">Cbasecontrolvideo. get \_ sourceLeft-Methode</span><span class="sxs-lookup"><span data-stu-id="568a2-103">CBaseControlVideo.get\_SourceLeft method</span></span>

<span data-ttu-id="568a2-104">Die- `get_SourceLeft` Methode ruft die linke Koordinate des aktuellen Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="568a2-104">The `get_SourceLeft` method retrieves the left coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="568a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="568a2-105">Syntax</span></span>


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="568a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="568a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="568a2-107">*psourceleft*</span><span class="sxs-lookup"><span data-stu-id="568a2-107">*pSourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="568a2-108">Ein Zeiger auf die linke Koordinate des aktuellen Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="568a2-108">Pointer to the left coordinate of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="568a2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="568a2-109">Return value</span></span>

<span data-ttu-id="568a2-110">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="568a2-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="568a2-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="568a2-111">Return code</span></span>                                                                                           | <span data-ttu-id="568a2-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="568a2-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="568a2-113"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="568a2-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="568a2-114">Fehler.</span><span class="sxs-lookup"><span data-stu-id="568a2-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="568a2-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="568a2-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="568a2-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="568a2-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="568a2-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="568a2-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="568a2-118">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="568a2-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="568a2-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="568a2-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="568a2-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="568a2-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="568a2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="568a2-121">Remarks</span></span>

<span data-ttu-id="568a2-122">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="568a2-122">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="568a2-123">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="568a2-123">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="568a2-124">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="568a2-124">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="568a2-125">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="568a2-125">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="568a2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="568a2-126">Requirements</span></span>



| <span data-ttu-id="568a2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="568a2-127">Requirement</span></span> | <span data-ttu-id="568a2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="568a2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="568a2-129">Header</span><span class="sxs-lookup"><span data-stu-id="568a2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="568a2-130"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="568a2-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="568a2-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="568a2-131">Library</span></span><br/> | <dl> <span data-ttu-id="568a2-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="568a2-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="568a2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="568a2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="568a2-134">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="568a2-134">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




