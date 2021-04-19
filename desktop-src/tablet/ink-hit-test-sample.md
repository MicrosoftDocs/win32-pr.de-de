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
# <a name="ink-hit-test-sample"></a>Beispiel für den Ink-Treffer Test

In diesem Beispiel werden zwei Methoden zum Suchen von frei Hand Eingaben anhand eines Bildschirm Orts veranschaulicht.

In diesem Beispiel werden die folgenden Funktionen verwendet:

-   Verwenden eines Ink Collector
-   Ausführen eines Treffer Tests
-   Auffinden des nächsten Punkts

## <a name="accessing-the-ink-api"></a>Zugreifen auf die Ink-API

Verweisen Sie zunächst auf die Tablet PC-Klassen, die sich im Windows Vista-oder Windows XP Tablet PC Edition Software Development Kit (SDK) befinden.


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Behandeln von Formular Lade-und Zeichnungs Ereignissen

Der Lade Ereignishandler des Formulars:

-   Erstellt ein [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt (IC) für das Formular.
-   Legt die [CollectionMode](/previous-versions/ms836497(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekts auf das Ignorieren von Gesten fest.
-   Aktiviert den [InkCollector](/previous-versions/ms583683(v=vs.100)).
-   Legt die [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekts auf " **true**" fest.


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



Der Paint-Ereignishandler des Formulars überprüft den Anwendungsmodus:

-   Im HitTest-Modus wird ein Kreis um den Cursor gezeichnet. Der aktive Stift wird in der "Lenker Test"-Methode der Anwendung festgelegt.
-   Im NearestPoint-Modus wird eine rote Linie zwischen dem Cursor und dem Punkt gezeichnet, der dem Cursor am nächsten liegt. Der nächste Punkt wird in der handlenearestpoint-Methode der Anwendung berechnet.


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



Dieses Beispiel enthält einen sehr einfachen Repaint-Algorithmus. Wenn die [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) -Eigenschaft auf **true** festgelegt ist, zeichnet sich der Ink Collector selbst auf, wenn das Formular neu gezeichnet wird. Um das Neuzeichnen des Formulars zu vereinfachen, verfolgt die Anwendung ein umgebendes Feld, die ungültige Member-Variable, für den Bereich, in dem Paint hinzugefügt wird, das bei jedem erneuten Zeichnen des Formulars ungültig wird.

## <a name="handling-menu-events"></a>Behandeln von Menü Ereignissen

Der Exit-Befehl deaktiviert den [InkCollector](/previous-versions/ms583683(v=vs.100)) , bevor die Anwendung beendet wird.

Der Ink-Befehl aktualisiert den Anwendungsmodus und den Menü Status, aktiviert den Ink Collector und macht den zuvor gezeichneten Bereich des Formulars ungültig.

Sowohl die Befehle Treffer Test als auch nächster Punkt ändern den Cursor, aktualisieren den Anwendungsmodus und den Menü Status, deaktivieren den frei Hand Sammler und machen den zuvor gezeichneten Bereich des Formulars ungültig.

Das Löschen! der Befehl deaktiviert den [InkCollector](/previous-versions/ms583683(v=vs.100)) , während die [Ink](/previous-versions/ms836505(v=msdn.10)) -Eigenschaft des InkCollector-Objekts durch ein neues [Ink](/previous-versions/ms571716(v=vs.100)) -Objekt ersetzt wird, generiert ein Ink-Befehls Ereignis und erzwingt eine Aktualisierung des Steuer Elements.

## <a name="handling-mouse-events"></a>Behandeln von Mausereignissen

Der [MouseMove](/previous-versions/ms567617(v=vs.100)) -Ereignishandler überprüft den Anwendungsmodus:

-   Im frei Hand Modus wird nichts ausgeführt, sodass frei Hand Eingaben vom frei Hand Sammler normal erfasst werden können.
-   Im Modus "HitTest" werden die Ereignis Argumente an die "Lenker Test"-Methode der Anwendung gesendet.
-   Im NearestPoint-Modus werden die Ereignis Argumente an die handlenearestpoint-Methode der Anwendung gesendet.

## <a name="performing-a-hit-test"></a>Ausführen eines Treffer Tests

Die "Lenker Test"-Methode der Anwendung erstellt zwei Punkte, die Cursorposition und einen Punkt, auf den die Pixel von dem Cursor entfernt sind, und konvertiert dann diese beiden Punkte von Pixel in frei Hand Raumkoordinaten.


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



Anschließend verwendet das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt die [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) -Methode, um beliebige Striche in PT3 zu suchen. X-PT2. X-frei Hand Raumeinheiten des Cursors, PT2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



Die "Lenker Test"-Methode legt dann die Stift Farbe fest, je nachdem, ob Striche gefunden wurden, erklärt den invalidaterierten Bereich für ungültig, berechnet einen neuen Bereich, in dem der Treffer Test Kreis gezeichnet wird, und macht dann die neue Region ungültig.

## <a name="locating-the-nearest-point"></a>Auffinden des nächsten Punkts

Die handlenearestpoint-Methode der Anwendung erstellt zwei Punkte, die beide mit der Position des Cursors identisch sind. einer dieser Punkte, PT, wird in den frei Hand Raum konvertiert und im Aufrufen der NearestPoint-Methode des [InkCollector](/previous-versions/ms583683(v=vs.100))- [Ink](/previous-versions/ms836505(v=msdn.10)) -Objekts verwendet. Die NearestPoint-Methode gibt das [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekt zurück, das dem Punkt am nächsten liegt, und legt den Parameter für den Gleit Komma Index Output fest.


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



Wenn keine Striche vorhanden sind, gibt die NearestPoint-Methode **null** zurück, und die Cursorposition wird als nächster Punkt verwendet. Andernfalls wird die Position auf dem Strich berechnet, die dem Gleit Komma Index entspricht.

Die nächsten Punkt Koordinaten werden dann aus dem frei Handbereich in Pixel konvertiert. die handlenearestpoint-Methode macht dann den invalidaterierten Bereich ungültig, berechnet eine neue Region, in der die Zeile zum nächsten Punkt gezeichnet wird, und macht die neue Region ebenfalls ungültig.

## <a name="closing-the-form"></a>Schließen des Formulars

Die verwerfen-Methode des Formulars gibt das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt frei.

 

 
