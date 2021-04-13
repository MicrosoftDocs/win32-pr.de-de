---
title: Glu-Funktionen
description: Glu-Funktionen
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- OpenGL-, Glu-Bibliotheksfunktionen
- OpenGL-Referenz, Glu-Bibliotheksfunktionen
- Glu-Bibliothek, Funktionen
- OpenGL-Hilfsprogramm (GLU), Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae3ece873f4e1e015861f597c0d51ebfc3436de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388178"
---
# <a name="glu-functions"></a>Glu-Funktionen

Dieser Abschnitt enthält Referenzseiten in alphabetischer Reihenfolge für alle OpenGL-hilfsprogrammbibliotheks-Funktionen. Hintergrundinformationen zu diesen Funktionen finden Sie unter [OpenGL Utility Library](opengl-utility-library.md).



| Funktion                                                                                           | BESCHREIBUNG                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**glubegincurve**](glubegincurve.md), [ **gluendcurve**](gluendcurve.md)                         | Begrenzt eine nicht einheitliche ([NURBS](using-nurbs-curves-and-surfaces.md))-Kurven Definition (Rational B-Spline). |
| [**glubeginpolygon**](glubeginpolygon.md), [ **gluendpolygon**](gluendpolygon.md)                 | Begrenzen einer Polygon Beschreibung.                                                                           |
| [**glubeginsurface**](glubeginsurface.md), [ **gluendsurface**](gluendsurface.md)                 | Begrenzen einer nursb-Oberflächen Definition.                                                                      |
| [**glubegintrim**](glubegintrim.md), [ **gluendtrim**](gluendtrim.md)                             | Begrenzen Sie die Definition einer nursb-Kürzungs Schleife.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Erstellt 1-D-Mipmaps.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Erstellt 2D-Mipmaps.                                                                                     |
| [**gluzylinder**](glucylinder.md)                                                                 | Zeichnet einen Zylinder.                                                                                        |
| [**gludeletenurbsrenderer**](gludeletenurbsrenderer.md)                                           | Zerstört ein nursb-Objekt.                                                                                 |
| [**gludeletequadric**](gludeletequadric.md)                                                       | Zerstört ein Quadric-Objekt.                                                                               |
| [**gludeletetess**](gludeletetess.md)                                                             | Zerstört ein Mosaik Objekt.                                                                          |
| [**gludisk**](gludisk.md)                                                                         | Zeichnet einen Datenträger.                                                                                            |
| [**gluerrorstring**](gluerrorstring.md)                                                           | Erzeugt eine Fehler Zeichenfolge aus einem OpenGL-oder glu-Fehlercode. Die Fehler Zeichenfolge ist nur ANSI.                |
| [**glugetnurbsproperty**](glugetnurbsproperty.md)                                                 | Ruft eine nursb-Eigenschaft ab.                                                                              |
| [**glugetstring**](glugetstring.md)                                                               | Ruft eine Zeichenfolge ab, die die glu-Versionsnummer oder die unterstützten glu-Erweiterungs Aufrufe beschreibt.               |
| [**"glugettessproperty"**](glugettessproperty.md)                                                   | Ruft eine Mosaik Objekt Eigenschaft ab.                                                                |
| [**gluloadsamplingmatrices**](gluloadsamplingmatrices.md)                                         | Lädt nursb-Sampling-und-cullinger-Matrizen.                                                               |
| [**glulookat**](glulookat.md)                                                                     | Definiert eine Anzeige Transformation.                                                                        |
| [**glunewnurbsrenderer**](glunewnurbsrenderer.md)                                                 | Erstellt ein nursb-Objekt.                                                                                  |
| [**glunewquadric**](glunewquadric.md)                                                             | Erstellt ein Quadric-Objekt.                                                                                |
| [**glunewtess**](glunewtess.md)                                                                   | Erstellt ein Mosaik Objekt.                                                                           |
| [**glunextcontour**](glunextcontour.md)                                                           | Markiert den Anfang einer anderen Kontur.                                                                  |
| [*glunurbscallback*](glunurbs.md)                                                                 | Definiert einen Rückruf für ein nursb-Objekt.                                                                   |
| [**glunurbscurve**](glunurbscurve.md)                                                             | Definiert die Form einer nursb-Kurve.                                                                      |
| [**glunurbsproperty**](glunurbsproperty.md)                                                       | Legt eine nursb-Eigenschaft fest.                                                                                   |
| [**glunurbssurface**](glunurbssurface.md)                                                         | Definiert die Form einer nursb-Oberfläche.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Definiert eine 2D-Projektions Matrix (orthografische).                                                            |
| [**glupartialdisk**](glupartialdisk.md)                                                           | Zeichnet einen Bogen eines Datenträgers.                                                                                  |
| [**gluperspective**](gluperspective.md)                                                           | Richtet eine perspektivische Projektions Matrix ein.                                                                 |
| [**glupickmatrix**](glupickmatrix.md)                                                             | Definiert einen Auswahlbereich.                                                                                |
| [**gluproject**](gluproject.md)                                                                   | Ordnet den Fenster Koordinaten Objekt Koordinaten zu.                                                           |
| [**glupwlcurve**](glupwlcurve.md)                                                                 | Beschreibt eine schrittweise lineare, lineare nursb-Kürzungs Kurve.                                                       |
| [*gluvierccallback*](gluquadric.md)                                                             | Definiert einen Rückruf für ein Quadric-Objekt.                                                                 |
| [**gluquadricdrawstyle**](gluquadricdrawstyle.md)                                                 | Gibt die gewünschte Zeichnungs Art für viercs an.                                                           |
| [**gluquadricnormals**](gluquadricnormals.md)                                                     | Gibt an, welche Art von normalen für viercs verwendet werden sollen.                                              |
| [**gluquadricorientation**](gluquadricorientation.md)                                             | Gibt die Ausrichtung innerhalb oder außerhalb von viercs an.                                                    |
| [**gluquadrictexture**](gluquadrictexture.md)                                                     | Gibt an, ob viercs texturiert werden sollen.                                                           |
| [**gluscaleimage**](gluscaleimage.md)                                                             | Skaliert ein Bild auf eine beliebige Größe.                                                                    |
| [**glusphere**](glusphere.md)                                                                     | Zeichnet eine Kugel.                                                                                          |
| [**glutess begincontour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Trennzeichen für eine Kontur Beschreibung.                                                                           |
| [**glutess beginpolygon**](glutessbeginpolygon.md), [ **glutessendpolygon**](glutessendpolygon.md) | Begrenzen einer Polygon Beschreibung.                                                                           |
| [*glutesscallback*](glutess.md)                                                                   | Definiert einen Rückruf für ein Mosaik Objekt.                                                            |
| [**glutess normal**](glutessnormal.md)                                                             | Gibt einen normalen für ein Polygon an.                                                                        |
| [**glutessproperty**](glutessproperty.md)                                                         | Legt die-Eigenschaft eines Mosaik Objekts fest.                                                              |
| [**glutess Vertex**](glutessvertex.md)                                                             | Gibt einen Scheitelpunkt auf einem Polygon an.                                                                         |
| [**"gluunproject"**](gluunproject.md)                                                               | Ordnet Fenster Koordinaten den Objekt Koordinaten zu.                                                           |



 

 

 




