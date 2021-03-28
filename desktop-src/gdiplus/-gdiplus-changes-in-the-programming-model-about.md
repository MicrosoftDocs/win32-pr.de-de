---
description: In den folgenden Abschnitten werden verschiedene Möglichkeiten beschrieben, wie sich die Programmierung mit Windows GDI+ von der Programmierung mit Windows Graphics Device Interface (GDI) unterscheidet.
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Änderungen am Programmiermodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90cd6f1c3a6ebab1e55562e67cb4926f0ffedf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042112"
---
# <a name="changes-in-the-programming-model"></a>Änderungen am Programmiermodell

In den folgenden Abschnitten werden verschiedene Möglichkeiten beschrieben, wie sich die Programmierung mit Windows GDI+ von der Programmierung mit Windows Graphics Device Interface (GDI) unterscheidet.

-   [Geräte Kontexte, Handles und Grafik Objekte](#device-contexts-handles-and-graphics-objects)
-   [Zwei Möglichkeiten zum Zeichnen einer Linie](#two-ways-to-draw-a-line)
    -   [Zeichnen einer Linie mit GDI](#drawing-a-line-with-gdi)
    -   [Zeichnen einer Linie mit GDI+ und der C++-Klassen Schnittstelle](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Stifte, Pinsel, Pfade, Bilder und Schriftarten als Parameter](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Methoden Überladung](#method-overloading)
-   [Keine aktuelle Position mehr](#no-more-current-position)
-   [Separate Methoden zum Zeichnen und ausfüllen](#separate-methods-for-draw-and-fill)
-   [Erstellen von Regionen](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Geräte Kontexte, Handles und Grafik Objekte

Wenn Sie Programme mit GDI geschrieben haben (die Grafikgeräte Schnittstelle, die in früheren Versionen von Windows enthalten war), sind Sie mit der Idee eines Geräte Kontexts (DC) vertraut. Ein Gerätekontext ist eine Struktur, die von Windows verwendet wird, um Informationen über die Funktionen eines bestimmten Anzeige Geräts und Attribute zu speichern, die angeben, wie Elemente auf diesem Gerät gezeichnet werden. Ein Gerätekontext für eine Videoanzeige ist auch einem bestimmten Fenster auf der Anzeige zugeordnet. Zuerst erhalten Sie ein Handle für einen Gerätekontext (HDC), und Sie übergeben dieses Handle als Argument an GDI-Funktionen, die die Zeichnung tatsächlich durchführen. Außerdem übergeben Sie das Handle als Argument an GDI-Funktionen, die die Attribute des Geräte Kontexts abrufen oder festlegen.

Wenn Sie GDI+ verwenden, müssen Sie sich nicht wie bei der Verwendung von GDI mit Handles und Geräte Kontexten beschäftigen. Sie erstellen einfach ein [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) -Objekt und rufen dann seine Methoden im vertrauten objektorientierten Stil auf – mygraphicsobject. DrawLine (*Parameters*). Das **Grafik** Objekt ist das Kernstück von GDI+, ebenso wie der Gerätekontext im Kern von GDI. Der Gerätekontext und das **Grafik** Objekt spielen ähnliche Rollen. es gibt jedoch einige grundlegende Unterschiede zwischen dem Handle-basierten Programmiermodell, das mit den Geräte Kontexten verwendet wird, und dem objektorientierten Modell, das mit **Grafik** Objekten (GDI+) verwendet wird.

Das [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, wie z. b. der Gerätekontext, ist einem bestimmten Fenster auf dem Bildschirm zugeordnet und enthält Attribute (z. b. Glättungs Modus und Text Rendering Hint), die angeben, wie Elemente gezeichnet werden sollen. Das **Grafik** Objekt ist jedoch nicht an einen Stift, Pinsel, Pfad, ein Bild oder eine Schriftart gebunden, wenn ein Gerätekontext ist. Wenn Sie z. b. in GDI einen Gerätekontext zum Zeichnen einer Linie verwenden können, müssen Sie [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) aufrufen, um dem Gerätekontext ein Pen-Objekt zuzuordnen. Dies wird als auswählen des Stifts in den Gerätekontext bezeichnet. Alle Zeilen, die im Gerätekontext gezeichnet werden, verwenden diesen Stift, bis Sie einen anderen Stift auswählen. Mit GDI+ übergeben Sie ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt als Argument an die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) -Methode der **Grafik** Klasse. Sie können ein anderes **Stift** Objekt in jeder Reihe von DrawLine-aufrufen verwenden, ohne ein bestimmtes **Pen** -Objekt einem **Grafik** Objekt zuordnen zu müssen.

## <a name="two-ways-to-draw-a-line"></a>Zwei Möglichkeiten zum Zeichnen einer Linie

In den beiden folgenden Beispielen wird jeweils eine rote Linie der Breite 3 von der Position (20, 10) bis zum Speicherort (200.100) gezeichnet. Im ersten Beispiel wird GDI aufgerufen, und der zweite ruft GDI+ über die C++-Klassen Schnittstelle auf.

-   [Zeichnen einer Linie mit GDI](#drawing-a-line-with-gdi)
-   [Zeichnen einer Linie mit GDI+ und der C++-Klassen Schnittstelle](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Zeichnen einer Linie mit GDI

Um eine Linie mit GDI zu zeichnen, benötigen Sie zwei Objekte: einen Gerätekontext und einen Stift. Sie erhalten ein Handle für einen Gerätekontext durch Aufrufen von [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)und ein Handle für einen Stift durch Aufrufen von [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen). Als nächstes wird [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) aufgerufen, um den Stift in den Gerätekontext auszuwählen. Legen Sie die Position des Stifts auf (20, 10) fest, indem Sie " [muvetoex](/windows/win32/api/wingdi/nf-wingdi-movetoex) " aufrufen und dann eine Linie von dieser Stift Position in (200, 100) ziehen, indem Sie " **LineTo**" aufrufen. Beachten Sie, dass "muveumex" und " [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) " den **hdc** als Argument empfangen.


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>Zeichnen einer Linie mit GDI+ und der C++-Klassen Schnittstelle

Um eine Linie mit GDI+ und der C++-Klassen Schnittstelle zu zeichnen, benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt. Beachten Sie, dass Sie Windows nicht nach Handles für diese Objekte Fragen. Stattdessen verwenden Sie Konstruktoren, um eine Instanz der **Grafik** Klasse (ein **Grafik** Objekt) und eine Instanz der **Stift** Klasse (ein **Pen** -Objekt) zu erstellen. Das Zeichnen einer Linie umfasst das Aufrufen der [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) -Methode der **Grafik** Klasse. Der erste Parameter der **Grafik::D rawline** -Methode ist ein Zeiger auf das **Pen** -Objekt. Dies ist ein einfacheres und flexibleres Schema als das Auswählen eines Stifts in einen Gerätekontext, wie im vorangehenden GDI-Beispiel gezeigt.


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>Stifte, Pinsel, Pfade, Bilder und Schriftarten als Parameter

In den vorangehenden Beispielen wird gezeigt, dass [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekte separat vom [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt und verwaltet werden können, das die Zeichnungs Methoden bereitstellt. [**Pinsel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)-, [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath)-, [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)-und [**Schriftart**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Objekte können auch getrennt vom **Grafik** Objekt erstellt und verwaltet werden. Viele der Zeichnungs Methoden, die von der **Grafik** Klasse bereitgestellt werden, erhalten einen **Pinsel**, **GraphicsPath**, ein **Bild** oder ein **Schriftart** Objekt als Argument. Beispielsweise wird die Adresse eines **Pinsel** Objekts als Argument an die [fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) -Methode übergeben, und die Adresse eines **GraphicsPath** -Objekts wird als Argument an die [**Grafik::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode übergeben. Ebenso werden Adressen von **Bild** -und **Schriftart** Objekten an die [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) -und [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methoden übermittelt. Dies steht im Gegensatz zu GDI, bei der Sie einen Pinsel, Pfad, ein Bild oder eine Schriftart in den Gerätekontext auswählen und dann ein Handle an den Gerätekontext als Argument an eine Zeichnungs Funktion übergeben.

## <a name="method-overloading"></a>Methoden Überladung

Viele der GDI+-Methoden sind überladen. Das heißt, dass mehrere Methoden denselben Namen aufweisen, aber über unterschiedliche Parameterlisten verfügen. Beispielsweise ist die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse in den folgenden Formen:


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



Alle vier der [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) -Variationen übernehmen einen Zeiger auf ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt, die Koordinaten des Anfangs Punkts und die Koordinaten des Endpunkts. Die ersten beiden Variationen empfangen die Koordinaten als Gleit Komma Zahlen, und die beiden letzten Variationen empfangen die Koordinaten als ganze Zahlen. Die erste und die dritte Variation empfangen die Koordinaten als eine Liste von vier separaten Zahlen, während die zweite und die vierte Variation die Koordinaten als Paar von [**Punkt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) -(oder [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)-) Objekten erhalten.

## <a name="no-more-current-position"></a>Keine aktuelle Position mehr

Beachten Sie, dass in den zuvor gezeigten [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) -Methoden sowohl der Anfangspunkt als auch der Endpunkt der Zeile als Argumente empfangen werden. Dabei handelt es sich um einen Abbruch des GDI-Schemas, in dem Sie die aktuelle Stift Position, gefolgt von **"LineTo** ", zum Zeichnen einer **Linie aufrufen,** die bei (**x1**, **Y1**) beginnt und am endet (**x2**, **Y2**). GDI+ als Ganzes hat das Konzept der aktuellen Position abgebrochen.

## <a name="separate-methods-for-draw-and-fill"></a>Separate Methoden zum Zeichnen und ausfüllen

GDI+ ist flexibler als GDI, wenn es um das Zeichnen der Kontur und das Auffüllen des Inneren von Formen wie Rechtecke geht. GDI verfügt über eine [Rechteck](/windows/win32/api/wingdi/nf-wingdi-rectangle) Funktion, die die Kontur zeichnet und das Innere eines Rechtecks in einem einzigen Schritt füllt. Der Umriss wird mit dem aktuell ausgewählten Stift gezeichnet, und das innere wird mit dem aktuell ausgewählten Pinsel gefüllt.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ verfügt über separate Methoden zum Zeichnen der Kontur und zum Ausfüllen des Inneren eines Rechtecks. Die [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verfügt über die Adresse eines [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Objekts als einen seiner Parameter, und die [fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) -Methode hat die Adresse eines [**Pinsel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekts als einen seiner Parameter.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Beachten Sie, dass die [fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) -und [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) -Methoden in GDI+ Argumente empfangen, die den linken Rand des Rechtecks, Top, Width und Height angeben. Dies steht im Gegensatz zur GDI-[rechteenfunktion](/windows/win32/api/wingdi/nf-wingdi-rectangle) , die Argumente annimmt, die den linken Rand des Rechtecks, den rechten Rand, den oberen und den unteren Rand angeben. Beachten Sie außerdem, dass der Konstruktor für die [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Klasse in GDI+ über vier Parameter verfügt. Die letzten drei Parameter sind die üblichen Werte für Rot, grün und blau. der erste Parameter ist der Alpha-Wert, der angibt, in welchem Ausmaß die Farbe, die gezeichnet wird, mit der Hintergrundfarbe gemischt wird.

## <a name="constructing-regions"></a>Erstellen von Regionen

GDI bietet verschiedene Funktionen zum Erstellen von Bereichen: "kreaterectrgn", "kreateellpticrgn", "anateroundrectrgn", "kreatepolygonrgn" und "kreatepolypolygonrgn". Sie erwarten möglicherweise, dass die [**Regions**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) Klasse in GDI+ über analoge Konstruktoren verfügt, die Rechtecke, Ellipsen, abgerundete Rechtecke und Polygone als Argumente annehmen, dies ist jedoch nicht der Fall. Die **Regions** Klasse in GDI+ bietet einen Konstruktor, der einen [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt Verweis empfängt, und einen weiteren Konstruktor, der die Adresse eines [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekts empfängt. Wenn Sie **einen Bereich auf** der Grundlage einer Ellipse, eines abgerundeten Rechtecks oder eines Polygons erstellen möchten, können Sie dies problemlos erreichen, indem Sie ein **GraphicsPath** -Objekt erstellen (z. b. eine Ellipse) und dann die Adresse des **GraphicsPath** -Objekts an einen bereichskonstruktor übergeben.

GDI+ vereinfacht das bilden komplexer Regionen, indem Formen und Pfade kombiniert werden. Die [**Regions**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) Klasse verfügt über [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) -und [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) -Methoden, die Sie verwenden können, um einen vorhandenen Bereich durch einen Pfad oder einen anderen Bereich zu erweitern. Ein nützliches Feature des GDI+-Schemas besteht darin, dass ein [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt nicht zerstört wird, wenn es als Argument **an einen** bereichskonstruktor übergeben wird. In GDI können Sie einen Pfad in einen Bereich mit der [pathtoregion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) -Funktion konvertieren, aber der Pfad wird im Prozess zerstört. Außerdem wird ein **GraphicsPath** -Objekt nicht zerstört, wenn die Adresse als Argument an eine Union-oder Intersect-Methode übergeben wird, sodass Sie einen bestimmten Pfad als Baustein für mehrere separate Regionen verwenden können. Dies wird im folgenden Beispiel gezeigt. Angenommen, **onepath** ist ein Zeiger auf ein **GraphicsPath** -Objekt (einfach oder Komplex), das bereits initialisiert wurde.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
