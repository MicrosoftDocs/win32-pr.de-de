---
description: Die getdestinationposition-Methode ruft das Ziel Rechteck in einem atomaren Vorgang ab.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Cbasecontrolvideo. getdestinationposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371570"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a><span data-ttu-id="b8e66-103">Cbasecontrolvideo. getdestinationposition-Methode</span><span class="sxs-lookup"><span data-stu-id="b8e66-103">CBaseControlVideo.GetDestinationPosition method</span></span>

<span data-ttu-id="b8e66-104">Die- `GetDestinationPosition` Methode ruft das Ziel Rechteck in einem atomaren Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="b8e66-104">The `GetDestinationPosition` method retrieves the destination rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8e66-105">Syntax</span></span>


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="b8e66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8e66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e66-107">*pleft*</span><span class="sxs-lookup"><span data-stu-id="b8e66-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e66-108">Ein Zeiger auf die linke Koordinate des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="b8e66-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b8e66-109">*ptop*</span><span class="sxs-lookup"><span data-stu-id="b8e66-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e66-110">Ein Zeiger auf die obere Koordinate des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="b8e66-110">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b8e66-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="b8e66-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e66-112">Ein Zeiger auf die Breite des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="b8e66-112">Pointer to the width of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b8e66-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="b8e66-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e66-114">Ein Zeiger auf die Höhe des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="b8e66-114">Pointer to the height of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e66-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8e66-115">Return value</span></span>

<span data-ttu-id="b8e66-116">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b8e66-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="b8e66-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b8e66-117">Return code</span></span>                                                                                           | <span data-ttu-id="b8e66-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8e66-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8e66-119"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="b8e66-120">Fehler.</span><span class="sxs-lookup"><span data-stu-id="b8e66-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b8e66-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="b8e66-122">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="b8e66-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b8e66-123"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b8e66-124">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="b8e66-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="b8e66-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="b8e66-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b8e66-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b8e66-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8e66-127">Remarks</span></span>

<span data-ttu-id="b8e66-128">Diese Member-Funktion kann anstelle von separaten Aufrufen der [**cbasecontrolvideo:: get \_ destinationleft**](cbasecontrolvideo-get-destinationleft.md)-, [**cbasecontrolvideo:: get \_ destinationtop**](cbasecontrolvideo-get-destinationtop.md)-, [**cbasecontrolvideo:: get \_ destinationwidth**](cbasecontrolvideo-get-destinationwidth.md)-und [**cbasecontrolvideo:: get \_ destinationheight**](cbasecontrolvideo-get-destinationheight.md) -Member-Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8e66-128">This member function can be used in place of separate calls to the [**CBaseControlVideo::get\_DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get\_DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get\_DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md), and [**CBaseControlVideo::get\_DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) member functions.</span></span> <span data-ttu-id="b8e66-129">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="b8e66-129">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="b8e66-130">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e66-130">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="b8e66-131">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e66-131">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="b8e66-132">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="b8e66-132">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e66-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8e66-133">Requirements</span></span>



| <span data-ttu-id="b8e66-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8e66-134">Requirement</span></span> | <span data-ttu-id="b8e66-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b8e66-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e66-136">Header</span><span class="sxs-lookup"><span data-stu-id="b8e66-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b8e66-137"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8e66-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8e66-138">Library</span></span><br/> | <dl> <span data-ttu-id="b8e66-139">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b8e66-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e66-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8e66-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e66-141">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b8e66-141">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




