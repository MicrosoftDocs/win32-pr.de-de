---
description: Ein einzelnes Matrix Objekt kann eine einzelne Transformation oder eine Sequenz von Transformationen speichern.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Bedeutung der Transformationsreihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977528"
---
# <a name="why-transformation-order-is-significant"></a><span data-ttu-id="91868-103">Bedeutung der Transformationsreihenfolge</span><span class="sxs-lookup"><span data-stu-id="91868-103">Why Transformation Order Is Significant</span></span>

<span data-ttu-id="91868-104">Ein einzelnes [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt kann eine einzelne Transformation oder eine Sequenz von Transformationen speichern.</span><span class="sxs-lookup"><span data-stu-id="91868-104">A single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object can store a single transformation or a sequence of transformations.</span></span> <span data-ttu-id="91868-105">Letzteres wird als zusammen *gesetzte*  *Transformation* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="91868-105">The latter is called a *composite*  *transformation*.</span></span> <span data-ttu-id="91868-106">Die Matrix einer zusammengesetzten Transformation wird durch Multiplikation der Matrizen der einzelnen Transformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="91868-106">The matrix of a composite transformation is obtained by multiplying the matrices of the individual transformations.</span></span>

<span data-ttu-id="91868-107">In einer zusammengesetzten Transformation ist die Reihenfolge der einzelnen Transformationen wichtig.</span><span class="sxs-lookup"><span data-stu-id="91868-107">In a composite transformation, the order of the individual transformations is important.</span></span> <span data-ttu-id="91868-108">Wenn Sie z. b. zuerst drehen, dann skalieren und dann übersetzen, erhalten Sie ein anderes Ergebnis als bei der ersten Übersetzung, dann drehen und skalieren.</span><span class="sxs-lookup"><span data-stu-id="91868-108">For example, if you first rotate, then scale, then translate, you get a different result than if you first translate, then rotate, then scale.</span></span> <span data-ttu-id="91868-109">In Windows GDI+ werden zusammengesetzte Transformationen von links nach rechts erstellt.</span><span class="sxs-lookup"><span data-stu-id="91868-109">In Windows GDI+, composite transformations are built from left to right.</span></span> <span data-ttu-id="91868-110">Wenn es sich bei S, R und T um Skalierungs-, Rotations-und Übersetzungs Matrizen handelt, ist das Produkt SRT (in dieser Reihenfolge) die Matrix der zusammengesetzten Transformation, die zuerst skaliert, dann rotiert und dann übersetzt.</span><span class="sxs-lookup"><span data-stu-id="91868-110">If S, R, and T are scale, rotation, and translation matrices respectively, then the product SRT (in that order) is the matrix of the composite transformation that first scales, then rotates, then translates.</span></span> <span data-ttu-id="91868-111">Die vom Produkt SRT erzeugte Matrix unterscheidet sich von der Matrix, die vom Produkt TRS erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="91868-111">The matrix produced by the product SRT is different from the matrix produced by the product TRS.</span></span>

<span data-ttu-id="91868-112">Eine Grundordnung ist wichtig, wenn Transformationen wie Drehung und Skalierung in Bezug auf den Ursprung des Koordinatensystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="91868-112">One reason order is significant is that transformations like rotation and scaling are done with respect to the origin of the coordinate system.</span></span> <span data-ttu-id="91868-113">Das Skalieren eines Objekts, das am Ursprung zentriert ist, erzeugt ein anderes Ergebnis als das Skalieren eines Objekts, das vom Ursprung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="91868-113">Scaling an object that is centered at the origin produces a different result than scaling an object that has been moved away from the origin.</span></span> <span data-ttu-id="91868-114">Entsprechend erzeugt das Drehen eines Objekts, das am Ursprung zentriert ist, ein anderes Ergebnis als das Drehen eines Objekts, das vom Ursprung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="91868-114">Similarly, rotating an object that is centered at the origin produces a different result than rotating an object that has been moved away from the origin.</span></span>

<span data-ttu-id="91868-115">Im folgenden Beispiel werden die Skalierung, Drehung und Übersetzung (in dieser Reihenfolge) kombiniert, um eine zusammengesetzte Transformation zu bilden.</span><span class="sxs-lookup"><span data-stu-id="91868-115">The following example combines scaling, rotation and translation (in that order) to form a composite transformation.</span></span> <span data-ttu-id="91868-116">Das Argument [\* \* \* matrixorderappend \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) , das an die [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) -Methode übermittelt wird, gibt an, dass die Drehung der Skalierung folgt.</span><span class="sxs-lookup"><span data-stu-id="91868-116">The argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) method specifies that the rotation will follow the scaling.</span></span> <span data-ttu-id="91868-117">Ebenso gibt das Argument [\* \* \* matrixorderappend \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) , das an die [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) -Methode übergebenen wird, an, dass die Übersetzung der Drehung folgt.</span><span class="sxs-lookup"><span data-stu-id="91868-117">Likewise, the argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method specifies that the translation will follow the rotation.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="91868-118">Im folgenden Beispiel wird dieselbe Methode wie im vorherigen Beispiel aufgerufen, aber die Reihenfolge der Aufrufe wird umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="91868-118">The following example makes the same method calls as the previous example, but the order of the calls is reversed.</span></span> <span data-ttu-id="91868-119">Die sich ergebende Reihenfolge der Vorgänge erfolgt zunächst übersetzen, dann drehen, dann skalieren, was zu einem sehr anderen Ergebnis als der ersten Skalierung, zum anschließenden drehen und zum Übersetzen führt:</span><span class="sxs-lookup"><span data-stu-id="91868-119">The resulting order of operations is first translate, then rotate, then scale, which produces a very different result than first scale, then rotate, then translate:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="91868-120">Eine Möglichkeit, die Reihenfolge der einzelnen Transformationen in einer zusammengesetzten Transformation umzukehren, besteht darin, die Reihenfolge einer Sequenz von Methoden aufrufen umzukehren.</span><span class="sxs-lookup"><span data-stu-id="91868-120">One way to reverse the order of the individual transformations in a composite transformation is to reverse the order of a sequence of method calls.</span></span> <span data-ttu-id="91868-121">Eine zweite Möglichkeit, die Reihenfolge der Vorgänge zu steuern, besteht darin, das Matrix Reihen folgen Argument zu ändern.</span><span class="sxs-lookup"><span data-stu-id="91868-121">A second way to control the order of operations is to change the matrix order argument.</span></span> <span data-ttu-id="91868-122">Das folgende Beispiel ist mit dem vorherigen Beispiel identisch, mit der Ausnahme, dass [\* \* \* \* matrixorderappend \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) in [\* \* \* \* matrixorderprepend \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)\* geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="91868-122">The following example is the same as the previous example, except that [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) has been changed to [\*\*\*\*MatrixOrderPrepend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder).</span></span> <span data-ttu-id="91868-123">Die Matrix Multiplikation erfolgt in der Reihenfolge SRT, in der "S", "R" und "T" die Matrizen für "Scale", "Rotation" und "Translation" sind.</span><span class="sxs-lookup"><span data-stu-id="91868-123">The matrix multiplication is done in the order SRT, where S, R, and T are the matrices for scale, rotate, and translate, respectively.</span></span> <span data-ttu-id="91868-124">Die Reihenfolge der zusammengesetzten Transformation ist die erste Skalierung, dann drehen und dann übersetzen.</span><span class="sxs-lookup"><span data-stu-id="91868-124">The order of the composite transformation is first scale, then rotate, then translate.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="91868-125">Das Ergebnis des vorhergehenden Beispiels ist das gleiche Ergebnis, das wir im ersten Beispiel dieses Abschnitts erzielt haben.</span><span class="sxs-lookup"><span data-stu-id="91868-125">The result of the preceding example is the same result that we achieved in the first example of this section.</span></span> <span data-ttu-id="91868-126">Dies liegt daran, dass wir sowohl die Reihenfolge der Methodenaufrufe als auch die Reihenfolge der Matrix Multiplikation rückgängig gemacht haben.</span><span class="sxs-lookup"><span data-stu-id="91868-126">This is because we reversed both the order of the method calls and the order of the matrix multiplication.</span></span>

 

 



