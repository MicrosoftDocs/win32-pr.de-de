---
description: Die get \_ Height-Methode ruft die aktuelle Fensterhöhe ab.
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: CBaseControlWindow.get_Height-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369488"
---
# <a name="cbasecontrolwindowget_height-method"></a><span data-ttu-id="35e9d-103">Cbasecontrolwindow. get \_ Height-Methode</span><span class="sxs-lookup"><span data-stu-id="35e9d-103">CBaseControlWindow.get\_Height method</span></span>

<span data-ttu-id="35e9d-104">Die- `get_Height` Methode ruft die aktuelle Fensterhöhe ab.</span><span class="sxs-lookup"><span data-stu-id="35e9d-104">The `get_Height` method retrieves the current window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e9d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35e9d-105">Syntax</span></span>


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="35e9d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35e9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e9d-107">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="35e9d-107">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="35e9d-108">Zeiger auf die aktuelle Fensterhöhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="35e9d-108">Pointer to the current window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e9d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35e9d-109">Return value</span></span>

<span data-ttu-id="35e9d-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="35e9d-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35e9d-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35e9d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e9d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35e9d-112">Remarks</span></span>

<span data-ttu-id="35e9d-113">Das Fenster hat eine Position auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="35e9d-113">The window has a position on the desktop.</span></span> <span data-ttu-id="35e9d-114">Dies wird in Pixel durch vier Koordinaten (Links, oben, rechts und unten) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="35e9d-114">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="35e9d-115">Schnittstellen, die von OLE automatisiert werden, stellen diese Position normalerweise durch Left, Top, Width und Height dar. Dies ist die in DirectShow verwendete Konvention.</span><span class="sxs-lookup"><span data-stu-id="35e9d-115">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="35e9d-116">Alle Koordinaten werden in Pixel ausgedrückt, und durch Ändern der Koordinaten wird das Fenster sofort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="35e9d-116">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="35e9d-117">Durch Festlegen der linken oder oberen Koordinaten wird das Fenster nach links bzw. nach oben verschoben. Diese Koordinaten haben keine Auswirkung auf die Breite und Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="35e9d-117">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="35e9d-118">Ebenso wirkt sich die Festlegung von Breite und Höhe nicht auf die linke und die obere Koordinate aus.</span><span class="sxs-lookup"><span data-stu-id="35e9d-118">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e9d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35e9d-119">Requirements</span></span>



| <span data-ttu-id="35e9d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35e9d-120">Requirement</span></span> | <span data-ttu-id="35e9d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="35e9d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e9d-122">Header</span><span class="sxs-lookup"><span data-stu-id="35e9d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="35e9d-123"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35e9d-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35e9d-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35e9d-124">Library</span></span><br/> | <dl> <span data-ttu-id="35e9d-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="35e9d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e9d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35e9d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e9d-127">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="35e9d-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




