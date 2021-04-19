---
description: In diesem Beispiel werden zwei Methoden zum Suchen von frei Hand Eingaben anhand eines Bildschirm Orts veranschaulicht.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Beispiel für den Ink-Treffer Test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356743"
---
# <a name="ink-hit-test-sample"></a><span data-ttu-id="f1d82-103">Beispiel für den Ink-Treffer Test</span><span class="sxs-lookup"><span data-stu-id="f1d82-103">Ink Hit Test Sample</span></span>

<span data-ttu-id="f1d82-104">In diesem Beispiel werden zwei Methoden zum Suchen von frei Hand Eingaben anhand eines Bildschirm Orts veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f1d82-104">This sample illustrates two methods to find ink, given a screen location.</span></span>

<span data-ttu-id="f1d82-105">In diesem Beispiel werden die folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="f1d82-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="f1d82-106">Verwenden eines Ink Collector</span><span class="sxs-lookup"><span data-stu-id="f1d82-106">Using an ink collector</span></span>
-   <span data-ttu-id="f1d82-107">Ausführen eines Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="f1d82-107">Performing a hit test</span></span>
-   <span data-ttu-id="f1d82-108">Auffinden des nächsten Punkts</span><span class="sxs-lookup"><span data-stu-id="f1d82-108">Locating the nearest point</span></span>

## <a name="accessing-the-ink-api"></a><span data-ttu-id="f1d82-109">Zugreifen auf die Ink-API</span><span class="sxs-lookup"><span data-stu-id="f1d82-109">Accessing the Ink API</span></span>

<span data-ttu-id="f1d82-110">Verweisen Sie zunächst auf die Tablet PC-Klassen, die sich im Windows Vista-oder Windows XP Tablet PC Edition Software Development Kit (SDK) befinden.</span><span class="sxs-lookup"><span data-stu-id="f1d82-110">First, reference the Tablet PC classes, located in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a><span data-ttu-id="f1d82-111">Behandeln von Formular Lade-und Zeichnungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f1d82-111">Handling Form Load and Paint Events</span></span>

<span data-ttu-id="f1d82-112">Der Lade Ereignishandler des Formulars:</span><span class="sxs-lookup"><span data-stu-id="f1d82-112">The form's Load event handler:</span></span>

