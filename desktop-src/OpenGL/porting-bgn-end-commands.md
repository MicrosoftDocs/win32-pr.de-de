---
title: Portieren von bgn/end-Befehlen
description: IRIS GL verwendet das Start-/Endparadigma, verfügt aber über eine andere Funktion für jedes primitive Grafikelement.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- IRIS GL-Portierung, Bgn-/Endbefehle
- Portieren von IRIS GL,bgn/end-Befehlen
- Portieren von IRIS GL,bgn/end-Befehlen zu OpenGL
- OpenGL-Portierung von IRIS GL,bgn/end-Befehlen
- Zeichnungsfunktionen, Bgn-/Endbefehle
- bgn/end-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63084b1f05d984fdc19254edaadaca9098d13f974a433f5c6ff7c5d370ec223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485970"
---
# <a name="porting-bgnend-commands"></a>Portieren von bgn/end-Befehlen

IRIS GL verwendet das Start-/Endparadigma, verfügt aber über eine andere Funktion für jedes primitive Grafikelement. Beispielsweise verwenden Sie wahrscheinlich **bgnpolygon** und **endpolygon,** um Polygone zu zeichnen, und **bgnline** und **endline,** um Linien zu zeichnen. In OpenGL verwenden Sie die [**glBegin**](glbegin.md)  /  [**glEnd-Struktur**](glend.md) für beide. In OpenGL zeichnen Sie die meisten geometrischen Objekte, indem Sie eine Reihe von Funktionen einschließen, die Scheitelpunkte, Normalitäten, Texturen und Farben zwischen Paaren von **glBegin-** und **glEnd-Aufrufen** angeben. Beispiel:

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

Die **glBegin-Funktion** verwendet einen einzelnen Parameter, der den Zeichnungsmodus und somit den Primitiven angibt. Hier sehen Sie ein OpenGL-Codebeispiel, das ein Polygon und dann eine Linie zeichnet:

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

Mit OpenGL zeichnen Sie verschiedene geometrische Objekte, indem Sie unterschiedliche Parameter für [**glBegin**](glbegin.md)angeben. In der folgenden Tabelle sind die OpenGL **glBegin-Parameter** aufgeführt, die entsprechenden IRIS GL-Funktionen entsprechen.



| IRIS GL-Funktion  | Wert des glBegin-Modus | Bedeutung                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | GL \_ POINTS            | Einzelne Punkte.                                                                       |
| **bgnline**       | GL \_ LINE \_ STRIP       | Reihe verbundener Liniensegmente.                                                       |
| **bgnclosedline** | GL \_ LINE \_ LOOP        | Reihe verbundener Liniensegmente, wobei ein Segment zwischen dem ersten und dem letzten Scheitelpunkt hinzugefügt wird. |
|                   | GL \_ LINES             | Paare von Scheitelpunkten, die als einzelne Liniensegmente interpretiert werden.                               |
| **bgnpolygon**    | \_GL-POLYGON           | Begrenzung eines einfachen konvexen Polygons.                                                     |
|                   | GL \_ TRIANGLES         | Triples von Scheitelpunkten, die als Dreiecke interpretiert werden.                                            |
| **bgntmesh**      | GL \_ TRIANGLE \_ STRIP   | Verknüpfte Dreiecksstreifen.                                                              |
|                   | GL \_ TRIANGLE \_ FAN     | Verknüpfte Lüfter von Dreiecken.                                                                |
|                   | GL \_ QUADS             | Quadruples von Scheitelpunkten, die als Quaderaterale interpretiert werden.                                    |
| **bgnqstrip**     | GL \_ QUAD \_ STRIP       | Verknüpfte Quaderateralstrips.                                                         |



 

Eine ausführliche Erläuterung der Unterschiede zwischen Dreiecksgittern, Strips und Lüftern finden Sie unter [Portieren von Dreiecken.](porting-triangles.md)

Es gibt keine Beschränkung für die Anzahl der Scheitelpunkte, die Sie zwischen einem [**glBegin**](glbegin.md)  /  [**glEnd-Paar**](glend.md) angeben können.

Zusätzlich zur Angabe von Scheitelpunkten innerhalb eines **glBegin**  /  **glEnd-Paars** können Sie eine aktuelle Normalität, aktuelle Texturkoordinaten und eine aktuelle Farbe angeben. In der folgenden Tabelle sind die Befehle aufgeführt, die innerhalb eines **glBegin**  /  **glEnd-Paars** gültig sind.



| IRIS GL-Funktion        | OpenGL-Funktion                                                      | Bedeutung                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2,** **v3,** **v4**  | [glVertex](glvertex-functions.md)                                   | Legt Scheitelpunktkoordinaten fest.                         |
| **RGBcolor**, **cpack** | [glColor](glcolor-functions.md)                                     | Legt die aktuelle Farbe fest.                              |
| **color**               | [glIndex](glindex-functions.md)                                     | Legt den aktuellen Farbindex fest.                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | Legt normale Vektorkoordinaten fest.                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | Wertet aktivierte ein- und zweidimensionale Zuordnungen aus. |
| **callobj**             | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Führt Anzeigelisten aus.                        |
| **t2**                  | [glTexCoord](gltexcoord-functions.md)                               | Legt Texturkoordinaten fest.                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | Steuert das Zeichnen von Rändern.                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | Legt Materialeigenschaften fest.                        |



 

> [!Note]
>
> Wenn Sie eine andere OpenGL-Funktion als die in der vorherigen Tabelle aufgeführten in einem [**glBegin**](glbegin.md)  /  [**glEnd-Paar**](glend.md) verwenden, erhalten Sie unvorhersehbare Ergebnisse oder möglicherweise einen Fehler.

 

 

 




