---
description: Die setdefaultdestinationposition-Methode legt den Renderer wieder auf die Standardziel Position (in der Regel auf den gesamten Fenster Client Bereich) fest.
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: Cbasecontrolvideo. setdefaultdestinationposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357557"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a><span data-ttu-id="3125e-103">Cbasecontrolvideo. setdefaultdestinationposition-Methode</span><span class="sxs-lookup"><span data-stu-id="3125e-103">CBaseControlVideo.SetDefaultDestinationPosition method</span></span>

<span data-ttu-id="3125e-104">Die- `SetDefaultDestinationPosition` Methode legt den Renderer mithilfe der Standardziel Position (in der Regel der gesamte Fenster Client Bereich) auf zurück.</span><span class="sxs-lookup"><span data-stu-id="3125e-104">The `SetDefaultDestinationPosition` method sets the renderer back to using the default destination position (typically the entire window client area).</span></span>

## <a name="syntax"></a><span data-ttu-id="3125e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3125e-105">Syntax</span></span>


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a><span data-ttu-id="3125e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3125e-106">Parameters</span></span>

<span data-ttu-id="3125e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3125e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3125e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3125e-108">Return value</span></span>

<span data-ttu-id="3125e-109">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3125e-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="3125e-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3125e-110">Return code</span></span>                                                                                           | <span data-ttu-id="3125e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3125e-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3125e-112"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="3125e-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="3125e-113">Fehler.</span><span class="sxs-lookup"><span data-stu-id="3125e-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="3125e-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="3125e-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="3125e-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3125e-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="3125e-116"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="3125e-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3125e-117">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="3125e-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3125e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3125e-118">Remarks</span></span>

<span data-ttu-id="3125e-119">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="3125e-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="3125e-120">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3125e-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="3125e-121">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="3125e-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="3125e-122">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="3125e-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="3125e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3125e-123">Requirements</span></span>



| <span data-ttu-id="3125e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3125e-124">Requirement</span></span> | <span data-ttu-id="3125e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3125e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3125e-126">Header</span><span class="sxs-lookup"><span data-stu-id="3125e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3125e-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3125e-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3125e-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3125e-128">Library</span></span><br/> | <dl> <span data-ttu-id="3125e-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3125e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3125e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3125e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3125e-131">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3125e-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




