---
description: Die get \_ Left-Methode ruft die aktuelle linke Fenster Koordinate ab.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: CBaseControlWindow.get_Left-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362052"
---
# <a name="cbasecontrolwindowget_left-method"></a><span data-ttu-id="b23cc-103">Cbasecontrolwindow. get \_ Left-Methode</span><span class="sxs-lookup"><span data-stu-id="b23cc-103">CBaseControlWindow.get\_Left method</span></span>

<span data-ttu-id="b23cc-104">Die- `get_Left` Methode ruft die aktuelle linke Fenster Koordinate ab.</span><span class="sxs-lookup"><span data-stu-id="b23cc-104">The `get_Left` method retrieves the current left window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b23cc-105">Syntax</span></span>


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a><span data-ttu-id="b23cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b23cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b23cc-107">*pleft*</span><span class="sxs-lookup"><span data-stu-id="b23cc-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="b23cc-108">Zeiger auf die linke Koordinate in Pixel.</span><span class="sxs-lookup"><span data-stu-id="b23cc-108">Pointer to the left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b23cc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b23cc-109">Return value</span></span>

<span data-ttu-id="b23cc-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b23cc-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b23cc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b23cc-111">Remarks</span></span>

<span data-ttu-id="b23cc-112">Das Fenster hat eine Position auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="b23cc-112">The window has a position on the desktop.</span></span> <span data-ttu-id="b23cc-113">Diese Position wird in Pixel durch vier Koordinaten (Links, oben, rechts und unten) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="b23cc-113">This position is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="b23cc-114">Schnittstellen, die von OLE automatisiert werden, stellen diese Position normalerweise durch Left, Top, Width und Height dar. Dies ist die in DirectShow verwendete Konvention.</span><span class="sxs-lookup"><span data-stu-id="b23cc-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="b23cc-115">Alle Koordinaten werden in Pixel ausgedrückt, und durch Ändern der Koordinaten wird das Fenster sofort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b23cc-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="b23cc-116">Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links und nach oben verschoben. Diese Koordinaten haben keine Auswirkung auf die Breite und Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b23cc-116">Setting the left or top coordinates moves the window left and up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="b23cc-117">Ebenso hat das Festlegen von Breite und Höhe keine Auswirkung auf die linke und die obere Koordinate.</span><span class="sxs-lookup"><span data-stu-id="b23cc-117">Likewise, setting the width and height have no effect on the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="b23cc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b23cc-118">Requirements</span></span>



| <span data-ttu-id="b23cc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b23cc-119">Requirement</span></span> | <span data-ttu-id="b23cc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b23cc-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b23cc-121">Header</span><span class="sxs-lookup"><span data-stu-id="b23cc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b23cc-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b23cc-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b23cc-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b23cc-123">Library</span></span><br/> | <dl> <span data-ttu-id="b23cc-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b23cc-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b23cc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b23cc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23cc-126">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b23cc-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




