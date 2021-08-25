---
title: Unterstützte Pixelformate und Alpha-Modi
description: Beschreibt die Pixelformate und Alphamodi, die von den einzelnen Renderzieltypen unterstützt werden.
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D,Pixelformate
- Direct2D, Alphamodi
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d5b260741cae6aebb447a11692f03dad6e35498a19f33221aa77ac8a8507144a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917160"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Unterstützte Pixelformate und Alpha-Modi

In diesem Thema werden die Pixelformate und Alphamodi beschrieben, die von den verschiedenen Teilen von Direct2D unterstützt werden, einschließlich der einzelnen Renderzieltypen, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)und [**ID2D1ImageSource.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) Der Abschnitt ist wie folgt gegliedert.

-   [Unterstützte YUV-Formate für DXGI-Bildquelle](#supported-yuv-formats-for-dxgi-image-source)
-   [Angeben eines Pixelformats für ein Renderziel](#specifying-a-pixel-format-for-a-render-target)
-   [Unterstützte Formate für ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Unterstützte Formate für ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Unterstützte Formate für kompatibles Renderziel](#supported-formats-for-compatible-render-target)
-   [Unterstützte Formate für DXGI Surface Render Target](#supported-formats-for-dxgi-surface-render-target)
-   [Unterstützte Formate für das WIC-Bitmaprenderingziel](#supported-formats-for-wic-bitmap-render-target)
-   [Unterstützte Formate für ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Angeben eines Pixelformats für eine ID2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Unterstützte WIC-Formate](#supported-wic-formats)
-   [Verwenden eines nicht unterstützten Formats](#using-an-unsupported-format)
-   [Informationen zu Alphamodi](#about-alpha-modes)
    -   [Informationen zu prämultipliierten und geraden Alphamodi](#about-premultiplied-and-straight-alpha-modes)
    -   [Unterschiede zwischen geradem und prämultipliiertem Alpha](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Alphamodus für Renderziele](#alpha-mode-for-render-targets)
    -   [ClearType- und Alphamodi](#cleartype-and-alpha-modes)
-   [Zugehörige Themen](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Unterstützte YUV-Formate für DXGI-Bildquelle

Eine [**ID2D1ImageSource ist**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) ein abstrahiertes Pixelanbieter. Sie kann entweder von WIC ([**CreateImageSourceFromWic oder**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) [**idXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi ) instanziiert werden.**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)

[**ID2D1ImageSourceFromWic unterstützt**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) den gleichen Satz von Pixelformaten und Alphamodi wie [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

Darüber hinaus unterstützt eine [**ID2D1ImageSource,**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) die von [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) instanziiert wird, auch einige YUV-Pixelformate, einschließlich planarer Daten, die in mehrere Oberflächen aufgeteilt sind. Weitere Informationen zu den Anforderungen für jedes Pixelformat finden Sie unter [**CreateImageSourceFromDxgi.**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)



| Format                    |
|---------------------------|
| DXGI \_ FORMAT \_ AYUV        |
| DXGI \_ FORMAT \_ NV12        |
| \_DXGI-FORMAT \_ YUY2        |
| \_DXGI-FORMAT \_ P208        |
| DXGI \_ FORMAT \_ V208        |
| DXGI \_ FORMAT \_ V408        |
| DXGI \_ FORMAT \_ R8 \_ UNORM   |
| DXGI \_ FORMAT \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Angeben eines Pixelformats für ein Renderziel

Wenn Sie ein Renderziel erstellen, müssen Sie dessen Pixelformat angeben. Um das Pixelformat anzugeben, verwenden Sie eine [**D2D1 \_ PIXEL \_ FORMAT-Struktur,**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) um den **pixelFormat-Member** einer [**D2D1 \_ RENDER TARGET \_ \_ PROPERTIES-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) festzulegen. Anschließend übergeben Sie diese Struktur an die entsprechende Create-Methode, z.B. [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

Die [**Struktur D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) verfügt über zwei Felder:

-   **format**, ein [DXGI \_ FORMAT-Wert,](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) der die Größe und Anordnung von Kanälen in jedem Pixel beschreibt, und
-   **alpha**, ein [**D2D1 \_ ALPHA \_ MODE-Wert,**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) der beschreibt, wie Alphainformationen interpretiert werden.

Im folgenden Beispiel wird eine [**D2D1 \_ PIXEL \_ FORMAT-Struktur**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) erstellt und verwendet, um das Pixelformat und den Alphamodus einer [**ID2D1HwndRenderTarget anzugeben.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)


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



Verschiedene Renderziele unterstützen unterschiedliche Format- und Alphamoduskombinationen. In den folgenden Abschnitten werden die Format- und Alphakombinationen aufgeführt, die von den einzelnen Renderziel unterstützt werden.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Unterstützte Formate für ID2D1HwndRenderTarget

Die unterstützten Formate für [**ein ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) hängen davon ab, ob es mithilfe von Hardware oder Software gerendert wird oder ob Direct2D den Renderingmodus standardmäßig automatisch behandelt.

> [!Note]  
> Es wird empfohlen, [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) als Pixelformat zu verwenden, um die Leistung zu verbessern. Dies ist besonders hilfreich für Softwarerenderingziele. BGRA-Formatziele sind besser als RGBA-Formate.

 

Wenn Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)erstellen, verwenden Sie die [**D2D1 \_ RENDER TARGET \_ \_ PROPERTIES-Struktur,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) um Renderingoptionen anzugeben. Die Optionen umfassen das Pixelformat, wie im vorherigen Abschnitt erwähnt. Mit dem Typfeld dieser Struktur können Sie angeben, ob das Renderziel auf Hardware oder Software gerendert wird oder ob Direct2D den Renderingmodus automatisch bestimmen soll.

Um Direct2D zu aktivieren, um zu bestimmen, ob das Renderziel Hardware- oder Softwarerendering verwendet, verwenden Sie die [**Einstellung D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)

In der folgenden Tabelle sind die unterstützten Formate für [**ID2D1HwndRenderTarget-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) aufgeführt, die mithilfe der [**Einstellung D2D1 \_ RENDER TARGET TYPE DEFAULT \_ \_ \_ erstellt**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) werden.



| Format                        | Alphamodus                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ ALPHA-MODUS \_ VORMULTIPLIED |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ ALPHA-MODUS \_ IGNORIEREN        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ ALPHAMODUS \_ UNBEKANNT       |
| DXGI \_ FORMAT \_ UNKNOWN         | D2D1 \_ \_ ALPHA-MODUS \_ VORMULTIPLIED |
| DXGI \_ FORMAT \_ UNKNOWN         | D2D1 \_ \_ ALPHA-MODUS \_ IGNORIEREN        |
| DXGI \_ FORMAT \_ UNKNOWN         | D2D1 \_ \_ ALPHAMODUS \_ UNBEKANNT       |



 

Um zu erzwingen, dass ein Renderziel Hardwarerendering verwendet, verwenden Sie die [**HARDWAREeinstellung D2D1 \_ RENDER TARGET TYPE \_ \_ \_ HARDWARE.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) In der folgenden Tabelle sind die unterstützten Formate für [**ID2D1HwndRenderTarget-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) aufgeführt, die explizit Hardwarerendering verwenden.



| Format                        | Alphamodus                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ ALPHA-MODUS \_ VORMULTIPLIED |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ ALPHA-MODUS \_ IGNORIEREN        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ ALPHAMODUS \_ UNBEKANNT       |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ ALPHA-MODUS \_ VORMULTIPLIED |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ ALPHA-MODUS \_ IGNORIEREN        |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ ALPHAMODUS \_ UNBEKANNT       |
| DXGI \_ FORMAT \_ UNKNOWN         | D2D1 \_ \_ ALPHA-MODUS \_ VORMULTIPLIED |
| DXGI \_ FORMAT \_ UNKNOWN         | D2D1 \_ \_ ALPHA-MODUS \_ IGNORIEREN        |
| DXGI \_ FORMAT \_ UNKNOWN         | D2D1 \_ \_ ALPHAMODUS \_ UNBEKANNT       |



 

Um zu erzwingen, dass ein Renderziel Softwarerendering verwendet, verwenden Sie die [**Einstellung D2D1 \_ RENDER TARGET TYPE \_ \_ \_ SOFTWARE.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) In der folgenden Tabelle sind die unterstützten Formate für [**ID2D1HwndRenderTarget-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) aufgeführt, die explizit Softwarerendering verwenden.



| Format                        | Alphamodus                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |



 

Unabhängig davon, ob [**id2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) hardwarebeschleunigt ist, verwendet das [DXGI \_ FORMAT \_ UNKNOWN-Format](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) standardmäßig [DXGI \_ FORMAT \_ B8G8R8A8,](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) und der [**D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha-Modus verwendet standardmäßig **D2D1 \_ ALPHA MODE \_ \_ IGNORE.**

## <a name="supported-formats-for-id2d1devicecontext"></a>Unterstützte Formate für ID2D1DeviceContext

Ab Windows 8 nutzt der [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) mehr [**direct3D-Formate**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) mit hoher Farbe, z. B.:

-   \_DXGI-FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB
-   \_DXGI-FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB
-   \_DXGI-FORMAT \_ R16G16B16A16 \_ UNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT
-   \_DXGI-FORMAT \_ R32G32B32A32 \_ FLOAT

Verwenden Sie die [**ID2D1DeviceContext::IsDxgiFormatSupported-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) um festzustellen, ob ein Format in einem bestimmten Gerätekontext funktioniert. Diese Formate können auch für eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)funktionieren.

Diese Formate werden zusätzlich zu den Formaten unterstützt, die von der [**ID2D1HwndRenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) in Windows 7 unterstützt werden. Weitere Informationen finden Sie unter [Geräte und Gerätekontexte.](devices-and-device-contexts.md)

## <a name="supported-formats-for-compatible-render-target"></a>Unterstützte Formate für kompatibles Renderziel

Ein kompatibles Renderziel (ein [**ID2D1BitmapRenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) das von einer der [**ID2D1RenderTarget::CreateCompatibleRenderTarget-Methoden**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) erstellt wird) erbt die unterstützten Formate und Alphamodi des Renderziels, das es erstellt hat. Ein kompatibles Renderziel unterstützt auch die folgenden Format- und Alphamoduskombinationen, unabhängig davon, was das übergeordnete Element unterstützt.



| Format                  | Alphamodus                       |
|-------------------------|----------------------------------|
| \_DXGI-FORMAT \_ A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| \_DXGI-FORMAT \_ UNBEKANNT   | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |



 

Das [DXGI \_ FORMAT \_ UNKNOWN-Format](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) verwendet standardmäßig das übergeordnete Renderzielformat, und im [**Modus D2D1 ALPHA MODE \_ \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha wird standardmäßig **D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED verwendet.**

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Unterstützte Formate für DXGI Surface Render Target

Ein DXGI-Renderziel ist ein [**ID2D1RenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) das von einer der [**ID2D1Factory::CreateDxgiSurfaceRenderTarget-Methoden**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) erstellt wird. Es unterstützt die folgenden Format- und Alphamoduskombinationen.



| Format                        | Alphamodus                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| \_DXGI-FORMAT \_ A8 \_ UNORM       | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ A8 \_ UNORM       | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |



 

> [!Note]  
> Das Format muss mit dem Format der DXGI-Oberfläche übereinstimmen, auf die die DXGI-Oberfläche das Renderziel zeichnet.

 

Das [DXGI \_ FORMAT \_ UNKNOWN-Format](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) verwendet standardmäßig das DXGI-Oberflächenformat. Verwenden Sie nicht den [**Alphamodus D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) mit einem DXGI-Oberflächenrenderziel. Er hat keinen Standardwert und führt dazu, dass die Erstellung des DXGI-Oberflächenrenderingziels fehlschlägt.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Unterstützte Formate für WIC-Bitmap-Renderziel

Ein WIC-Bitmaprenderziel ist ein [**ID2D1RenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) das von einer der [**ID2D1Factory::CreateWicBitmapRenderTarget-Methoden**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) erstellt wird. Es unterstützt die folgenden Format- und Alphamoduskombinationen.



| Format                        | Alphamodus                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| \_DXGI-FORMAT \_ A8 \_ UNORM       | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ A8 \_ UNORM       | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| \_DXGI-FORMAT \_ A8 \_ UNORM       | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| \_DXGI-FORMAT \_ UNBEKANNT         | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |



 

Das Pixelformat des WIC-Bitmapziels muss mit dem Pixelformat der WIC-Bitmap übereinstimmen.

Das [FORMAT DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) verwendet standardmäßig das WIC-Bitmapformat, und der [**Alphamodus D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha verwendet standardmäßig den WIC-Bitmap-Alphamodus.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Unterstützte Formate für ID2D1DCRenderTarget

Ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) unterstützt die folgenden Format- und Alphamoduskombinationen.



| Format                        | Alphamodus                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |



 

Verwenden Sie nicht das [FORMAT DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) oder den [**Alphamodus D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) mit einem [**ID2D1DCRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) Er hat keinen Standardwert und führt dazu, dass die **ID2D1DCRenderTarget-Erstellung** fehlschlägt.

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Angeben eines Pixelformats für eine ID2D1Bitmap

Im Allgemeinen unterstützen [**ID2D1Bitmap-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) die folgenden Formate und Alphamodi (mit einigen Einschränkungen, die in den folgenden Absätzen beschrieben werden).



| Format                                                      | Alphamodus                       |
|-------------------------------------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| \_DXGI-FORMAT \_ A8 \_ UNORM                                     | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ A8 \_ UNORM                                     | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| \_DXGI-FORMAT \_ A8 \_ UNORM                                     | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| \_DXGI-FORMAT \_ UNBEKANNT                                       | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| \_DXGI-FORMAT \_ UNBEKANNT                                       | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| \_DXGI-FORMAT \_ UNBEKANNT                                       | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (nur Windows 8.1 und höher) | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (nur Windows 8.1 und höher)      | D2D1 \_ ALPHA \_ MODE \_ UNKNOWN       |



 

Wenn Sie die [**ID2D1RenderTarget::CreateSharedBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) verwenden, verwenden Sie das **Feld pixelFormat** einer [**D2D1 \_ BITMAP \_ PROPERTIES-Struktur,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) um das Pixelformat des neuen Renderziels anzugeben. Sie muss mit dem Pixelformat der [**ID2D1Bitmap-Quelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) übereinstimmen.

Wenn Sie die [**CreateBitmapFromWicBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) verwenden, verwenden Sie das **Feld pixelFormat** einer [**D2D1 \_ BITMAP \_ PROPERTIES-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (anstelle des **pixelsFormat-Members** einer [**D2D1 \_ RENDER TARGET \_ \_ PROPERTIES-Struktur),**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) um das Pixelformat des neuen Renderziels anzugeben. Sie muss mit dem Pixelformat der WIC-Bitmapquelle übereinstimmen.

> [!Note]  
> Weitere Informationen zur Unterstützung für blockkomprimierte Pixelformate (BCn) finden Sie unter [Blockkomprimierung.](block-compression.md)

 

### <a name="supported-wic-formats"></a>Unterstützte WIC-Formate

Wenn Sie die [**CreateBitmapFromWicBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) verwenden, um eine Bitmap aus einer WIC-Bitmap zu erstellen, oder wenn Sie die [**CreateSharedBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) mit einem [**IWICBitmapLock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock)verwenden, muss die WIC-Quelle in einem von Direct2D unterstützten Format vorliegen.



| WIC-Format                     | Entsprechendes DXGI-Format     | Entsprechender Alphamodus                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | \_DXGI-FORMAT \_ A8 \_ UNORM       | D2D1 \_ ALPHA MODE STRAIGHT oder \_ \_ D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED |
| GUID \_ WICPixelFormat32bppPRGBA | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED oder D2D1 \_ ALPHA MODE \_ \_ IGNORE   |
| GUID \_ WICPixelFormat32bppBGR   | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE                                       |
| GUID \_ WICPixelFormat32bppPBGRA | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED                                |



 

Ein Beispiel, das zeigt, wie eine WIC-Bitmap in ein unterstütztes Format konvertiert wird, finden Sie unter [Laden einer Bitmap aus einer Datei.](how-to-load-a-direct2d-bitmap-from-a-file.md)

## <a name="using-an-unsupported-format"></a>Verwenden eines nicht unterstützten Formats

Die Verwendung einer beliebigen Kombination außer den Pixelformaten und Alphamodi, die in den vorherigen Tabellen aufgeführt sind, führt zu einem [**D2DERR \_ UNSUPPORTED \_ PIXEL \_ FORMAT**](direct2d-error-codes.md) oder einem **E \_ INVALIDARG-Fehler.**

## <a name="about-alpha-modes"></a>Informationen zu Alphamodi

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Informationen zu prämultipliierten und geraden Alphamodi

Die [**D2D1 \_ ALPHA \_ MODE-Enumeration**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) gibt an, ob der Alphakanal prämultipliiertes Alpha, gerades Alpha verwendet oder ignoriert und als nicht transparent betrachtet werden soll. Bei geradem Alpha gibt der Alphakanal einen Wert an, der der Transparenz einer Farbe entspricht.

Farben werden von Direct2D-Zeichnungsbefehlen und Pinseln unabhängig vom Zielformat immer als gerades Alpha behandelt.

Bei einem prämultiplizierten Alpha wird jeder Farbkanal durch den Alphawert skaliert. In der Regel ist kein Farbkanalwert größer als der Alphakanalwert. Wenn ein Farbkanalwert in einem vormultiplizierenden Format größer als der Alphakanal ist, erstellt die Standardmathematik für die Quellüberblendung eine additive Mischung.

Der Wert des Alphakanals selbst ist sowohl im geraden als auch im vor multiplizierten Alpha identisch.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>Unterschiede zwischen geradem und prämultipliiertem Alpha

Beim Beschreiben einer RGBA-Farbe mithilfe von geradem Alpha wird der Alphawert der Farbe im Alphakanal gespeichert. Um beispielsweise eine rote Farbe zu beschreiben, die zu 60 % nicht transparent ist, verwenden Sie die folgenden Werte: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). Der Wert 255 gibt vollständiges Rot und 153 (60 Prozent von 255) an, dass die Farbe eine Deckkraft von 60 Prozent aufweisen soll.

Wenn eine RGBA-Farbe mithilfe von prämultiplizierendem Alpha beschrieben wird, wird jede Farbe mit dem Alphawert multipliziert: (255 \* 0,6, 0 \* 0,6, \* 0 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Unabhängig vom Alphamodus des Renderziels werden [**D2D1 \_ COLOR \_ F-Werte**](d2d1-color-f.md) immer als gerades Alpha interpretiert. Wenn Sie z. B. die Farbe eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) für die Verwendung mit einem Renderziel angeben, das den prämultiplizierenden Alphamodus verwendet, geben Sie die Farbe genau so an, wie Sie es beim Renderziel mit geradem Alpha verwenden würden. Wenn Sie mit dem Pinsel zeichnen, übersetzt Direct2D die Farbe für Sie in das Zielformat.

### <a name="alpha-mode-for-render-targets"></a>Alphamodus für Renderziele

Unabhängig von der Einstellung für den Alphamodus unterstützen die Inhalte eines Renderziels Transparenz. Wenn Sie z. B. ein teilweise transparentes rotes Rechteck mit einem Renderziel mit dem Alphamodus [**D2D1 \_ ALPHA \_ MODE \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)zeichnen, wird das Rechteck rot angezeigt (wenn der Hintergrund weiß ist).

Wenn Sie ein teilweise transparentes rotes Rechteck zeichnen, wenn der Alphamodus [**D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)ist, wird das Rechteck rosa angezeigt (vorausgesetzt, der Hintergrund ist weiß), und Sie können es bis zu dem sehen, was sich hinter dem Renderziel befindet. Dies ist nützlich, wenn Sie ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) verwenden, um in einem transparenten Fenster zu rendern, oder wenn Sie ein kompatibles Renderziel (ein Renderziel, das von der [**CreateCompatibleRenderTarget-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) erstellt wurde) verwenden, um eine Bitmap zu erstellen, die Transparenz unterstützt.

### <a name="cleartype-and-alpha-modes"></a>ClearType- und Alphamodi

Wenn Sie für ein Renderziel einen anderen Alphamodus als [**D2D1 \_ ALPHA \_ MODE \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) angeben, ändert sich der Text-Antialiasingmodus automatisch von [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) in **D2D1 \_ TEXT \_ ANTIALIAS \_ MODE GRAYSCALE**. (Wenn Sie den Alphamodus **D2D1 \_ ALPHA \_ MODE \_ UNKNOWN** angeben, legt Direct2D das Alpha für Sie fest, je nach Art des Renderziels.)

Sie können die [**SetTextAntialiasMode-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) verwenden, um den Text-Antialiasmodus zurück in [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode)zu ändern. Das Rendern von ClearType-Text in eine transparente Oberfläche kann jedoch unvorhersehbare Ergebnisse liefern. Wenn Sie ClearType-Text in einem transparenten Renderziel rendern möchten, empfiehlt es sich, eine der beiden folgenden Verfahren zu verwenden.

-   Verwenden Sie die [**PushAxisAlignedClip-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) um das Renderziel auf den Bereich zu beschneiden, in dem der Text gerendert wird. Rufen Sie dann die [**Clear-Methode**](id2d1rendertarget-clear.md) auf, geben Sie eine nicht transparente Farbe an, und rendern Sie ihren Text.
-   Verwenden Sie [**DrawRectangle,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) um ein nicht transparentes Rechteck hinter dem Bereich zu zeichnen, in dem der Text gerendert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_D2D1-PIXELFORMAT \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**\_D2D1-ALPHAMODUS \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[\_DXGI-FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 