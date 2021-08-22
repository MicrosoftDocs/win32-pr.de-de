---
title: Erstellen eines Volltonfarbpinsels
description: Zeigt, wie Sie mit Direct2D einen Volltonfarbpinsel erstellen.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 395652a33f8541a825bab9f2ababcceb4b31d7c8d46458a08148e63c85b2afff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259454"
---
# <a name="how-to-create-a-solid-color-brush"></a>Erstellen eines Volltonfarbpinsels

Verwenden Sie zum Erstellen eines Volltonfarbpinsels die [**ID2DRenderTarget::CreateSolidColorBrush-Methode,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) und geben Sie die Farbe an, mit der Sie zeichnen möchten. Einige der **CreateSolidColorBrush-Überladungen** ermöglichen es Ihnen auch, die Deckkraft des Pinsels anzugeben.

Der folgende Code zeigt, wie Sie einen gelb-grünen Pinsel erstellen, um ein Quadrat zu füllen, und einen soliden schwarzen Pinsel, um den Umriss des Quadrats zu zeichnen. Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Rechtecks, das mit einer vollfarbigen gelb-grünen Farbe gefüllt ist](images/brushes-ovw-solidcolor.png)

1.  [**Deklarieren Sie zwei ID2D1SolidColorBrush-Zeiger:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) einen zum Malen von Schwarz und einen zum Malen gelbgrün.
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  Rufen Sie [**die CreateSolidColorBrush-Methode auf,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) um die Pinsel zu erstellen:
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  Rufen Sie [**die FillRectangle-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) auf, um das Innere des Rechtecks mit dem gelben grünen Pinsel zu zeichnen, und die [**DrawRectangle-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) um den Umriss des Rechtecks mit dem schwarzen Pinsel zu zeichnen:
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 