---
title: ID2D1RenderTarget drawrechteck-Methoden (D2d1 \_ 1. h)
description: Zeichnet den Umriss eines Rechtecks, das über die angegebenen Dimensionen und den angegebenen Strich Stil verfügt.
ms.assetid: 3f8c0754-fa68-4b5b-812f-24d8b544ba6e
keywords:
- Drawrechteck-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4c1f846ca0bc1ddcb52696667edcb87291ae05df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369958"
---
# <a name="id2d1rendertargetdrawrectangle-methods"></a><span data-ttu-id="2b2db-104">ID2D1RenderTarget::D rawrechteck-Methoden</span><span class="sxs-lookup"><span data-stu-id="2b2db-104">ID2D1RenderTarget::DrawRectangle methods</span></span>

<span data-ttu-id="2b2db-105">Zeichnet den Umriss eines Rechtecks, das über die angegebenen Dimensionen und den angegebenen Strich Stil verfügt.</span><span class="sxs-lookup"><span data-stu-id="2b2db-105">Draws the outline of a rectangle that has the specified dimensions and stroke style.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2b2db-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="2b2db-106">Overload list</span></span>



| <span data-ttu-id="2b2db-107">Methode</span><span class="sxs-lookup"><span data-stu-id="2b2db-107">Method</span></span>                                                                                                                                                                   | <span data-ttu-id="2b2db-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b2db-108">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2db-109">[**Drawrechteck (D2D1 \_ Rect \_ F&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="2b2db-109">[**DrawRectangle(D2D1\_RECT\_F&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="2b2db-110">Zeichnet den Umriss eines Rechtecks, das über die angegebenen Dimensionen und den angegebenen Strich Stil verfügt.</span><span class="sxs-lookup"><span data-stu-id="2b2db-110">Draws the outline of a rectangle that has the specified dimensions and stroke style.</span></span> <br/> |
| <span data-ttu-id="2b2db-111">[**Drawrechteck (D2D1 \_ Rect \_ F \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="2b2db-111">[**DrawRectangle(D2D1\_RECT\_F\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="2b2db-112">Zeichnet den Umriss eines Rechtecks, das über die angegebenen Dimensionen und den angegebenen Strich Stil verfügt.</span><span class="sxs-lookup"><span data-stu-id="2b2db-112">Draws the outline of a rectangle that has the specified dimensions and stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="2b2db-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b2db-113">Remarks</span></span>

<span data-ttu-id="2b2db-114">Wenn diese Methode fehlschlägt, wird kein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b2db-114">When this method fails, it does not return an error code.</span></span> <span data-ttu-id="2b2db-115">Um zu ermitteln, ob eine Zeichnungs Methode (z. b. **drawrechteck**) fehlgeschlagen ist, überprüfen Sie das Ergebnis, das von der [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode oder der [**ID2D1RenderTarget:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)</span><span class="sxs-lookup"><span data-stu-id="2b2db-115">To determine whether a drawing method (such as **DrawRectangle**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2b2db-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b2db-116">Examples</span></span>

<span data-ttu-id="2b2db-117">Im folgenden Beispiel wird ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) -Zeichen verwendet, um mehrere Rechtecke zu zeichnen und auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="2b2db-117">The following example uses an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) to draw and fill several rectangles.</span></span> <span data-ttu-id="2b2db-118">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="2b2db-118">This example produces the output shown in the following illustration.</span></span>

![Abbildung von zwei Rechtecke in einem Raster Hintergrund](images/drawrectangleexample-small.png)


```C++
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&amp;rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&amp;rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="2b2db-120">Ein verwandtes Tutorial finden Sie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="2b2db-120">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2db-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b2db-121">Requirements</span></span>



| <span data-ttu-id="2b2db-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b2db-122">Requirement</span></span> | <span data-ttu-id="2b2db-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2b2db-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2db-124">Header</span><span class="sxs-lookup"><span data-stu-id="2b2db-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2b2db-125"><dt>D2d1 \_ 1. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b2db-125"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="2b2db-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b2db-126">Library</span></span><br/> | <dl> <span data-ttu-id="2b2db-127"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b2db-127"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2b2db-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2b2db-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b2db-129"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b2db-129"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="2b2db-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b2db-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2db-131">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="2b2db-131">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="2b2db-132">Erstellen einer einfachen Direct2D-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2b2db-132">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="2b2db-133">Zeichnen und Ausfüllen einer einfachen Form</span><span class="sxs-lookup"><span data-stu-id="2b2db-133">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="2b2db-134">�</span><span class="sxs-lookup"><span data-stu-id="2b2db-134">�</span></span>

<span data-ttu-id="2b2db-135">�</span><span class="sxs-lookup"><span data-stu-id="2b2db-135">�</span></span>
