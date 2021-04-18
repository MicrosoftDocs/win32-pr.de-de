---
description: Die setdefaultsourceposition-Methode legt den Renderer wieder auf die standardmäßige Quell Position (in der Regel das gesamte native Video) fest.
ms.assetid: 1ac03298-4c25-45f7-9719-ea03fe4699b2
title: Cbasecontrolvideo. setdefaultsourceposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6296683235a3cf051d0b9f4ee56ce51a3516f66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371036"
---
# <a name="cbasecontrolvideosetdefaultsourceposition-method"></a><span data-ttu-id="1eed9-103">Cbasecontrolvideo. setdefaultsourceposition-Methode</span><span class="sxs-lookup"><span data-stu-id="1eed9-103">CBaseControlVideo.SetDefaultSourcePosition method</span></span>

<span data-ttu-id="1eed9-104">Die- `SetDefaultSourcePosition` Methode legt den Renderer mithilfe der standardmäßigen Quell Position (in der Regel mit dem systemeigenen Video) wieder auf fest.</span><span class="sxs-lookup"><span data-stu-id="1eed9-104">The `SetDefaultSourcePosition` method sets the renderer back to using the default source position (typically all the native video).</span></span>

## <a name="syntax"></a><span data-ttu-id="1eed9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1eed9-105">Syntax</span></span>


```C++
HRESULT SetDefaultSourcePosition();
```



## <a name="parameters"></a><span data-ttu-id="1eed9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1eed9-106">Parameters</span></span>

<span data-ttu-id="1eed9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1eed9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1eed9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1eed9-108">Return value</span></span>

<span data-ttu-id="1eed9-109">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1eed9-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="1eed9-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1eed9-110">Return code</span></span>                                                                                           | <span data-ttu-id="1eed9-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1eed9-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1eed9-112"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="1eed9-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="1eed9-113">Fehler.</span><span class="sxs-lookup"><span data-stu-id="1eed9-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1eed9-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="1eed9-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="1eed9-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1eed9-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1eed9-116"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="1eed9-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1eed9-117">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="1eed9-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1eed9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eed9-118">Remarks</span></span>

<span data-ttu-id="1eed9-119">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="1eed9-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="1eed9-120">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1eed9-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="1eed9-121">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="1eed9-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="1eed9-122">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="1eed9-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="1eed9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eed9-123">Requirements</span></span>



| <span data-ttu-id="1eed9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1eed9-124">Requirement</span></span> | <span data-ttu-id="1eed9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1eed9-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eed9-126">Header</span><span class="sxs-lookup"><span data-stu-id="1eed9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1eed9-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1eed9-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1eed9-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1eed9-128">Library</span></span><br/> | <dl> <span data-ttu-id="1eed9-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1eed9-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eed9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1eed9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eed9-131">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1eed9-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




