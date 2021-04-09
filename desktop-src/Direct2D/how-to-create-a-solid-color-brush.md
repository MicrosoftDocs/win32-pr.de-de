---
title: Erstellen eines Pinsel mit voll Tonfarbe
description: Zeigt, wie ein vollfarbiger Farbpinsel mit Direct2D erstellt wird.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948823"
---
# <a name="how-to-create-a-solid-color-brush"></a>Erstellen eines Pinsel mit voll Tonfarbe

Um einen Pinsel mit voll Tonfarbe zu erstellen, verwenden Sie die [**ID2DRenderTarget:: froatesolidcolorbrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Methode, und geben Sie die Farbe an, mit der Sie zeichnen möchten. Einige der " **kreatesolidcolorbrush** "-über Ladungen ermöglichen auch die Angabe der Deckkraft des Pinsels.

Der folgende Code zeigt, wie Sie einen soliden gelben grünen Pinsel zum Auffüllen eines Quadrats erstellen, und einen Pinsel mit einem Pinsel, um die Kontur des Quadrats zu zeichnen. Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Rechtecks, das mit einer grünen gelb grünen Farbe gefüllt ist](images/brushes-ovw-solidcolor.png)

1.  Deklarieren Sie zwei [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Zeiger: einen zum Zeichnen von schwarz und einen für das gelbe grün.
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  Rufen Sie die Methode " [**kreatesolidcolorbrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) " auf, um die Pinsel zu erstellen:
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

    

3.  Wenn Sie die [**fillrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) -Methode aufzeichnen, zeichnen Sie das Innere des Rechtecks mit dem gelben grünen Pinsel und der [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode, um die Kontur des Rechtecks mit dem schwarzen Pinsel zu zeichnen:
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 