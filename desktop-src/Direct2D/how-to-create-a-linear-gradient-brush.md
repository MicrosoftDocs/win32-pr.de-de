---
title: Erstellen eines linearen Farbverlaufs Pinsels
description: Zeigt, wie ein linearer Farbverlaufs Pinsel mit Direct2D erstellt wird.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 3a50a6e3ab421e2275644051ed647d5c4501f8e0
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858620"
---
# <a name="how-to-create-a-linear-gradient-brush"></a>Erstellen eines linearen Farbverlaufs Pinsels

Verwenden Sie zum Erstellen eines linearen Farbverlaufs Pinsels die Methode " [**kreatelineargradientbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) ", und geben Sie die Eigenschaften für den linearen Farbverlaufs Pinsel und die Auflistung für den Mit einigen über Ladungen können Sie die Pinsel Eigenschaften angeben. Der folgende Code zeigt, wie ein linearer Farbverlaufs Pinsel zum Auffüllen eines Quadrats erstellt wird, und ein solider schwarzer Pinsel zum Zeichnen der Kontur des Quadrats.

Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Quadrats mit einem linearen Farbverlaufs Pinsel](images/brushes-ovw-lineargradient.png)

1.  Deklarieren Sie eine Variable vom Typ [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  Verwenden Sie die [**ID2D1RenderTarget:: kreategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) -Methode, um die [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) -Auflistung mit einem deklarierten Array von [**D2D1 Gradient- \_ \_ Stopp**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) Strukturen zu erstellen, wie im folgenden Code dargestellt.
    > [!Note]  
    > Ab Windows 8 können Sie stattdessen die [**ID2D1DeviceContext::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) up-Auflistungs Methode verwenden, um eine [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) -Sammlung zu erstellen. Diese Schnittstelle fügt Farbverläufe mit hoher Farbe und die interpolung von Farbverläufen entweder in geraden oder in den Sonderfarben hinzu. Weitere Informationen finden Sie auf der Seite " **ID2DDeviceContext:: kreategradientstopcollection** ".

     

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  Verwenden Sie [**ID2D1RenderTarget:: kreatelineargradientbrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) zum Erstellen eines linearen Farbverlaufs Pinsels, füllen Sie das Quadrat mit dem Pinsel aus, und zeichnen Sie das Quadrat mit dem schwarzen Farbpinsel.
    ```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 
