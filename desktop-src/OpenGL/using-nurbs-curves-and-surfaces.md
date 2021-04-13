---
title: Verwenden von nursb-Kurven und-Oberflächen
description: Non-Uniform rationb-Spline (NURBS)-Funktionen bieten allgemeine und leistungsstarke Beschreibungen von Kurven und Oberflächen in zwei und drei Dimensionen, wobei die Kurven und Oberflächen in OpenGL-Evaluatoren konvertiert werden.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- OpenGL-Hilfsprogramm (GLU), nicht einheitliche Rational B-Spline (NURBS)
- GLU (OpenGL-Hilfsprogramm), nicht einheitliche Rational B-Spline (NURBS)
- Nicht einheitlicher Rational B-Spline (NURBS) OpenGL
- NURBS (Non-Uniform Rational B-Spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309640"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Verwenden von nursb-Kurven und-Oberflächen

Non-Uniform rationb-Spline (NURBS)-Funktionen bieten allgemeine und leistungsstarke Beschreibungen von Kurven und Oberflächen in zwei und drei Dimensionen, wobei die Kurven und Oberflächen in OpenGL-Evaluatoren konvertiert werden. Die nursb-Funktionen können Geometrie in vielen Computern unterstützten mechanischen Entwurfs Systemen darstellen. Sie können Kurven und Oberflächen in einer Vielzahl von Formaten darstellen, und Sie können automatisch die Adaptive Unterteilung verarbeiten, die die Domäne in kleinere Dreiecke in Regionen mit hoher Krümmung und Near Silhouette-Rändern zerlegt. Nursb-Funktionen fallen in die folgenden Kategorien.

Verwenden Sie zum Verwalten eines nursb-Objekts Folgendes:

-   [**glunewnurbsrenderer**](glunewnurbsrenderer.md) (Erstellen eines NURBS-Objekts)
-   [**gludeletenurbsrenderer**](gludeletenurbsrenderer.md) (löscht ein NURBS-Objekt)
-   [*glunurbscallback*](glunurbs.md) (stellt eine Fehler Behandlungs Funktion her)

Verwenden Sie zum Angeben der gewünschten Kurven Folgendes:

-   [**glubegincurve**](glubegincurve.md)
-   [**glunurbscurve**](glunurbscurve.md)
-   [**gluendcurve**](gluendcurve.md)

Verwenden Sie zum Angeben der gewünschten Oberflächen Folgendes:

-   [**glubeginsurface**](glubeginsurface.md)
-   [**glunurbssurface**](glunurbssurface.md)
-   [**gluendsurface**](gluendsurface.md)

Sie können auch einen Kürzungs Bereich angeben, der eine Teilmenge der zu bewertenden nursb-Oberflächen Domäne definiert, damit Sie Oberflächen erstellen können, die über glatte Begrenzungen verfügen oder Löcher enthalten.

Verwenden Sie zum Angeben der Kürzungs Region Folgendes:

-   [**glubegintrim**](glubegintrim.md)
-   [**glupwlcurve**](glupwlcurve.md)
-   [**glunurbscurve**](glunurbscurve.md)
-   [**gluendtrim**](gluendtrim.md)

Wie bei quadrischen Objekten können Sie auch steuern, wie nursb-Kurven und-Oberflächen gerendert werden. Sie können Folgendes bestimmen:

-   Gibt an, ob eine Kurve oder eine Oberfläche verworfen werden soll, deren Steuerelement Polyhedron außerhalb des aktuellen Viewports liegt.
-   Die maximale Länge (in Pixel) der Kanten von Polygonen, die zum Rendering von Kurven und Oberflächen verwendet werden.
-   Gibt an, ob Sie die Projektions Matrix, die Modelview-Matrix und den Viewport vom OpenGL-Server verwenden oder explizit mit " [**gluloadsamplingmatrices**](gluloadsamplingmatrices.md)" bereitstellen.

Verwenden Sie " [**glunurbsproperty**](glunurbsproperty.md) ", um diese Eigenschaften festzulegen, oder verwenden Sie die Standardwerte. Sie können ein nurb-Objekt über den Renderingstil mit " [**glugetnurbsproperty**](glugetnurbsproperty.md)" Abfragen.

 

 




