---
title: Übersicht über kompatible A8-Renderziele
description: Beschreibt die Grundlagen von kompatiblen A8-Renderingzielen und bietet Beispiele für die Verwendung.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "103949281"
---
# <a name="compatible-a8-render-targets-overview"></a><span data-ttu-id="b5429-103">Übersicht über kompatible A8-Renderziele</span><span class="sxs-lookup"><span data-stu-id="b5429-103">Compatible A8 render targets overview</span></span>

<span data-ttu-id="b5429-104">In diesem Thema werden die Grundlagen eines kompatiblen A8-Renderziels beschrieben und Beispiele für deren Verwendung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b5429-104">This topic describes the basics of a compatible A8 render target, and provides examples of how to use it.</span></span>

<span data-ttu-id="b5429-105">Ein kompatibles A8-Renderziel ist ein kompatibles Renderziel ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)), das ein A8-Pixel Format (DXGI- \_ Format \_ a8 \_ unorm) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5429-105">A compatible A8 render target is a compatible render target ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) that uses an A8 pixel format (DXGI\_FORMAT\_A8\_UNORM).</span></span> <span data-ttu-id="b5429-106">Sie können ein kompatibles A8-Renderziel verwenden, um die Leistung der Anwendung zu verbessern und während der Text Animation ein reibungsloseres</span><span class="sxs-lookup"><span data-stu-id="b5429-106">You can use a compatible A8 render target to improve the application's performance and provide smoother transitions during text animation.</span></span> <span data-ttu-id="b5429-107">Ein kompatibles A8-Renderziel ist besonders nützlich, wenn Sie versuchen, Folgendes zu verbessern:</span><span class="sxs-lookup"><span data-stu-id="b5429-107">A compatible A8 render target is particular useful when you try to improve the following:</span></span>

-   <span data-ttu-id="b5429-108">Die Framerate der Anwendung, die Text oder eine Antialiasing-Geometrie rendert, die nur einfache Animationen enthält, wie z. b. Übersetzung, Drehung, Skalierung oder Farbänderungen.</span><span class="sxs-lookup"><span data-stu-id="b5429-108">The frame rate of the application that renders text or anti-aliased geometry that includes only simple animations, such as translation, rotation, scale, or color changes.</span></span>

-   <span data-ttu-id="b5429-109">Die visuelle Kontinuität der Anwendung, die Text während einer Animation ausdehnt und abmindert.</span><span class="sxs-lookup"><span data-stu-id="b5429-109">The visual continuity of the application that stretches and diminshes text during an animation.</span></span>

<span data-ttu-id="b5429-110">Wenn Sie ein kompatibles A8-Renderziel erstellen möchten, verwenden Sie die ID2D1RenderTarget::-Methode der Methode " [**:: kreatecompatiblerendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) " \_ und das \_ \_ unorm-Pixel Format für das DXGI-Format.</span><span class="sxs-lookup"><span data-stu-id="b5429-110">To create a compatible A8 render target, use the [**ID2D1RenderTarget::CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) method together with the DXGI\_FORMAT\_A8\_UNORM pixel format, and specify a returned compatible render target.</span></span> <span data-ttu-id="b5429-111">Weitere Informationen zu Pixel Formaten finden Sie [unter Unterstützte Pixel Formate und Alpha-Modi](./supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="b5429-111">For more information about pixel formats, see [Supported pixel formats and alpha modes](./supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="b5429-112">Wenn Sie z. b. den im folgenden Screenshot gezeigten Text effizient animieren möchten, verwenden Sie ein kompatibles A8-Renderziel, um den Text als Deck Kraft Maske zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="b5429-112">For example, to efficiently animate the text that is shown in the following screen shot, use a compatible A8 render target to cache the text as an opacity mask.</span></span> <span data-ttu-id="b5429-113">Wenden Sie dann Transformationen auf die Deck Kraft Maske an, um schnelle renderingergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="b5429-113">Then, apply transformations to the opacity mask to achieve fast rendering results.</span></span>

![Screenshot des zu animierenden Texts](images/a8rendertarget.png)

<span data-ttu-id="b5429-115">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b5429-115">The following code shows how to do this.</span></span> <span data-ttu-id="b5429-116">Er erstellt ein kompatibles A8-Renderziel, ruft die Bitmap davon ab und rendert dann die Bitmap mithilfe von [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md).</span><span class="sxs-lookup"><span data-stu-id="b5429-116">It creates a compatible A8 render target, retrieves the bitmap from it, and then renders the bitmap by using [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).</span></span>

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a><span data-ttu-id="b5429-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5429-117">Related topics</span></span>

[<span data-ttu-id="b5429-118">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="b5429-118">Direct2D Reference</span></span>](reference.md)