---
description: Eine Ellipse wird durch das umgebende Rechteck angegeben. In der folgenden Abbildung wird eine Ellipse zusammen mit dem umgebenden Rechteck gezeigt.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Ellipsen und Bögen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131345"
---
# <a name="ellipses-and-arcs"></a><span data-ttu-id="e5b81-104">Ellipsen und Bögen</span><span class="sxs-lookup"><span data-stu-id="e5b81-104">Ellipses and Arcs</span></span>

<span data-ttu-id="e5b81-105">Eine Ellipse wird durch das umgebende Rechteck angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5b81-105">An ellipse is specified by its bounding rectangle.</span></span> <span data-ttu-id="e5b81-106">In der folgenden Abbildung wird eine Ellipse zusammen mit dem umgebenden Rechteck gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5b81-106">The following illustration shows an ellipse along with its bounding rectangle.</span></span>

![Abbildung einer Ellipse in einem umschließenden Rechteck](images/aboutgdip02-art05.png)

<span data-ttu-id="e5b81-108">Zum Zeichnen einer Ellipse benötigen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="e5b81-108">To draw an ellipse, you need a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e5b81-109">Das **Grafik** Objekt stellt die [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) -Methode bereit, und das **Pen** -Objekt speichert Attribute der Ellipse, z. b. Linienstärke und Farbe.</span><span class="sxs-lookup"><span data-stu-id="e5b81-109">The **Graphics** object provides the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, and the **Pen** object stores attributes of the ellipse, such as line width and color.</span></span> <span data-ttu-id="e5b81-110">Die Adresse des **Stift** Objekts wird als eines der Argumente an die DrawEllipse-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e5b81-110">The address of the **Pen** object is passed as one of the arguments to the DrawEllipse method.</span></span> <span data-ttu-id="e5b81-111">Die übrigen Argumente, die an die DrawEllipse-Methode übergeben werden, geben das Begrenzungs Rechteck für die Ellipse an.</span><span class="sxs-lookup"><span data-stu-id="e5b81-111">The remaining arguments passed to the DrawEllipse method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="e5b81-112">Im folgenden Beispiel wird eine Ellipse gezeichnet. das umgebende Rechteck hat eine Breite von 160, eine Höhe von 80 und eine linke obere Ecke von (100, 50).</span><span class="sxs-lookup"><span data-stu-id="e5b81-112">The following example draws an ellipse; the bounding rectangle has a width of 160, a height of 80, and an upper-left corner of (100, 50).</span></span>


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



<span data-ttu-id="e5b81-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) ist eine überladene Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse, sodass Sie Sie mit Argumenten bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="e5b81-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) is an overloaded method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="e5b81-114">Beispielsweise können Sie ein [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt erstellen und einen Verweis auf das **Rect** -Objekt als Argument der DrawEllipse-Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="e5b81-114">For example, you can construct a [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawEllipse method.</span></span>


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



<span data-ttu-id="e5b81-115">Ein Bogen ist ein Teil einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="e5b81-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="e5b81-116">Zum Zeichnen eines Bogens wird die [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e5b81-116">To draw an arc, you call the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="e5b81-117">Die Parameter der DrawArc-Methode sind identisch mit den Parametern der [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) -Methode, mit dem Unterschied, dass DrawArc einen Anfangs Winkel und einen Pfeil Winkel erfordert.</span><span class="sxs-lookup"><span data-stu-id="e5b81-117">The parameters of the DrawArc method are the same as the parameters of the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, except that DrawArc requires a starting angle and sweep angle.</span></span> <span data-ttu-id="e5b81-118">Im folgenden Beispiel wird ein Bogen mit einem Anfangs Winkel von 30 Grad und einem Mittelpunktswinkel von 180 Grad gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e5b81-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees.</span></span>


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



<span data-ttu-id="e5b81-119">Die folgende Abbildung zeigt den Bogen, die Ellipse und das umgebende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="e5b81-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>

![Abbildung einer Ellipse in einem umgebenden Rechteck die untere linke Hälfte der Ellipse wird rot gezeichnet.](images/aboutgdip02-art06.png)

 

 



