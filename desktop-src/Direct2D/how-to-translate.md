---
title: Übersetzen eines Objekts
description: Zeigt, wie ein-Objekt übersetzt wird.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316088"
---
# <a name="how-to-translate-an-object"></a><span data-ttu-id="7b9cb-103">Übersetzen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="7b9cb-103">How to Translate an Object</span></span>

<span data-ttu-id="7b9cb-104">Wenn Sie ein 2D-Objekt übersetzen möchten, verschieben Sie das Objekt auf die x-Achse, die y-Achse oder beides.</span><span class="sxs-lookup"><span data-stu-id="7b9cb-104">To translate a 2-D object is to move the object along the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="7b9cb-105">Sie können eine der beiden folgenden Methoden zum Erstellen einer Übersetzungs Transformation aufruft.</span><span class="sxs-lookup"><span data-stu-id="7b9cb-105">You can call either one of the following two methods to create a translation transformation.</span></span>

-   <span data-ttu-id="7b9cb-106">[**Translation (D2D1 \_ size \_ F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): nimmt ein geordnetes Paar an, das den Abstand auf der x-Achse und der y-Achse definiert.</span><span class="sxs-lookup"><span data-stu-id="7b9cb-106">[**Translation(D2D1\_SIZE\_F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): takes an ordered pair that defines the distance to translate along the x-axis and the y-axis.</span></span>
-   <span data-ttu-id="7b9cb-107">[**Übersetzung (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): übernimmt den Abstand, der entlang der x-Achse übersetzt werden soll, und die Distanz, die auf der y-Achse übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b9cb-107">[**Translation(float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): takes the distance to translate along the x-axis and the distance to translate along the y-axis.</span></span>

<span data-ttu-id="7b9cb-108">Der folgende Code erstellt eine Transformationsmatrix für die Konvertierung, die die Quadrat 20 Einheiten entlang der x-Achse nach rechts und 10 Einheiten entlang der y-Achse nach unten verschiebt.</span><span class="sxs-lookup"><span data-stu-id="7b9cb-108">The following code creates a translation transformation matrix that moves the square 20 units to the right along the x-axis and 10 units downward along the y-axis.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="7b9cb-109">In der folgenden Abbildung werden die Auswirkungen der Anwendung der Translation-Transformation auf das Quadrat dargestellt, wobei das ursprüngliche Quadrat ein gepunkteter Umriss und das übersetzte Quadrat ein voll Bild Umriss ist.</span><span class="sxs-lookup"><span data-stu-id="7b9cb-109">The following illustration shows the effect of applying the translation transformation to the square, where the original square is a dotted outline and the translated square is a solid outline.</span></span>

![Abbildung eines Quadrats mit 20 Einheiten nach rechts entlang der x-Achse und 10 Einheiten entlang der y-Achse](images/translation-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="7b9cb-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b9cb-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b9cb-112">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="7b9cb-112">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="7b9cb-113">Übersicht über Direct2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="7b9cb-113">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 