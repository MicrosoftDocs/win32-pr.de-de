---
title: ID2D1RenderTarget FillEllipse-Methoden (D2d1. h)
description: Zeichnet das Innere der angegebenen Ellipse.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- FillEllipse-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359246"
---
# <a name="id2d1rendertargetfillellipse-methods"></a><span data-ttu-id="d141f-104">ID2D1RenderTarget:: FillEllipse-Methoden</span><span class="sxs-lookup"><span data-stu-id="d141f-104">ID2D1RenderTarget::FillEllipse methods</span></span>

<span data-ttu-id="d141f-105">Zeichnet das Innere der angegebenen Ellipse.</span><span class="sxs-lookup"><span data-stu-id="d141f-105">Paints the interior of the specified ellipse.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d141f-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="d141f-106">Overload list</span></span>



| <span data-ttu-id="d141f-107">Methode</span><span class="sxs-lookup"><span data-stu-id="d141f-107">Method</span></span>                                                                                                             | <span data-ttu-id="d141f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d141f-108">Description</span></span>                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span data-ttu-id="d141f-109">[**FillEllipse (D2D1 \_ Ellipse&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="d141f-109">[**FillEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span>  | <span data-ttu-id="d141f-110">Zeichnet das Innere der angegebenen Ellipse.</span><span class="sxs-lookup"><span data-stu-id="d141f-110">Paints the interior of the specified ellipse.</span></span> <br/> |
| <span data-ttu-id="d141f-111">[**FillEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="d141f-111">[**FillEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span> | <span data-ttu-id="d141f-112">Zeichnet das Innere der angegebenen Ellipse.</span><span class="sxs-lookup"><span data-stu-id="d141f-112">Paints the interior of the specified ellipse.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d141f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d141f-113">Remarks</span></span>

<span data-ttu-id="d141f-114">Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d141f-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="d141f-115">Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **FillEllipse**) fehlgeschlagen ist, überprüfen Sie das Ergebnis, das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="d141f-115">To determine whether a drawing operation (such as **FillEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="d141f-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d141f-116">Examples</span></span>

<span data-ttu-id="d141f-117">Ein Beispiel finden Sie unter [Zeichnen und Ausfüllen einer einfachen Form](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="d141f-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d141f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d141f-118">Requirements</span></span>



| <span data-ttu-id="d141f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d141f-119">Requirement</span></span> | <span data-ttu-id="d141f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d141f-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d141f-121">Header</span><span class="sxs-lookup"><span data-stu-id="d141f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d141f-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="d141f-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="d141f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d141f-123">Library</span></span><br/> | <dl> <span data-ttu-id="d141f-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d141f-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="d141f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d141f-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d141f-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d141f-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d141f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d141f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d141f-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="d141f-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="d141f-129">Zeichnen und Ausfüllen einer einfachen Form</span><span class="sxs-lookup"><span data-stu-id="d141f-129">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="d141f-130">�</span><span class="sxs-lookup"><span data-stu-id="d141f-130">�</span></span>

<span data-ttu-id="d141f-131">�</span><span class="sxs-lookup"><span data-stu-id="d141f-131">�</span></span>
