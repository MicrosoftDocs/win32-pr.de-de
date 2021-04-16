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
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="1912f-103">Zeichnen und Ausfüllen einer einfachen Form</span><span class="sxs-lookup"><span data-stu-id="1912f-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="1912f-104">In diesem Thema wird beschrieben, wie Sie eine einfache Form zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1912f-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="1912f-105">Die [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle stellt Methoden zum Gliedern und Ausfüllen von Ellipsen, Rechtecke und Linien bereit.</span><span class="sxs-lookup"><span data-stu-id="1912f-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="1912f-106">In den folgenden Beispielen wird gezeigt, wie eine Ellipse erstellt und gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1912f-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="1912f-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="1912f-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1912f-108">Zeichnen einer Ellipse mit einem Strich Strich</span><span class="sxs-lookup"><span data-stu-id="1912f-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="1912f-109">Zeichnen einer Ellipse mit einem gestrichelten Strich</span><span class="sxs-lookup"><span data-stu-id="1912f-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="1912f-110">Eine Ellipse zeichnen und ausfüllen</span><span class="sxs-lookup"><span data-stu-id="1912f-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="1912f-111">Zeichnen komplexer Formen</span><span class="sxs-lookup"><span data-stu-id="1912f-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="1912f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1912f-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="1912f-113">Zeichnen einer Ellipse mit einem Strich Strich</span><span class="sxs-lookup"><span data-stu-id="1912f-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="1912f-114">Um die Gliederung einer Ellipse zu zeichnen, definieren Sie einen Pinsel (z. b. ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) oder [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) zum Zeichnen der Kontur und eine [**D2D1- \_ Ellipse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) zum Beschreiben der Position und Dimensionen der Ellipse. übergeben Sie diese Objekte dann an die [**ID2D1RenderTarget::D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1912f-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="1912f-115">Im folgenden Beispiel wird ein schwarzer Pinsel mit voll Tonfarbe erstellt und im m \_ spblackbrush-Klassenmember gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1912f-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="1912f-116">Im nächsten Beispiel wird eine [**D2D1- \_ Ellipse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) definiert und mit dem im vorherigen Beispiel definierten Pinsel verwendet, um die Gliederung einer Ellipse zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1912f-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="1912f-117">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1912f-117">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse mit einem voll Bild Strich](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="1912f-119">Zeichnen einer Ellipse mit einem gestrichelten Strich</span><span class="sxs-lookup"><span data-stu-id="1912f-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="1912f-120">Im vorherigen Beispiel wurde ein einfacher Strich verwendet.</span><span class="sxs-lookup"><span data-stu-id="1912f-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="1912f-121">Sie können das Aussehen eines Strichs auf verschiedene Weise ändern, indem Sie eine [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)erstellen.</span><span class="sxs-lookup"><span data-stu-id="1912f-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="1912f-122">Mit **ID2D1StrokeStyle** können Sie die Form am Anfang und Ende eines Strichs angeben, unabhängig davon, ob er über ein Bindestrich-Muster verfügt usw.</span><span class="sxs-lookup"><span data-stu-id="1912f-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="1912f-123">Im folgenden Beispiel wird ein **ID2D1StrokeStyle** erstellt, in dem ein gestrichelter Strich beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1912f-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="1912f-124">Dieses Beispiel verwendet ein vordefiniertes Bindestrich Muster, D2D1 Dash-Punkt-Punkt- [**\_ \_ \_ \_ \_ Punkt**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)-Punkt, Sie können aber auch eigene Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="1912f-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


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



<span data-ttu-id="1912f-125">Im nächsten Beispiel wird der Strich Stil mit der [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="1912f-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="1912f-126">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1912f-126">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse mit einem gestrichelten Strich](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="1912f-128">Eine Ellipse zeichnen und ausfüllen</span><span class="sxs-lookup"><span data-stu-id="1912f-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="1912f-129">Um das Innere einer Ellipse zu zeichnen, verwenden Sie die [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1912f-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="1912f-130">Im folgenden Beispiel wird die [**DrawEllipse**]/Windows/Desktop/API/d2d1/NF-d2d1-id2d1rendertarget-DrawEllipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))-Methode verwendet, um die Ellipse zu gliedern, und anschließend wird die **FillEllipse** -Methode verwendet, um das Innere zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1912f-130">The following example uses the [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="1912f-131">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1912f-131">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse mit einem gestrichelten Strich und dann mit einer ausgefüllten grauen Farbe](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="1912f-133">Im nächsten Beispiel wird die Ellipse zuerst gefüllt und dann die Gliederung gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1912f-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="1912f-134">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1912f-134">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse, die mit einer ausgefüllten grauen Farbe gefüllt und dann mit einem gestrichelten Strich dargestellt wird](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="1912f-136">Code wurde in diesen Beispielen ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="1912f-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="1912f-137">Zeichnen komplexer Formen</span><span class="sxs-lookup"><span data-stu-id="1912f-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="1912f-138">Um komplexere Formen zu zeichnen, definieren Sie ID2D1Geometry-Objekte und verwenden Sie mit der [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode und der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1912f-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="1912f-139">Weitere Informationen finden Sie in der [Übersicht über Geometrien](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1912f-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1912f-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1912f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1912f-141">Übersicht über Geometrien</span><span class="sxs-lookup"><span data-stu-id="1912f-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="1912f-142">Übersicht über Pinsel</span><span class="sxs-lookup"><span data-stu-id="1912f-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 