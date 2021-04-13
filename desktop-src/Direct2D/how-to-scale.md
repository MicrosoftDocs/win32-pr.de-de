---
title: Skalieren eines Objekts
description: Zeigt, wie ein Objekt skaliert wird.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473829"
---
# <a name="how-to-scale-an-object"></a><span data-ttu-id="6c9c1-103">Skalieren eines Objekts</span><span class="sxs-lookup"><span data-stu-id="6c9c1-103">How to Scale an Object</span></span>

<span data-ttu-id="6c9c1-104">In diesem Thema wird beschrieben, wie ein Objekt mithilfe der [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-104">This topic describes how to scale an object by using the [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="6c9c1-105">Das Skalieren eines Objekts bedeutet, dass das Objekt größer oder kleiner wird.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-105">To scale an object means to make the object larger or smaller.</span></span> <span data-ttu-id="6c9c1-106">Sie können eine der beiden folgenden Methoden zum Skalieren eines Objekts aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-106">You can call one of the following two methods to scale an object.</span></span>

-   <span data-ttu-id="6c9c1-107">**Matrix3x2F:: Scale (D2D1 \_ size \_ F scalefactor, D2D1 \_ Point \_ 2F Centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="6c9c1-107">**Matrix3x2F::Scale(D2D1\_SIZE\_F scalefactor, D2D1\_POINT\_2F centerpoint)**</span></span>
-   <span data-ttu-id="6c9c1-108">**Matrix3x2F:: Scale (float ScaleX, float ScaleY, D2D1 \_ Point \_ 2F Centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="6c9c1-108">**Matrix3x2F::Scale(float scalex, float scaley, D2D1\_POINT\_2F centerpoint)**</span></span>

<span data-ttu-id="6c9c1-109">Die erste Methode speichert *ScaleX* und *ScaleY* als geordnetes Paar von Gleit Komma Werten in der [**D2D1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-109">The first method stores *scalex* and *scaley* as an ordered pair of floating-point values in the [**D2D1\_SIZE\_F**](/windows/desktop/Direct2D/d2d1-size-f) structure.</span></span> <span data-ttu-id="6c9c1-110">Mit der zweiten Methode werden *ScaleX* und *ScaleY* als einzelne Parameter definiert.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-110">The second method defines *scalex* and *scaley* as individual parameters.</span></span>

<span data-ttu-id="6c9c1-111">Unabhängig davon, welche Methode Sie verwenden, müssen Sie sowohl *ScaleX* -als auch *ScaleY* -Faktoren angeben.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-111">Regardless of which method that you use, you must specify both *scalex* and *scaley* factors.</span></span> <span data-ttu-id="6c9c1-112">Der *ScaleX* -Wert ist der Skalierungsfaktor in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-112">The *scalex* value is the scale factor in the x direction.</span></span> <span data-ttu-id="6c9c1-113">Beispielsweise wird das Objekt von einem *ScaleX* -Wert von 1,5 auf 150 Prozent entlang der x-Achse gestreckt.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-113">For example, a *scalex* value of 1.5 stretches the object to 150 percent along the x-axis.</span></span> <span data-ttu-id="6c9c1-114">Ebenso ist der *Skalarwert der Skalierungs* Faktor in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-114">Similarly, the *scaley* value is the scale factor in the y direction.</span></span> <span data-ttu-id="6c9c1-115">Beispielsweise verkleinert ein *ScaleY* -Wert von 0,5 die Höhe des Objekts um 50 Prozent entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-115">For example, a *scaley* value of 0.5 shrinks the height of the object by 50 percent along the y-axis.</span></span>

<span data-ttu-id="6c9c1-116">Um einen Punkt als Mittelpunkt des Skalierungs Vorgangs anzugeben, verwenden Sie den *CenterPoint* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-116">To specify a point as the center of the scaling operation, use the *centerpoint* parameter.</span></span> <span data-ttu-id="6c9c1-117">Standardmäßig wird ein Objekt über den Ursprung (0, 0) zentriert.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-117">By default, an object is centered about its origin (0,0).</span></span>

<span data-ttu-id="6c9c1-118">Im folgenden Beispielcode wird eine Skalierungs Transformation erstellt, um die Größe eines Quadrats auf 130% seiner ursprünglichen Größe zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-118">The following example code creates a scale transformation to increase the size of a square to 130% of its original size.</span></span> <span data-ttu-id="6c9c1-119">Der Mittel *Punkt* wird auf die obere linke Ecke des ursprünglichen Quadrats festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-119">The *centerpoint* is set to be the upper-left corner of the original square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="6c9c1-120">Die folgende Abbildung zeigt die Auswirkung der Anwendung der Skalierungs Transformation auf das Quadrat.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-120">The following illustration shows the effect of applying the scale transformation to the square.</span></span> <span data-ttu-id="6c9c1-121">Das ursprüngliche Quadrat ist eine gepunktete Gliederung, und das skalierte Quadrat ist ein voll solider Umriss.</span><span class="sxs-lookup"><span data-stu-id="6c9c1-121">The original square is a dotted outline and the scaled square is a solid outline.</span></span>

![Abbildung der Quadrat Größe, die auf 130% der ursprünglichen Größe angepasst wurde](images/scale-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="6c9c1-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6c9c1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c9c1-124">Übersicht über Direct2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="6c9c1-124">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="6c9c1-125">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="6c9c1-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 