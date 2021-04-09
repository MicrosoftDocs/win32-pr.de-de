---
title: D2D1_RECT_F (D2DBaseTypes. h)
description: Stellt ein Rechteck dar, das von den Koordinaten der linken oberen Ecke (Links, oben) und den Koordinaten der unteren rechten Ecke (rechts, unten) definiert wird. | D2D1_RECT_F (D2DBaseTypes. h)
ms.assetid: a961c0e3-fb76-4c07-b76e-47d8c09ada08
keywords:
- D2D1_RECT_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93ce4700e093b9e82fd4334ae9e01485a7fcbb4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050758"
---
# <a name="d2d1_rect_f"></a><span data-ttu-id="cfa59-105">D2D1 \_ Rect \_ F</span><span class="sxs-lookup"><span data-stu-id="cfa59-105">D2D1\_RECT\_F</span></span>

<span data-ttu-id="cfa59-106">Stellt ein Rechteck dar, das von den Koordinaten der linken oberen Ecke (Links, oben) und den Koordinaten der unteren rechten Ecke (rechts, unten) definiert wird.</span><span class="sxs-lookup"><span data-stu-id="cfa59-106">Represents a rectangle defined by the coordinates of the upper-left corner (left, top) and the coordinates of the lower-right corner (right, bottom).</span></span>


```C++
typedef D2D_RECT_F D2D1_RECT_F;
```



## <a name="remarks"></a><span data-ttu-id="cfa59-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfa59-107">Remarks</span></span>

<span data-ttu-id="cfa59-108">**D2D1 \_ Rect \_ f** ist ein neuer Name für die bereits definierte [**D2D \_ Rect \_ f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cfa59-108">**D2D1\_RECT\_F** is a new name for the already defined [**D2D\_RECT\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) struct.</span></span>

## <a name="examples"></a><span data-ttu-id="cfa59-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfa59-109">Examples</span></span>

<span data-ttu-id="cfa59-110">Im folgenden Beispiel wird ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Zeichen verwendet, um mehrere Rechtecke zu zeichnen und auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="cfa59-110">The following example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw and fill several rectangles.</span></span> <span data-ttu-id="cfa59-111">Dieses Beispiel erzeugt eine Ausgabe, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cfa59-111">This example produces output as shown in the following illustration.</span></span>

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
        m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);

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



<span data-ttu-id="cfa59-113">Ein verwandtes Tutorial finden Sie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="cfa59-113">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa59-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfa59-114">Requirements</span></span>



| <span data-ttu-id="cfa59-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfa59-115">Requirement</span></span> | <span data-ttu-id="cfa59-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cfa59-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa59-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfa59-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa59-118">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa59-118">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="cfa59-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfa59-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa59-120">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa59-120">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="cfa59-121">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="cfa59-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="cfa59-122">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa59-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="cfa59-123">Header</span><span class="sxs-lookup"><span data-stu-id="cfa59-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa59-124"><dt>D2DBaseTypes. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfa59-124"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cfa59-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfa59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa59-126">**D2D \_ Rect \_ F**</span><span class="sxs-lookup"><span data-stu-id="cfa59-126">**D2D\_RECT\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f)
</dt> <dt>

[<span data-ttu-id="cfa59-127">Erstellen einer einfachen Direct2D-Anwendung</span><span class="sxs-lookup"><span data-stu-id="cfa59-127">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

