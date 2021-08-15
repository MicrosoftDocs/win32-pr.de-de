---
description: In den folgenden Abschnitten werden verschiedene Möglichkeiten beschrieben, wie sich das Programmieren mit Windows GDI+ von der Programmierung mit Windows Graphics Device Interface (GDI) unterscheiden kann.
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Änderungen am Programmiermodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05dd8b74662d0141405b9d11b9b4446ffb19dd4ef3bfdec788afe7a51a8c681a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249887"
---
# <a name="changes-in-the-programming-model"></a>Änderungen am Programmiermodell

In den folgenden Abschnitten werden verschiedene Möglichkeiten beschrieben, wie sich das Programmieren mit Windows GDI+ von der Programmierung mit Windows Graphics Device Interface (GDI) unterscheiden kann.

-   [Gerätekontexte, Handles und Grafikobjekte](#device-contexts-handles-and-graphics-objects)
-   [Zwei Möglichkeiten zum Zeichnen einer Linie](#two-ways-to-draw-a-line)
    -   [Zeichnen einer Linie mit GDI](#drawing-a-line-with-gdi)
    -   [Zeichnen einer Linie mit GDI+ und der C++-Klassenschnittstelle](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Stifte, Pinsel, Pfade, Bilder und Schriftarten als Parameter](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Methodenüberladung](#method-overloading)
-   [Keine aktuelle Position mehr](#no-more-current-position)
-   [Separate Methoden für Zeichnen und Füllen](#separate-methods-for-draw-and-fill)
-   [Erstellen von Regionen](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Gerätekontexte, Handles und Grafikobjekte

Wenn Sie Programme mit GDI (der Grafikgeräteschnittstelle in früheren Versionen von Windows) geschrieben haben, sind Sie mit der Idee eines Gerätekontexts (DC) vertraut. Ein Gerätekontext ist eine Struktur, die von Windows verwendet wird, um Informationen über die Funktionen eines bestimmten Anzeigegeräts und Attribute zu speichern, die angeben, wie Elemente auf diesem Gerät gezeichnet werden. Ein Gerätekontext für eine Videoanzeige ist auch einem bestimmten Fenster auf der Anzeige zugeordnet. Zuerst erhalten Sie ein Handle für einen Gerätekontext (HDC) und übergeben dieses Handle dann als Argument an GDI-Funktionen, die die Zeichnung tatsächlich ausführen. Sie übergeben das Handle auch als Argument an GDI-Funktionen, die die Attribute des Gerätekontexts abrufen oder festlegen.

Wenn Sie GDI+ verwenden, müssen Sie sich nicht um Handles und Gerätekontexte wie bei der Verwendung von GDI sorgen. Sie erstellen einfach ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und rufen dann seine Methoden im vertrauten objektorientierten Stil auf : myGraphicsObject.DrawLine(*Parameter*). Das **Grafikobjekt** ist das Kernstück GDI+ wie der Gerätekontext der Kern von GDI ist. Der Gerätekontext und das **Grafikobjekt** spielen ähnliche Rollen, aber es gibt einige grundlegende Unterschiede zwischen dem handlebasierten Programmiermodell, das mit Gerätekontexten (GDI) verwendet wird, und dem objektorientierten Modell, das mit Grafikobjekten (GDI+) verwendet wird. 

Das [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ist wie der Gerätekontext einem bestimmten Fenster auf dem Bildschirm zugeordnet und enthält Attribute (z. B. Glättungsmodus und Textrenderinghinweis), die angeben, wie Elemente gezeichnet werden sollen. Das **Grafikobjekt ist** jedoch nicht an einen Stift, Pinsel, Pfad, Bild oder eine Schriftart gebunden, wie es ein Gerätekontext ist. Bevor Sie beispielsweise in GDI einen Gerätekontext zum Zeichnen einer Linie verwenden können, müssen Sie [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) aufrufen, um dem Gerätekontext ein Stiftobjekt zu zuordnen. Dies wird als Auswählen des Stifts im Gerätekontext bezeichnet. Alle im Gerätekontext gezeichneten Linien verwenden diesen Stift, bis Sie einen anderen Stift auswählen. Mit GDI+ übergeben Sie ein [**Pen-Objekt**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) als Argument an die [DrawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) der **Graphics-Klasse.** Sie können in jeder **Reihe** von DrawLine-Aufrufen ein anderes Pen-Objekt verwenden, ohne ein bestimmtes **Stiftobjekt** einem **Graphics-Objekt zuordnen zu** müssen.

## <a name="two-ways-to-draw-a-line"></a>Zwei Möglichkeiten zum Zeichnen einer Linie

In den folgenden beiden Beispielen wird jeweils eine rote Linie der Breite 3 von position (20, 10) bis location (200.100) ge zeichnen. Das erste Beispiel ruft GDI auf, das zweite GDI+ über die C++-Klassenschnittstelle.

-   [Zeichnen einer Linie mit GDI](#drawing-a-line-with-gdi)
-   [Zeichnen einer Linie mit GDI+ und der C++-Klassenschnittstelle](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Zeichnen einer Linie mit GDI

Um eine Linie mit GDI zu zeichnen, benötigen Sie zwei Objekte: einen Gerätekontext und einen Stift. Sie erhalten ein Handle für einen Gerätekontext, indem Sie [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)aufrufen, und ein Handle für einen Stift, indem Sie [CreatePen aufrufen.](/windows/win32/api/wingdi/nf-wingdi-createpen) Als Nächstes rufen Sie [SelectObject auf,](/windows/win32/api/wingdi/nf-wingdi-selectobject) um den Stift im Gerätekontext auszuwählen. Sie legen die Stiftposition auf (20, 10) fest, indem Sie [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) aufrufen und dann eine Linie von dieser Stiftposition auf (200, 100) zeichnen, indem Sie **LineTo aufrufen.** Beachten Sie, dass MoveToEx [und LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) **beide hdc als** Argument empfangen.


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



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>Zeichnen einer Linie mit GDI+ und der C++-Klassenschnittstelle

Zum Zeichnen einer Linie mit GDI+ und der C++-Klassenschnittstelle benötigen Sie ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein [**Pen-Objekt.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Beachten Sie, dass Sie nicht Windows handles für diese Objekte fragen. Stattdessen verwenden Sie Konstruktoren, um eine Instanz der **Graphics-Klasse** (ein **Graphics-Objekt)** und eine Instanz der **Pen-Klasse** (ein **Pen-Objekt) zu** erstellen. Das Zeichnen einer Linie umfasst das Aufrufen der [**Graphics::D rawLine-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) der **Graphics-Klasse.** Der erste Parameter der **Graphics::D rawLine-Methode** ist ein Zeiger auf Ihr **Pen-Objekt.** Dies ist ein einfacheres und flexibleres Schema als das Auswählen eines Stifts in einen Gerätekontext, wie im vorherigen GDI-Beispiel gezeigt.


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

Die vorangehenden Beispiele zeigen, dass [**Stiftobjekte**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) getrennt vom [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) erstellt und verwaltet werden können, das die Zeichnungsmethoden liefert. [**Brush-,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) [**GraphicsPath-,**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) [**Image-**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)und [**Font-Objekte**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) können auch getrennt vom Graphics-Objekt erstellt **und verwaltet** werden. Viele der von der  Graphics-Klasse bereitgestellten Zeichnungsmethoden erhalten ein **Brush-,** **GraphicsPath-,** **Image-** oder **Font-Objekt** als Argument. Beispielsweise wird die Adresse eines **Brush-Objekts** als Argument an die [FillRectangle-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) übergeben, und die Adresse eines **GraphicsPath-Objekts** wird als Argument an die [**Graphics::D rawPath-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) übergeben. Auf ähnliche Weise werden Adressen von **Image-** **und Font-Objekten** an die [DrawImage-](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) und [DrawString-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) übergeben. Dies steht im Gegensatz zu GDI, bei dem Sie einen Pinsel, Pfad, ein Bild oder eine Schriftart im Gerätekontext auswählen und dann ein Handle als Argument an eine Zeichnungsfunktion an den Gerätekontext übergeben.

## <a name="method-overloading"></a>Methodenüberladung

Viele der GDI+ methoden sind überladen. Das heißt, dass mehrere Methoden denselben Namen haben, aber unterschiedliche Parameterlisten haben. Die [DrawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) hat beispielsweise folgende Formen:


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



Alle vier oben genannten [DrawLine-Variationen](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) erhalten einen Zeiger auf ein [**Pen-Objekt,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) die Koordinaten des Ausgangspunkts und die Koordinaten des Endpunkts. Die ersten beiden Variationen empfangen die Koordinaten als Gleitkommazahlen, und die letzten beiden Variationen empfangen die Koordinaten als ganze Zahlen. Die erste und dritte Variation empfangen die Koordinaten als Liste mit vier separaten Zahlen, während die zweite und vierte Variation die Koordinaten als Paar aus [**Point-Objekten**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (oder [**PointF)**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)empfangen.

## <a name="no-more-current-position"></a>Keine aktuelle Position mehr

Beachten Sie, dass in den zuvor gezeigten [DrawLine-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) sowohl der Anfangspunkt als auch der Endpunkt der Zeile als Argumente empfangen werden. Dies ist eine Abweichung vom GDI-Schema, bei dem Sie **MoveToEx** aufrufen, um die aktuelle Stiftposition, gefolgt von **LineTo,** zu setzen, um eine Linie zu zeichnen, die bei (**x1**, **y1**) beginnt und bei endet (**x2**, **y2**). GDI+ als Ganzes hat das Konzept der aktuellen Position verworfen.

## <a name="separate-methods-for-draw-and-fill"></a>Separate Methoden für Zeichnen und Füllen

GDI+ ist flexibler als GDI, wenn es darum geht, die Konturen zu zeichnen und das Innere von Formen wie Rechtecke zu füllen. GDI verfügt über eine [Rectangle-Funktion,](/windows/win32/api/wingdi/nf-wingdi-rectangle) die die Kontur zeichnet und das Innere eines Rechtecks in einem Schritt ausfüllt. Die Kontur wird mit dem aktuell ausgewählten Stift gezeichnet, und das Innere wird mit dem aktuell ausgewählten Pinsel gefüllt.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ verfügt über separate Methoden zum Zeichnen der Kontur und zum Auffüllen des Inneren eines Rechtecks. Die [DrawRectangle-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verfügt über die Adresse eines [**Stiftobjekts**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) als einen ihrer Parameter, und die [FillRectangle-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) verfügt über die Adresse eines [**Brush-Objekts**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) als einen ihrer Parameter.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Beachten Sie, dass die [Methoden FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) und [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) in GDI+ Argumente empfangen, die den linken Rand, den oberen Rand, die Breite und die Höhe des Rechtecks angeben. Dies steht im Gegensatz[](/windows/win32/api/wingdi/nf-wingdi-rectangle) zur GDI-Rechteckfunktion, die Argumente verwendet, die den linken Rand, den rechten Rand, den oberen und den unteren Rand des Rechtecks angeben. Beachten Sie auch, dass der Konstruktor für die [**Color-Klasse**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) in GDI+ über vier Parameter verfügt. Die letzten drei Parameter sind die üblichen Werte für Rot, Grün und Blau. Der erste Parameter ist der Alphawert, der den Umfang angibt, in dem die gezeichnete Farbe mit der Hintergrundfarbe gemischt wird.

## <a name="constructing-regions"></a>Erstellen von Regionen

GDI bietet mehrere Funktionen zum Erstellen von Regionen: CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn und CreatePolyPolygonRgn. Möglicherweise erwarten Sie, dass die [**Region-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) in GDI+ analoge Konstruktoren hat, die Rechtecke, Ellipsen, abgerundete Rechtecke und Polygone als Argumente verwenden. Dies ist jedoch nicht der Fall. Die **Region-Klasse** in GDI+ einen Konstruktor, der einen [**Rect-Objektverweis**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) empfängt, und einen anderen Konstruktor, der die Adresse eines [**GraphicsPath-Objekts**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) empfängt. Wenn Sie einen Bereich auf Der Grundlage einer Ellipse, eines abgerundeten Rechtecks oder eines Polygons erstellen möchten, können Sie dies problemlos tun, indem Sie ein **GraphicsPath-Objekt** (das z. B. eine Ellipse enthält) erstellen und dann die Adresse dieses **GraphicsPath-Objekts** an einen **Region-Konstruktor** übergeben.

GDI+ einfaches Erstellen komplexer Bereiche durch Kombinieren von Formen und Pfaden. Die [**Region-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) verfügt [über Union-](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) und [Intersect-Methoden,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) die Sie verwenden können, um eine vorhandene Region mit einem Pfad oder einer anderen Region zu vergrößern. Ein gutes Feature des GDI+ ist, dass ein [**GraphicsPath-Objekt**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) nicht zerstört wird, wenn es als Argument an einen **Region-Konstruktor übergeben** wird. In GDI können Sie einen Pfad mit der [PathToRegion-Funktion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) in eine Region konvertieren, aber der Pfad wird im Prozess zerstört. Außerdem wird ein **GraphicsPath-Objekt** nicht zerstört, wenn seine Adresse als Argument an eine Union- oder Intersect-Methode übergeben wird, sodass Sie einen bestimmten Pfad als Baustein für mehrere separate Regionen verwenden können. Dies wird im folgenden Beispiel gezeigt. Angenommen, **onePath** ist ein Zeiger auf ein **GraphicsPath-Objekt** (einfach oder komplex), das bereits initialisiert wurde.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
