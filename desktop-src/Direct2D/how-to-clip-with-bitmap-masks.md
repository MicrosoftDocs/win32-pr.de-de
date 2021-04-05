---
title: Verwenden einer Bitmap als Deck Kraft Maske
description: Zeigt, wie Sie einen Bereich mit bitmapmasken Ausschneiden.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948985"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Verwenden einer Bitmap als Deck Kraft Maske

In diesem Thema wird beschrieben, wie Sie eine Bitmap als eine opacty mask verwenden, indem Sie die [**ID2D1Factory:: fillopacitymask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) -Methode aufrufen. Die Deck Kraft Maske ist eine Bitmap, die die durch den Alphakanal dargestellten Abdeckungs Informationen bereitstellt, die die Transparenz des gerenderten Inhalts steuert. Diese Vorgehensweise ist effizienter als die Verwendung von Ebenen mit einer Deck Kraft Maske. Weitere Informationen finden Sie unter [Übersicht über Ebenen](direct2d-layers-overview.md).

**So schneiden Sie einen Bereich ab**

1.  Laden Sie die ursprüngliche Bitmap aus einer Ressource. Weitere Informationen zum Laden einer Bitmap finden Sie unter Gewusst [wie: Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md).
2.  Laden Sie die bitmapmaske aus einer Ressource.
3.  Erstellen Sie einen Bitmap-Pinsel mit der ursprünglichen Bitmap. Informationen zum Erstellen eines Bitmap-Pinsels finden Sie unter [Erstellen eines Bitmap-Pinsels](how-to-create-a-bitmap-brush.md).
4.  Aufrufen von [**ID2D1Factory:: setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , um den AntiAlias Modus für das Renderziel auf den D2D1- \_ Antialias \_ Modus \_ für [**ID2D1Factory:: fillopacitymask**](id2d1rendertarget-fillopacitymask.md) festzulegen, um zu funktionieren.
5.  Ruft [**fillopacitymask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) mit der Bitmap-Maske und dem Bitmap-Pinsel auf dem Renderziel auf, um den Clip auszufüllen.

Die folgende Abbildung zeigt die ursprüngliche Bitmap auf der linken Seite, die bitmapmaske in der Mitte und die Bitmap, die auf die Maske auf der rechten Seite abgeschnitten wird.

![Abbildung einer Goldfisch-Bitmap, einer aus der Bitmap erstellten fischförmigen Maske und der resultierenden fischförmigen Bitmap nach der Maske](images/cliparegion-opacitymask.png)

Der folgende Code zeigt, wie Sie den Bereich mit der in der vorherigen Abbildung gezeigten Maske Ausschneiden. Zuerst werden die ursprüngliche Bitmap und die bitmapmaske geladen. Und erstellt dann einen Bitmap-Pinsel mit der ursprünglichen Bitmap.


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



Anschließend wird [**setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) aufgerufen, um den AntiAlias Modus festzulegen. Ruft [**fillopacitymask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) auf, um eine Bitmap-Maske zum Ausschneiden der ursprünglichen Bitmap zu verwenden.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Weitere Informationen zu Deck Kraft Masken finden Sie unter [Übersicht über die Deckkraft Masken](opacity-masks-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 