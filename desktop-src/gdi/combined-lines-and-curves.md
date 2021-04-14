---
description: Zusätzlich zum Zeichnen von Linien oder Kurven können Anwendungen Kombinationen aus Zeilen-und Kurven Ausgabe zeichnen, indem Sie eine einzelne Funktion aufrufen. Beispielsweise kann eine Anwendung die Gliederung eines Kreis Diagramms zeichnen, indem die anglearc-Funktion aufgerufen wird.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Kombinierte Linien und Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978736"
---
# <a name="combined-lines-and-curves"></a><span data-ttu-id="d3fb0-104">Kombinierte Linien und Kurven</span><span class="sxs-lookup"><span data-stu-id="d3fb0-104">Combined Lines and Curves</span></span>

<span data-ttu-id="d3fb0-105">Zusätzlich zum Zeichnen von Linien oder Kurven können Anwendungen Kombinationen aus Zeilen-und Kurven Ausgabe zeichnen, indem Sie eine einzelne Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d3fb0-105">In addition to drawing lines or curves, applications can draw combinations of line and curve output by calling a single function.</span></span> <span data-ttu-id="d3fb0-106">Beispielsweise kann eine Anwendung die Gliederung eines Kreis Diagramms zeichnen, indem die [**anglearc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d3fb0-106">For example, an application can draw the outline of a pie chart by calling the [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function.</span></span>

<span data-ttu-id="d3fb0-107">Die [**anglearc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) -Funktion zeichnet einen Bogen entlang des Umkreis Bereichs eines Kreises und zeichnet eine Linie, die den Anfangspunkt des Bogens mit der Mitte des Kreises verbindet.</span><span class="sxs-lookup"><span data-stu-id="d3fb0-107">The [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function draws an arc along a circle's perimeter and draws a line connecting the starting point of the arc to the circle's center.</span></span> <span data-ttu-id="d3fb0-108">Zusätzlich zur Verwendung der **anglearc** -Funktion kann eine Anwendung auch die Zeilen-und unregelmäßige Kurven Ausgabe mithilfe der [**polydraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) -Funktion kombinieren.</span><span class="sxs-lookup"><span data-stu-id="d3fb0-108">In addition to using the **AngleArc** function, an application can also combine line and irregular curve output by using the [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) function.</span></span>

 

 



