---
title: Verwenden einer Bitmap als Deckkraftmaske
description: Zeigt, wie ein Bereich mit Bitmapmasken abgeschnitten wird.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42829ab9a873be9adbeca7795dd87aed62a258ce5737db6e3f86612b4ffef43c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259615"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Verwenden einer Bitmap als Deckkraftmaske

In diesem Thema wird beschrieben, wie Sie eine Bitmap als Opactymaske verwenden, indem Sie die [**ID2D1Factory::FillOpacityMask-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) aufrufen. Die Deckkraftmaske ist eine Bitmap, die die Abdeckungsinformationen liefert, die durch den Alphakanal dargestellt werden, der die Transparenz des gerenderten Inhalts steuert. Dieser Ansatz ist effizienter als die Verwendung von Ebenen mit einer Deckkraftmaske. Weitere Informationen finden Sie unter [Übersicht über Ebenen.](direct2d-layers-overview.md)

**So beschneiden Sie einen Bereich**

1.  Laden Sie die ursprüngliche Bitmap aus einer Ressource. Informationen zum Laden einer Bitmap finden Sie unter Laden einer [Bitmap aus einer Ressource.](how-to-load-a-bitmap-from-a-resource.md)
2.  Laden Sie die Bitmapmaske aus einer Ressource.
3.  Erstellen Sie einen Bitmappinsel mit der ursprünglichen Bitmap. Informationen zum Erstellen eines Bitmappinsels finden Sie unter [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).
4.  Rufen Sie [**ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) auf, um den Antialiasmodus auf dem Renderziel auf D2D1 \_ ANTIALIAS MODE ALIASED für \_ \_ [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) zu setzen.
5.  Rufen [**Sie FillOpacityMask mit**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) der Bitmapmaske und dem Bitmappinsel auf dem Renderziel auf, um den Clip zu füllen.

Die folgende Abbildung zeigt die ursprüngliche Bitmap auf der linken Seite, die Bitmapmaske in der Mitte und die Bitmap, die an die Maske auf der rechten Seite abgeschnitten ist.

![Abbildung einer Goldfish-Bitmap, einer aus der Bitmap erstellten Maske und der resultierenden fishförmigen Bitmap nach der Maske](images/cliparegion-opacitymask.png)

Der folgende Code zeigt, wie sie den Bereich mit der in der vorherigen Abbildung gezeigten Maske beschneiden. Zuerst werden die ursprüngliche Bitmap und die Bitmapmaske geladen. Anschließend wird ein Bitmappinsel mit der ursprünglichen Bitmap erstellt.


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



Anschließend wird [**SetAntialiasMode zum**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) Festlegen des Antialias-Modus verwendet. Rufen [**Sie FillOpacityMask auf,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) um die ursprüngliche Bitmap mithilfe einer Bitmapmaske zu beschneiden.


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



Weitere Informationen zu Deckkraftmasken finden Sie unter Übersicht über [Deckkraftmasken.](opacity-masks-overview.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 