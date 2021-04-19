---
title: ID2D1Brush setTransform-Methoden (D2d1 \_ 1. h)
description: Legt die auf den Pinsel angewendete Transformation fest.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- SetTransform-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367132"
---
# <a name="id2d1brushsettransform-methods"></a><span data-ttu-id="11d36-104">ID2D1Brush:: setTransform-Methoden</span><span class="sxs-lookup"><span data-stu-id="11d36-104">ID2D1Brush::SetTransform methods</span></span>

<span data-ttu-id="11d36-105">Legt die auf den Pinsel angewendete Transformation fest.</span><span class="sxs-lookup"><span data-stu-id="11d36-105">Sets the transformation applied to the brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="11d36-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="11d36-106">Overload list</span></span>



| <span data-ttu-id="11d36-107">Methode</span><span class="sxs-lookup"><span data-stu-id="11d36-107">Method</span></span>                                                                                       | <span data-ttu-id="11d36-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11d36-108">Description</span></span>                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span data-ttu-id="11d36-109">[**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="11d36-109">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="11d36-110">Legt die auf den Pinsel angewendete Transformation fest.</span><span class="sxs-lookup"><span data-stu-id="11d36-110">Sets the transformation applied to the brush.</span></span><br/> |
| <span data-ttu-id="11d36-111">[**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="11d36-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="11d36-112">Legt die auf den Pinsel angewendete Transformation fest.</span><span class="sxs-lookup"><span data-stu-id="11d36-112">Sets the transformation applied to the brush.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="11d36-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11d36-113">Remarks</span></span>

<span data-ttu-id="11d36-114">Wenn Sie mit einem Pinsel zeichnen, zeichnet Sie den Koordinaten Bereich des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="11d36-114">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="11d36-115">Pinsel positionieren sich nicht automatisch so, dass Sie an dem Objekt ausgerichtet werden, das gezeichnet wird. Standardmäßig beginnen Sie mit dem Zeichnen am Ursprung (0,0) des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="11d36-115">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="11d36-116">Durch Festlegen des Startpunkts und des Endpunkts können Sie den durch ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) definierten Farbverlauf in einen Zielbereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="11d36-116">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="11d36-117">Entsprechend können Sie den von einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) definierten Farbverlauf durch Ändern seiner Mitte und Radii verschieben.</span><span class="sxs-lookup"><span data-stu-id="11d36-117">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="11d36-118">Um den Inhalt eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) an den Bereich auszurichten, der gezeichnet wird, können Sie die **setTransform** -Methode verwenden, um die Bitmap an die gewünschte Stelle zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="11d36-118">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="11d36-119">Diese Transformation wirkt sich nur auf den Pinsel aus. Er wirkt sich nicht auf andere Inhalte aus, die vom Renderziel gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="11d36-119">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="11d36-120">Die folgenden Abbildungen zeigen die Auswirkung der Verwendung eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Auffüllen eines Rechtecks, das sich unter (100, 100) befindet.</span><span class="sxs-lookup"><span data-stu-id="11d36-120">The following illustrations show the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="11d36-121">Die Abbildung in der linken Abbildung zeigt das Ergebnis der Füllung des Rechtecks ohne Umwandlung des Pinsels: die Bitmap wird am Ursprung des Renderziels gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="11d36-121">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="11d36-122">Daher wird nur ein Teil der Bitmap im Rechteck angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11d36-122">As a result, only a portion of the bitmap appears in the rectangle.</span></span>

<span data-ttu-id="11d36-123">Die Abbildung auf der rechten Seite zeigt das Ergebnis der Transformation des [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , sodass der Inhalt 50 Pixel nach rechts und 50 Pixel nach unten verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="11d36-123">The illustration on the right shows the result of transforming the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="11d36-124">Die Bitmap füllt nun das Rechteck aus.</span><span class="sxs-lookup"><span data-stu-id="11d36-124">The bitmap now fills the rectangle.</span></span>

![Abbildung von zwei Quadraten, eine mit einer Bitmap ohne transformierten Pinsel und eine mit einem transformierten Pinsel gezeichnet](images/brushes-ovw-transform.png)

## <a name="examples"></a><span data-ttu-id="11d36-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11d36-126">Examples</span></span>

<span data-ttu-id="11d36-127">In den folgenden Codebeispielen wird veranschaulicht, wie die Transformation erstellt wird, die im rechten Diagramm in der obigen Abbildung gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="11d36-127">The following code examples show how to create the transformation shown in the right diagram in the preceding illustration.</span></span> <span data-ttu-id="11d36-128">Wenden Sie zuerst eine Übersetzung auf den [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)an, und bewegen Sie den Pinsel 50 Pixel direkt entlang der x-Achse und 50 Pixel entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="11d36-128">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="11d36-129">Verwenden Sie dann **ID2D1BitmapBrush** , um das Rechteck mit der linken oberen Ecke bei (100, 100) und der unteren rechten Ecke um (200, 200) auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="11d36-129">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a><span data-ttu-id="11d36-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11d36-130">Requirements</span></span>



| <span data-ttu-id="11d36-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11d36-131">Requirement</span></span> | <span data-ttu-id="11d36-132">Wert</span><span class="sxs-lookup"><span data-stu-id="11d36-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d36-133">Header</span><span class="sxs-lookup"><span data-stu-id="11d36-133">Header</span></span><br/>  | <dl> <span data-ttu-id="11d36-134"><dt>D2d1 \_ 1. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11d36-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="11d36-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11d36-135">Library</span></span><br/> | <dl> <span data-ttu-id="11d36-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11d36-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="11d36-137">DLL</span><span class="sxs-lookup"><span data-stu-id="11d36-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="11d36-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11d36-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="11d36-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11d36-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d36-140">Übersicht über Pinsel</span><span class="sxs-lookup"><span data-stu-id="11d36-140">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="11d36-141">**ID2D1Brush**</span><span class="sxs-lookup"><span data-stu-id="11d36-141">**ID2D1Brush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

<span data-ttu-id="11d36-142">�</span><span class="sxs-lookup"><span data-stu-id="11d36-142">�</span></span>

<span data-ttu-id="11d36-143">�</span><span class="sxs-lookup"><span data-stu-id="11d36-143">�</span></span>
