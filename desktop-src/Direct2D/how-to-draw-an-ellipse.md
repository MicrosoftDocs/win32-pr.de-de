---
title: Zeichnen und Ausfüllen einer einfachen Form
description: In diesem Thema wird beschrieben, wie Sie eine einfache Form zeichnen.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6b6b5a6fb08ac962475c2f0aa2812b4c3ae5da03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104559241"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Zeichnen und Ausfüllen einer einfachen Form

In diesem Thema wird beschrieben, wie Sie eine einfache Form zeichnen. Die [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle stellt Methoden zum Gliedern und Ausfüllen von Ellipsen, Rechtecke und Linien bereit. In den folgenden Beispielen wird gezeigt, wie eine Ellipse erstellt und gezeichnet wird.

Dieses Thema enthält folgende Abschnitte:

-   [Zeichnen einer Ellipse mit einem Strich Strich](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Zeichnen einer Ellipse mit einem gestrichelten Strich](#draw-an-ellipse-with-a-dashed-stroke)
-   [Eine Ellipse zeichnen und ausfüllen](#draw-and-fill-an-ellipse)
-   [Zeichnen komplexer Formen](#drawing-more-complex-shapes)
-   [Zugehörige Themen](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Zeichnen einer Ellipse mit einem Strich Strich

Um die Gliederung einer Ellipse zu zeichnen, definieren Sie einen Pinsel (z. b. ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) oder [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) zum Zeichnen der Kontur und eine [**D2D1- \_ Ellipse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) zum Beschreiben der Position und Dimensionen der Ellipse. übergeben Sie diese Objekte dann an die [**ID2D1RenderTarget::D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) -Methode. Im folgenden Beispiel wird ein schwarzer Pinsel mit voll Tonfarbe erstellt und im m \_ spblackbrush-Klassenmember gespeichert.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



Im nächsten Beispiel wird eine [**D2D1- \_ Ellipse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) definiert und mit dem im vorherigen Beispiel definierten Pinsel verwendet, um die Gliederung einer Ellipse zu zeichnen. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse mit einem voll Bild Strich](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Zeichnen einer Ellipse mit einem gestrichelten Strich

Im vorherigen Beispiel wurde ein einfacher Strich verwendet. Sie können das Aussehen eines Strichs auf verschiedene Weise ändern, indem Sie eine [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)erstellen. Mit **ID2D1StrokeStyle** können Sie die Form am Anfang und Ende eines Strichs angeben, unabhängig davon, ob er über ein Bindestrich-Muster verfügt usw. Im folgenden Beispiel wird ein **ID2D1StrokeStyle** erstellt, in dem ein gestrichelter Strich beschrieben wird. Dieses Beispiel verwendet ein vordefiniertes Bindestrich Muster, D2D1 Dash-Punkt-Punkt- [**\_ \_ \_ \_ \_ Punkt**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)-Punkt, Sie können aber auch eigene Werte angeben.


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



Im nächsten Beispiel wird der Strich Stil mit der [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) -Methode verwendet. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse mit einem gestrichelten Strich](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Eine Ellipse zeichnen und ausfüllen

Um das Innere einer Ellipse zu zeichnen, verwenden Sie die [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methode. Im folgenden Beispiel wird die [**DrawEllipse**]/Windows/Desktop/API/d2d1/NF-d2d1-id2d1rendertarget-DrawEllipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))-Methode verwendet, um die Ellipse zu gliedern, und anschließend wird die **FillEllipse** -Methode verwendet, um das Innere zu zeichnen. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse mit einem gestrichelten Strich und dann mit einer ausgefüllten grauen Farbe](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



Im nächsten Beispiel wird die Ellipse zuerst gefüllt und dann die Gliederung gezeichnet. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse, die mit einer ausgefüllten grauen Farbe gefüllt und dann mit einem gestrichelten Strich dargestellt wird](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



Code wurde in diesen Beispielen ausgelassen.

## <a name="drawing-more-complex-shapes"></a>Zeichnen komplexer Formen

Um komplexere Formen zu zeichnen, definieren Sie ID2D1Geometry-Objekte und verwenden Sie mit der [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode und der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode. Weitere Informationen finden Sie in der [Übersicht über Geometrien](direct2d-geometries-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Geometrien](direct2d-geometries-overview.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>

 

 