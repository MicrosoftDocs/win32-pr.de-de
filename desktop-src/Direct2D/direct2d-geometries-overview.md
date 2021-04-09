---
title: Übersicht über Geometrien
description: Beschreibt die Grundlagen von Direct2D Geometries,-Objekten, die Sie zum darstellen, bearbeiten und Analysieren von Formen verwenden können.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D, Übersicht über Geometrien
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734569"
---
# <a name="geometries-overview"></a><span data-ttu-id="7265f-104">Übersicht über Geometrien</span><span class="sxs-lookup"><span data-stu-id="7265f-104">Geometries overview</span></span>

<span data-ttu-id="7265f-105">In dieser Übersicht wird beschrieben, wie [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekte zum Definieren und Bearbeiten von 2D-Abbildungen erstellt und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7265f-105">This overview describes how to create and use [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) objects to define and manipulate 2D figures.</span></span> <span data-ttu-id="7265f-106">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="7265f-106">It contains the following sections.</span></span>

## <a name="what-is-a-direct2d-geometry"></a><span data-ttu-id="7265f-107">Was ist eine Direct2D-Geometrie?</span><span class="sxs-lookup"><span data-stu-id="7265f-107">What is a Direct2D geometry?</span></span>

<span data-ttu-id="7265f-108">Eine Direct2D-Geometrie ist ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7265f-108">A Direct2D geometry is an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object.</span></span> <span data-ttu-id="7265f-109">Bei diesem Objekt kann es sich um eine einfache Geometrie ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)oder [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), eine Pfad Geometrie ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) oder eine zusammengesetzte Geometrie ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) und [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)) handeln.</span><span class="sxs-lookup"><span data-stu-id="7265f-109">This object can be a simple geometry ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), or [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), a path geometry ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)), or a composite geometry ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) and [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span></span>

<span data-ttu-id="7265f-110">Mit Direct2D Geometrien können Sie zweidimensionale Abbildungen beschreiben und viele Verwendungsmöglichkeiten anbieten, wie z. b. das Definieren von Treffer-/Testbereichen, Clip Bereichen und sogar Animations Pfaden.</span><span class="sxs-lookup"><span data-stu-id="7265f-110">Direct2D geometries enable you to describe two-dimensional figures and offer many uses, such as defining hit-test regions, clip regions, and even animation paths.</span></span>

<span data-ttu-id="7265f-111">Direct2D-Geometrien sind unveränderliche und geräteunabhängige Ressourcen, die von [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7265f-111">Direct2D geometries are immutable and device-independent resources created by [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span> <span data-ttu-id="7265f-112">Im Allgemeinen sollten Sie Geometrien einmal erstellen und Sie für die Lebensdauer der Anwendung aufbewahren, oder bis Sie geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7265f-112">Generally, you should create geometries one time and keep them for the life of the application, or until they have to be changed.</span></span> <span data-ttu-id="7265f-113">Weitere Informationen zu geräteunabhängigen und geräteabhängigen Ressourcen finden Sie in der Übersicht über [Ressourcen](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="7265f-113">For more information about device-independent and device-dependent resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="7265f-114">In den folgenden Abschnitten werden die verschiedenen Arten von Geometrien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7265f-114">The following sections describe the different kinds of geometries.</span></span>

## <a name="simple-geometries"></a><span data-ttu-id="7265f-115">Einfache Geometrien</span><span class="sxs-lookup"><span data-stu-id="7265f-115">Simple geometries</span></span>

<span data-ttu-id="7265f-116">Einfache Geometrien schließen [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)-, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)-und [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) -Objekte ein und können verwendet werden, um grundlegende geometrische Abbildungen, wie Rechtecke, abgerundete Rechtecke, Kreise und Ellipsen, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7265f-116">Simple geometries include [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), and [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects, and can be used to create basic geometric figures, such as rectangles, rounded rectangles, circles, and ellipses.</span></span>

<span data-ttu-id="7265f-117">Verwenden Sie zum Erstellen einer einfachen Geometrie eine der [**ID2D1Factory:: Create<*geometrytype\* ->Geometry*\*](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="7265f-117">To create a simple geometry, use one of the [**ID2D1Factory::Create<*geometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) methods.</span></span> <span data-ttu-id="7265f-118">Diese Methoden erstellen ein Objekt vom angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="7265f-118">These methods create an object of the specified type.</span></span> <span data-ttu-id="7265f-119">Um z. b. ein Rechteck zu erstellen, rufen Sie [**ID2D1Factory:: froaterectanglegeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))auf, das ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) -Objekt zurückgibt. um ein abgerundetes Rechteck zu erstellen, rufen Sie [**ID2D1Factory:: froateroundrechglegeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry))auf, das ein [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) -Objekt zurückgibt, usw.</span><span class="sxs-lookup"><span data-stu-id="7265f-119">For example, to create a rectangle, call [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), which returns an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object; to create a rounded rectangle, call [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), which returns an [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) object, and so on.</span></span>

