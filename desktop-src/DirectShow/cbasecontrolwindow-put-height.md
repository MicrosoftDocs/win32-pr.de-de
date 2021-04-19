---
description: Die Put \_ Height-Methode legt die Fensterhöhe fest.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: CBaseControlWindow.put_Height-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798719c60b830caebee348032abce3e39a742e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359753"
---
# <a name="cbasecontrolwindowput_height-method"></a><span data-ttu-id="9564f-103">Cbasecontrolwindow. Put \_ Height-Methode</span><span class="sxs-lookup"><span data-stu-id="9564f-103">CBaseControlWindow.put\_Height method</span></span>

<span data-ttu-id="9564f-104">Die- `put_Height` Methode legt die Fensterhöhe fest.</span><span class="sxs-lookup"><span data-stu-id="9564f-104">The `put_Height` method sets the window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="9564f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9564f-105">Syntax</span></span>


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="9564f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9564f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9564f-107">*Height*</span><span class="sxs-lookup"><span data-stu-id="9564f-107">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="9564f-108">Neue Fensterhöhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="9564f-108">New window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9564f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9564f-109">Return value</span></span>

<span data-ttu-id="9564f-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9564f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9564f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9564f-111">Remarks</span></span>

<span data-ttu-id="9564f-112">Das Fenster hat eine Position auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="9564f-112">The window has a position on the desktop.</span></span> <span data-ttu-id="9564f-113">Dies wird in Pixel durch vier Koordinaten (Links, oben, rechts und unten) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="9564f-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="9564f-114">Schnittstellen, die von OLE automatisiert werden, stellen diese Position normalerweise durch Left, Top, Width und Height dar. Dies ist die in DirectShow verwendete Konvention.</span><span class="sxs-lookup"><span data-stu-id="9564f-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="9564f-115">Alle Koordinaten werden in Pixel ausgedrückt, und durch Ändern der Koordinaten wird das Fenster sofort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9564f-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="9564f-116">Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links bzw. nach oben verschoben. Diese Koordinaten haben keine Auswirkung auf die Breite und Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="9564f-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="9564f-117">Ebenso wirkt sich die Festlegung von Breite und Höhe nicht auf die linke und die obere Koordinate aus.</span><span class="sxs-lookup"><span data-stu-id="9564f-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="9564f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9564f-118">Requirements</span></span>



| <span data-ttu-id="9564f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9564f-119">Requirement</span></span> | <span data-ttu-id="9564f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9564f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9564f-121">Header</span><span class="sxs-lookup"><span data-stu-id="9564f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9564f-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9564f-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9564f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9564f-123">Library</span></span><br/> | <dl> <span data-ttu-id="9564f-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9564f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9564f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9564f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9564f-126">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9564f-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




