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
# <a name="compatible-a8-render-targets-overview"></a>Übersicht über kompatible A8-Renderziele

In diesem Thema werden die Grundlagen eines kompatiblen A8-Renderziels beschrieben und Beispiele für deren Verwendung beschrieben.

Ein kompatibles A8-Renderziel ist ein kompatibles Renderziel ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)), das ein A8-Pixel Format (DXGI- \_ Format \_ a8 \_ unorm) verwendet. Sie können ein kompatibles A8-Renderziel verwenden, um die Leistung der Anwendung zu verbessern und während der Text Animation ein reibungsloseres Ein kompatibles A8-Renderziel ist besonders nützlich, wenn Sie versuchen, Folgendes zu verbessern:

-   Die Framerate der Anwendung, die Text oder eine Antialiasing-Geometrie rendert, die nur einfache Animationen enthält, wie z. b. Übersetzung, Drehung, Skalierung oder Farbänderungen.

-   Die visuelle Kontinuität der Anwendung, die Text während einer Animation ausdehnt und abmindert.

Wenn Sie ein kompatibles A8-Renderziel erstellen möchten, verwenden Sie die ID2D1RenderTarget::-Methode der Methode " [**:: kreatecompatiblerendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) " \_ und das \_ \_ unorm-Pixel Format für das DXGI-Format. Weitere Informationen zu Pixel Formaten finden Sie [unter Unterstützte Pixel Formate und Alpha-Modi](./supported-pixel-formats-and-alpha-modes.md).

Wenn Sie z. b. den im folgenden Screenshot gezeigten Text effizient animieren möchten, verwenden Sie ein kompatibles A8-Renderziel, um den Text als Deck Kraft Maske zwischenzuspeichern. Wenden Sie dann Transformationen auf die Deck Kraft Maske an, um schnelle renderingergebnisse zu erzielen.

![Screenshot des zu animierenden Texts](images/a8rendertarget.png)

Dies wird im folgenden Code veranschaulicht. Er erstellt ein kompatibles A8-Renderziel, ruft die Bitmap davon ab und rendert dann die Bitmap mithilfe von [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md).

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

## <a name="related-topics"></a>Zugehörige Themen

[Direct2D-Referenz](reference.md)