<span data-ttu-id="7265f-120">Im folgenden Codebeispiel wird die [**Methode "**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) -Methode" (Methode) aufgerufen, wobei eine Ellipse-Struktur mit dem *Mittelpunkt* (100, 100), *x-Radius* und 100 und *y-Radius* an 50 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7265f-120">The following code example calls the [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) method, passing in an ellipse structure with the *center* set to (100, 100), *x-radius* to 100, and *y-radius* to 50.</span></span> <span data-ttu-id="7265f-121">Anschließend ruft Sie [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)auf und übergibt die zurückgegebene Ellipse-Geometrie, einen Zeiger auf ein schwarzes [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)und eine Strichbreite von 5.</span><span class="sxs-lookup"><span data-stu-id="7265f-121">Then, it calls [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passing in the returned ellipse geometry, a pointer to a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), and a stroke width of 5.</span></span> <span data-ttu-id="7265f-122">Die folgende Abbildung zeigt die Ausgabe des Code Beispiels.</span><span class="sxs-lookup"><span data-stu-id="7265f-122">The following illustration shows the output from the code example.</span></span>

![Abbildung einer Ellipse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



<span data-ttu-id="7265f-124">Verwenden Sie die [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode, um die Kontur der Geometrie zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7265f-124">To draw the outline of any geometry, use the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method.</span></span> <span data-ttu-id="7265f-125">Um das Innere zu zeichnen, verwenden Sie die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7265f-125">To paint its interior, use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

## <a name="path-geometries"></a><span data-ttu-id="7265f-126">Pfadgeometrien</span><span class="sxs-lookup"><span data-stu-id="7265f-126">Path geometries</span></span>

<span data-ttu-id="7265f-127">Pfadgeometrien werden durch die [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7265f-127">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="7265f-128">Diese Objekte können verwendet werden, um komplexe geometrische Abbildungen zu beschreiben, die aus Segmenten wie Arcs, Kurven und Linien bestehen.</span><span class="sxs-lookup"><span data-stu-id="7265f-128">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="7265f-129">In der folgenden Abbildung wird eine Zeichnung gezeigt, die mit der Pfad Geometrie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7265f-129">The following illustration shows a drawing created by using path geometry.</span></span>

![Darstellung eines Flusses, eines Gebirges und der Sonne](images/path-geo-mnts.png)

<span data-ttu-id="7265f-131">Weitere Informationen und Beispiele finden Sie in der [Übersicht über Pfadgeometrien](path-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7265f-131">For more information and examples, see the [Path Geometries Overview](path-geometries-overview.md).</span></span>

## <a name="composite-geometries"></a><span data-ttu-id="7265f-132">Zusammengesetzte Geometrien</span><span class="sxs-lookup"><span data-stu-id="7265f-132">Composite geometries</span></span>

<span data-ttu-id="7265f-133">Eine zusammengesetzte Geometrie ist eine mit einem anderen Geometry-Objekt oder mit einer Transformation gruppierte Geometrie.</span><span class="sxs-lookup"><span data-stu-id="7265f-133">A composite geometry is a geometry grouped or combined with another geometry object, or with a transform.</span></span> <span data-ttu-id="7265f-134">Zusammengesetzte Geometrien schließen [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) -und [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) -Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="7265f-134">Composite geometries include [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) and [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) objects.</span></span>

### <a name="geometry-groups"></a><span data-ttu-id="7265f-135">Geometrie Gruppen</span><span class="sxs-lookup"><span data-stu-id="7265f-135">Geometry groups</span></span>

<span data-ttu-id="7265f-136">Geometry-Gruppen stellen eine bequeme Möglichkeit dar, mehrere Geometrien gleichzeitig zu gruppieren, sodass alle Abbildungen verschiedener geometrischer Geometrien in eins verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="7265f-136">Geometry groups are a convenient way to group several geometries at the same time so all figures of several distinct geometries are concatenated into one.</span></span> <span data-ttu-id="7265f-137">Um ein [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) -Objekt zu erstellen, rufen Sie [**die Methode "**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) -Methode" für das [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt auf, und übergeben Sie den *FillMode* -Wert mit möglichen Werten der alternativen (Alternativen) [**D2D1 \_ Fill \_ Mode \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) -Methode (Alternative) und **D2D1 Fill- \_ \_ Modus \_**, einem Array von Geometrie Objekten, das der Geometrie Gruppe hinzugefügt werden soll, und der Anzahl der Elemente in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="7265f-137">To create a [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) object, call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in the *fillMode* with possible values of [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) and **D2D1\_FILL\_MODE\_WINDING**, an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>

<span data-ttu-id="7265f-138">Im folgenden Codebeispiel wird zunächst ein Array von Geometry-Objekten deklariert.</span><span class="sxs-lookup"><span data-stu-id="7265f-138">The following code example first declares an array of geometry objects.</span></span> <span data-ttu-id="7265f-139">Bei diesen Objekten handelt es sich um vier konzentrische Kreise mit den folgenden Radii-Objekten: 25, 50, 75 und 100.</span><span class="sxs-lookup"><span data-stu-id="7265f-139">These objects are four concentric circles that have the following radii: 25, 50, 75, and 100.</span></span> <span data-ttu-id="7265f-140">Aufrufen Sie anschließend [**die Datei**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) "" für das Objekt " [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ", und übergeben Sie den [**D2D1 Fill- \_ \_ Modus \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), ein Array von Geometry-Objekten, die der Geometrie Gruppe hinzugefügt werden sollen, und die Anzahl der Elemente in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="7265f-140">Then call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

<span data-ttu-id="7265f-141">In der folgenden Abbildung werden die Ergebnisse des Renderings der beiden Gruppen Geometrien aus dem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7265f-141">The following illustration shows the results of rendering the two group geometries from the example.</span></span>

![Abbildung von zwei Sätzen von vier konzentrischen Kreisen, eine mit abwechselnden Ringen und eine mit allen Ringen gefüllt](images/create-geometry-group.png)

### <a name="transformed-geometries"></a><span data-ttu-id="7265f-143">Transformierte Geometrien</span><span class="sxs-lookup"><span data-stu-id="7265f-143">Transformed geometries</span></span>

<span data-ttu-id="7265f-144">Es gibt mehrere Möglichkeiten, eine Geometrie zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="7265f-144">There are multiple ways to transform a geometry.</span></span> <span data-ttu-id="7265f-145">Mit der [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) -Methode eines Renderziels können Sie alle Elemente transformieren, die das Renderziel zeichnet, oder Sie können eine Transformation direkt einer Geometrie zuordnen, indem Sie mithilfe der Methode "| [**atetransformedgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) " eine [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))erstellen.</span><span class="sxs-lookup"><span data-stu-id="7265f-145">You can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of a render target to transform everything that the render target draws, or you can associate a transform directly with a geometry by using the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) method to create an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span></span>

<span data-ttu-id="7265f-146">Die Methode, die Sie verwenden sollten, hängt von den gewünschten Auswirkungen ab.</span><span class="sxs-lookup"><span data-stu-id="7265f-146">The method that you should use depends on the effect that you want.</span></span> <span data-ttu-id="7265f-147">Wenn Sie das Renderziel zum Transformieren und anschließenden Rendern einer Geometrie verwenden, wirkt sich die Transformation auf alles über die Geometrie aus, einschließlich der Breite eines beliebigen Strichs, den Sie angewendet haben.</span><span class="sxs-lookup"><span data-stu-id="7265f-147">When you use the render target to transform and then render a geometry, the transform affects everything about the geometry, including the width of any stroke that you have applied.</span></span> <span data-ttu-id="7265f-148">Wenn Sie hingegen ein [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)verwenden, wirkt sich die Transformation nur auf die Koordinaten aus, die die Form beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7265f-148">On the other hand, when you use an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), the transform affects only the coordinates that describe the shape.</span></span> <span data-ttu-id="7265f-149">Die Transformation wirkt sich nicht auf die Strichstärke aus, wenn die Geometrie gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7265f-149">The transformation will not affect the stroke thickness when the geometry is drawn.</span></span>

> [!Note]  
> <span data-ttu-id="7265f-150">Ab Windows 8 wirkt sich die Welt Transformation nicht auf die Strichstärke von Strichen mit dem Typ [**\_ \_ \_ \_ Fixed**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)oder [**D2D1 \_ Stroke \_ Transform \_ Type \_ Hairline**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)aus.</span><span class="sxs-lookup"><span data-stu-id="7265f-150">Starting with Windows 8 the world transform will not affect the stroke thickness of strokes with [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span> <span data-ttu-id="7265f-151">Sie sollten diese Transformations Typen verwenden, um transformier unabhängige Striche zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="7265f-151">You should use these transform types to achieve transform independent strokes</span></span>

 

<span data-ttu-id="7265f-152">Im folgenden Beispiel wird ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)erstellt und dann gezeichnet, ohne es zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="7265f-152">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), then draws it without transforming it.</span></span> <span data-ttu-id="7265f-153">Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7265f-153">It produces the output shown in the following illustration.</span></span>

![Abbildung eines Rechtecks](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="7265f-155">Im nächsten Beispiel wird das Renderziel verwendet, um die Geometrie um den Faktor 3 zu skalieren, und dann gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7265f-155">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="7265f-156">Die folgende Abbildung zeigt das Ergebnis des Zeichnens des Rechtecks ohne die Transformation und mit der Transformation.</span><span class="sxs-lookup"><span data-stu-id="7265f-156">The following illustration shows the result of drawing the rectangle without the transform and with the transform.</span></span> <span data-ttu-id="7265f-157">Beachten Sie, dass der Strich nach der Transformation dicker ist, auch wenn die Strichstärke 1 ist.</span><span class="sxs-lookup"><span data-stu-id="7265f-157">Notice that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![Darstellung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit einem dickeren Strich](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="7265f-159">Im nächsten Beispiel wird die Methode " [**kreatetransformedgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) " verwendet, um die Geometrie mit dem Faktor 3 zu skalieren, und dann gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7265f-159">The next example uses the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="7265f-160">Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7265f-160">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="7265f-161">Beachten Sie, dass, obwohl das Rechteck größer ist, der Strich nicht vergrößert wurde.</span><span class="sxs-lookup"><span data-stu-id="7265f-161">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![Abbildung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit derselben Strichstärke](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a><span data-ttu-id="7265f-163">Geometrien als Masken</span><span class="sxs-lookup"><span data-stu-id="7265f-163">Geometries as masks</span></span>

<span data-ttu-id="7265f-164">Sie können ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt als geometrische Maske verwenden, wenn Sie die [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7265f-164">You can use an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object as a geometric mask when you call the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="7265f-165">Die geometrische Maske gibt den Bereich der Ebene an, der in das Renderziel zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7265f-165">The geometric mask specifies the area of the layer that is composited into the render target.</span></span> <span data-ttu-id="7265f-166">Weitere Informationen finden Sie im Abschnitt geometrische Masken der Übersicht über [Ebenen](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7265f-166">For more information, see the Geometric Masks section of the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="geometric-operations"></a><span data-ttu-id="7265f-167">Geometrische Vorgänge</span><span class="sxs-lookup"><span data-stu-id="7265f-167">Geometric operations</span></span>

<span data-ttu-id="7265f-168">Die [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Schnittstelle stellt verschiedene geometrische Vorgänge bereit, mit denen Sie geometrische Abbildungen bearbeiten und messen können.</span><span class="sxs-lookup"><span data-stu-id="7265f-168">The [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) interface provides several geometric operations that you can use to manipulate and measure geometric figures.</span></span> <span data-ttu-id="7265f-169">Beispielsweise können Sie Sie zum Berechnen und zurückgeben ihrer Begrenzungen verwenden, vergleichen, um zu sehen, wie sich eine Geometrie räumlich mit einem anderen (nützlich für Treffer Tests), Berechnen der Bereiche und Längen und mehr eignet.</span><span class="sxs-lookup"><span data-stu-id="7265f-169">For example, you can use them to calculate and return their bounds, compare to see how one geometry is spatially related to another (useful for hit testing), calculate the areas and lengths, and more.</span></span> <span data-ttu-id="7265f-170">In der folgenden Tabelle werden die gängigen geometrischen Vorgänge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7265f-170">The following table describes the common geometric operations.</span></span>



| <span data-ttu-id="7265f-171">Vorgang</span><span class="sxs-lookup"><span data-stu-id="7265f-171">Operation</span></span>                                                   | <span data-ttu-id="7265f-172">Methode</span><span class="sxs-lookup"><span data-stu-id="7265f-172">Method</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7265f-173">Kombinieren</span><span class="sxs-lookup"><span data-stu-id="7265f-173">Combine</span></span>                                                     | [<span data-ttu-id="7265f-174">**Combinewithgeometry**</span><span class="sxs-lookup"><span data-stu-id="7265f-174">**CombineWithGeometry**</span></span>](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| <span data-ttu-id="7265f-175">Begrenzungen/erweiterte Begrenzungen/Abruf Begrenzungen, geänderte Regions Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="7265f-175">Bounds/ Widened Bounds/Retrieve Bounds, Dirty Region update</span></span> | <span data-ttu-id="7265f-176">[**Erweitert**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**getwidenedbounds**](id2d1geometry-getwidenedbounds.md)</span><span class="sxs-lookup"><span data-stu-id="7265f-176">[**Widen**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span></span>                             |
| <span data-ttu-id="7265f-177">Treffertests</span><span class="sxs-lookup"><span data-stu-id="7265f-177">Hit Testing</span></span>                                                 | <span data-ttu-id="7265f-178">[**Fillcontainspoint**](id2d1geometry-fillcontainspoint.md), [ **strokecontainspoint**](id2d1geometry-strokecontainspoint.md)</span><span class="sxs-lookup"><span data-stu-id="7265f-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span></span>                                             |
| <span data-ttu-id="7265f-179">Stroke</span><span class="sxs-lookup"><span data-stu-id="7265f-179">Stroke</span></span>                                                      | [<span data-ttu-id="7265f-180">**Strokecontainspoint**</span><span class="sxs-lookup"><span data-stu-id="7265f-180">**StrokeContainsPoint**</span></span>](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| <span data-ttu-id="7265f-181">Vergleich</span><span class="sxs-lookup"><span data-stu-id="7265f-181">Comparison</span></span>                                                  | [<span data-ttu-id="7265f-182">**Comparewithgeometry**</span><span class="sxs-lookup"><span data-stu-id="7265f-182">**CompareWithGeometry**</span></span>](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| <span data-ttu-id="7265f-183">Vereinfachung (entfernt Bögen und quadratische Bezier-Kurven)</span><span class="sxs-lookup"><span data-stu-id="7265f-183">Simplification (removes arcs and quadratic Bezier curves)</span></span>   | [<span data-ttu-id="7265f-184">**Vereinfachen**</span><span class="sxs-lookup"><span data-stu-id="7265f-184">**Simplify**</span></span>](id2d1geometry-simplify.md)                                                                                                                                 |
| <span data-ttu-id="7265f-185">Mosaik</span><span class="sxs-lookup"><span data-stu-id="7265f-185">Tessellation</span></span>                                                | [<span data-ttu-id="7265f-186">**& Nbsp;**</span><span class="sxs-lookup"><span data-stu-id="7265f-186">**Tessellate**</span></span>](id2d1geometry-tessellate.md)                                                                                                                             |
| <span data-ttu-id="7265f-187">Gliederung (Schnittmenge entfernen)</span><span class="sxs-lookup"><span data-stu-id="7265f-187">Outline (remove intersection)</span></span>                               | [<span data-ttu-id="7265f-188">**Outline**</span><span class="sxs-lookup"><span data-stu-id="7265f-188">**Outline**</span></span>](id2d1geometry-outline.md)                                                                                                                                   |
| <span data-ttu-id="7265f-189">Berechnen des Bereichs oder der Länge einer Geometrie</span><span class="sxs-lookup"><span data-stu-id="7265f-189">Calculate the area or length of a geometry</span></span>                  | <span data-ttu-id="7265f-190">[**Computearea**](id2d1geometry-computearea.md), [**computelength**](id2d1geometry-computelength.md), [**computepointatlength**](id2d1geometry-computepointatlength.md)</span><span class="sxs-lookup"><span data-stu-id="7265f-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span></span> |



 

> [!Note]  
> <span data-ttu-id="7265f-191">Ab Windows 8 können Sie die [**computepointandsegmentatlength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) -Methode für den [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) verwenden, um den Bereich oder die Länge einer Geometrie zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7265f-191">Starting in Windows 8, you can use the [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) method on the [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) to calculate the area or length of a geometry.</span></span>

 

### <a name="combining-geometries"></a><span data-ttu-id="7265f-192">Kombinieren von Geometrien</span><span class="sxs-lookup"><span data-stu-id="7265f-192">Combining geometries</span></span>

<span data-ttu-id="7265f-193">Um eine Geometrie mit einer anderen zu kombinieren, nennen Sie die [**ID2D1Geometry:: combinewithgeometry**](id2d1geometry-combinewithgeometry.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7265f-193">To combine one geometry with another, call the [**ID2D1Geometry::CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) method.</span></span> <span data-ttu-id="7265f-194">Wenn Sie die Geometrien kombinieren, geben Sie eine der vier Möglichkeiten zum Durchführen des kombinierungsvorgangs an: [**D2D1 \_ Combine \_ Mode \_ Union**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Union), [**D2D1 \_ Combine \_ Mode \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**D2D1 \_ Combine \_ Mode \_ Xor**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) und [**D2D1 \_ Combine \_ Mode \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Exclude).</span><span class="sxs-lookup"><span data-stu-id="7265f-194">When you combine the geometries, you specify one of the four ways to perform the combine operation: [**D2D1\_COMBINE\_MODE\_UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1\_COMBINE\_MODE\_INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1\_COMBINE\_MODE\_XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor), and [**D2D1\_COMBINE\_MODE\_EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude).</span></span> <span data-ttu-id="7265f-195">Im folgenden Codebeispiel werden zwei Kreise veranschaulicht, die mithilfe des Union-kombinierungsmodus kombiniert werden, wobei der erste Kreis den Mittelpunkt von (75, 75) und den RADIUS 50 hat und der zweite Kreis den Mittelpunkt von (125, 75) und den Radius von 50 hat.</span><span class="sxs-lookup"><span data-stu-id="7265f-195">The following code example shows two circles that are combined by using the union combine mode, where the first circle has the center point of (75, 75) and the radius of 50, and the second circle has the center point of (125, 75) and the radius of 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



<span data-ttu-id="7265f-196">In der folgenden Abbildung werden zwei Kreise in Kombination mit einem kombinierungsmodus von Union gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7265f-196">The following illustration shows two circles combined with a combine mode of union.</span></span>

![Abbildung von zwei überlappenden Kreisen, kombiniert zu einer Union](images/combine-mode-union.png)

<span data-ttu-id="7265f-198">Abbildungen aller kombinierungsmodi finden Sie unter [**D2D1 \_ Combine \_ Mode Enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span><span class="sxs-lookup"><span data-stu-id="7265f-198">For illustrations of all the combine modes, see the [**D2D1\_COMBINE\_MODE enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span></span>

### <a name="widen"></a><span data-ttu-id="7265f-199">Ausbreiten</span><span class="sxs-lookup"><span data-stu-id="7265f-199">Widen</span></span>

<span data-ttu-id="7265f-200">Die [**Methode "**](id2d1geometry-widen.md) -Methode" generiert eine neue Geometrie, deren Füllung dem Überschreiben der vorhandenen Geometrie entspricht, und schreibt dann das Ergebnis in das angegebene [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7265f-200">The [**Widen**](id2d1geometry-widen.md) method generates a new geometry whose fill is equivalent to stroking the existing geometry, and then writes the result to the specified [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span> <span data-ttu-id="7265f-201">Im folgenden Codebeispiel wird [**geöffnet**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) für das [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7265f-201">The following code example calls [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) on the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object.</span></span> <span data-ttu-id="7265f-202">Wenn das **Öffnen** erfolgreich ist, wird die **Erweiterung** für das Geometry-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7265f-202">If **Open** succeeds, it calls **Widen** on the geometry object.</span></span>


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a><span data-ttu-id="7265f-203">& Nbsp;</span><span class="sxs-lookup"><span data-stu-id="7265f-203">Tessellate</span></span>

<span data-ttu-id="7265f-204">Die [**Mosaik Methode erstellt**](id2d1geometry-tessellate.md) eine Reihe von Dreiecken im Uhrzeigersinn, die die Geometrie abdecken, nachdem Sie mithilfe der angegebenen Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde.</span><span class="sxs-lookup"><span data-stu-id="7265f-204">The [**Tessellate**](id2d1geometry-tessellate.md) method creates a set of clockwise-wound triangles that cover the geometry after it is transformed by using the specified matrix and flattened by using the specified tolerance.</span></span> <span data-ttu-id="7265f-205">Im folgenden Codebeispiel wird **Mosaik verwendet,** um eine Liste von Dreiecken zu erstellen, die *ppathgeometry* darstellen.</span><span class="sxs-lookup"><span data-stu-id="7265f-205">The following code example uses **Tessellate** to create a list of triangles that represent *pPathGeometry*.</span></span> <span data-ttu-id="7265f-206">Die Dreiecke werden in [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pmesh*, gespeichert und dann für die spätere Verwendung beim Rendern an den Klassenmember *m \_ pstrokemesh* übertragen.</span><span class="sxs-lookup"><span data-stu-id="7265f-206">The triangles are stored in an [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, then transferred to a class member, *m\_pStrokeMesh*, for later use when rendering.</span></span>


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a><span data-ttu-id="7265f-207">Fillcontainspoint und strokecontainspoint</span><span class="sxs-lookup"><span data-stu-id="7265f-207">FillContainsPoint and StrokeContainsPoint</span></span>

<span data-ttu-id="7265f-208">Die [**fillcontainspoint**](id2d1geometry-fillcontainspoint.md) -Methode gibt an, ob der von der Geometrie gefüllte Bereich den angegebenen Punkt enthält.</span><span class="sxs-lookup"><span data-stu-id="7265f-208">The [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) method indicates whether the area filled by the geometry contains the specified point.</span></span> <span data-ttu-id="7265f-209">Mit dieser Methode können Sie Treffer Tests durchführen.</span><span class="sxs-lookup"><span data-stu-id="7265f-209">You can use this method to do hit testing.</span></span> <span data-ttu-id="7265f-210">Das folgende Codebeispiel ruft **fillcontainspoint** für ein [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) -Objekt auf und übergibt einen Punkt an (0,0) und eine [**Identitäts**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) Matrix.</span><span class="sxs-lookup"><span data-stu-id="7265f-210">The following code example calls **FillContainsPoint** on an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) object, passing in a point at (0,0) and an [**Identity**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) matrix.</span></span>


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



<span data-ttu-id="7265f-211">Die [**strokecontainspoint**](id2d1geometry-strokecontainspoint.md) -Methode bestimmt, ob der Strich der Geometrie den angegebenen Punkt enthält.</span><span class="sxs-lookup"><span data-stu-id="7265f-211">The [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) method determines whether the geometry's stroke contains the specified point.</span></span> <span data-ttu-id="7265f-212">Mit dieser Methode können Sie Treffer Tests durchführen.</span><span class="sxs-lookup"><span data-stu-id="7265f-212">You can use this method to do hit testing.</span></span> <span data-ttu-id="7265f-213">Im folgenden Codebeispiel wird **strokecontainspoint** verwendet.</span><span class="sxs-lookup"><span data-stu-id="7265f-213">The following code example uses **StrokeContainsPoint**.</span></span>


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a><span data-ttu-id="7265f-214">Vereinfachen von </span><span class="sxs-lookup"><span data-stu-id="7265f-214">Simplify</span></span>

<span data-ttu-id="7265f-215">Die Methode " [**vereinfachen**](id2d1geometry-simplify.md) " entfernt Bögen und quadratische Bezier-Kurven aus einer angegebenen Geometrie.</span><span class="sxs-lookup"><span data-stu-id="7265f-215">The [**Simplify**](id2d1geometry-simplify.md) method removes arcs and quadratic Bezier curves from a specified geometry.</span></span> <span data-ttu-id="7265f-216">Daher enthält die resultierende Geometrie nur Zeilen und optional kubische Bezier-Kurven.</span><span class="sxs-lookup"><span data-stu-id="7265f-216">So, the resulting geometry contains only lines and, optionally, cubic Bezier curves.</span></span> <span data-ttu-id="7265f-217">Im folgenden Codebeispiel wird die Verwendung von **vereinfachen** , um eine Geometrie mit Bezier-Kurven in eine Geometrie umzuwandeln, die nur Liniensegmente enthält.</span><span class="sxs-lookup"><span data-stu-id="7265f-217">The following code example uses **Simplify** to transform a geometry with Bezier curves into a geometry that contains only line segments.</span></span>


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a><span data-ttu-id="7265f-218">Computelength und computearea</span><span class="sxs-lookup"><span data-stu-id="7265f-218">ComputeLength and ComputeArea</span></span>

<span data-ttu-id="7265f-219">Die [**computelength**](id2d1geometry-computelength.md) -Methode berechnet die Länge der angegebenen Geometrie, wenn für jedes Segment ein Rollback in eine Zeile durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7265f-219">The [**ComputeLength**](id2d1geometry-computelength.md) method calculates the length of the specified geometry if each segment were unrolled into a line.</span></span> <span data-ttu-id="7265f-220">Dies schließt das implizite schließende Segment ein, wenn die Geometrie geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7265f-220">This includes the implicit closing segment if the geometry is closed.</span></span> <span data-ttu-id="7265f-221">Im folgenden Codebeispiel wird **computelength** verwendet, um die Länge eines angegebenen Kreises (**m \_ pCircleGeometry1**) zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7265f-221">The following code example uses **ComputeLength** to compute the length of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



<span data-ttu-id="7265f-222">Die [**computearea**](id2d1geometry-computearea.md) -Methode berechnet den Bereich der angegebenen Geometrie.</span><span class="sxs-lookup"><span data-stu-id="7265f-222">The [**ComputeArea**](id2d1geometry-computearea.md) method calculates the area of the specified geometry.</span></span> <span data-ttu-id="7265f-223">Im folgenden Codebeispiel wird **computearea** verwendet, um den Bereich eines angegebenen Kreises (**m \_ pCircleGeometry1**) zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7265f-223">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a><span data-ttu-id="7265f-224">Comparewithgeometry</span><span class="sxs-lookup"><span data-stu-id="7265f-224">CompareWithGeometry</span></span>

<span data-ttu-id="7265f-225">Die [**comparewithgeometry**](id2d1geometry-comparewithgeometry.md) -Methode beschreibt die Schnittmenge zwischen der Geometrie, die diese Methode aufruft, und der angegebenen Geometrie.</span><span class="sxs-lookup"><span data-stu-id="7265f-225">The [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) method describes the intersection between the geometry that calls this method and the specified geometry.</span></span> <span data-ttu-id="7265f-226">Die möglichen Werte für die Schnittmenge umfassen [**D2D1 \_ Geometry- \_ Beziehung \_ Disjoint**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (Disjoint), **D2D1 \_ Geometry \_ Relation \_ ist \_** enthalten (ist enthalten), **D2D1 \_ Geometry- \_ Beziehung \_ enthält** (enthält) und **D2D1 Geometry- \_ \_ Beziehungs \_ Überschneidung** (überlappend).</span><span class="sxs-lookup"><span data-stu-id="7265f-226">The possible values for intersection include [**D2D1\_GEOMETRY\_RELATION\_DISJOINT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjoint), **D2D1\_GEOMETRY\_RELATION\_IS\_CONTAINED** (is contained), **D2D1\_GEOMETRY\_RELATION\_CONTAINS** (contains), and **D2D1\_GEOMETRY\_RELATION\_OVERLAP** (overlap).</span></span> <span data-ttu-id="7265f-227">"Disjoint" bedeutet, dass sich zwei Geometrie Füllungen überhaupt nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="7265f-227">"disjoint" means that two geometry fills do not intersect at all.</span></span> <span data-ttu-id="7265f-228">"ist enthalten" bedeutet, dass die Geometrie vollständig in der angegebenen Geometrie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7265f-228">"is contained" means that the geometry is completely contained by the specified geometry.</span></span> <span data-ttu-id="7265f-229">"enthält" bedeutet, dass die Geometrie die angegebene Geometrie vollständig enthält und "Überlappend" bedeutet, dass sich die beiden Geometrien überlappen, aber keines der anderen enthält.</span><span class="sxs-lookup"><span data-stu-id="7265f-229">"contains" means that the geometry completely contains the specified geometry, and "overlap" means the two geometries overlap but neither completely contains the other.</span></span>

<span data-ttu-id="7265f-230">Im folgenden Codebeispiel wird gezeigt, wie zwei Kreise verglichen werden, die den gleichen RADIUS von 50 aufweisen, aber um 50 versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7265f-230">The following code example shows how to compare two circles that have the same radius of 50 but are offset by 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a><span data-ttu-id="7265f-231">Outline</span><span class="sxs-lookup"><span data-stu-id="7265f-231">Outline</span></span>

<span data-ttu-id="7265f-232">Die Gliederungs [**Methode berechnet die**](id2d1geometry-outline.md) Gliederung der Geometrie (eine Version der Geometrie, in der keine Abbildung sich selbst oder eine andere Abbildung überschneidet) und schreibt das Ergebnis in ein [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="7265f-232">The [**Outline**](id2d1geometry-outline.md) method computes the outline of the geometry (a version of the geometry in which no figure crosses itself or any other figure) and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="7265f-233">Im folgenden Codebeispiel wird **Gliederung verwendet,** um eine äquivalente Geometrie ohne selbst Austausch Vorgänge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7265f-233">The following code example uses **Outline** to construct an equivalent geometry without any self-intersections.</span></span> <span data-ttu-id="7265f-234">Sie verwendet die standardmäßige Vereinfachungs Toleranz.</span><span class="sxs-lookup"><span data-stu-id="7265f-234">It uses the default flattening tolerance.</span></span>


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a><span data-ttu-id="7265f-235">GetBounds und getwidenedbounds</span><span class="sxs-lookup"><span data-stu-id="7265f-235">GetBounds and GetWidenedBounds</span></span>

<span data-ttu-id="7265f-236">Die [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) -Methode ruft die Begrenzungen der Geometrie ab.</span><span class="sxs-lookup"><span data-stu-id="7265f-236">The [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) method retrieves the bounds of the geometry.</span></span> <span data-ttu-id="7265f-237">Im folgenden Codebeispiel wird **GetBounds** verwendet, um die Begrenzungen eines angegebenen Kreises (**m \_ pCircleGeometry1**) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7265f-237">The following code example uses **GetBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



<span data-ttu-id="7265f-238">Die [**getwidenedbounds**](id2d1geometry-getwidenedbounds.md) -Methode ruft die Grenzen der Geometrie ab, nachdem Sie durch die angegebene Strichbreite und den angegebenen Stil erweitert und durch die angegebene Matrix transformiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7265f-238">The [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) method retrieves the bounds of the geometry after it is widened by the specified stroke width and style and transformed by the specified matrix.</span></span> <span data-ttu-id="7265f-239">Im folgenden Codebeispiel wird **getwidenedbounds** verwendet, um die Begrenzungen eines angegebenen Kreises (**m \_ pCircleGeometry1**) abzurufen, nachdem er um die angegebene Strichbreite erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="7265f-239">The following code example uses **GetWidenedBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**) after it is widened by the specified stroke width.</span></span>


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a><span data-ttu-id="7265f-240">Computepointatlength</span><span class="sxs-lookup"><span data-stu-id="7265f-240">ComputePointAtLength</span></span>

<span data-ttu-id="7265f-241">Die [**computepointatlength**](id2d1geometry-computepointatlength.md) -Methode berechnet den Punkt und den Tangenten Vektor in der angegebenen Entfernung entlang der Geometrie.</span><span class="sxs-lookup"><span data-stu-id="7265f-241">The [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) method calculates the point and tangent vector at the specified distance along the geometry.</span></span> <span data-ttu-id="7265f-242">Im folgenden Codebeispiel wird **computepointatlength** verwendet.</span><span class="sxs-lookup"><span data-stu-id="7265f-242">The following code example uses **ComputePointAtLength**.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a><span data-ttu-id="7265f-243">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7265f-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7265f-244">Übersicht über Pfadgeometrien</span><span class="sxs-lookup"><span data-stu-id="7265f-244">Path Geometries Overview</span></span>](path-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="7265f-245">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="7265f-245">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 