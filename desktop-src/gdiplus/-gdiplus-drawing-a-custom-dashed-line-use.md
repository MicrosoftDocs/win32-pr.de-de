---
description: Windows GDI+ bietet mehrere Dash-Stile, die in der Enumeration des Dashboards aufgelistet sind. Wenn diese standardmäßigen Dash-Stile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrich Muster erstellen.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Zeichnen einer benutzerdefinierten gestrichelten Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988035"
---
# <a name="drawing-a-custom-dashed-line"></a><span data-ttu-id="477eb-104">Zeichnen einer benutzerdefinierten gestrichelten Linie</span><span class="sxs-lookup"><span data-stu-id="477eb-104">Drawing a Custom Dashed Line</span></span>

<span data-ttu-id="477eb-105">Windows GDI+ bietet mehrere Dash-Stile, die in der Enumeration des [**Dashboards**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="477eb-105">Windows GDI+ provides several dash styles that are listed in the [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) enumeration.</span></span> <span data-ttu-id="477eb-106">Wenn diese standardmäßigen Dash-Stile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrich Muster erstellen.</span><span class="sxs-lookup"><span data-stu-id="477eb-106">If those standard dash styles don't suit your needs, you can create a custom dash pattern.</span></span>

<span data-ttu-id="477eb-107">Fügen Sie zum Zeichnen einer benutzerdefinierten gestrichelten Linie die Längen der Bindestriche und Leerzeichen in ein Array ein, und übergeben Sie die Adresse des Arrays als Argument an die Methode [**Pen:: setdashpattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) eines [**Stift**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Objekts.</span><span class="sxs-lookup"><span data-stu-id="477eb-107">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and pass the address of the array as an argument to the [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) method of a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="477eb-108">Im folgenden Beispiel wird eine benutzerdefinierte gestrichelte Linie basierend auf dem Array {5, 2, 15, 4} gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="477eb-108">The following example draws a custom dashed line based on the array {5, 2, 15, 4}.</span></span> <span data-ttu-id="477eb-109">Wenn Sie die Elemente des Arrays mit der Stift Breite 5 multiplizieren, erhalten Sie {25, 10, 75, 20}.</span><span class="sxs-lookup"><span data-stu-id="477eb-109">If you multiply the elements of the array by the pen width of 5, you get {25, 10, 75, 20}.</span></span> <span data-ttu-id="477eb-110">Die angezeigten Bindestriche wechseln in eine Länge zwischen 25 und 75 und die Leerzeichen sind in der Länge zwischen 10 und 20.</span><span class="sxs-lookup"><span data-stu-id="477eb-110">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



<span data-ttu-id="477eb-111">In der folgenden Abbildung ist die resultierende gestrichelte Linie dargestellt.</span><span class="sxs-lookup"><span data-stu-id="477eb-111">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="477eb-112">Beachten Sie, dass der abschließende Bindestrich kürzer als 25 Einheiten sein muss, damit die Zeile auf (405, 5) enden kann.</span><span class="sxs-lookup"><span data-stu-id="477eb-112">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>

![Abbildung mit einer gestrichelten Linie jedes Segment ist eine kurze Zeile gefolgt von einem langen.](images/pens6.png)

 

 



