---
title: ID2D1RenderTarget DrawEllipse-Methoden (D2d1. h)
description: Zeichnet den Umriss einer Ellipse mit den angegebenen Dimensionen und dem angegebenen Strich.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- DrawEllipse-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370010"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a><span data-ttu-id="72983-104">ID2D1RenderTarget::D rawellipse-Methoden</span><span class="sxs-lookup"><span data-stu-id="72983-104">ID2D1RenderTarget::DrawEllipse methods</span></span>

<span data-ttu-id="72983-105">Zeichnet den Umriss einer Ellipse mit den angegebenen Dimensionen und dem angegebenen Strich.</span><span class="sxs-lookup"><span data-stu-id="72983-105">Draws the outline of an ellipse with the specified dimensions and stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="72983-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="72983-106">Overload list</span></span>



| <span data-ttu-id="72983-107">Methode</span><span class="sxs-lookup"><span data-stu-id="72983-107">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="72983-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72983-108">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72983-109">[**DrawEllipse (D2D1 \_ Ellipse&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="72983-109">[**DrawEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="72983-110">Zeichnet den Umriss der angegebenen Ellipse mit dem angegebenen Strich Stil.</span><span class="sxs-lookup"><span data-stu-id="72983-110">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |
| <span data-ttu-id="72983-111">[**DrawEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="72983-111">[**DrawEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="72983-112">Zeichnet den Umriss der angegebenen Ellipse mit dem angegebenen Strich Stil.</span><span class="sxs-lookup"><span data-stu-id="72983-112">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="72983-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72983-113">Remarks</span></span>

<span data-ttu-id="72983-114">Wenn ein Fehler auftritt, wird von der **DrawEllipse** -Methode kein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72983-114">The **DrawEllipse** method doesn't return an error code if it fails.</span></span> <span data-ttu-id="72983-115">Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **DrawEllipse**) fehlgeschlagen ist, überprüfen Sie das Ergebnis, das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="72983-115">To determine whether a drawing operation (such as **DrawEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="72983-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72983-116">Examples</span></span>

<span data-ttu-id="72983-117">Ein Beispiel finden Sie unter [Zeichnen und Ausfüllen einer einfachen Form](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="72983-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72983-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72983-118">Requirements</span></span>



| <span data-ttu-id="72983-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72983-119">Requirement</span></span> | <span data-ttu-id="72983-120">Wert</span><span class="sxs-lookup"><span data-stu-id="72983-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72983-121">Header</span><span class="sxs-lookup"><span data-stu-id="72983-121">Header</span></span><br/>  | <dl> <span data-ttu-id="72983-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="72983-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="72983-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72983-123">Library</span></span><br/> | <dl> <span data-ttu-id="72983-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72983-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="72983-125">DLL</span><span class="sxs-lookup"><span data-stu-id="72983-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="72983-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72983-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72983-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72983-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72983-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="72983-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

<span data-ttu-id="72983-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="72983-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span></span>
</dt> </dl>

<span data-ttu-id="72983-130">�</span><span class="sxs-lookup"><span data-stu-id="72983-130">�</span></span>

<span data-ttu-id="72983-131">�</span><span class="sxs-lookup"><span data-stu-id="72983-131">�</span></span>