-   <span data-ttu-id="f1d82-113">Erstellt ein [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt (IC) für das Formular.</span><span class="sxs-lookup"><span data-stu-id="f1d82-113">Creates an [InkCollector](/previous-versions/ms583683(v=vs.100)) object, ic, for the form.</span></span>
-   <span data-ttu-id="f1d82-114">Legt die [CollectionMode](/previous-versions/ms836497(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekts auf das Ignorieren von Gesten fest.</span><span class="sxs-lookup"><span data-stu-id="f1d82-114">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [CollectionMode](/previous-versions/ms836497(v=msdn.10)) property to ignore gestures.</span></span>
-   <span data-ttu-id="f1d82-115">Aktiviert den [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f1d82-115">Enables the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span>
-   <span data-ttu-id="f1d82-116">Legt die [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekts auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="f1d82-116">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property to **TRUE**.</span></span>


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



<span data-ttu-id="f1d82-117">Der Paint-Ereignishandler des Formulars überprüft den Anwendungsmodus:</span><span class="sxs-lookup"><span data-stu-id="f1d82-117">The form's Paint event handler checks the application mode:</span></span>

-   <span data-ttu-id="f1d82-118">Im HitTest-Modus wird ein Kreis um den Cursor gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f1d82-118">In the HitTest mode, it paints a circle around the cursor.</span></span> <span data-ttu-id="f1d82-119">Der aktive Stift wird in der "Lenker Test"-Methode der Anwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f1d82-119">The active pen is set in the application's handleHitTest method.</span></span>
-   <span data-ttu-id="f1d82-120">Im NearestPoint-Modus wird eine rote Linie zwischen dem Cursor und dem Punkt gezeichnet, der dem Cursor am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="f1d82-120">In the NearestPoint mode, it paints a red line between the cursor and the point nearest the cursor.</span></span> <span data-ttu-id="f1d82-121">Der nächste Punkt wird in der handlenearestpoint-Methode der Anwendung berechnet.</span><span class="sxs-lookup"><span data-stu-id="f1d82-121">The nearest point is calculated in the application's handleNearestPoint method.</span></span>


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



<span data-ttu-id="f1d82-122">Dieses Beispiel enthält einen sehr einfachen Repaint-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="f1d82-122">This sample has a very straightforward repaint algorithm.</span></span> <span data-ttu-id="f1d82-123">Wenn die [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) -Eigenschaft auf **true** festgelegt ist, zeichnet sich der Ink Collector selbst auf, wenn das Formular neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f1d82-123">With its [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property set to **TRUE**, the ink collector repaints itself when the form is redrawn.</span></span> <span data-ttu-id="f1d82-124">Um das Neuzeichnen des Formulars zu vereinfachen, verfolgt die Anwendung ein umgebendes Feld, die ungültige Member-Variable, für den Bereich, in dem Paint hinzugefügt wird, das bei jedem erneuten Zeichnen des Formulars ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="f1d82-124">To simplify redrawing the form, the application tracks a bounding box, the invalidateRect member variable, for the area where paint is added, which is invalidated each time the form is redrawn.</span></span>

## <a name="handling-menu-events"></a><span data-ttu-id="f1d82-125">Behandeln von Menü Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f1d82-125">Handling Menu Events</span></span>

<span data-ttu-id="f1d82-126">Der Exit-Befehl deaktiviert den [InkCollector](/previous-versions/ms583683(v=vs.100)) , bevor die Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1d82-126">The Exit command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) before exiting the application.</span></span>

<span data-ttu-id="f1d82-127">Der Ink-Befehl aktualisiert den Anwendungsmodus und den Menü Status, aktiviert den Ink Collector und macht den zuvor gezeichneten Bereich des Formulars ungültig.</span><span class="sxs-lookup"><span data-stu-id="f1d82-127">The Ink command updates the application mode and menu status, enables the ink collector, and invalidates the previously painted region of the form.</span></span>

<span data-ttu-id="f1d82-128">Sowohl die Befehle Treffer Test als auch nächster Punkt ändern den Cursor, aktualisieren den Anwendungsmodus und den Menü Status, deaktivieren den frei Hand Sammler und machen den zuvor gezeichneten Bereich des Formulars ungültig.</span><span class="sxs-lookup"><span data-stu-id="f1d82-128">Both the Hit Test and Nearest Point commands change the cursor, update the application mode and menu status, disable the ink collector, and invalidate the previously painted region of the form.</span></span>

<span data-ttu-id="f1d82-129">Das Löschen!</span><span class="sxs-lookup"><span data-stu-id="f1d82-129">The Clear!</span></span> <span data-ttu-id="f1d82-130">der Befehl deaktiviert den [InkCollector](/previous-versions/ms583683(v=vs.100)) , während die [Ink](/previous-versions/ms836505(v=msdn.10)) -Eigenschaft des InkCollector-Objekts durch ein neues [Ink](/previous-versions/ms571716(v=vs.100)) -Objekt ersetzt wird, generiert ein Ink-Befehls Ereignis und erzwingt eine Aktualisierung des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="f1d82-130">command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) while replacing InkCollector object's [Ink](/previous-versions/ms836505(v=msdn.10)) property with a new [Ink](/previous-versions/ms571716(v=vs.100)) object, generates an Ink command event, and forces a refresh on the control.</span></span>

## <a name="handling-mouse-events"></a><span data-ttu-id="f1d82-131">Behandeln von Mausereignissen</span><span class="sxs-lookup"><span data-stu-id="f1d82-131">Handling Mouse Events</span></span>

<span data-ttu-id="f1d82-132">Der [MouseMove](/previous-versions/ms567617(v=vs.100)) -Ereignishandler überprüft den Anwendungsmodus:</span><span class="sxs-lookup"><span data-stu-id="f1d82-132">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode:</span></span>

-   <span data-ttu-id="f1d82-133">Im frei Hand Modus wird nichts ausgeführt, sodass frei Hand Eingaben vom frei Hand Sammler normal erfasst werden können.</span><span class="sxs-lookup"><span data-stu-id="f1d82-133">In Ink mode, it does nothing, allowing ink to be collected normally by the ink collector.</span></span>
-   <span data-ttu-id="f1d82-134">Im Modus "HitTest" werden die Ereignis Argumente an die "Lenker Test"-Methode der Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f1d82-134">In HitTest mode, it sends the event arguments to the application's handleHitTest method.</span></span>
-   <span data-ttu-id="f1d82-135">Im NearestPoint-Modus werden die Ereignis Argumente an die handlenearestpoint-Methode der Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f1d82-135">In NearestPoint mode, it sends the event arguments to the application's handleNearestPoint method.</span></span>

## <a name="performing-a-hit-test"></a><span data-ttu-id="f1d82-136">Ausführen eines Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="f1d82-136">Performing a Hit Test</span></span>

<span data-ttu-id="f1d82-137">Die "Lenker Test"-Methode der Anwendung erstellt zwei Punkte, die Cursorposition und einen Punkt, auf den die Pixel von dem Cursor entfernt sind, und konvertiert dann diese beiden Punkte von Pixel in frei Hand Raumkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="f1d82-137">The application's handleHitTest method creates two points, the cursor location and a point HitSize pixels distant from the cursor, and then converts these two points from pixels to ink space coordinates.</span></span>


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



<span data-ttu-id="f1d82-138">Anschließend verwendet das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt die [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) -Methode, um beliebige Striche in PT3 zu suchen. X-PT2. X-frei Hand Raumeinheiten des Cursors, PT2.</span><span class="sxs-lookup"><span data-stu-id="f1d82-138">Then, the [InkCollector](/previous-versions/ms583683(v=vs.100)) object uses the [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to find any strokes that are within pt3.X - pt2.X ink space units of the cursor, pt2.</span></span>


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



<span data-ttu-id="f1d82-139">Die "Lenker Test"-Methode legt dann die Stift Farbe fest, je nachdem, ob Striche gefunden wurden, erklärt den invalidaterierten Bereich für ungültig, berechnet einen neuen Bereich, in dem der Treffer Test Kreis gezeichnet wird, und macht dann die neue Region ungültig.</span><span class="sxs-lookup"><span data-stu-id="f1d82-139">The handleHitTest method then sets the pen color based on whether strokes were found, invalidates the invalidateRect region, calculates a new region that the hit test circle is drawn in, and then invalidates the new region.</span></span>

## <a name="locating-the-nearest-point"></a><span data-ttu-id="f1d82-140">Auffinden des nächsten Punkts</span><span class="sxs-lookup"><span data-stu-id="f1d82-140">Locating the Nearest Point</span></span>

<span data-ttu-id="f1d82-141">Die handlenearestpoint-Methode der Anwendung erstellt zwei Punkte, die beide mit der Position des Cursors identisch sind. einer dieser Punkte, PT, wird in den frei Hand Raum konvertiert und im Aufrufen der NearestPoint-Methode des [InkCollector](/previous-versions/ms583683(v=vs.100))- [Ink](/previous-versions/ms836505(v=msdn.10)) -Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1d82-141">The application's handleNearestPoint method creates two points both equal to the cursor's location, one of these points, pt, is converted to ink space and used in the call to the NearestPoint method of the [InkCollector](/previous-versions/ms583683(v=vs.100))'s [Ink](/previous-versions/ms836505(v=msdn.10)) object.</span></span> <span data-ttu-id="f1d82-142">Die NearestPoint-Methode gibt das [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekt zurück, das dem Punkt am nächsten liegt, und legt den Parameter für den Gleit Komma Index Output fest.</span><span class="sxs-lookup"><span data-stu-id="f1d82-142">The NearestPoint method returns the [Stroke](/previous-versions/ms827842(v=msdn.10)) object closest to the point, and sets the floating point index output parameter.</span></span>


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



<span data-ttu-id="f1d82-143">Wenn keine Striche vorhanden sind, gibt die NearestPoint-Methode **null** zurück, und die Cursorposition wird als nächster Punkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1d82-143">If no strokes are present, the NearestPoint method returns **NULL**, and the cursor location is used as the nearest point.</span></span> <span data-ttu-id="f1d82-144">Andernfalls wird die Position auf dem Strich berechnet, die dem Gleit Komma Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="f1d82-144">Otherwise, the location on the stroke that corresponds to the floating point index is calculated.</span></span>

<span data-ttu-id="f1d82-145">Die nächsten Punkt Koordinaten werden dann aus dem frei Handbereich in Pixel konvertiert. die handlenearestpoint-Methode macht dann den invalidaterierten Bereich ungültig, berechnet eine neue Region, in der die Zeile zum nächsten Punkt gezeichnet wird, und macht die neue Region ebenfalls ungültig.</span><span class="sxs-lookup"><span data-stu-id="f1d82-145">The nearest point coordinates are then converted to pixels from ink space, The handleNearestPoint method then invalidates the invalidateRect region, calculates a new region the line to the nearest point is drawn in, and invalidates the new region, too.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="f1d82-146">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="f1d82-146">Closing the Form</span></span>

<span data-ttu-id="f1d82-147">Die verwerfen-Methode des Formulars gibt das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="f1d82-147">The form's Dispose method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
