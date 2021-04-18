---
description: Mit der Put \_ Width-Methode wird die Fensterbreite festgelegt.
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: CBaseControlWindow.put_Width-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5235e2b842b26f3f05c31c9f19a16c7630c80c13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365402"
---
# <a name="cbasecontrolwindowput_width-method"></a><span data-ttu-id="63735-103">Cbasecontrolwindow. Put \_ Width-Methode</span><span class="sxs-lookup"><span data-stu-id="63735-103">CBaseControlWindow.put\_Width method</span></span>

<span data-ttu-id="63735-104">Die- `put_Width` Methode legt die Fensterbreite fest.</span><span class="sxs-lookup"><span data-stu-id="63735-104">The `put_Width` method sets the window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="63735-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63735-105">Syntax</span></span>


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a><span data-ttu-id="63735-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63735-107">*Width*</span><span class="sxs-lookup"><span data-stu-id="63735-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="63735-108">Neue Fensterbreite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="63735-108">New window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63735-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63735-109">Return value</span></span>

<span data-ttu-id="63735-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="63735-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63735-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63735-111">Remarks</span></span>

<span data-ttu-id="63735-112">Das Fenster hat eine Position auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="63735-112">The window has a position on the desktop.</span></span> <span data-ttu-id="63735-113">Dies wird in Pixel durch vier Koordinaten (Links, oben, rechts und unten) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="63735-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="63735-114">Schnittstellen, die von OLE automatisiert werden, stellen diese Position normalerweise durch Left, Top, Width und Height dar. Dies ist die in DirectShow verwendete Konvention.</span><span class="sxs-lookup"><span data-stu-id="63735-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="63735-115">Alle Koordinaten werden in Pixel ausgedrückt, und durch Ändern der Koordinaten wird das Fenster sofort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="63735-115">All coordinates are expressed in pixels and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="63735-116">Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links bzw. nach oben verschoben. Diese Koordinaten haben keine Auswirkung auf die Breite und Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="63735-116">Setting the left or top coordinates moves the window left or up respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="63735-117">Ebenso wirkt sich die Festlegung von Breite und Höhe nicht auf die linke und die obere Koordinate aus.</span><span class="sxs-lookup"><span data-stu-id="63735-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="63735-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63735-118">Requirements</span></span>



| <span data-ttu-id="63735-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63735-119">Requirement</span></span> | <span data-ttu-id="63735-120">Wert</span><span class="sxs-lookup"><span data-stu-id="63735-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63735-121">Header</span><span class="sxs-lookup"><span data-stu-id="63735-121">Header</span></span><br/>  | <dl> <span data-ttu-id="63735-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63735-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63735-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63735-123">Library</span></span><br/> | <dl> <span data-ttu-id="63735-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="63735-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63735-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63735-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63735-126">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="63735-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




