---
title: Unterstützte Pixelformate und Alpha-Modi
description: Beschreibt die Pixel Formate und Alpha Modi, die von den einzelnen renderzieltypen unterstützt werden.
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D, Pixel Formate
- Direct2D, Alpha-Modi
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9a3777cac7cc0a258002d1475fb7b1c6dd2546ca
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104102538"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Unterstützte Pixelformate und Alpha-Modi

In diesem Thema werden die Pixel Formate und Alpha Modi beschrieben, die von den verschiedenen Teilen von Direct2D unterstützt werden, einschließlich der einzelnen renderzieltypen, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)und [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource). Der Abschnitt ist wie folgt gegliedert.

-   [Unterstützte YUV-Formate für die DXGI-Image Quelle](#supported-yuv-formats-for-dxgi-image-source)
-   [Angeben eines Pixel Formats für ein Renderziel](#specifying-a-pixel-format-for-a-render-target)
-   [Unterstützte Formate für ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Unterstützte Formate für ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Unterstützte Formate für kompatibles Renderziel](#supported-formats-for-compatible-render-target)
-   [Unterstützte Formate für das DXGI-Oberflächen Renderziel](#supported-formats-for-dxgi-surface-render-target)
-   [Unterstützte Formate für das Renderziel der WIC-Bitmap](#supported-formats-for-wic-bitmap-render-target)
-   [Unterstützte Formate für ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Angeben eines Pixel Formats für ein ID2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Unterstützte WIC-Formate](#supported-wic-formats)
-   [Verwenden eines nicht unterstützten Formats](#using-an-unsupported-format)
-   [Informationen zu Alpha-Modi](#about-alpha-modes)
    -   [Informationen zu vormultiplizierten und geraden Alpha Modi](#about-premultiplied-and-straight-alpha-modes)
    -   [Die Unterschiede zwischen einem geraden und einem prämultiplizierten Alpha](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Alpha Modus für Renderziele](#alpha-mode-for-render-targets)
    -   [ClearType-und Alpha-Modi](#cleartype-and-alpha-modes)
-   [Zugehörige Themen](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Unterstützte YUV-Formate für die DXGI-Image Quelle

Bei einem [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) handelt es sich um einen abstrahierten Anbieter von Pixeln. Sie kann entweder von WIC ("[**kreateimagesourcefromwic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) " oder " [**idxgisurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) " ("[**kreateimagesourcefromdxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)") aus instanziiert werden.

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) unterstützt denselben Satz von Pixel Formaten und Alpha Modi wie [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

Zusätzlich zu den oben genannten unterstützt ein [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) , das von [**idxgisurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) instanziiert wird, auch einige YUV-Pixel Formate, einschließlich planaren Daten, die in mehrere Oberflächen aufgeteilt sind. Weitere Informationen zu den Anforderungen für die einzelnen Pixel Formate finden Sie unter " [**kreateimagesourcefromdxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) ".



| Format                    |
|---------------------------|
| DXGI- \_ Format \_ ayuv        |
| DXGI- \_ Format \_ NV12        |
| DXGI- \_ Format \_ im YUY2        |
| DXGI- \_ Format \_ P208        |
| DXGI- \_ Format \_ V208        |
| DXGI- \_ Format \_ v408        |
| DXGI- \_ Format \_ R8 \_ unorm   |
| DXGI- \_ Format \_ R8G8 \_ unorm |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Angeben eines Pixel Formats für ein Renderziel

Wenn Sie ein Renderziel erstellen, müssen Sie das zugehörige Pixel Format angeben. Um das Pixel Format anzugeben, verwenden Sie eine [**D2D1 \_ Pixel \_ Format**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) -Struktur, um den **Pixel Format** -Member einer [**D2D1- \_ \_ Renderziel- \_ Eigenschaften**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Struktur festzulegen. Anschließend übergeben Sie diese Struktur an die entsprechende Create-Methode, wie z. b. [**ID2D1Factory:: anatehwndrendertarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

Die Struktur des [**D2D1- \_ Pixel \_ Formats**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) weist zwei Felder auf:

-   **Format**, ein [DXGI- \_ Format](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Wert, der die Größe und Anordnung von Kanälen in jedem Pixel beschreibt, und
-   **Alpha**, ein [**D2D1- \_ alpha \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) -Moduswert, der beschreibt, wie Alpha Informationen interpretiert werden.

Im folgenden Beispiel wird eine [**D2D1 \_ Pixel- \_ Format**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) Struktur erstellt und verwendet, um das Pixel Format und den Alpha Modus eines [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)anzugeben.


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );

```



Verschiedene Renderziele unterstützen verschiedene Kombinationen aus Format und Alpha Modus. In den folgenden Abschnitten werden die von jedem Renderziel unterstützten Formate und Alpha Kombinationen aufgelistet.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Unterstützte Formate für ID2D1HwndRenderTarget

Die unterstützten Formate für ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) sind davon abhängig, ob es mithilfe von Hardware oder Software gerendert wird oder ob Direct2D standardmäßig automatisch den Renderingmodus behandelt.

> [!Note]  
> Es wird empfohlen, dass Sie das [**DXGI- \_ Format \_ B8G8R8A8 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) als Pixel Format verwenden, um die Leistung zu verbessern. Dies ist besonders hilfreich für softwarerenderziele. BGRA-Format Ziele erzielen eine bessere Leistung als RGBA-Formate.

 

Wenn Sie ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)erstellen, verwenden Sie die [**D2D1 \_ \_ Renderziel \_ Eigenschaften**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) -Struktur, um Renderingoptionen anzugeben. Die Optionen umfassen das Pixel Format, wie im vorherigen Abschnitt erwähnt. Mit dem type-Feld dieser Struktur können Sie angeben, ob das Renderziel in Hardware oder Software gerendert wird oder ob Direct2D den Renderingmodus automatisch bestimmen soll.

Um Direct2D zu ermöglichen, festzustellen, ob das Renderziel Hardware-oder Software Rendering verwendet, verwenden Sie die [**Standardeinstellung D2D1 \_ \_ renderzieltyp \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .

In der folgenden Tabelle werden die unterstützten Formate für [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekte aufgelistet, die mit der [**Standardeinstellung D2D1- \_ \_ renderzieltyp \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) erstellt werden.



| Format                        | Alpha-Modus                       |
|-------------------------------|----------------------------------|
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ unbekannt       |



 

Wenn Sie erzwingen möchten, dass ein Renderziel das Hardware Rendering verwendet, verwenden Sie die [**Hardware Einstellung D2D1 \_ Rendering \_ Target \_ Type \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . In der folgenden Tabelle sind die unterstützten Formate für [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekte aufgeführt, die das Hardware Rendering explizit verwenden.



| Format                        | Alpha-Modus                       |
|-------------------------------|----------------------------------|
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ R8G8B8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ R8G8B8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ R8G8B8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ unbekannt       |



 

Wenn Sie erzwingen möchten, dass ein Renderziel das Software Rendering verwendet, verwenden Sie die [**Software Einstellung D2D1 \_ \_ renderzieltyp \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . In der folgenden Tabelle sind die unterstützten Formate für [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekte aufgeführt, die das Software Rendering explizit verwenden.



| Format                        | Alpha-Modus                       |
|-------------------------------|----------------------------------|
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ unbekannt       |



 

Unabhängig davon, ob die [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) Hardware beschleunigt ist, verwendet das [DXGI-Format \_ \_ unbekanntes](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Format B8G8R8A8 standardmäßig das [DXGI \_ \_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Format, und der Modus " [**\_ \_ \_ unbekannter**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha Modus im D2D1 Alpha Modus" verwendet standardmäßig den **D2D1 \_ alpha \_ Modus \_** .

## <a name="supported-formats-for-id2d1devicecontext"></a>Unterstützte Formate für ID2D1DeviceContext

Ab Windows 8 nutzt der [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) mehr der Direct3D-High- [**Color-Formate**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , wie z. b.:

-   DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ R16G16B16A16 \_ unorm
-   DXGI- \_ Format \_ R16G16B16A16 \_ float
-   DXGI- \_ Format \_ R32G32B32A32 \_ float

Verwenden Sie die [**ID2D1DeviceContext:: isdxgiformatsupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) -Methode, um festzustellen, ob ein Format in einem bestimmten Gerätekontext funktioniert. Diese Formate können auch in einem [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)funktionieren.

Diese Formate sind zusätzlich zu den von der [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Schnittstelle in Windows 7 unterstützten Formaten. Weitere Informationen finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md) .

## <a name="supported-formats-for-compatible-render-target"></a>Unterstützte Formate für kompatibles Renderziel

Ein kompatibles Renderziel (ein [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) , das von einer der [**ID2D1RenderTarget:: foratecompatiblerendertarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) -Methoden erstellt wird) erbt die unterstützten Formate und Alpha Modi des Renderziels, von dem es erstellt wurde. Ein kompatibles Renderziel unterstützt auch die folgenden Kombinationen aus Format und Alpha Modus, unabhängig davon, was das übergeordnete Element unterstützt



| Format                  | Alpha-Modus                       |
|-------------------------|----------------------------------|
| DXGI- \_ Format \_ a8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ a8 \_ unorm | D2D1 \_ alpha \_ Modus \_ direkt      |
| DXGI- \_ Format \_ unbekannt   | D2D1 \_ alpha \_ Modus \_ unbekannt       |



 

Im [DXGI \_ \_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Format "unbekanntes Format" wird standardmäßig das übergeordnete renderzielformat verwendet, und der D2D1-Alpha Modus " [**\_ \_ \_ unbekannter**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha Modus" verwendet standardmäßig den **D2D1 \_ alpha- \_ Modus \_** .

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Unterstützte Formate für das DXGI-Oberflächen Renderziel

Ein DXGI-Renderziel ist ein [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Wert, der von einer der [**ID2D1Factory:: erendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) -Methoden erstellt wird. Es unterstützt die folgenden Kombinationen aus Format und Alpha Modus.



| Format                        | Alpha-Modus                       |
|-------------------------------|----------------------------------|
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ R8G8B8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ R8G8B8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ a8 \_ unorm       | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ a8 \_ unorm       | D2D1 \_ alpha \_ Modus \_ direkt      |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ ignorieren        |



 

> [!Note]  
> Das Format muss mit dem Format der DXGI-Oberfläche identisch sein, mit der das Renderziel der DXGI-Oberfläche gezeichnet wird.

 

Das Format " [ \_ \_ unbekanntes DXGI-Format](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) " verwendet standardmäßig das Format der DXGI-Oberfläche. Verwenden Sie nicht den Modus "Unbekannter Alpha Modus im [**D2D1 \_ alpha \_ Modus \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) " mit einem DXGI-Oberflächen Renderziel. Es hat keinen Standardwert und bewirkt, dass das Renderziel der DXGI-Oberfläche nicht ausgeführt wird.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Unterstützte Formate für das Renderziel der WIC-Bitmap

Ein WIC-Bitmap-Renderziel ist eine [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) , die von einer der [**ID2D1Factory:: | atewicbitmaprendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) -Methoden erstellt wird. Es unterstützt die folgenden Kombinationen aus Format und Alpha Modus.



| Format                        | Alpha-Modus                       |
|-------------------------------|----------------------------------|
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ a8 \_ unorm       | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ a8 \_ unorm       | D2D1 \_ alpha \_ Modus \_ direkt      |
| DXGI- \_ Format \_ a8 \_ unorm       | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ unbekannt         | D2D1 \_ alpha \_ Modus \_ unbekannt       |



 

Das Pixel Format des WIC-Bitmap-Ziels muss mit dem Pixel Format der WIC-Bitmap identisch sein.

Im [DXGI \_ \_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Format "unbekanntes Format" wird standardmäßig das WIC-Bitmapformat verwendet, und im Modus " [**D2D1 \_ alpha \_ Mode \_ Unknown**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha" wird standardmäßig der WIC-bitmapmodus verwendet.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Unterstützte Formate für ID2D1DCRenderTarget

Ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) unterstützt die folgenden Kombinationen aus Format und Alpha Modus.



| Format                        | Alpha-Modus                       |
|-------------------------------|----------------------------------|
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren        |



 

Verwenden Sie nicht das Format " [ \_ \_ unbekanntes DXGI-Format](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) " oder den D2D1-Alpha Modus " [**\_ \_ \_ unbekannter**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha Modus" mit einem [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)-Wert. Es hat keinen Standardwert und bewirkt, dass die **ID2D1DCRenderTarget** -Erstellung fehlschlägt.

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Angeben eines Pixel Formats für ein ID2D1Bitmap

Im allgemeinen unterstützen [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekte die folgenden Formate und Alpha Modi (mit einigen Einschränkungen, die in den folgenden Abschnitten beschrieben werden).



| Format                                                      | Alpha-Modus                       |
|-------------------------------------------------------------|----------------------------------|
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm                               | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm                               | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ B8G8R8A8 \_ unorm                               | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ a8 \_ unorm                                     | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ a8 \_ unorm                                     | D2D1 \_ alpha \_ Modus \_ direkt      |
| DXGI- \_ Format \_ a8 \_ unorm                                     | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI- \_ Format \_ unbekannt                                       | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI- \_ Format \_ unbekannt                                       | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI- \_ Format \_ unbekannt                                       | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI \_ \_ -Format B8G8R8X8 \_ unorm (nur Windows 8.1 und höher) | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI \_ \_ -Format BC1 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI \_ \_ -Format BC1 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI \_ \_ -Format BC1 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI \_ \_ -Format BC2 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI \_ \_ -Format BC2 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI \_ \_ -Format BC2 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus \_ unbekannt       |
| DXGI \_ \_ -Format BC3 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert |
| DXGI \_ \_ -Format BC3 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus \_ ignorieren        |
| DXGI \_ \_ -Format BC3 \_ unorm (nur Windows 8.1 und höher)      | D2D1 \_ alpha \_ Modus \_ unbekannt       |



 

Wenn Sie die [**ID2D1RenderTarget:: kreatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) -Methode verwenden, verwenden Sie das Pixel **Format** -Feld einer [**D2D1 \_ Bitmap \_ Properties**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) -Struktur, um das Pixel Format des neuen Renderziels anzugeben. Es muss dem Pixel Format der [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Quelle entsprechen.

Wenn Sie [**die Methode "**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) " mit der Methode "D2D1" verwenden, verwenden Sie das Feld " **Pixel Format** " einer [**\_ Bitmap \_ Properties**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) -Struktur (anstelle des **Pixel Format** -Members einer [**D2D1 \_ \_ Renderziel- \_ Eigenschaften**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Struktur), um das Pixel Format des neuen Renderziels anzugeben. Es muss dem Pixel Format der WIC-Bitmapquelle entsprechen.

> [!Note]  
> Weitere Informationen zur Unterstützung für Block komprimierte Pixel Formate (BCN) finden Sie unter [Block Komprimierung (Block Komprimierung](block-compression.md)).

 

### <a name="supported-wic-formats"></a>Unterstützte WIC-Formate

Wenn Sie die Methode " [**kreatebitmapfromwicbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) " verwenden, um eine Bitmap aus einer WIC-Bitmap zu erstellen, oder wenn Sie die Methode " [**kreatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) " mit [**iwicbitmaplock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock)verwenden, muss die WIC-Quelle in einem von Direct2D unterstützten Format vorliegen.



| WIC-Format                     | Entsprechendes DXGI-Format     | Entsprechender Alpha-Modus                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | DXGI- \_ Format \_ a8 \_ unorm       | D2D1 \_ alpha \_ Modus im \_ geraden-oder D2D1- \_ alpha \_ Modus \_ |
| GUID \_ WICPixelFormat32bppPRGBA | DXGI- \_ Format \_ R8G8B8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert oder D2D1 \_ alpha \_ Modus \_ ignorieren   |
| GUID \_ WICPixelFormat32bppBGR   | DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus \_ ignorieren                                       |
| GUID \_ WICPixelFormat32bppPBGRA | DXGI- \_ Format \_ B8G8R8A8 \_ unorm | D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert                                |



 

Ein Beispiel, das zeigt, wie Sie eine WIC-Bitmap in ein unterstütztes Format konvertieren, finden Sie unter Gewusst [wie: Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="using-an-unsupported-format"></a>Verwenden eines nicht unterstützten Formats

Die Verwendung einer beliebigen Kombination aus den in den früheren Tabellen aufgeführten Pixel Formaten und Alpha Modi führt zu einem [**D2DERR \_ nicht unterstützten \_ Pixel \_ Format**](direct2d-error-codes.md) oder einem **E \_ invalidArg** -Fehler.

## <a name="about-alpha-modes"></a>Informationen zu Alpha-Modi

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Informationen zu vormultiplizierten und geraden Alpha Modi

Die [**D2D1 \_ alpha \_ Mode**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) -Enumeration gibt an, ob der Alphakanal ein prämultipliziertes Alpha, ein einfaches Alpha oder eine ignoriert und als nicht transparent angesehen werden soll. Bei der geraden Alpha Angabe gibt der Alphakanal einen Wert an, der der Transparenz einer Farbe entspricht.

Farben werden unabhängig vom Zielformat immer als geradliniges Alpha durch Direct2D Zeichnungs Befehle und Pinsel behandelt.

Mit einem prämultiplizierten Alpha wird jeder Farbkanal durch den Alpha-Wert skaliert. In der Regel ist kein Farb Kanal Wert größer als der Wert des Alphakanals. Wenn ein farbchannelwert in einem vorab multiplizierten Format größer als der Alphakanal ist, erstellt der standardmäßige quellenover-Mischungs mathematische eine Additive Mischung.

Der Wert des Alphakanals selbst ist sowohl in der geraden als auch im vorab multiplizierten Alpha identisch.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>Die Unterschiede zwischen einem geraden und einem prämultiplizierten Alpha

Beim Beschreiben einer RGBA-Farbe mithilfe von gerader Alpha wird der Alpha-Wert der Farbe im Alphakanal gespeichert. Um z. b. eine rote Farbe zu beschreiben, die 60% undurchsichtig ist, verwenden Sie die folgenden Werte: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). Der Wert 255 gibt vollständig rot an, und 153 (60 Prozent von 255) gibt an, dass die Farbe eine Deckkraft von 60 Prozent aufweisen soll.

Beim Beschreiben einer RGBA-Farbe mithilfe von prämultipliziertem Alpha wird jede Farbe mit dem Alpha-Wert multipliziert: (255 \* 0,6, 0 \* 0,6, 0 \* 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Unabhängig vom Alpha Modus des Renderziels werden [**D2D1 \_ Color \_ F**](d2d1-color-f.md) -Werte immer als gerades Alpha interpretiert. Wenn Sie z. b. die Farbe eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) für die Verwendung mit einem Renderziel angeben, das den Modus mit dem prämultiplizierten Alpha verwendet, geben Sie die Farbe genau so an, als wäre das Renderziel gerade alpha. Wenn Sie mit dem Pinsel zeichnen, übersetzt Direct2D die Farbe für Sie in das Zielformat.

### <a name="alpha-mode-for-render-targets"></a>Alpha Modus für Renderziele

Unabhängig von der Alpha Modus-Einstellung unterstützen die Inhalte eines Renderziels Transparenz. Wenn Sie z. b. ein teilweise transparentes rotes Rechteck mit einem Renderziel mit dem Alpha Modus " [**D2D1 \_ alpha \_ Mode \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)" zeichnen, wird das Rechteck als Rosa angezeigt (wenn der Hintergrund weiß ist).

Wenn Sie ein teilweise transparentes rotes Rechteck zeichnen, während der Alpha Modus den [**D2D1- \_ alpha \_ Modus \_ vormultipliziert**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)ist, wird das Rechteck als Rosa angezeigt (vorausgesetzt, der Hintergrund ist weiß), und Sie können es bis auf das Renderziel sehen. Dies ist hilfreich, wenn Sie ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) verwenden, um ein transparentes Fenster zu Renten, oder wenn Sie ein kompatibles Renderziel (ein [**Renderziel, das von der Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) "Methode" erstellt wurde) zum Erstellen einer Bitmap verwenden, die Transparenz unterstützt.

### <a name="cleartype-and-alpha-modes"></a>ClearType-und Alpha-Modi

Wenn Sie für ein Renderziel einen anderen Alpha Modus als [**D2D1 \_ alpha \_ Mode \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) angeben, ändert sich der Text-Antialiasing-Modus automatisch von [**D2D1 \_ Text \_ Antialias Mode \_ ClearType**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) in **D2D1 \_ Text \_ Antialias \_ Mode Grayscale**. (Wenn Sie den Alpha Modus " **D2D1 \_ alpha \_ Mode \_ Unknown**" angeben, legt Direct2D abhängig von der Art des Renderziels das Alpha für Sie fest.)

Sie können die [**settextantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) -Methode verwenden, um den Text-antialiasmodus wieder in den [**D2D1-Text-antialiasmoduscleartype \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode)zu ändern, aber das Rendern von ClearType-Text auf eine transparente Oberfläche kann zu Wenn Sie ClearType-Text in einem transparenten Renderziel Renderziel, empfiehlt es sich, eine der beiden folgenden Techniken zu verwenden.

-   Verwenden Sie die [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) -Methode, um das Renderziel in den Bereich zu schneiden, in dem der Text gerendert wird, und geben Sie dann die [**Clear**](id2d1rendertarget-clear.md) -Methode an, und geben Sie eine nicht transparente Farbe an.
-   Verwenden Sie [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) , um ein undurchsichtiges Rechteck hinter dem Bereich zu zeichnen, in dem der Text gerendert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**D2D1 \_ Pixel \_ Format**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**D2D1 \_ alpha \_ Modus**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[DXGI- \_ Format](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 