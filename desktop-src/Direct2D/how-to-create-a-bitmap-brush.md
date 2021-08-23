---
title: Erstellen eines Bitmappinsels
description: Zeigt, wie ein Bitmappinsel mit Direct2D erstellt wird.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274d359b8ad8298a4e45d01014a6e9b19aa58c4b81725c5d8c41ac931e24eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569295"
---
# <a name="how-to-create-a-bitmap-brush"></a>Erstellen eines Bitmappinsels

Verwenden Sie zum Erstellen eines Bitmappinsels die [**ID2D1RenderTarget::CreateBitmapBrush-Methode,**](id2d1rendertarget-createbitmapbrush.md) und geben Sie die Eigenschaften des Bitmappinsels an. Mit einigen Überladungen können Sie die Pinseleigenschaften angeben. Der folgende Code zeigt, wie ein Bitmappinsel zum Füllen eines Quadrats und ein solider schwarzer Pinsel zum Zeichnen der Kontur des Quadrats erstellt werden. Der Code erzeugt die Ausgabe, die im folgenden Screenshot gezeigt wird.

> [!Note]  
> Ab Windows 8 können Sie die [**CreateBitmapBrush-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) auf der [**ID2D1DeviceContext-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) verwenden, um eine [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) anstelle einer **ID2D1BitmapBrush** zu erstellen. **ID2D1BitmapBrush1** fügt dem Bitmappinsel hochwertige Skalierungsmodi hinzu.

 

![Screenshot eines Quadrats, das mit einer Plantmap gefüllt ist](images/brushes-ovw-bitmap.png)

1.  Deklarieren Sie eine Variable vom Typ [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Laden einer Bitmap aus einer Ressource. Weitere Informationen finden Sie unter [Laden einer Bitmap aus einer Ressource.](how-to-load-a-bitmap-from-a-resource.md)
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  Wählen Sie die Erweiterungsmodi ([**D2D1 \_ EXTEND \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) und den Interpolationsmodus ([**D2D1 \_ BITMAP \_ INTERPOLATION \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) des Bitmappinsels aus, und rufen Sie dann die [**CreateBitmapBrush-Methode**](id2d1rendertarget-createbitmapbrush.md) auf, um einen Pinsel zu erstellen, wie im folgenden Code gezeigt.
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 