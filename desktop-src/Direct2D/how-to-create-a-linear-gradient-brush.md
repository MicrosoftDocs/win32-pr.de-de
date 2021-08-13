---
title: Erstellen eines Pinsels mit linearem Farbverlauf
description: Zeigt, wie sie mit Direct2D einen Pinsel mit linearem Farbverlauf erstellen.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c9223eb561ecc391014bc4a89c86a634181bec6d1e3917866aeef2723f1510a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259534"
---
# <a name="how-to-create-a-linear-gradient-brush"></a>Erstellen eines Pinsels mit linearem Farbverlauf

Um einen linearen Farbverlaufspinsel zu erstellen, verwenden Sie die [**CreateLinearGradientBrush-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) und geben Sie die Eigenschaften des linearen Farbverlaufpinsels und die Gradientenstoppsammlung an. Mit einigen Überladungen können Sie die Pinseleigenschaften angeben. Der folgende Code zeigt, wie Ein linearer Farbverlaufspinsel zum Füllen eines Quadrats und ein solider schwarzer Pinsel zum Zeichnen der Kontur des Quadrats erstellt wird.

Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines quadratischen, mit einem linearen Farbverlaufspinsel gefüllten Quadrats](images/brushes-ovw-lineargradient.png)

1.  Deklarieren Sie eine Variable vom Typ [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  Verwenden Sie die [**ID2D1RenderTarget::CreateGradientStopCollection-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) um die [**ID2D1GradientStopCollection-Auflistung**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) mit einem deklarierten Array von [**D2D1 \_ GRADIENT \_ STOP-Strukturen**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) zu erstellen, wie im folgenden Code gezeigt.
    > [!Note]  
    > Ab Windows 8 können Sie stattdessen die [**ID2D1DeviceContext::CreateGradientStopCollection-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) verwenden, um eine [**ID2D1GradientStopCollection1-Sammlung**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) zu erstellen. Diese Schnittstelle fügt farblich hochwertige Farbverläufe und die Interpolation von Farbverläufen in geraden oder prmultipliierten Farben hinzu. Weitere Informationen finden Sie auf der Seite **ID2DDeviceContext::CreateGradientStopCollection.**

     

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

    

3.  Verwenden Sie [**id2D1RenderTarget::CreateLinearGradientBrush,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) um einen Pinsel für linearen Farbverlauf zu erstellen, das Quadrat mit dem Pinsel zu füllen und das Quadrat mit dem schwarzen Farbpinsel zu zeichnen.
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

 

 
