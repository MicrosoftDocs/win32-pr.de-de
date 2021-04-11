---
title: Portieren von tiefen Cube-und Nebel Befehlen
description: Portieren von tiefen Cube-und Nebel Befehlen
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- IRIS GL portieren, Tiefe Cueing
- Portieren von IRIS GL, Tiefe Cueing
- Portieren auf OpenGL von IRIS GL, Tiefe Cueing
- OpenGL-Portierung von IRIS GL, Tiefe Cueing
- IRIS GL portieren, Nebel
- Portieren von IRIS GL, Nebel
- Portieren auf OpenGL von IRIS GL, Nebel
- OpenGL-Portierung von IRIS GL, Nebel
- tiefen Cueing
- Nebel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207153"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>Portieren von tiefen Cube-und Nebel Befehlen

Beachten Sie beim Portieren von tiefen-und Nebel Befehlen die folgenden Punkte:

-   Der Iris GL-Befehl, **fogvertex**, legt einen Modus und die Parameter fest, die diesen Modus beeinflussen. In OpenGL wird [**glfog**](glfog.md) einmal aufgerufen, um den Modus festzulegen, und dann zweimal oder mehr, um verschiedene Parameter festzulegen.
-   In OpenGL handelt es sich bei der tiefen Kürzung nicht um ein separates Feature. Verwenden Sie lineare Nebel anstelle der Tiefe der Tiefe. (Dieser Abschnitt enthält ein Beispiel dazu, wie Sie dies tun können.) Die folgenden IRIS GL-Funktionen haben keine direkte OpenGL-Entsprechung:

    **Depthcue**

    **lrgbrange**

    **lshaderange**

    **getdcm**

-   Verwenden Sie zum Anpassen der Nebel Qualität [**glhint**](glhint.md)(GL- \_ Nebel \_ Hinweis).

In der folgenden Tabelle werden die Iris GL-Funktionen für die Verwaltung von Nebel und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion         | OpenGL-Funktion                                     | Bedeutung                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **fogvertex**            | [**glnebel**](glfog.md)                              | Legt verschiedene Nebel Parameter fest.      |
| **fogvertex**(FG \_ auf)  | [**glEnable**](glenable.md) (GL- \_ Nebel)            | Schaltet den Nebel ein.                     |
| **fogvertex**(FG \_ Off) | [**gldeaktiviert**](gldisable.md) (GL- \_ Nebel)          | Schaltet den Nebel aus.                    |
| **Depthcue**             | [**glnebel**](glfog.md) (GL \_ Nebel \_ mod, GL \_ linear) | Verwendet linearen Nebel zum Durchsuchen der Tiefe. |



 

In der folgenden Tabelle sind die Parameter aufgeführt, die Sie an **glnebel** übergeben können.



| Nebel Parameter    | Bedeutung                       | Standard                  |
|------------------|-------------------------------|--------------------------|
| GL- \_ Nebel \_ Dichte | Nebeldichte.                  | 1.0                      |
| GL. \_ Nebel \_ Anfang   | Fast Distance für linearen Nebel. | 0,0                      |
| GL- \_ Nebel \_ Ende     | Weit Entfernungs Abstand für linearen Nebel.  | 1.0                      |
| GL- \_ Nebel \_ Index   | Nebel Farbindex.              | 0,0                      |
| GL- \_ Nebel \_ Farbe   | RGBA-Farbe des NEMS.               | (0, 0, 0, 0)             |
| GL- \_ Nebel \_ Modus    | Nebelmodus.                     | Siehe hierzu die folgende Tabelle. |



 

Der Parameter für die Nebeldichte von OpenGL unterscheidet sich von dem in IRIS GL. Sie sind wie folgt verknüpft:

-   If *FogMode* = exp2
     

    *openglfogdensity* = (*irisglfogdensity* ) ( **sqrt** ( **Log** (1/255)))
-   If *FogMode* = Exp
     

    *openglfogdensity* = (*irisglfogdensity* ) ( **Protokoll** (1/255))

Wenn **sqrt** der Quadratwurzel Vorgang ist, ist **Log** der natürliche Logarithmus, *irisglfogdensity* ist die Schwert Dichte IRIS GL, und *openglfogdensity* ist die OpenGL-Nebeldichte.

Verwenden Sie [**glhint**](glhint.md)(GL- \_ Nebel \_ Hinweis, *hintmode*), um zwischen dem Berechnen von Nebel im Pixel-und pro-Vertex-Modus zu wechseln. Zwei Hinweis Modi sind verfügbar:

-   GL \_ schönste Berechnung pro Pixel-Nebel
-   GL \_ schnellste Berechnung pro Vertex-Nebel

In der folgenden Tabelle sind die Iris GL-Nebel Modi und ihre OpenGL-Entsprechungen aufgelistet.



| IRIS GL-Nebel Modus                       | OpenGL-Nebel Modus | Hinweis Modus                         | Bedeutung                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ VTX \_ Exp, FG \_ pix \_ Exp<br/>   | GL- \_ Exp         | GL \_ schnellste, GL am \_ schönsten<br/> | Starker Nebel Modus (Standard).                |
| FG \_ VTX \_ exp2, FG \_ pix \_ exp2<br/> | GL \_ exp2        | GL \_ schnellste, GL am \_ schönsten<br/> | Dunst Modus.                               |
| FG \_ VTX \_ Lin, FG \_ pix \_ Lin<br/>   | GL \_ linear      | GL \_ schnellste, GL am \_ schönsten<br/> | Linearer Nebel Modus. (Für die tiefen Cube.) |



 

Im folgenden Codebeispiel wird die Tiefe in OpenGL veranschaulicht:


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





