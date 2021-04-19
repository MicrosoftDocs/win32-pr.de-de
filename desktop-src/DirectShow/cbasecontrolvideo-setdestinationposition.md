---
description: Die setdestinationposition-Methode legt das Ziel Rechteck für das Video fest.
ms.assetid: 397e90ea-7535-4cac-9f47-7a93737b1e3a
title: Cbasecontrolvideo. setdestinationposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798a65c44dd490587e3ad46fcae2c61a03986df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365836"
---
# <a name="cbasecontrolvideosetdestinationposition-method"></a><span data-ttu-id="1fd0f-103">Cbasecontrolvideo. setdestinationposition-Methode</span><span class="sxs-lookup"><span data-stu-id="1fd0f-103">CBaseControlVideo.SetDestinationPosition method</span></span>

<span data-ttu-id="1fd0f-104">Die- `SetDestinationPosition` Methode legt das Ziel Rechteck für das Video fest.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-104">The `SetDestinationPosition` method sets the destination rectangle for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fd0f-105">Syntax</span></span>


```C++
HRESULT SetDestinationPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="1fd0f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fd0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fd0f-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="1fd0f-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd0f-108">Neue linke Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="1fd0f-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="1fd0f-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd0f-110">Neue obere Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="1fd0f-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="1fd0f-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd0f-112">Neue Breite.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="1fd0f-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="1fd0f-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd0f-114">Neue Höhe.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fd0f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fd0f-115">Return value</span></span>

<span data-ttu-id="1fd0f-116">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="1fd0f-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1fd0f-117">Return code</span></span>                                                                                           | <span data-ttu-id="1fd0f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fd0f-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fd0f-119"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd0f-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="1fd0f-120">Fehler.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1fd0f-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd0f-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="1fd0f-122">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="1fd0f-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd0f-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1fd0f-124">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1fd0f-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd0f-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="1fd0f-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1fd0f-127"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd0f-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1fd0f-128">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1fd0f-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fd0f-129">Remarks</span></span>

<span data-ttu-id="1fd0f-130">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="1fd0f-131">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="1fd0f-132">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="1fd0f-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="1fd0f-133">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="1fd0f-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd0f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fd0f-134">Requirements</span></span>



| <span data-ttu-id="1fd0f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fd0f-135">Requirement</span></span> | <span data-ttu-id="1fd0f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1fd0f-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd0f-137">Header</span><span class="sxs-lookup"><span data-stu-id="1fd0f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1fd0f-138"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd0f-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fd0f-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1fd0f-139">Library</span></span><br/> | <dl> <span data-ttu-id="1fd0f-140">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd0f-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd0f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fd0f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd0f-142">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1fd0f-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




