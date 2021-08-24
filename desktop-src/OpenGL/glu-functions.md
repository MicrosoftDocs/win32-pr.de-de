---
title: GLU-Funktionen
description: GLU-Funktionen
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- OpenGL,GLU-Bibliotheksfunktionen
- OpenGL-Referenz, GLU-Bibliotheksfunktionen
- GLU-Bibliothek, Funktionen
- OpenGL-Hilfsprogramm (GLU), Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4483b364d2d67daff0bbc04b9a30cd7cdb3059f3977f763b247f77be74d62f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777700"
---
# <a name="glu-functions"></a>GLU-Funktionen

Dieser Abschnitt enthält Referenzseiten in alphabetischer Reihenfolge für alle Funktionen der OpenGL-Hilfsprogrammbibliothek. Hintergrundinformationen zu diesen Funktionen finden Sie unter [OpenGL-Hilfsprogrammbibliothek.](opengl-utility-library.md)



| Funktion                                                                                           | Beschreibung                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Trenne eine nicht einheitliche rationale B-Spline-Kurvendefinition[(NURBS).](using-nurbs-curves-and-surfaces.md) |
| [**gluBeginPolygon,**](glubeginpolygon.md) [ **gluEndPolygon**](gluendpolygon.md)                 | Trennzeichen für eine Polygonbeschreibung.                                                                           |
| [**gluBeginSurface,**](glubeginsurface.md) [ **gluEndSurface**](gluendsurface.md)                 | Trennzeichen für eine NURBS-Oberflächendefinition.                                                                      |
| [**gluBeginTrim,**](glubegintrim.md) [ **gluEndTrim**](gluendtrim.md)                             | Trennzeichen für eine NURBS-Kürzungsschleifendefinition.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Erstellt 1D-Mipmaps.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Erstellt 2D-Mipmaps.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Zeichnet einen Zylinder.                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | Zerstört ein NURBS-Objekt.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Zerstört ein quadrisches Objekt.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Zerstört ein Mosaikobjekt.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Zeichnet einen Datenträger.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Erzeugt eine Fehlerzeichenfolge aus einem OpenGL- oder GLU-Fehlercode. Die Fehlerzeichenfolge ist nur ANSI.                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | Ruft eine NURBS-Eigenschaft ab.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Ruft eine Zeichenfolge ab, die die GLU-Versionsnummer oder unterstützte GLU-Erweiterungsaufrufe beschreibt.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Ruft eine Mosaikobjekteigenschaft ab.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Lädt NURBS-Sampling- und Cullingmatrizen.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Definiert eine Anzeigetransformation.                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | Erstellt ein NURBS-Objekt.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Erstellt ein quadrisches -Objekt.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Erstellt ein Mosaikobjekt.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Markiert den Anfang einer anderen Kontur.                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | Definiert einen Rückruf für ein NURBS-Objekt.                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | Definiert die Form einer NURBS-Kurve.                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | Legt eine NURBS-Eigenschaft fest.                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | Definiert die Form einer NURBS-Oberfläche.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Definiert eine 2D-orthografische Projektionsmatrix.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Zeichnet einen Bogen eines Datenträgers.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Richtet eine perspektivische Projektionsmatrix ein.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Definiert eine Auswahlregion.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Karten Objektkoordinaten zu Fensterkoordinaten.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Beschreibt eine schrittweise lineare NURBS-Kürzungskurve.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Definiert einen Rückruf für ein quadrisches Objekt.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Gibt den gewünschten Zeichnen-Stil für Quadrics an.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Gibt an, welche Art von Normalitäten für Quadrics verwendet werden sollen.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Gibt innerhalb oder außerhalb der Ausrichtung für Quadrics an.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Gibt an, ob Quadrics texturiert werden sollen.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Skaliert ein Bild auf eine beliebige Größe.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Zeichnet eine Kugel.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Trennzeichen für eine Beschreibung der Kontur.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Trennzeichen für eine Polygonbeschreibung.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Definiert einen Rückruf für ein Mosaikobjekt.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Gibt einen normalen für ein Polygon an.                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | Legt die -Eigenschaft eines Mosaikobjekts fest.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Gibt einen Scheitelpunkt auf einem Polygon an.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Karten fensterkoordinaten zu Objektkoordinaten.                                                           |



 

 

 




