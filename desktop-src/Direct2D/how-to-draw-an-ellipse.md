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
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="0aaab-103">Zeichnen und Füllen einer einfachen Form</span><span class="sxs-lookup"><span data-stu-id="0aaab-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="0aaab-104">In diesem Thema wird beschrieben, wie eine einfache Form gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0aaab-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="0aaab-105">Die [**ID2D1RenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) stellt Methoden zum Gliederung und Auffüllen von Ellipsen, Rechtecke und Linien bereit.</span><span class="sxs-lookup"><span data-stu-id="0aaab-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="0aaab-106">Die folgenden Beispiele zeigen, wie eine Ellipse erstellt und gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0aaab-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="0aaab-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="0aaab-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0aaab-108">Zeichnen der Kontur einer Ellipse mit einem Vollstrich</span><span class="sxs-lookup"><span data-stu-id="0aaab-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="0aaab-109">Zeichnen einer Ellipse mit einem gestrichelten Strich</span><span class="sxs-lookup"><span data-stu-id="0aaab-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="0aaab-110">Zeichnen und Füllen einer Ellipse</span><span class="sxs-lookup"><span data-stu-id="0aaab-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="0aaab-111">Zeichnen komplexerer Formen</span><span class="sxs-lookup"><span data-stu-id="0aaab-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="0aaab-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0aaab-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="0aaab-113">Zeichnen der Kontur einer Ellipse mit einem Vollstrich</span><span class="sxs-lookup"><span data-stu-id="0aaab-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="0aaab-114">Um die Kontur einer Ellipse zu zeichnen, definieren Sie einen Pinsel (z. B. eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) oder [**ID2D1LinearGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)zum Zeichnen der Gliederung und eine [**D2D1-ELLIPSE \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) zum Beschreiben der Position und Dimensionen der Ellipse und übergeben diese Objekte dann an die [**ID2D1RenderTarget::D rawEllipse-Methode.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="0aaab-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="0aaab-115">Im folgenden Beispiel wird ein schwarzer Volltonfarbpinsel erstellt und im \_ m spBlackBrush-Klassenmember gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0aaab-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="0aaab-116">Im nächsten Beispiel wird eine [**D2D1-ELLIPSE \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) definiert und mit dem im vorherigen Beispiel definierten Pinsel verwendet, um die Kontur einer Ellipse zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0aaab-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="0aaab-117">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="0aaab-117">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse mit einem Vollstrich](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="0aaab-119">Zeichnen einer Ellipse mit einem gestrichelten Strich</span><span class="sxs-lookup"><span data-stu-id="0aaab-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="0aaab-120">Im vorherigen Beispiel wurde ein einfacher Strich verwendet.</span><span class="sxs-lookup"><span data-stu-id="0aaab-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="0aaab-121">Sie können das Aussehen eines Strichs auf verschiedene Weise ändern, indem Sie eine [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)erstellen.</span><span class="sxs-lookup"><span data-stu-id="0aaab-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="0aaab-122">Mit **ID2D1StrokeStyle** können Sie die Form am Anfang und Ende eines Strichs angeben, ob sie über ein Bindestrichmuster verfügt usw.</span><span class="sxs-lookup"><span data-stu-id="0aaab-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="0aaab-123">Im folgenden Beispiel wird ein **ID2D1StrokeStyle-Objekt** erstellt, das einen gestrichelten Strich beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0aaab-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="0aaab-124">In diesem Beispiel wird ein vordefiniertes Bindestrichmuster verwendet, [**D2D1 \_ DASH \_ STYLE \_ DASH \_ DOT DOT \_ .**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)Sie können aber auch ein eigenes angeben.</span><span class="sxs-lookup"><span data-stu-id="0aaab-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


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



<span data-ttu-id="0aaab-125">Im nächsten Beispiel wird der Strichstil mit der [**DrawEllipse-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0aaab-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="0aaab-126">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="0aaab-126">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse mit einem gestrichelten Strich](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="0aaab-128">Zeichnen und Füllen einer Ellipse</span><span class="sxs-lookup"><span data-stu-id="0aaab-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="0aaab-129">Um das Innere einer Ellipse zu zeichnen, verwenden Sie die [**FillEllipse-Methode.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="0aaab-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="0aaab-130">Im folgenden Beispiel wird die [**DrawEllipse-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) verwendet, um die Ellipse zu umranden, und anschließend wird die **FillEllipse-Methode** verwendet, um ihr Innere zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0aaab-130">The following example uses the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="0aaab-131">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="0aaab-131">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse mit einem gestrichelten Strich und anschließendem Auffüllen mit einer vollgrauen Farbe](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="0aaab-133">Im nächsten Beispiel wird zuerst die Ellipse ausgefüllt und dann die Kontur zeichnet.</span><span class="sxs-lookup"><span data-stu-id="0aaab-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="0aaab-134">In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="0aaab-134">This example produces the output shown in the following illustration.</span></span>

![Abbildung einer Ellipse, die mit einer vollgrauen Farbe gefüllt und dann mit einem gestrichelten Strich umrandet ist](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="0aaab-136">Code wurde in diesen Beispielen ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="0aaab-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="0aaab-137">Zeichnen komplexerer Formen</span><span class="sxs-lookup"><span data-stu-id="0aaab-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="0aaab-138">Um komplexere Formen zu zeichnen, definieren Sie ID2D1Geometry-Objekte und verwenden sie mit den [**DrawGeometry-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) und [**FillGeometry-Methoden.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)</span><span class="sxs-lookup"><span data-stu-id="0aaab-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="0aaab-139">Weitere Informationen finden Sie in der [Übersicht über Geometrien.](direct2d-geometries-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0aaab-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aaab-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0aaab-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aaab-141">Übersicht über Geometrien</span><span class="sxs-lookup"><span data-stu-id="0aaab-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="0aaab-142">Übersicht über Pinsel</span><span class="sxs-lookup"><span data-stu-id="0aaab-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 
