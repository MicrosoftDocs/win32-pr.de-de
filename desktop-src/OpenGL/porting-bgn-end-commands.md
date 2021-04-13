---
title: Portieren von BGN-/End-Befehlen
description: IRIS GL verwendet das Begin/End-Paradigma, verfügt aber über eine andere Funktion für jede Grafik primitive.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- IRIS GL Porting, BGN/End-Befehle
- Portieren von IRIS GL, BGN/End-Befehlen
- Portieren auf OpenGL von IRIS GL, BGN/End-Befehlen
- OpenGL-Portierung von IRIS GL, BGN/End-Befehlen
- Zeichenfunktionen, BGN/End-Befehle
- BGN-/End-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388631"
---
# <a name="porting-bgnend-commands"></a>Portieren von BGN-/End-Befehlen

IRIS GL verwendet das Begin/End-Paradigma, verfügt aber über eine andere Funktion für jede Grafik primitive. Beispielsweise verwenden Sie ggf. **bgnpolygon** und **endpolygon** , um Polygone zu zeichnen, und **bgnline** und **EndLine** zum Zeichnen von Linien. In OpenGL verwenden Sie die [**glBegin**](glbegin.md)-  /  [**glEnd**](glend.md) -Struktur für beide. In OpenGL zeichnen Sie die meisten geometrischen Objekte durch Einschließen einer Reihe von Funktionen, die Scheitel Punkte, normale, Texturen und Farben zwischen Paaren von **glBegin** -und **glEnd** -aufrufen angeben. Beispiel:

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

Die **glBegin** -Funktion nimmt einen einzelnen Parameter an, der den Zeichnungsmodus und somit den primitiven angibt. Hier sehen Sie ein OpenGL-Codebeispiel, das ein Polygon und eine Zeile zeichnet:

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

Mit OpenGL zeichnen Sie verschiedene geometrische Objekte, indem Sie verschiedene Parameter für [**glBegin**](glbegin.md)angeben. In der folgenden Tabelle sind die OpenGL- **glBegin** -Parameter aufgeführt, die äquivalenten IRIS GL-Funktionen entsprechen.



| IRIS GL-Funktion  | Wert des glBegin-Modus | Bedeutung                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | GL- \_ Punkte            | Einzelne Punkte.                                                                       |
| **bgnline**       | GL- \_ Zeilen \_ Streifen       | Reihe verbundener Liniensegmente.                                                       |
| **bgnclosedline** | GL- \_ Zeilen \_ Schleife        | Eine Reihe verbundener Liniensegmente, wobei ein Segment zwischen der ersten und letzten Vertices hinzugefügt wird. |
|                   | GL- \_ Zeilen             | Paare von Vertices, die als einzelne Liniensegmente interpretiert werden.                               |
| **bgnpolygon**    | GL- \_ Polygon           | Grenze eines einfachen, zusammen gevexen Polygons.                                                     |
|                   | GL- \_ Dreiecke         | Die als Dreiecke interpretierten Scheitel Punkte.                                            |
| **bgntmesh**      | GL- \_ Dreiecks \_ Streifen   | Verknüpfte Streifen von Dreiecken.                                                              |
|                   | GL- \_ Dreiecks \_ Lüfter     | Verknüpfte Fans von Dreiecken.                                                                |
|                   | GL \_ .             | Vierbeiner von Vertices, die als viereckale interpretiert werden.                                    |
| **bgnqstrip**     | GL \_ Quad \_ Strip       | Verknüpfte Streifen von viereckalen.                                                         |



 

Eine ausführliche Erläuterung der Unterschiede zwischen Dreiecksnetzen, Streifen und Lüfter finden Sie unter [Portieren von Dreiecken](porting-triangles.md).

Es gibt keine Beschränkung für die Anzahl der Scheitel Punkte, die zwischen einem [**glBegin**](glbegin.md)-  /  [**glEnd**](glend.md) -Paar angegeben werden können.

Zusätzlich zum Angeben von Vertices in einem **glBegin**-  /  **glEnd** -paar können Sie eine aktuelle normale, aktuelle Textur Koordinate und eine aktuelle Farbe angeben. In der folgenden Tabelle sind die in einem **glBegin**-  /  **glEnd** -paar gültigen Befehle aufgeführt.



| IRIS GL-Funktion        | OpenGL-Funktion                                                      | Bedeutung                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2**, **V3**, **V4**  | [glVertex](glvertex-functions.md)                                   | Legt Scheitelpunkt Koordinaten fest.                         |
| **RGBColor**, **CPack** | [glcolor](glcolor-functions.md)                                     | Legt die aktuelle Farbe fest.                              |
| **color**               | [glindex](glindex-functions.md)                                     | Legt den aktuellen Farbindex fest.                        |
| **n3f**                 | [glnormal](glnormal-functions.md)                                   | Legt normale Vektor Koordinaten fest.                  |
|                         | [glevalcoord](glevalcoord-functions.md)                             | Wertet aktivierte ein-und zweidimensionale Zuordnungen aus. |
| **czuweisung**             | [**glCallList**](glcalllist.md), [ **glcalllists**](glcalllists.md) | Führt Anzeigelisten aus.                        |
| **T2**                  | [gltexcoord](gltexcoord-functions.md)                               | Legt Texturkoordinaten fest.                        |
|                         | [gledgeflag](gledgeflag-functions.md)                               | Steuert Zeichnungs Kanten.                          |
| **lmbind**              | [glmaterial](glmaterial-functions.md)                               | Legt Materialeigenschaften fest.                        |



 

> [!Note]
>
> Wenn Sie eine andere als die in der obigen Tabelle aufgeführten OpenGL-Funktionen in einem [**glBegin**](glbegin.md)-  /  [**glEnd**](glend.md) -paar verwenden, erhalten Sie unvorhersehbare Ergebnisse oder möglicherweise einen Fehler.

 

 

 




