---
description: In diesem Beispiel werden zwei Methoden zum Suchen von Ink anhand einer Bildschirmposition veranschaulicht.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Beispiel für einen Ink-Treffertest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995bd6f14b4a0a014452ae9392fa744ab93f01f9047c79e5dc30652c243473db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713080"
---
# <a name="ink-hit-test-sample"></a>Beispiel für einen Ink-Treffertest

In diesem Beispiel werden zwei Methoden zum Suchen von Ink anhand einer Bildschirmposition veranschaulicht.

In diesem Beispiel werden die folgenden Features verwendet:

-   Verwenden eines Ink-Collectors
-   Ausführen eines Treffertests
-   Suchen des nächstgelegenen Punkts

## <a name="accessing-the-ink-api"></a>Zugreifen auf die Ink-API

Verweisen Sie zunächst auf die Tablet PC-Klassen im Windows Vista oder Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Behandeln von Formularlade- und Paint Ereignissen

Der Load-Ereignishandler des Formulars:

-   Erstellt das [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100)) ic für das Formular.
-   Legt die [CollectionMode-Eigenschaft](/previous-versions/ms836497(v=msdn.10)) des [InkCollector-Objekts](/previous-versions/ms583683(v=vs.100)) fest, um Gesten zu ignorieren.
-   Aktiviert den [InkCollector.](/previous-versions/ms583683(v=vs.100))
-   Legt die [AutoRedraw-Eigenschaft](/previous-versions/ms836495(v=msdn.10)) des [InkCollector-Objekts](/previous-versions/ms583683(v=vs.100)) auf **TRUE fest.**


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

-   Im HitTest-Modus wird ein Kreis um den Cursor gestrichen. Der aktive Stift wird in der handleHitTest-Methode der Anwendung festgelegt.
-   Im NearestPoint-Modus zeichnet sie eine rote Linie zwischen dem Cursor und dem Punkt, der dem Cursor am nächsten liegt. Der nächste Punkt wird in der handleRestPoint-Methode der Anwendung berechnet.


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



Dieses Beispiel verfügt über einen sehr unkomplizierten Neupaintalgorithmus. Wenn die [AutoRedraw-Eigenschaft](/previous-versions/ms836495(v=msdn.10)) auf **TRUE** festgelegt ist, wird der Ink-Collector selbst neu gezeichnet, wenn das Formular neu gezeichnet wird. Um die Neuzeichnung des Formulars zu vereinfachen, verfolgt die Anwendung ein Begrenzungsfeld, die InvalidateRect-Membervariable, für den Bereich, in dem Die Farbe hinzugefügt wird, der bei jedem Neuzeichneten des Formulars ungültig wird.

## <a name="handling-menu-events"></a>Behandeln von Menüereignissen

Der Befehl Exit deaktiviert den [InkCollector,](/previous-versions/ms583683(v=vs.100)) bevor die Anwendung beendet wird.

Der Befehl Ink aktualisiert den Anwendungsmodus und den Menüstatus, aktiviert den Ink-Collector und macht den zuvor gestrichelten Bereich des Formulars ungültig.

Sowohl der Befehl Treffertest als auch der nächste Punkt ändern den Cursor, aktualisieren den Anwendungsmodus und den Menüstatus, deaktivieren den Ink-Collector und machen den zuvor gestrichenen Bereich des Formulars ungültig.

The Clear! der Befehl deaktiviert den [InkCollector,](/previous-versions/ms583683(v=vs.100)) während die InkCollector-Eigenschaft des InkCollector-Objekts durch ein neues [Ink-Objekt](/previous-versions/ms571716(v=vs.100)) ersetzt wird, generiert ein Ink-Befehlsereignis und erzwingt eine Aktualisierung des Steuerelements. [](/previous-versions/ms836505(v=msdn.10))

## <a name="handling-mouse-events"></a>Behandeln von Mausereignissen

Der [MouseMove-Ereignishandler](/previous-versions/ms567617(v=vs.100)) überprüft den Anwendungsmodus:

-   Im Ink-Modus wird nichts ausgeführt, sodass die Ink-Sammlung normal vom Ink-Collector erfolgt.
-   Im HitTest-Modus werden die Ereignisargumente an die handleHitTest-Methode der Anwendung sendet.
-   Im NearestPoint-Modus werden die Ereignisargumente an die handleRestPoint-Methode der Anwendung sendet.

## <a name="performing-a-hit-test"></a>Ausführen eines Treffertests

Die handleHitTest-Methode der Anwendung erstellt zwei Punkte, die Cursorposition und einen Punkt HitSize-Pixel, die vom Cursor entfernt sind, und konvertiert diese beiden Punkte von Pixeln in Freihandraumkoordinaten.


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



Anschließend verwendet das [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100)) die [Microsoft.Ink.Ink.HitTest()-Methode,](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) um alle Striche innerhalb von pt3 zu finden. X - pt2. X Freiraumeinheiten des Cursors, pt2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



Die handleHitTest-Methode legt dann die Stiftfarbe basierend darauf fest, ob Striche gefunden wurden, erklärt den InvalidateRect-Bereich für ungültig, berechnet einen neuen Bereich, in dem der Treffertestkreis gezeichnet wird, und erklärt dann den neuen Bereich für ungültig.

## <a name="locating-the-nearest-point"></a>Suchen des nächsten Punkts

Die handleRestPoint-Methode der Anwendung erstellt zwei Punkte, die beide gleich der Position des Cursors sind. Einer dieser Punkte, pt, wird in Freihandraum konvertiert und im Aufruf der NearestPoint-Methode des Freihandobjekts des [InkCollector](/previous-versions/ms583683(v=vs.100))verwendet. [](/previous-versions/ms836505(v=msdn.10)) Die NearestPoint-Methode gibt das [Stroke-Objekt](/previous-versions/ms827842(v=msdn.10)) zurück, das dem Punkt am nächsten ist, und legt den Gleitkommaindex-Ausgabeparameter fest.


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



Wenn keine Striche vorhanden sind, gibt die NearestPoint-Methode **NULL zurück,** und die Cursorposition wird als nächster Punkt verwendet. Andernfalls wird die Position auf dem Strich berechnet, die dem Gleitkommaindex entspricht.

Die nächstgelegenen Punktkoordinaten werden dann aus dem Freihandraum in Pixel konvertiert. Die handleRestPoint-Methode macht dann den InvalidateRect-Bereich ungültig, berechnet einen neuen Bereich, in dem die Linie bis zum nächsten Punkt gezeichnet wird, und macht auch den neuen Bereich ungültig.

## <a name="closing-the-form"></a>Schließen des Formulars

Die Dispose-Methode des Formulars gibt das [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100)) zurück.

 

 
