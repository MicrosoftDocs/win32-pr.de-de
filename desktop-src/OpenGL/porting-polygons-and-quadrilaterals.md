---
title: Portieren von Polygonen und Quadrieren
description: Beachten Sie beim Portieren von Polygonen und Quadrierten die folgenden Punkte.
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- IRIS GL-Portierung, Quadrierung
- Portieren von IRIS GL,quadralrals
- Portieren von IRIS GL,quadrataterals zu OpenGL
- OpenGL-Portierung von IRIS GL,quadrataterals
- Zeichnungsfunktionen,quadralrals
- quadrals
- IRIS GL-Portierung, Polygone
- Portieren von IRIS GL,Polygonen
- Portieren von IRIS GL,Polygonen zu OpenGL
- OpenGL-Portierung von IRIS GL,Polygonen
- Zeichnungsfunktionen,Polygone
- Polygone,Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908458"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Portieren von Polygonen und Quadrieren

Beachten Sie beim Portieren von Polygonen und Quadrieren die folgenden Punkte:

-   Es gibt kein direktes Äquivalent für **Konkave**(**TRUE**). Stattdessen können Sie die Mosaikroutinen in der GLU verwenden, die unter [Mosaikpolygone beschrieben sind.](tessellating-polygons.md)
-   Polygonmodi werden unterschiedlich festgelegt.
-   Diese Polygonzeichnungsfunktionen haben keine direkten Entsprechungen in OpenGL: die **Polyfamilie** von Routinen; die **Polf-Familie** von Routinen; **pmv**, **pdr** und **pclos**; **rpmv** und **rpdr**; **splf**; und **spclos**.

Wenn Ihr IRIS GL-Code diese Funktionen verwendet, müssen Sie den Code mit [**glBegin**](glbegin.md)( GL \_ POLYGON ) umschreiben.

In der folgenden Tabelle sind die IRIS GL-Polygonzeichnungsfunktionen und ihre entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion         | OpenGL-Funktion                                                    | Bedeutung                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) ( GL \_ POLYGON )[**glEnd**](glend.md)   | Scheitelpunkte definieren die Grenze eines einfachen konvexen Polygons.    |
|                          | **glBegin**( GL \_ QUADS )**glEnd**<br/>                       | Interpretiert Quadruples von Scheitelpunkten als Quaderaterale.    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) ( GL \_ QUAD STRIP ) \_ **glEnd**<br/> | Interpretiert Scheitelpunkte als verknüpfte Stripes von Quaderateralen. |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **polymode**             | [**glPolygonMode**](glpolygonmode.md)                             | Legt den Polygonzeichnungsmodus fest.                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | Zeichnet ein Rechteck.                                      |
| **sboxsboxf**<br/> |                                                                    | Zeichnet ein am Bildschirm ausgerichtetes Rechteck.                       |



 

??

## <a name="porting-polygon-modes"></a>Portieren von Polygonmodi

Mit der [**OpenGL-Funktion glPolygonMode**](glpolygonmode.md) können Sie angeben, auf welche Seite eines Polygons (die Rückseite oder die Vorderseite) der Modus angewendet wird. Die Syntax sieht wie folgt aus:

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

dabei ist das Gesicht eines der:



|GLenum-Wert                      |  Bedeutung                                                          |
|----------------------|------------------------------------------------------------|
| GL \_ FRONT            | -Modus, der für nach vorne gerichtete Polygone gilt                |
| GL \_ BACK             | -Modus, der für nach hinten gerichtete Polygone gilt                 |
| GL \_ FRONT \_ AND \_ BACK | -Modus, der sowohl für front- als auch für hintere Polygone gilt. |



 

Der GL \_ FRONT \_ AND \_ BACK-Modus entspricht der **POLYMODE-Funktion** IRIS GL. In der folgenden Tabelle sind die IRIS GL-Polygonmodi und die entsprechenden OpenGL-Modi aufgeführt.



| IRIS GL-Modus | OpenGL-Modus | Bedeutung                                       |
|--------------|-------------|-----------------------------------------------|
| \_PYM-PUNKT   | GL \_ POINT   | Zeichnet Scheitelpunkte als Punkte.                     |
| PYM \_ LINE    | GL \_ LINE    | Zeichnet Begrenzungsränder als Liniensegmente.        |
| PYM \_ FILL    | GL \_ FILL    | Zeichnet polygoneinnere Flächen.                |
| \_PYM-ENTHMUS  |             | Füllt nur innere Pixel an den Grenzen aus. |



 

## <a name="porting-polygon-stipples"></a>Portieren von Polygonstipples

Beachten Sie beim Portieren von IRIS GL-Polygonstipples die folgenden Punkte:

-   OpenGL verwendet keine Tabellen für Polygonstipples. es wird nur ein Stipplemuster beibehalten. Sie können Anzeigelisten verwenden, um verschiedene Stipplemuster zu speichern.
-   Die Bitmapgröße der OpenGL-Polygonstipple ist immer ein 32 x 32-Bit-Muster.
-   Die Stipplecodierung wird von [**glPixelStore**](glpixelstore-functions.md)beeinflusst.

Weitere Informationen zum Portieren von Polygonstipples finden Sie unter [Portieren von Pixelvorgängen.](porting-pixel-operations.md)

In der folgenden Tabelle sind IRIS GL-Polygonspitzenfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                                    | Bedeutung                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | Legt das Stipplemuster fest.                             |
| **setpattern**   |                                                    | OpenGL behält nur ein Polygonstipplemuster bei.        |
| **getpattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | Gibt die Ausschnittbitmap zurück (wird verwendet, um einen Index zurückgibt). |



 

In OpenGL aktivieren und deaktivieren Sie polygonische Ausschnitte, indem Sie GL POLYGON STIPPLE als Parameter für \_ \_ [**glEnable**](glenable.md) und [**glDisable übergeben.**](gldisable.md)

Im folgenden OpenGL-Codebeispiel wird das Ausschnitten von Polygonen veranschaulicht:


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



## <a name="porting-tessellated-polygons"></a>Portieren von Mosaikpolygonen

In IRIS GL verwenden Sie **concave**(**TRUE**) und dann **bgnpolygon,** um konkave Polygone zu zeichnen. OpenGL GLU enthält Funktionen, mit derenHilfe Sie konkave Polygone zeichnen können.

**So zeichnen Sie ein konkaves Polygon mit OpenGL**

1.  Erstellen Sie ein Mosaikobjekt.
2.  Definieren Sie Rückrufe, die verwendet werden, um die vom Mosaik generierten Dreiecke zu verarbeiten.
3.  Geben Sie das konkave Polygon an, für das ein Mosaik erstellt werden soll.

In der folgenden Tabelle sind die OpenGL-Funktionen zum Zeichnen von Mosaikpolygonen aufgeführt.



| OpenGL-GLU-Funktion                        | Bedeutung                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | Erstellt ein neues Mosaikobjekt.                                 |
| [**gluDeleteTess**](gludeletetess.md)     | Löscht ein Mosaikobjekt.                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | Beginnt die Polygonspezifikation.                                  |
| [**gluTessVertex**](glutessvertex.md)     | Gibt einen Polygonvertex in einer Kontur an.                           |
| [**gluNextContour**](glunextcontour.md)   | Gibt an, dass die nächste Reihe von Scheitelpunkten eine neue Kontur beschreibt. |
| [**gluEndPolygon**](gluendpolygon.md)     | Beendet die Polygonspezifikation.                                    |



 

 

 





