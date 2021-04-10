---
title: Drehen eines Objekts
description: Zeigt, wie ein Objekt gedreht wird.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948938"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="70185-103">Drehen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="70185-103">How to Rotate an Object</span></span>

<span data-ttu-id="70185-104">In diesem Thema wird beschrieben, wie ein Objekt um einen angegebenen Punkt gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="70185-104">This topic describes how to rotate an object about a specified point.</span></span> <span data-ttu-id="70185-105">Um ein Objekt zu drehen, nennen Sie die [**Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) -Methode.</span><span class="sxs-lookup"><span data-stu-id="70185-105">To rotate an object, call [**Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method.</span></span> <span data-ttu-id="70185-106">Diese Methode erfordert zwei Parameter, den angegebenen Winkel und den Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="70185-106">This method takes two parameters, the specified angle and the center point.</span></span> <span data-ttu-id="70185-107">Der Winkel ist ein Drehungs Winkel im Uhrzeigersinn in Grad, und der Mittelpunkt ist der Punkt, an dem sich das Objekt dreht.</span><span class="sxs-lookup"><span data-stu-id="70185-107">The angle is a clockwise rotation angle in degrees, and the center point is the point about which the object rotates.</span></span> <span data-ttu-id="70185-108">Der Mittelpunkt wird im Koordinatensystem des Objekts ausgedrückt, das transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="70185-108">The center point is expressed in the coordinate system of the object that is transformed.</span></span>

<span data-ttu-id="70185-109">Der folgende Code dreht z. b. einen quadratischen Uhrzeigersinn um 45 Grad um die Mitte des Quadrats.</span><span class="sxs-lookup"><span data-stu-id="70185-109">For example, the following code rotates a square clockwise 45 degrees about the center of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="70185-110">Die folgende Abbildung zeigt die Auswirkung der Anwendung der vorangehenden Rotations Transformation auf das Quadrat.</span><span class="sxs-lookup"><span data-stu-id="70185-110">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="70185-111">Das ursprüngliche Quadrat ist ein gepunkteter Umriss, und das gedrehte Quadrat ist ein voll solider Umriss.</span><span class="sxs-lookup"><span data-stu-id="70185-111">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![Abbildung eines Quadrats um 45 Grad im Uhrzeigersinn um die Mitte des ursprünglichen Quadrats gedreht](images/rotate-ovw.png)

<span data-ttu-id="70185-113">In der folgenden Abbildung wird gezeigt, wie sich die Drehung mit dem gleichen Winkel an einem anderen Mittelpunkt dreht.</span><span class="sxs-lookup"><span data-stu-id="70185-113">The following illustration shows the effect of rotating by the same angle about a different center point.</span></span> <span data-ttu-id="70185-114">Beachten Sie, dass sich die gedrehten Objekte in Relation zum ursprünglichen an verschiedenen Positionen befinden.</span><span class="sxs-lookup"><span data-stu-id="70185-114">Notice that the rotated objects are in different positions relative to the original.</span></span> <span data-ttu-id="70185-115">Das linke eckige Quadrat ist das Ergebnis der Drehung über den Mittelpunkt des ursprünglichen Quadrats, und das Recht Umriss Quadrat ist das Ergebnis der Rotation der oberen linken Ecke des ursprünglichen Quadrats.</span><span class="sxs-lookup"><span data-stu-id="70185-115">The left outlined square is the result of rotating about the center of the original square, and the right outlined square is the result of rotating about the upper-left corner of the original square.</span></span>

![Abbildung eines Quadrats um 45 Grad im Uhrzeigersinn um einen anderen Mittelpunkt gedreht](images/translate-rotationcompare.png)

## <a name="related-topics"></a><span data-ttu-id="70185-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70185-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70185-118">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="70185-118">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="70185-119">Übersicht über Direct2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="70185-119">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 