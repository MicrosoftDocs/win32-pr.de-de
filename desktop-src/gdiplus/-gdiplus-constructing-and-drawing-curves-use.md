---
description: 'GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Arcs, kardinale Splines und B&\# 233; Zier-Splines.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Erstellen und Zeichnen von Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994310"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="62701-103">Erstellen und Zeichnen von Kurven</span><span class="sxs-lookup"><span data-stu-id="62701-103">Constructing and Drawing Curves</span></span>

<span data-ttu-id="62701-104">GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Arcs, kardinale Splines und Bézier-Splines.</span><span class="sxs-lookup"><span data-stu-id="62701-104">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="62701-105">Eine Ellipse wird durch das umgebende Rechteck definiert. ein Bogen ist ein Teil einer Ellipse, die durch einen Anfangs Winkel und einen Pfeil Winkel definiert wird.</span><span class="sxs-lookup"><span data-stu-id="62701-105">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="62701-106">Ein kardinalspline wird durch ein Array von Punkten und einen Spannungs Parameter definiert – die Kurve verläuft nahtlos durch jeden Punkt im Array, und der Tension-Parameter wirkt sich auf die Art und Weise der Kurve aus.</span><span class="sxs-lookup"><span data-stu-id="62701-106">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="62701-107">Eine Bézier-Spline wird von zwei Endpunkten und zwei Kontrollpunkten definiert – die Kurve übergibt nicht die Steuerungs Punkte, aber die Steuerungs Punkte beeinflussen die Richtung und die Kurve, wenn die Kurve von einem Endpunkt zum anderen wechselt.</span><span class="sxs-lookup"><span data-stu-id="62701-107">A Bézier spline is defined by two end points and two control points — the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one end point to the other.</span></span>

<span data-ttu-id="62701-108">In den folgenden Themen werden die wichtigsten Splines und die Bézier-Splines ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="62701-108">The following topics cover cardinal splines and Bézier splines in more detail:</span></span>

-   [<span data-ttu-id="62701-109">Zeichnen von kardinalen Splines</span><span class="sxs-lookup"><span data-stu-id="62701-109">Drawing Cardinal Splines</span></span>](-gdiplus-drawing-cardinal-splines-use.md)
-   [<span data-ttu-id="62701-110">Zeichnen von Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="62701-110">Drawing Bézier Splines</span></span>](-gdiplus-drawing-bezier-splines-use.md)

 

 



