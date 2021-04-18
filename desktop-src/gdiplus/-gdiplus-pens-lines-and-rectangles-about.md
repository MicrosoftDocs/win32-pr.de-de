---
description: Zum Zeichnen von Linien mit Windows GDI+ müssen Sie ein Grafik Objekt und ein Pen-Objekt erstellen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Stifte, Linien und Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978960"
---
# <a name="pens-lines-and-rectangles"></a><span data-ttu-id="52d4f-103">Stifte, Linien und Rechtecke</span><span class="sxs-lookup"><span data-stu-id="52d4f-103">Pens, Lines, and Rectangles</span></span>

<span data-ttu-id="52d4f-104">Zum Zeichnen von Linien mit Windows GDI+ müssen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="52d4f-104">To draw lines with Windows GDI+ you need to create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="52d4f-105">Das **Grafik** Objekt stellt die Methoden bereit, die die Zeichnung tatsächlich durchführen, und das **Stift** -Objekt speichert Attribute der Zeile, z. b. Farbe, Breite und Stil.</span><span class="sxs-lookup"><span data-stu-id="52d4f-105">The **Graphics** object provides the methods that actually do the drawing, and the **Pen** object stores attributes of the line, such as color, width, and style.</span></span> <span data-ttu-id="52d4f-106">Das Zeichnen einer Linie ist einfach eine Frage des Aufrufs der [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode des **Grafik** Objekts.</span><span class="sxs-lookup"><span data-stu-id="52d4f-106">Drawing a line is simply a matter of calling the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object.</span></span> <span data-ttu-id="52d4f-107">Die Adresse des **Stift** Objekts wird als eines der Argumente an die DrawLine-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="52d4f-107">The address of the **Pen** object is passed as one of the arguments to the DrawLine method.</span></span> <span data-ttu-id="52d4f-108">Im folgenden Beispiel wird eine Linie vom Punkt (4, 2) bis zum Punkt (12, 6) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="52d4f-108">The following example draws a line from the point (4, 2) to the point (12, 6).</span></span>


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



<span data-ttu-id="52d4f-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) ist eine überladene Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse, sodass Sie Sie mit Argumenten bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="52d4f-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="52d4f-110">Beispielsweise können Sie zwei [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) -Objekte erstellen und Verweise auf die **Point** -Objekte als Argumente an die DrawLine-Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="52d4f-110">For example, you can construct two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects and pass references to the **Point** objects as arguments to the DrawLine method.</span></span>


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



<span data-ttu-id="52d4f-111">Sie können bestimmte Attribute angeben, wenn Sie ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="52d4f-111">You can specify certain attributes when you construct a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="52d4f-112">Beispielsweise können Sie mit einem [Stift](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) -Konstruktor Farbe und Breite angeben.</span><span class="sxs-lookup"><span data-stu-id="52d4f-112">For example, one [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) constructor allows you to specify color and width.</span></span> <span data-ttu-id="52d4f-113">Im folgenden Beispiel wird eine blaue Linie der Breite 2 von (0,0) bis (60, 30) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="52d4f-113">The following example draws a blue line of width 2 from (0, 0) to (60, 30).</span></span>


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



<span data-ttu-id="52d4f-114">Das [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt verfügt auch über Attribute, wie z. b. den Dash-Stil, mit denen Sie Features der Linie angeben können.</span><span class="sxs-lookup"><span data-stu-id="52d4f-114">The [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object also has attributes, such as dash style, that you can use to specify features of the line.</span></span> <span data-ttu-id="52d4f-115">Im folgenden Beispiel wird z. b. eine gestrichelte Linie von (100, 50) zu (300, 80) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="52d4f-115">For example, the following example draws a dashed line from (100, 50) to (300, 80).</span></span>


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



<span data-ttu-id="52d4f-116">Sie können verschiedene Methoden des [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekts verwenden, um viele weitere Attribute der Zeile festzulegen.</span><span class="sxs-lookup"><span data-stu-id="52d4f-116">You can use various methods of the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to set many more attributes of the line.</span></span> <span data-ttu-id="52d4f-117">Die [**Pen:: setstartcap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) -Methode und die [**Pen:: setendcap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) -Methode geben die Darstellung der Zeilenenden an. die enden können flach, quadratisch, gerundet, dreieckig oder eine benutzerdefinierte Form sein.</span><span class="sxs-lookup"><span data-stu-id="52d4f-117">The [**Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) and [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) methods specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="52d4f-118">Mit der Methode [**Pen:: setlinejoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) können Sie angeben, ob verbundene Linien gezippt (mit spitzen Ecken verknüpft), geglättet, gerundet oder abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="52d4f-118">The [**Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="52d4f-119">In der folgenden Abbildung werden Zeilen mit verschiedenen Obergrenzen und joinstilen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="52d4f-119">The following illustration shows lines with various cap and join styles.</span></span>

![Abbildung von zwei Zeilen, die gerundete und zirkuläre enden, gerundete und unterteilte Ecken und zwei Pfeil Stile demonstrieren](images/aboutgdip02-art04.png)

<span data-ttu-id="52d4f-121">Zeichnungs Rechtecke mit GDI+ ähneln Zeichnungslinien.</span><span class="sxs-lookup"><span data-stu-id="52d4f-121">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="52d4f-122">Zum Zeichnen eines Rechtecks benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="52d4f-122">To draw a rectangle, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="52d4f-123">Das **Grafik** Objekt stellt eine [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt speichert Attribute, z. b. Linienstärke und Farbe.</span><span class="sxs-lookup"><span data-stu-id="52d4f-123">The **Graphics** object provides a [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores attributes, such as line width and color.</span></span> <span data-ttu-id="52d4f-124">Die Adresse des **Stift** Objekts wird als eines der Argumente an die drawrechteck-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="52d4f-124">The address of the **Pen** object is passed as one of the arguments to the DrawRectangle method.</span></span> <span data-ttu-id="52d4f-125">Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (100, 50), einer Breite von 80 und einer Höhe von 40 gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="52d4f-125">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40.</span></span>


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



<span data-ttu-id="52d4f-126">[Drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) ist eine überladene Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52d4f-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="52d4f-127">Beispielsweise können Sie ein [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt erstellen und einen Verweis auf das **Rect** -Objekt als Argument an die drawrechteck-Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="52d4f-127">For example, you can construct a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawRectangle method.</span></span>


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



<span data-ttu-id="52d4f-128">Ein [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt verfügt über Methoden zum Bearbeiten und Sammeln von Informationen über das Rechteck.</span><span class="sxs-lookup"><span data-stu-id="52d4f-128">A [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object has methods for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="52d4f-129">Beispielsweise ändern die Methoden zum [aufblasen](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) und [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) die Größe und Position des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="52d4f-129">For example, the [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) and [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) methods change the size and position of the rectangle.</span></span> <span data-ttu-id="52d4f-130">Die [**Rect:: IntersectWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) -Methode gibt Aufschluss darüber, ob das Rechteck ein anderes angegebenes Rechteck überschneidet, und die [enthält](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) -Methode gibt an, ob sich ein bestimmter Punkt innerhalb des Rechtecks befindet.</span><span class="sxs-lookup"><span data-stu-id="52d4f-130">The [**Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) method tells you whether the rectangle intersects another given rectangle, and the [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) method tells you whether a given point is inside the rectangle.</span></span>

 

 
