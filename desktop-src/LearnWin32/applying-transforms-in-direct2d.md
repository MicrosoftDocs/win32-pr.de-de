---
title: Anwenden von Transformationen in Direct2D
description: Anwenden von Transformationen in Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727337"
---
# <a name="applying-transforms-in-direct2d"></a><span data-ttu-id="14dec-103">Anwenden von Transformationen in Direct2D</span><span class="sxs-lookup"><span data-stu-id="14dec-103">Applying Transforms in Direct2D</span></span>

<span data-ttu-id="14dec-104">Beim [Zeichnen mit Direct2D](drawing-with-direct2d.md)haben wir gesehen, dass die [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methode eine Ellipse zeichnet, die an der x-und y-Achse ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="14dec-104">In [Drawing with Direct2D](drawing-with-direct2d.md), we saw that the [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws an ellipse that is aligned to the x- and y-axes.</span></span> <span data-ttu-id="14dec-105">Angenommen, Sie möchten eine Ellipse, die an einem Winkel gekippt ist, zeichnen?</span><span class="sxs-lookup"><span data-stu-id="14dec-105">But suppose that you want to draw an ellipse tilted at an angle?</span></span>

![ein Bild, das eine gekippte Ellipse anzeigt.](images/graphics16.png)

<span data-ttu-id="14dec-107">Mithilfe von Transformationen können Sie eine Form wie folgt ändern.</span><span class="sxs-lookup"><span data-stu-id="14dec-107">By using transforms, you can alter a shape in the following ways.</span></span>

-   <span data-ttu-id="14dec-108">Drehung um einen Punkt.</span><span class="sxs-lookup"><span data-stu-id="14dec-108">Rotation around a point.</span></span>
-   <span data-ttu-id="14dec-109">Skalieren.</span><span class="sxs-lookup"><span data-stu-id="14dec-109">Scaling.</span></span>
-   <span data-ttu-id="14dec-110">Übersetzung (Verschiebung in der X-oder Y-Richtung).</span><span class="sxs-lookup"><span data-stu-id="14dec-110">Translation (displacement in the X or Y direction).</span></span>
-   <span data-ttu-id="14dec-111">Schiefe (auch als *Schere* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="14dec-111">Skew (also known as *shear*).</span></span>

<span data-ttu-id="14dec-112">Eine Transformation ist eine mathematische Operation, bei der eine Gruppe von Punkten einem neuen Satz von Punkten zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="14dec-112">A transform is a mathematical operation that maps a set of points to a new set of points.</span></span> <span data-ttu-id="14dec-113">Das folgende Diagramm zeigt z. b. ein Dreieck, das um den Punkt P3 gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="14dec-113">For example, the following diagram shows a triangle rotated around the point P3.</span></span> <span data-ttu-id="14dec-114">Nachdem die Drehung angewendet wurde, wird der Punkt P1 "P1" zugeordnet, der Punkt P2 wird P2 zugeordnet, und der Punkt P3 wird sich selbst zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="14dec-114">After the rotation is applied, the point P1 is mapped to P1', the point P2 is mapped to P2', and the point P3 maps to itself.</span></span>

![ein Diagramm, das die Drehung um einen Punkt zeigt.](images/graphics17.png)

<span data-ttu-id="14dec-116">Transformationen werden mithilfe von Matrizen implementiert.</span><span class="sxs-lookup"><span data-stu-id="14dec-116">Transforms are implemented by using matrices.</span></span> <span data-ttu-id="14dec-117">Allerdings müssen Sie die Mathematik von Matrizen nicht verstehen, um Sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="14dec-117">However, you do not have to understand the mathematics of matrices in order to use them.</span></span> <span data-ttu-id="14dec-118">Weitere Informationen über die mathematische Informationen finden Sie unter [Anhang: Matrix Transformationen](appendix--matrix-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="14dec-118">If you want to learn more about the math, see [Appendix: Matrix Transforms](appendix--matrix-transforms.md).</span></span>

<span data-ttu-id="14dec-119">Um eine Transformation in Direct2D anzuwenden, müssen Sie die [**ID2D1RenderTarget:: setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14dec-119">To apply a transform in Direct2D, call the [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) method.</span></span> <span data-ttu-id="14dec-120">Diese Methode nimmt eine [**D2D1 \_ Matrix \_ 3x2 \_ F-**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) Struktur an, die die Transformation definiert.</span><span class="sxs-lookup"><span data-stu-id="14dec-120">This method takes a [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure that defines the transformation.</span></span> <span data-ttu-id="14dec-121">Sie können diese Struktur initialisieren, indem Sie Methoden für die [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14dec-121">You can initialize this structure by calling methods on the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="14dec-122">Diese Klasse enthält statische Methoden, die eine Matrix für jede Art von Transformation zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="14dec-122">This class contains static methods that return a matrix for each kind of transform:</span></span>

-   [<span data-ttu-id="14dec-123">**Matrix3x2F:: Rotation**</span><span class="sxs-lookup"><span data-stu-id="14dec-123">**Matrix3x2F::Rotation**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   <span data-ttu-id="14dec-124">[**Matrix3x2F:: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="14dec-124">[**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span>
-   <span data-ttu-id="14dec-125">[**Matrix3x2F:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="14dec-125">[**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>
-   [<span data-ttu-id="14dec-126">**Matrix3x2F:: schiefe**</span><span class="sxs-lookup"><span data-stu-id="14dec-126">**Matrix3x2F::Skew**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

<span data-ttu-id="14dec-127">Mit dem folgenden Code wird z. b. eine 20-Grad-Drehung um den Punkt (100, 100) angewendet.</span><span class="sxs-lookup"><span data-stu-id="14dec-127">For example, the following code applies a 20-degree rotation around the point (100, 100).</span></span>


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

<span data-ttu-id="14dec-128">Die Transformation wird auf alle späteren Zeichnungsvorgänge angewendet, bis Sie [**setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) erneut aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14dec-128">The transform is applied to all later drawing operations until you call [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) again.</span></span> <span data-ttu-id="14dec-129">Zum Entfernen der aktuellen Transformation aufrufen Sie **setTransform** mit der Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="14dec-129">To remove the current transform, call **SetTransform** with the identity matrix.</span></span> <span data-ttu-id="14dec-130">Um die Identitätsmatrix zu erstellen, rufen Sie die [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="14dec-130">To create the identity matrix, call the [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) function.</span></span>


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a><span data-ttu-id="14dec-131">Zeichnen von Takt Händen</span><span class="sxs-lookup"><span data-stu-id="14dec-131">Drawing Clock Hands</span></span>

<span data-ttu-id="14dec-132">Wir setzen Transformationen ein, indem wir unser kreisprogramm in eine analoge Uhr umrechnen.</span><span class="sxs-lookup"><span data-stu-id="14dec-132">Let's put transforms to use by converting our Circle program into an analog clock.</span></span> <span data-ttu-id="14dec-133">Dies erreichen Sie, indem Sie Zeilen für die Hände hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="14dec-133">We can do this by adding lines for the hands.</span></span>

![ein Screenshot des Programms zur analogen Uhr.](images/graphics18.png)

<span data-ttu-id="14dec-135">Anstatt die Koordinaten für die Linien zu berechnen, können wir den Winkel berechnen und dann eine Drehungs Transformation anwenden.</span><span class="sxs-lookup"><span data-stu-id="14dec-135">Instead of calculating the coordinates for the lines, we can calculate the angle and then apply a rotation transform.</span></span> <span data-ttu-id="14dec-136">Der folgende Code zeigt eine Funktion, die eine Uhr Hand zeichnet.</span><span class="sxs-lookup"><span data-stu-id="14dec-136">The following code shows a function that draws one clock hand.</span></span> <span data-ttu-id="14dec-137">Der *fangle* -Parameter gibt den Winkel der Hand in Grad an.</span><span class="sxs-lookup"><span data-stu-id="14dec-137">The *fAngle* parameter gives the angle of the hand, in degrees.</span></span>

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

<span data-ttu-id="14dec-138">Dieser Code zeichnet eine vertikale Linie, beginnend ab der Mitte der Uhr und endet am Punkt *Endpunkt*.</span><span class="sxs-lookup"><span data-stu-id="14dec-138">This code draws a vertical line, starting from the center of the clock face and ending at the point *endPoint*.</span></span> <span data-ttu-id="14dec-139">Die Linie wird um den Mittelpunkt der Ellipse gedreht, indem eine Rotations Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="14dec-139">The line is rotated around the center of the ellipse by applying a rotation transform.</span></span> <span data-ttu-id="14dec-140">Der Mittelpunkt der Drehung ist der Mittelpunkt der Ellipse, der die Uhr darstellt.</span><span class="sxs-lookup"><span data-stu-id="14dec-140">The center point for the rotation is the center of ellipse that forms the clock face.</span></span>

![ein Diagramm, das die Drehung der Uhrzeitangabe anzeigt.](images/graphics19.png)

<span data-ttu-id="14dec-142">Der folgende Code zeigt, wie die gesamte Takt Fläche gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="14dec-142">The following code shows how the whole clock face is drawn.</span></span>

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

<span data-ttu-id="14dec-143">Sie können das komplette Visual Studio-Projekt aus dem [Direct2D Clock-Beispiel](direct2d-clock-sample.md)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="14dec-143">You can download the complete Visual Studio project from [Direct2D Clock Sample](direct2d-clock-sample.md).</span></span> <span data-ttu-id="14dec-144">(Nur zum Spaß fügt die Download Version ein radiales gradiant zum Takt Gesicht hinzu.)</span><span class="sxs-lookup"><span data-stu-id="14dec-144">(Just for fun, the download version adds a radial gradiant to the clock face.)</span></span>

## <a name="combining-transforms"></a><span data-ttu-id="14dec-145">Kombinieren von Transformationen</span><span class="sxs-lookup"><span data-stu-id="14dec-145">Combining Transforms</span></span>

<span data-ttu-id="14dec-146">Die vier grundlegenden Transformationen können kombiniert werden, indem zwei oder mehr Matrizen multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="14dec-146">The four basic transforms can be combined by multiplying two or more matrices.</span></span> <span data-ttu-id="14dec-147">Der folgende Code kombiniert z. b. eine Drehung mit einer Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="14dec-147">For example, the following code combines a rotation with a translation.</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="14dec-148">Die [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse stellt [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) für die Matrix Multiplikation bereit.</span><span class="sxs-lookup"><span data-stu-id="14dec-148">The [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for matrix multiplication.</span></span> <span data-ttu-id="14dec-149">Die Reihenfolge, in der Sie die Matrizen multiplizieren, ist wichtig.</span><span class="sxs-lookup"><span data-stu-id="14dec-149">The order in which you multiply the matrices is important.</span></span> <span data-ttu-id="14dec-150">Das Festlegen einer Transformation (m × N) bedeutet "m zuerst anwenden, gefolgt von N".</span><span class="sxs-lookup"><span data-stu-id="14dec-150">Setting a transform (M × N) means "Apply M first, followed by N."</span></span> <span data-ttu-id="14dec-151">Hier sehen Sie beispielsweise die Drehung, gefolgt von der Übersetzung:</span><span class="sxs-lookup"><span data-stu-id="14dec-151">For example, here is rotation followed by translation:</span></span>

![ein Diagramm, das die Drehung anzeigt, gefolgt von der Übersetzung.](images/graphics20.png)

<span data-ttu-id="14dec-153">Dies ist der Code für diese Transformation:</span><span class="sxs-lookup"><span data-stu-id="14dec-153">Here is the code for this transform:</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="14dec-154">Vergleichen Sie nun diese Transformation mit einer Transformation in umgekehrter Reihenfolge, Übersetzung und Drehung, gefolgt von der Drehung.</span><span class="sxs-lookup"><span data-stu-id="14dec-154">Now compare that transform with a transform in the reverse order, translation followed by rotation.</span></span>

![ein Diagramm, das die Übersetzung anzeigt, gefolgt von der Drehung.](images/graphics21.png)

<span data-ttu-id="14dec-156">Die Drehung erfolgt um die Mitte des ursprünglichen Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="14dec-156">The rotation is performed around the center of the original rectangle.</span></span> <span data-ttu-id="14dec-157">Dies ist der Code für diese Transformation.</span><span class="sxs-lookup"><span data-stu-id="14dec-157">Here is the code for this transform.</span></span>

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

<span data-ttu-id="14dec-158">Wie Sie sehen können, sind die Matrizen identisch, aber die Reihenfolge der Vorgänge hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="14dec-158">As you can see, the matrices are the same, but the order of operations has changed.</span></span> <span data-ttu-id="14dec-159">Dies liegt daran, dass die Matrix Multiplikation nicht commutative ist: M × N ≠ N × M.</span><span class="sxs-lookup"><span data-stu-id="14dec-159">This happens because matrix multiplication is not commutative: M × N ≠ N × M.</span></span>

## <a name="next"></a><span data-ttu-id="14dec-160">Nächste</span><span class="sxs-lookup"><span data-stu-id="14dec-160">Next</span></span>

[<span data-ttu-id="14dec-161">Anhang: Matrix Transformationen</span><span class="sxs-lookup"><span data-stu-id="14dec-161">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)