---
description: Zum Erstellen eines Pfads und auswählen des Pfads in einen Domänen Controller müssen Sie zuerst die Punkte definieren, die ihn beschreiben.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Pfad Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215184"
---
# <a name="path-creation"></a><span data-ttu-id="e9ff8-103">Pfad Erstellung</span><span class="sxs-lookup"><span data-stu-id="e9ff8-103">Path Creation</span></span>

<span data-ttu-id="e9ff8-104">Zum Erstellen eines Pfads und auswählen des Pfads in einen Domänen Controller müssen Sie zuerst die Punkte definieren, die ihn beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-104">To create a path and select it into a DC, it is first necessary to define the points that describe it.</span></span> <span data-ttu-id="e9ff8-105">Dies erfolgt durch Aufrufen der [**beginpath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) -Funktion unter Angabe der entsprechenden Zeichnungsfunktionen und durch Aufrufen der [**endpath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-105">This is done by calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function, specifying the appropriate drawing functions, and then by calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="e9ff8-106">Diese Kombination von Funktionen (**beginpath**, Zeichnungsfunktionen und **endpath**) bilden eine *Pfad Klammer*.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-106">This combination of functions (**BeginPath**, drawing functions, and **EndPath**) constitute a *path bracket*.</span></span> <span data-ttu-id="e9ff8-107">Im folgenden finden Sie eine Liste der Zeichnungsfunktionen, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-107">The following is the list of drawing functions that can be used.</span></span>

-   [<span data-ttu-id="e9ff8-108">**Anglearc**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-108">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [<span data-ttu-id="e9ff8-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [<span data-ttu-id="e9ff8-110">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-110">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [<span data-ttu-id="e9ff8-111">**Chord**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-111">**Chord**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [<span data-ttu-id="e9ff8-112">**CloseFigure**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-112">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [<span data-ttu-id="e9ff8-113">**Ellipse**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-113">**Ellipse**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [<span data-ttu-id="e9ff8-114">**Exttextout**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-114">**ExtTextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="e9ff8-115">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-115">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [<span data-ttu-id="e9ff8-116">**"Muvezu Ex"**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-116">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [<span data-ttu-id="e9ff8-117">**Kreis**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-117">**Pie**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [<span data-ttu-id="e9ff8-118">**Polybezier**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-118">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [<span data-ttu-id="e9ff8-119">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-119">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [<span data-ttu-id="e9ff8-120">**Polydraw**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-120">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [<span data-ttu-id="e9ff8-121">**Polygon**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-121">**Polygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [<span data-ttu-id="e9ff8-122">**Polylinie**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-122">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [<span data-ttu-id="e9ff8-123">**PolyLineTo**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-123">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [<span data-ttu-id="e9ff8-124">**Polypolygon**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-124">**PolyPolygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [<span data-ttu-id="e9ff8-125">**Polypolyline**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-125">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [<span data-ttu-id="e9ff8-126">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-126">**Rectangle**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [<span data-ttu-id="e9ff8-127">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-127">**RoundRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [<span data-ttu-id="e9ff8-128">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="e9ff8-128">**TextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="e9ff8-129">Wenn eine Anwendung [**endpath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)aufruft, wählt das System den zugeordneten Pfad in den angegebenen Domänen Controller aus.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-129">When an application calls [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), the system selects the associated path into the specified DC.</span></span> <span data-ttu-id="e9ff8-130">(Wenn zuvor ein anderer Pfad in den Domänen Controller ausgewählt wurde, löscht das System diesen Pfad, ohne ihn zu speichern.) Nachdem das System den Pfad zum Domänen Controller ausgewählt hat, kann eine Anwendung auf eine der folgenden Arten mit dem Pfad arbeiten:</span><span class="sxs-lookup"><span data-stu-id="e9ff8-130">(If another path had previously been selected into the DC, the system deletes that path without saving it.) After the system selects the path into the DC, an application can operate on the path in one of the following ways:</span></span>

-   <span data-ttu-id="e9ff8-131">Zeichnen Sie den Umriss des Pfads (mit dem aktuellen Stift).</span><span class="sxs-lookup"><span data-stu-id="e9ff8-131">Draw the outline of the path (using the current pen).</span></span>
-   <span data-ttu-id="e9ff8-132">Zeichnen Sie das Innere des Pfads (mit dem aktuellen Pinsel).</span><span class="sxs-lookup"><span data-stu-id="e9ff8-132">Paint the interior of the path (using the current brush).</span></span>
-   <span data-ttu-id="e9ff8-133">Zeichnen Sie die Kontur, und füllen Sie das Innere des Pfads aus.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-133">Draw the outline and fill the interior of the path.</span></span>
-   <span data-ttu-id="e9ff8-134">Ändern des Pfads (umwandeln von Kurven in Liniensegmente).</span><span class="sxs-lookup"><span data-stu-id="e9ff8-134">Modify the path (converting curves to line segments).</span></span>
-   <span data-ttu-id="e9ff8-135">Konvertieren Sie den Pfad in einen Clip Pfad.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-135">Convert the path into a clip path.</span></span>
-   <span data-ttu-id="e9ff8-136">Konvertieren Sie den Pfad in einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-136">Convert the path into a region.</span></span>
-   <span data-ttu-id="e9ff8-137">Vereinfachen Sie den Pfad, indem Sie jede Kurve im Pfad in eine Reihe von Liniensegmenten umrechnen.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-137">Flatten the path by converting each curve in the path into a series of line segments.</span></span>
-   <span data-ttu-id="e9ff8-138">Rufen Sie die Koordinaten der Linien und Kurven ab, die einen Pfad bilden.</span><span class="sxs-lookup"><span data-stu-id="e9ff8-138">Retrieve the coordinates of the lines and curves that compose a path.</span></span>

 

 



