---
title: Portieren von NURBS-Oberflächen
description: In der folgenden Tabelle sind die IRIS GL-Funktionen zum Zeichnen von NURBS-Oberflächen und die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: d34ac6af-55d7-4128-bcd9-3c910607895f
keywords:
- IRIS GL-Portierung, NURBS-Oberflächen
- Portieren von IRIS GL,NURBS-Oberflächen
- Portieren von IRIS GL-, NURBS-Oberflächen zu OpenGL
- OpenGL-Portierung von IRIS GL,NURBS-Oberflächen
- NURBS-Oberflächen
- NURBS (Non-Uniform Rational B-Spline)
- Non-Uniform Rational B-Spline (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a57de3a3b413d909ed034e9d355f4099c196a89b1e7ed93a69fe99ea72fca54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132349"
---
# <a name="porting-nurbs-surfaces"></a>Portieren von NURBS-Oberflächen

In der folgenden Tabelle sind die IRIS GL-Funktionen zum Zeichnen von NURBS-Oberflächen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                            | Bedeutung                       |
|------------------|--------------------------------------------|-------------------------------|
| **bgnsurface**   | [**gluBeginSurface**](glubeginsurface.md) | Beginnt eine Oberflächendefinition.  |
| **nurbssurface** | [**gluNurbsSurface**](glunurbssurface.md) | Gibt Oberflächenattribute an. |
| **endsurface**   | [**gluEndSurface**](gluendsurface.md)     | Beendet eine Oberflächendefinition.    |



 

In der folgenden Tabelle sind IRIS GL-Parameter für Oberflächentypen und die entsprechenden OpenGL-Parameter aufgeführt.



| IRIS GL-Typ | OpenGL-Typ                 | Bedeutung                                                |
|--------------|-----------------------------|--------------------------------------------------------|
| N \_ V3D       | GL \_ MAP2 \_ VERTEX \_ 3         | Polynomiale Kurve.                                      |
| N \_ V3DR      | GL \_ MAP2 \_ VERTEX \_ 4         | Rationale Kurve.                                        |
| N \_ C4D       | GL \_ MAP2 \_ COLOR \_ 4          | Kontrollpunkte definieren die Farboberfläche im Formular (R, G, B, A). |
| N \_ C4DR      |                             |                                                        |
| N \_ T2D       | GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2 | Kontrollpunkte sind Texturkoordinaten.                |
| N \_ T2DR      | GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3 | Kontrollpunkte sind Texturkoordinaten.                |
|              | GL \_ MAP2 \_ NORMAL            | Kontrollpunkte sind Normals.                            |



 

Weitere Informationen zu verfügbaren Auswertungstypen finden Sie unter [**glMap2**](glmap2.md).

Im folgenden Codebeispiel wird eine gekürzte NURBS-Oberfläche ge zeichnet:


```C++
/* 
 *  trim.c 
 *  This program draws a NURBS surface in the shape of a 
 *  symmetrical hill, using both a NURBS curve and pwl 
 *  (piecewise linear) curve to trim part of the surface 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
GLfloat ctlpoints[4][4][3]; 
 
GLUnurbsObj *theNurb; 
 
/* 
 *  Initializes the control points of the surface to  
 *  a small hill. The control points range from -3 to  
 *  +3 in x, y, and z 
 */ 
void init_surface(void) 
{ 
    int u, v; 
    for (u = 0; u < 4; u++) { 
        for (v = 0; v < 4; v++) { 
            ctlpoints[u][v][0] = 2.0*((GLfloat)u - 1.5); 
            ctlpoints[u][v][1] = 2.0*((GLfloat)v - 1.5); 
 
            if ( (u == 1 || u == 2) && (v == 1 || v == 2)) 
                ctlpoints[u][v][2] = 3.0; 
            else 
                ctlpoints[u][v][2] = -3.0; 
        } 
    } 
} 
 
/*  Initialize material property and depth buffer 
 */ 
void myinit(void) 
{ 
    GLfloat mat_diffuse[] = { 0.6, 0.6, 0.6, 1.0 }; 
    GLfloat mat_specular[] = { 0.9, 0.9, 0.9, 1.0 }; 
    GLfloat mat_shininess[] = { 128.0 }; 
 
    glClearColor (0.0, 0.0, 0.0, 1.0); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_diffuse); 
    glMaterialfv(GL_FRONT, GL_SPECULAR, mat_specular); 
    glMaterialfv(GL_FRONT, GL_SHININESS, mat_shininess); 
 
    glEnable(GL_LIGHTING); 
    glEnable(GL_LIGHT0); 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glEnable(GL_AUTO_NORMAL); 
    glEnable(GL_NORMALIZE); 
 
    init_surface(); 
 
    theNurb = gluNewNurbsRenderer(); 
    gluNurbsProperty(theNurb, GLU_SAMPLING_TOLERANCE, 50.0); 
    gluNurbsProperty(theNurb, GLU_DISPLAY_MODE, GLU_FILL); 
} 
 
void display(void) 
{ 
    GLfloat knots[8] = {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat edgePt[5][2] = /* counter clockwise */ 
    {{0.0, 0.0}, {1.0, 0.0}, {1.0, 1.0}, {0.0, 1.0}, 
     {0.0, 0.0}}; 
    GLfloat curvePt[4][2] = /* clockwise */ 
    {{0.25, 0.5}, {0.25, 0.75}, {0.75, 0.75}, {0.75, 0.5}}; 
    GLfloat curveKnots[8] = 
        {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat pwlPt[4][2] = /* clockwise */ 
        {{0.75, 0.5}, {0.5, 0.25}, {0.25, 0.5}}; 
 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glPushMatrix(); 
    glRotatef(330.0, 1.,0.,0.); 
    glScalef (0.5, 0.5, 0.5); 
 
    gluBeginSurface(theNurb); 
    gluNurbsSurface(theNurb, 
            8, knots, 
            8, knots, 
            4 * 3, 
            3, 
            &ctlpoints[0][0][0], 
            4, 4, 
            GL_MAP2_VERTEX_3); 
    gluBeginTrim (theNurb); 
        gluPwlCurve (theNurb, 5, &edgePt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluBeginTrim (theNurb); 
        gluNurbsCurve (theNurb, 8, curveKnots, 2, 
                &curvePt[0][0], 4, GLU_MAP1_TRIM_2); 
        gluPwlCurve (theNurb, 3, &pwlPt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluEndSurface(theNurb); 
 
    glPopMatrix(); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLdouble)w/(GLdouble)h, 3.0, 8.0); 
 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity(); 
    glTranslatef (0.0, 0.0, -5.0); 
} 
 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 500, 500); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 




