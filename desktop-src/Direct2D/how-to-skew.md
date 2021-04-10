---
title: Vorgehensweise beim Verzerren eines Objekts
description: Zeigt, wie ein Objekt verzerrt wird.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858407"
---
# <a name="how-to-skew-an-object"></a><span data-ttu-id="a5327-103">Vorgehensweise beim Verzerren eines Objekts</span><span class="sxs-lookup"><span data-stu-id="a5327-103">How to Skew an Object</span></span>

<span data-ttu-id="a5327-104">Um ein Objekt zu neigen (oder zu scheren), bedeutet dies, dass ein Objekt um einen angegebenen Winkel von der x-Achse, der y-Achse oder beidem verzerrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5327-104">To skew (or shear) an object means to distort an object by a specified angle from the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="a5327-105">Wenn Sie beispielsweise ein Quadrat neigen, wird es zu einem Parallelogramm.</span><span class="sxs-lookup"><span data-stu-id="a5327-105">For example, when you skew a square, it becomes a parallelogram.</span></span>

<span data-ttu-id="a5327-106">Die [**Matrix3x2F:: schräw**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) -Methode nimmt 3 Parameter an:</span><span class="sxs-lookup"><span data-stu-id="a5327-106">The [**Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) method takes 3 parameters:</span></span>

-   <span data-ttu-id="a5327-107">*AngleX*: der Neigungswinkel der x-Achse, der in Grad gegen den Uhrzeigersinn von der y-Achse aus gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="a5327-107">*angleX*: The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.</span></span>
-   <span data-ttu-id="a5327-108">*AngleY*: der Neigungswinkel der y-Achse, der in Grad im Uhrzeigersinn von der x-Achse aus gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="a5327-108">*angleY*: The y-axis skew angle, which is measured in degrees clockwise from the x-axis.</span></span>
-   <span data-ttu-id="a5327-109">*CenterPoint*: der Punkt, an dem die Schiefe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5327-109">*centerPoint*: The point about which the skew is performed.</span></span>

<span data-ttu-id="a5327-110">Um die Auswirkung einer Neigungs Transformation vorherzusagen, sollten Sie Bedenken, dass *AngleX* der Neigungswinkel in Grad gegen den Uhrzeigersinn von der y-Achse aus gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="a5327-110">To predict the effect of a skew transformation, consider that *angleX* is the skew angle measured in degrees counterclockwise from the y-axis.</span></span> <span data-ttu-id="a5327-111">Wenn *AngleX* z. b. auf 30 festgelegt ist, wird das Objekt 30 Grad gegen den Uhrzeigersinn entlang der y-Achse um den Mittel *Punkt* gedreht.</span><span class="sxs-lookup"><span data-stu-id="a5327-111">For example, if *angleX* is set to 30, the object skews 30 degrees counterclockwise along the y-axis about the *centerPoint*.</span></span> <span data-ttu-id="a5327-112">In der folgenden Abbildung wird eine eckige eckige Abweichung von 30 Grad in der oberen linken Ecke des Quadrats gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5327-112">The following illustration shows a square skewed horizontally 30 degrees about the upper-left corner of the square.</span></span>

![Abbildung einer quadratischen Verzerrung von 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skewx.png)

<span data-ttu-id="a5327-114">Ebenso ist *AngleY* ein Neigungswinkel, der in Grad im Uhrzeigersinn von der x-Achse aus gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="a5327-114">Similarly, *angleY* is a skew angle measured in degrees clockwise from the x-axis.</span></span> <span data-ttu-id="a5327-115">Wenn *AngleY* z. b. auf 30 festgelegt ist, wird das Objekt 30 Grad im Uhrzeigersinn entlang der x-Achse um den Mittel *Punkt* gerengt.</span><span class="sxs-lookup"><span data-stu-id="a5327-115">For example, if *angleY* is set to 30, the object skews 30 degrees clockwise along the x-axis about the *centerPoint*.</span></span> <span data-ttu-id="a5327-116">In der folgenden Abbildung wird eine quadratische Breite von 30 Grad in der oberen linken Ecke des Quadrats gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5327-116">The following illustration shows a square skewed vertically 30 degrees about the upper-left corner of the square.</span></span>

![Abbildung einer quadratischen Verzerrung um 30 Grad im Uhrzeigersinn von der x-Achse](images/skewy.png)

<span data-ttu-id="a5327-118">Wenn Sie " *AngleX* " und " *AngleY* " auf 30 Grad festgelegt haben und der Mittel *Punkt* auf die linke obere Ecke des Quadrats festgelegt ist, wird das folgende schräge Quadrat angezeigt (durch ein Vollformat dargestellt).</span><span class="sxs-lookup"><span data-stu-id="a5327-118">If you set both *angleX* and *angleY* to 30 degrees, and the *centerPoint* to the upper-left corner of the square, you will see the following skewed square (solid outlined).</span></span> <span data-ttu-id="a5327-119">Beachten Sie, dass das rechteckige Quadrat 30 Grad gegen den Uhrzeigersinn von der y-Achse und 30 Grad im Uhrzeigersinn von der x-Achse aus verzerrt wird.</span><span class="sxs-lookup"><span data-stu-id="a5327-119">Notice that the skewed square is skewed 30 degrees counterclockwise from the y-axis and 30 degrees clockwise from the x-axis.</span></span>

![Abbildung einer quadratischen Verzerrung von 30 Grad gegen den Uhrzeigersinn von der y-Achse und 30 Grad im Uhrzeigersinn von der x-Achse](images/skewxy.png)

<span data-ttu-id="a5327-121">Im folgenden Codebeispiel wird die Quadrat-45 Grad horizontal um die obere linke Ecke des Quadrats bündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="a5327-121">The following code example skews the square 45 degrees horizontally about the upper-left corner of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="a5327-122">In der folgenden Abbildung wird gezeigt, wie sich die Schiefe-Transformation auf das Quadrat auswirkt, wobei das ursprüngliche Quadrat ein gepunkteter Umriss und das schiefe Objekt (Parallelogram) ein voll Bild Umriss ist.</span><span class="sxs-lookup"><span data-stu-id="a5327-122">The following illustration shows the effect of applying the skew transformation to the square, where the original square is a dotted outline and the skewed object (parallelogram) is a solid outline.</span></span> <span data-ttu-id="a5327-123">Beachten Sie, dass der Neigungswinkel von der y-Achse aus 45 Grad gegen den Uhrzeigersinn liegt.</span><span class="sxs-lookup"><span data-stu-id="a5327-123">Notice that the skew angle is 45 degrees counterclockwise from the y-axis.</span></span>

![Abbildung eines quadratischen verzerrt 45 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="a5327-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5327-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5327-126">Übersicht über Direct2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="a5327-126">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="a5327-127">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="a5327-127">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 