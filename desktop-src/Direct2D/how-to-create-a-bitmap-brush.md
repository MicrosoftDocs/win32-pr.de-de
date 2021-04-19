---
title: Erstellen eines Bitmap-Pinsels
description: Zeigt, wie ein Bitmap-Pinsel mit Direct2D erstellt wird.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341951"
---
# <a name="how-to-create-a-bitmap-brush"></a>Erstellen eines Bitmap-Pinsels

Um einen Bitmap-Pinsel zu erstellen, verwenden Sie die [**ID2D1RenderTarget:: kreatebitmapbrush**](id2d1rendertarget-createbitmapbrush.md) -Methode, und geben Sie die Bitmap-Pinsel Eigenschaften an. Mit einigen über Ladungen können Sie die Pinsel Eigenschaften angeben. Der folgende Code zeigt, wie Sie einen Bitmap-Pinsel zum Auffüllen eines Quadrats und einen Pinsel mit einem Pinsel zum Zeichnen der Kontur des Quadrats erstellen. Der Code erzeugt die Ausgabe, die im folgenden Screenshot gezeigt wird.

> [!Note]  
> Ab Windows 8 können Sie [**die Methode "**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) Methode" in der [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Schnittstelle verwenden, um eine [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) anstelle eines **ID2D1BitmapBrush** zu erstellen. **ID2D1BitmapBrush1** fügt dem Bitmap-Pinsel einen hochwertigen Skalierungs Modus hinzu.

 

![Screenshot eines Quadrats, das mit einer Werk Bitmap gefüllt ist](images/brushes-ovw-bitmap.png)

1.  Deklarieren Sie eine Variable vom Typ [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Laden einer Bitmap aus einer Ressource. Weitere Informationen finden Sie unter Vorgehens [Weise beim Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md).
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

    

3.  Wählen Sie den Erweiterungs Modus ([**D2D1 \_ Extended \_ Mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) und den Interpolations Modus ([**D2D1 \_ Bitmap \_ Interpolations \_ Mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) des Bitmap-Pinsels aus, und rufen Sie dann die Methode " [**foratebitmapbrush**](id2d1rendertarget-createbitmapbrush.md) " auf, um einen Pinsel zu erstellen, wie im folgenden Code gezeigt.
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

 

 