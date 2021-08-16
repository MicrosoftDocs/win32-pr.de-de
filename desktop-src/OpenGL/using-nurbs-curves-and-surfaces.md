---
title: Verwenden von NURBS-Kurven und -Oberflächen
description: NurBS-Funktionen (Non-Uniform Rational B-Spline) bieten allgemeine und leistungsstarke Beschreibungen von Kurven und Oberflächen in zwei und drei Dimensionen und konvertieren die Kurven und Oberflächen in OpenGL-Auswertungen.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- OpenGL Utility (GLU), Non-Uniform Rational B-Spline (NURBS)
- GLU (OpenGL Utility), Non-Uniform Rational B-Spline (NURBS)
- Non-Uniform Rational B-Spline (NURBS) OpenGL
- NURBS (Non-Uniform Rational B-Spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1b366571be7a9210576e78540c77970667aca2f37ec8a092de07edb97493d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932770"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Verwenden von NURBS-Kurven und -Oberflächen

NurBS-Funktionen (Non-Uniform Rational B-Spline) bieten allgemeine und leistungsstarke Beschreibungen von Kurven und Oberflächen in zwei und drei Dimensionen und konvertieren die Kurven und Oberflächen in OpenGL-Auswertungen. Die NURBS-Funktionen können Geometrie in vielen computergestützten, maschinellen Entwurfssystemen darstellen. Sie können Kurven und Oberflächen in einer Vielzahl von Stilen rendern, und sie können automatisch adaptive Unterteilungen verarbeiten, die die Domäne in kleinere Dreiecke in Regionen mit hoher Krümmung und in der Nähe von Eckenrändern mosaikieren. NURBS-Funktionen fallen in die folgenden Kategorien.

Verwenden Sie zum Verwalten eines NURBS-Objekts:

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (Erstellen eines NURBS-Objekts)
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (löscht ein NURBS-Objekt)
-   [*gluNurbsCallback*](glunurbs.md) (richtet eine Fehlerbehandlungsfunktion ein)

Verwenden Sie Folgendes, um die gewünschten Kurven anzugeben:

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Verwenden Sie Folgendes, um die gewünschten Oberflächen anzugeben:

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

Sie können auch einen Kürzungsbereich angeben, der eine Teilmenge der NURBS-Oberflächendomäne definiert, die ausgewertet werden soll, damit Sie Oberflächen erstellen können, die über reibungslose Grenzen verfügen oder Löcher enthalten.

Verwenden Sie Folgendes, um den Kürzungsbereich anzugeben:

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Wie bei quadrischen Objekten können Sie steuern, wie NURBS-Kurven und -Oberflächen gerendert werden. Sie können Dies bestimmen:

-   Gibt an, ob eine Kurve oder Oberfläche verworfen werden soll, deren Steuerpolyhedron außerhalb des aktuellen Viewports liegt.
-   Die maximale Länge (in Pixel) der Kanten von Polygonen, die zum Rendern von Kurven und Oberflächen verwendet werden.
-   Unabhängig davon, ob Sie die Projektionsmatrix, die Modellansichtsmatrix und den Viewport vom OpenGL-Server übernehmen oder diese mit [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)bereitstellen.

Verwenden Sie [**gluNurbsProperty,**](glunurbsproperty.md) um diese Eigenschaften festzulegen, oder verwenden Sie die Standardwerte. Sie können ein NURBS-Objekt über seinen Renderingstil mit [**gluGetNurbsProperty abfragen.**](glugetnurbsproperty.md)

 

 




