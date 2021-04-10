---
title: Zeichnen einer Bitmap
description: Zeigt, wie Bitmaps mit Direct2D dargestellt werden.
ms.assetid: 9c6fc8b1-47ba-46fa-b812-2636cd8ff2b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfa13b75b4fe34ce6ff2b80598fac35f8483a2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858298"
---
# <a name="how-to-draw-a-bitmap"></a><span data-ttu-id="02a80-103">Zeichnen einer Bitmap</span><span class="sxs-lookup"><span data-stu-id="02a80-103">How to Draw a Bitmap</span></span>

<span data-ttu-id="02a80-104">Verwenden Sie zum Rendering einer Bitmap die [**ID2D1RenderTarget::D rawbitmap**](id2d1rendertarget-drawbitmap.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="02a80-104">To render a bitmap, use the [**ID2D1RenderTarget::DrawBitmap**](id2d1rendertarget-drawbitmap.md) method.</span></span> <span data-ttu-id="02a80-105">Im folgenden Beispiel wird gezeigt, wie mit der **drawbitmap** -Methode ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="02a80-105">The following example shows how to use the **DrawBitmap** method to draw an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="02a80-106">Er erstellt die in der folgenden Abbildung gezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="02a80-106">It creates the output shown in the following illustration.</span></span>

![Abbildung einer ursprünglichen Bitmap und resultierenden Bitmaps mit unterschiedlichen Deckkraft Einstellungen und Transformationen](images/drawbitmapexample.png)

<span data-ttu-id="02a80-108">Erstellen Sie zuerst eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="02a80-108">First, create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="02a80-109">Im folgenden Beispiel wird eine Bitmap aus der Ressourcen Datei der Anwendung geladen und als *m \_ pbitmap* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="02a80-109">The following example loads a bitmap from the application's resource file and stores it as *m\_pBitmap*.</span></span> <span data-ttu-id="02a80-110">(Informationen zur Implementierung der-Methode finden Sie `LoadResourceBitmap` unter Gewusst [wie: Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md).)</span><span class="sxs-lookup"><span data-stu-id="02a80-110">(To see how the `LoadResourceBitmap` method is implemented, refer to [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).)</span></span>


```C++
// Create a bitmap from an application resource.
hr = LoadResourceBitmap(
    m_pRenderTarget,
    m_pWICFactory,
    L"SampleImage",
    L"Image",
    200,
    0,
    &m_pBitmap
    );
```



<span data-ttu-id="02a80-111">Erstellen Sie die [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) in derselben Methode, in der Sie das Renderziel erstellt haben, das Sie zum Zeichnen der Bitmap verwenden, und geben Sie die Bitmap frei, wenn das Renderziel freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02a80-111">Create the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) in the same method where you created the render target that you will use to draw the bitmap, and release the bitmap when the render target is released.</span></span>

<span data-ttu-id="02a80-112">Nachdem die Bitmap erstellt wurde, können Sie Sie darstellen.</span><span class="sxs-lookup"><span data-stu-id="02a80-112">Once the bitmap is created, render it.</span></span> <span data-ttu-id="02a80-113">Im folgenden Beispiel wird die [**drawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) -Methode verwendet, um eine Bitmap mehrmals mit unterschiedlichen Größen-und Deckkraft Einstellungen zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="02a80-113">The following example uses the [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) method to render a bitmap several times using different size and opacity settings.</span></span>


```C++
HRESULT DrawBitmapExample::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Retrieve the size of the bitmap.
        D2D1_SIZE_F size = m_pBitmap->GetSize();

        D2D1_POINT_2F upperLeftCorner = D2D1::Point2F(100.f, 10.f);

        // Draw a bitmap.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + size.width,
                upperLeftCorner.y + size.height)
            );

        // Draw the next bitmap below the first one.
        upperLeftCorner.y = upperLeftCorner.y + size.height + 10.f;

        // Scale the bitmap to half its size using the linear
        // interoplation mode and draw it.
        float scaledWidth = size.width / 2.f;
        float scaledHeight = size.height / 2.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw the bitmap at half its size and half its opacity.
        upperLeftCorner.y = upperLeftCorner.y + size.height / 2.f + 10.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw a series of bitmaps with different opacity and
        // rotation angles.
        upperLeftCorner.y = upperLeftCorner.y + scaledHeight + 20.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        D2D1_POINT_2F lowerLeftCorner = D2D1::Point2F(upperLeftCorner.x, upperLeftCorner.y + scaledHeight);
        D2D1_POINT_2F imageCenter = D2D1::Point2F(
            upperLeftCorner.x + scaledWidth / 2,
            upperLeftCorner.y + scaledHeight / 2
            );

        // Rotate the next bitmap by -20 degrees.
        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-20, imageCenter)
            );

        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.75,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-45, imageCenter)
            );

        // Make the last bitmap fully opaque.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="02a80-114">Die [**drawbitmap**](id2d1rendertarget-drawbitmap.md) -Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="02a80-114">The [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) method does not return an error code if it fails.</span></span> <span data-ttu-id="02a80-115">Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **drawbitmap**) fehlgeschlagen ist, überprüfen Sie das von der [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode zurückgegebene Ergebnis, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="02a80-115">To determine whether a drawing operation (such as **DrawBitmap**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method, as shown in the following example.</span></span>


```C++
hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="02a80-116">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="02a80-116">Code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02a80-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02a80-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02a80-118">**Drawbitmap**</span><span class="sxs-lookup"><span data-stu-id="02a80-118">**DrawBitmap**</span></span>](id2d1rendertarget-drawbitmap.md)
</dt> <dt>

[<span data-ttu-id="02a80-119">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="02a80-119">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="02a80-120">Laden einer Bitmap aus einer Ressource</span><span class="sxs-lookup"><span data-stu-id="02a80-120">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 