---
title: Zeichnen und Füllen einer einfachen Form
description: In diesem Thema wird beschrieben, wie eine einfache Form gezeichnet wird.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 93d8f3a3ddeb06c9168971789dff3ac8c9222d22
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826999"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Zeichnen und Füllen einer einfachen Form

In diesem Thema wird beschrieben, wie eine einfache Form gezeichnet wird. Die [**ID2D1RenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) stellt Methoden zum Gliederung und Auffüllen von Ellipsen, Rechtecke und Linien bereit. Die folgenden Beispiele zeigen, wie eine Ellipse erstellt und gezeichnet wird.

Dieses Thema enthält folgende Abschnitte:

-   [Zeichnen der Kontur einer Ellipse mit einem Vollstrich](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Zeichnen einer Ellipse mit einem gestrichelten Strich](#draw-an-ellipse-with-a-dashed-stroke)
-   [Zeichnen und Füllen einer Ellipse](#draw-and-fill-an-ellipse)
-   [Zeichnen komplexerer Formen](#drawing-more-complex-shapes)
-   [Verwandte Themen](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Zeichnen der Kontur einer Ellipse mit einem Vollstrich

Um die Kontur einer Ellipse zu zeichnen, definieren Sie einen Pinsel (z. B. eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) oder [**ID2D1LinearGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)zum Zeichnen der Gliederung und eine [**D2D1-ELLIPSE \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) zum Beschreiben der Position und Dimensionen der Ellipse und übergeben diese Objekte dann an die [**ID2D1RenderTarget::D rawEllipse-Methode.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) Im folgenden Beispiel wird ein schwarzer Volltonfarbpinsel erstellt und im \_ m spBlackBrush-Klassenmember gespeichert.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



Im nächsten Beispiel wird eine [**D2D1-ELLIPSE \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) definiert und mit dem im vorherigen Beispiel definierten Pinsel verwendet, um die Kontur einer Ellipse zu zeichnen. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse mit einem Vollstrich](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Zeichnen einer Ellipse mit einem gestrichelten Strich

Im vorherigen Beispiel wurde ein einfacher Strich verwendet. Sie können das Aussehen eines Strichs auf verschiedene Weise ändern, indem Sie eine [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)erstellen. Mit **ID2D1StrokeStyle** können Sie die Form am Anfang und Ende eines Strichs angeben, ob sie über ein Bindestrichmuster verfügt usw. Im folgenden Beispiel wird ein **ID2D1StrokeStyle-Objekt** erstellt, das einen gestrichelten Strich beschreibt. In diesem Beispiel wird ein vordefiniertes Bindestrichmuster verwendet, [**D2D1 \_ DASH \_ STYLE \_ DASH \_ DOT DOT \_ .**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)Sie können aber auch ein eigenes angeben.


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



Im nächsten Beispiel wird der Strichstil mit der [**DrawEllipse-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) verwendet. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse mit einem gestrichelten Strich](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Zeichnen und Füllen einer Ellipse

Um das Innere einer Ellipse zu zeichnen, verwenden Sie die [**FillEllipse-Methode.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) Im folgenden Beispiel wird die [**DrawEllipse-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) verwendet, um die Ellipse zu umranden, und anschließend wird die **FillEllipse-Methode** verwendet, um ihr Innere zu zeichnen. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse mit einem gestrichelten Strich und anschließendem Auffüllen mit einer vollgrauen Farbe](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



Im nächsten Beispiel wird zuerst die Ellipse ausgefüllt und dann die Kontur zeichnet. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Ellipse, die mit einer vollgrauen Farbe gefüllt und dann mit einem gestrichelten Strich umrandet ist](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



Code wurde in diesen Beispielen ausgelassen.

## <a name="drawing-more-complex-shapes"></a>Zeichnen komplexerer Formen

Um komplexere Formen zu zeichnen, definieren Sie ID2D1Geometry-Objekte und verwenden sie mit den [**DrawGeometry-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) und [**FillGeometry-Methoden.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) Weitere Informationen finden Sie in der [Übersicht über Geometrien.](direct2d-geometries-overview.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Geometrien](direct2d-geometries-overview.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>

 

 
