---
title: Portieren von Polygonen und vier eckalen
description: 'Beachten Sie beim Portieren von Polygonen und Vierecken die folgenden Punkte:'
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- IRIS GL portieren, viereckale
- Portieren von IRIS GL, viereckals
- Portieren auf OpenGL von IRIS GL, viereckals
- OpenGL-Portierung von IRIS GL, viereckals
- Zeichnungsfunktionen, viereckale
- viereckale
- IRIS GL portieren, Polygone
- Portieren von IRIS GL, Polygone
- Portieren auf OpenGL von IRIS GL, Polygone
- OpenGL-Portierung von IRIS GL, Polygone
- Zeichnungsfunktionen, Polygone
- Polygone, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712503"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Portieren von Polygonen und vier eckalen

Beachten Sie beim Portieren von Polygonen und Vierecken die folgenden Punkte:

-   Es gibt keine direkte Entsprechung für die **Konstante (****true**). Stattdessen können Sie die Mosaik Routinen in der-Datei verwenden, die unter Mosaik [Polygone](tessellating-polygons.md)beschrieben wird.
-   Polygon Modi werden unterschiedlich festgelegt.
-   Diese Polygon Zeichnungsfunktionen verfügen über keine direkten Entsprechungen in OpenGL: die **polyfamilie** von Routinen. die **POLF** -Familie von Routinen. **pmv**, **PDR** und **PCLOS**; **rpmv** und **rpdr**; **splf**; und **spclos**.

Wenn Ihr IRIS GL-Code diese Funktionen verwendet, müssen Sie den Code mithilfe von [**glBegin**](glbegin.md)(GL \_ Polygon) neu schreiben.

In der folgenden Tabelle sind die Funktionen des IRIS GL-Polygons und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion         | OpenGL-Funktion                                                    | Bedeutung                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) (GL \_ Polygon)[**glEnd**](glend.md)   | Vertices definieren die Begrenzung eines einfachen, zusammen gevexen Polygons.    |
|                          | **glBegin**(GL \_ QUADS)**glEnd**<br/>                       | Interpretiert Vierbeiner von Vertices als viereckale.    |
| **bgnqstripdqstrip**   | [**glBegin**](glbegin.md) (GL \_ Quad \_ Strip)<br/> | Interpretiert Scheitel Punkte als verknüpfte Streifen von Vierecken. |
|                          | [gledgeflag](gledgeflag-functions.md)                             |                                                         |
| **polymode**             | [**glpolygonmode**](glpolygonmode.md)                             | Legt den Polygon Zeichnungsmodus fest.                              |
| **rectrectf**<br/> | [glrect](glrect-functions.md)                                     | Zeichnet ein Rechteck.                                      |
| **sboxsboxf**<br/> |                                                                    | Zeichnet ein Bildschirm gerichtetes Rechteck.                       |



 

??

## <a name="porting-polygon-modes"></a>Portieren von Polygon Modi

Mit der OpenGL-Funktion " [**glpolygonmode**](glpolygonmode.md) " können Sie angeben, für welche Seite eines Polygons der Modus gilt. Die Syntax sieht wie folgt aus:

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

Dabei ist "Face" eines von:



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| GL. \_ Front            | Modus, der sich auf Front-on-Polygone bezieht                |
| GL \_ zurück             | Modus, der auf Polygone mit Rückstand angewendet wird                 |
| GL \_ vor \_ und \_ zurück | der Modus, der sowohl für Front-als auch für rückwärts gerichtete Polygone gilt. |



 

Der GL \_ \_ -Front-und- \_ Back-Modus entspricht der Iris GL **polymode** -Funktion. In der folgenden Tabelle sind die Iris GL-Polygon Modi und ihre entsprechenden OpenGL-Modi aufgeführt.



| IRIS GL-Modus | OpenGL-Modus | Bedeutung                                       |
|--------------|-------------|-----------------------------------------------|
| Pym- \_ Punkt   | GL- \_ Punkt   | Zeichnet Vertices als Punkte.                     |
| Pym- \_ Linie    | GL- \_ Zeile    | Zeichnet Begrenzungs Kanten als Liniensegmente.        |
| Pym- \_ Füllung    | Ausfüllen von GL \_    | Zeichnet Polygon-innere, gefüllt.                |
| Pym- \_ hohl  |             | Füllt nur innere Pixel an den Grenzen. |



 

## <a name="porting-polygon-stipples"></a>Portieren von Polygon-Stipeln

Beachten Sie beim Portieren von IRIS GL-Polygon-Stipeln die folgenden Punkte:

-   OpenGL verwendet keine Tabellen für Polygon-Stippel. Es wird nur ein stippingmuster beibehalten. Mit Anzeigelisten können Sie unterschiedliche stippmuster speichern.
-   Die Größe des OpenGL-Polygon-stippingbitmusters ist immer ein 32-Bit-32-Bit-Bit
-   Die Stippel Codierung ist von [**glpixelstore**](glpixelstore-functions.md)betroffen.

Weitere Informationen zum Portieren von Polygon-Stipeln finden Sie unter [Portieren von Pixel Vorgängen](porting-pixel-operations.md).

In der folgenden Tabelle sind die Funktionen von IRIS GL Polygon Stippel und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion | OpenGL-Funktion                                    | Bedeutung                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glpolygonstippel**](glpolygonstipple.md)       | Legt das Stippel Muster fest.                             |
| **SetPattern**   |                                                    | OpenGL behält nur ein Polygon-stippingmuster bei.        |
| **GetPattern**   | [**glgetpolygonstippel**](glgetpolygonstipple.md) | Gibt die Stippel Bitmap zurück (die zum Zurückgeben eines Indexes verwendet wird). |



 

In OpenGL aktivieren und deaktivieren Sie Polygon-stippling, indem Sie den GL \_ \_ -Polygon-Stippel als Parameter für [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md)übergeben.

Im folgenden OpenGL-Codebeispiel wird das Polygon-stippling veranschaulicht:


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a>Portieren von Mosaik Polygonen

In IRIS GL verwenden Sie die **Konfigurations**-und **bgnpolygon-Objekte** (**true**) und dann bgnpolygon. Der OpenGL-glu enthält Funktionen, die Sie zum Zeichnen von zwischen-Polygonen verwenden können.

**So zeichnen Sie ein-und-Polygon-Polygon**

1.  Erstellen Sie ein Mosaik Objekt.
2.  Definieren Sie Rückrufe, die zum Verarbeiten der vom Mosaik Prozess generierten Dreiecke verwendet werden.
3.  Geben Sie das zu Mosaik Ende Konstante Polygon an.

In der folgenden Tabelle werden die OpenGL-Funktionen zum Zeichnen von Mosaik Polygonen aufgelistet.



| OpenGL glu-Funktion                        | Bedeutung                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**glunewtess**](glunewtess.md)           | Erstellt ein neues Mosaik Objekt.                                 |
| [**gludeletetess**](gludeletetess.md)     | Löscht ein Mosaik Objekt.                                     |
| [*glutesscallback*](glutess.md)           |                                                                    |
| [**glubeginpolygon**](glubeginpolygon.md) | Beginnt die Polygon Spezifikation.                                  |
| [**glutess Vertex**](glutessvertex.md)     | Gibt einen Polygon Scheitelpunkt in einer Kontur an.                           |
| [**glunextcontour**](glunextcontour.md)   | Gibt an, dass die nächste Reihe von Vertices eine neue Kontur beschreiben. |
| [**gluendpolygon**](gluendpolygon.md)     | Beendet die Polygon Spezifikation.                                    |



 

 

 





