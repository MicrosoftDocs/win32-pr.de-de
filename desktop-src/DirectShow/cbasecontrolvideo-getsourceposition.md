---
description: Die getsourceposition-Methode ruft die Position und die Dimensionen des Quell Rechtecks in einem atomaren Vorgang ab.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: Cbasecontrolvideo. getsourceposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2422845a7b5c64bc07b8e8942b2f19cd10a54d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354846"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a><span data-ttu-id="76994-103">Cbasecontrolvideo. getsourceposition-Methode</span><span class="sxs-lookup"><span data-stu-id="76994-103">CBaseControlVideo.GetSourcePosition method</span></span>

<span data-ttu-id="76994-104">Die `GetSourcePosition` -Methode ruft die Position und die Dimensionen des Quell Rechtecks in einem atomaren Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="76994-104">The `GetSourcePosition` method retrieves the position and dimensions of the source rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="76994-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76994-105">Syntax</span></span>


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="76994-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76994-107">*pleft*</span><span class="sxs-lookup"><span data-stu-id="76994-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="76994-108">Ein Zeiger auf die linke Koordinate des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="76994-108">Pointer to the left coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="76994-109">*ptop*</span><span class="sxs-lookup"><span data-stu-id="76994-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="76994-110">Ein Zeiger auf die obere Koordinate des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="76994-110">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="76994-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="76994-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="76994-112">Ein Zeiger auf die Breite des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="76994-112">Pointer to the width of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="76994-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="76994-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="76994-114">Ein Zeiger auf die Höhe des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="76994-114">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76994-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76994-115">Return value</span></span>

<span data-ttu-id="76994-116">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="76994-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="76994-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76994-117">Return code</span></span>                                                                                           | <span data-ttu-id="76994-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76994-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76994-119"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="76994-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="76994-120">Fehler.</span><span class="sxs-lookup"><span data-stu-id="76994-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="76994-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="76994-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="76994-122">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="76994-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="76994-123"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="76994-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="76994-124">Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="76994-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="76994-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="76994-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="76994-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="76994-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="76994-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76994-127">Remarks</span></span>

<span data-ttu-id="76994-128">Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="76994-128">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="76994-129">Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="76994-129">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="76994-130">Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="76994-130">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="76994-131">Die linke obere Ecke des Fensters ist Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="76994-131">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="76994-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76994-132">Requirements</span></span>



| <span data-ttu-id="76994-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76994-133">Requirement</span></span> | <span data-ttu-id="76994-134">Wert</span><span class="sxs-lookup"><span data-stu-id="76994-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76994-135">Header</span><span class="sxs-lookup"><span data-stu-id="76994-135">Header</span></span><br/>  | <dl> <span data-ttu-id="76994-136"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76994-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="76994-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76994-137">Library</span></span><br/> | <dl> <span data-ttu-id="76994-138">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="76994-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76994-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76994-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76994-140">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="76994-140">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




