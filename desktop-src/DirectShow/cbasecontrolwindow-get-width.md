---
description: Die get \_ Width-Methode ruft die aktuelle Fensterbreite ab.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: CBaseControlWindow.get_Width-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361463"
---
# <a name="cbasecontrolwindowget_width-method"></a><span data-ttu-id="c9fe6-103">Cbasecontrolwindow. get \_ Width-Methode</span><span class="sxs-lookup"><span data-stu-id="c9fe6-103">CBaseControlWindow.get\_Width method</span></span>

<span data-ttu-id="c9fe6-104">Die- `get_Width` Methode ruft die aktuelle Fensterbreite ab.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-104">The `get_Width` method retrieves the current window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9fe6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9fe6-105">Syntax</span></span>


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a><span data-ttu-id="c9fe6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9fe6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9fe6-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="c9fe6-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="c9fe6-108">Zeiger auf die Fensterbreite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-108">Pointer to the window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9fe6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9fe6-109">Return value</span></span>

<span data-ttu-id="c9fe6-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9fe6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9fe6-111">Remarks</span></span>

<span data-ttu-id="c9fe6-112">Das Fenster hat eine Position auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-112">The window has a position on the desktop.</span></span> <span data-ttu-id="c9fe6-113">Dies wird in Pixel durch vier Koordinaten (Links, oben, rechts und unten) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="c9fe6-114">Schnittstellen, die von OLE automatisiert werden, stellen diese Position normalerweise durch Left, Top, Width und Height dar. Dies ist die in DirectShow verwendete Konvention.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="c9fe6-115">Alle Koordinaten werden in Pixel ausgedrückt, und durch Ändern der Koordinaten wird das Fenster sofort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="c9fe6-116">Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links bzw. nach oben verschoben. Diese Koordinaten haben keine Auswirkung auf die Breite und Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="c9fe6-117">Ebenso wirkt sich die Festlegung von Breite und Höhe nicht auf die linke und die obere Koordinate aus.</span><span class="sxs-lookup"><span data-stu-id="c9fe6-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9fe6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9fe6-118">Requirements</span></span>



| <span data-ttu-id="c9fe6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9fe6-119">Requirement</span></span> | <span data-ttu-id="c9fe6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c9fe6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fe6-121">Header</span><span class="sxs-lookup"><span data-stu-id="c9fe6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c9fe6-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9fe6-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9fe6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9fe6-123">Library</span></span><br/> | <dl> <span data-ttu-id="c9fe6-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c9fe6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9fe6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9fe6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9fe6-126">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c9fe6-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




