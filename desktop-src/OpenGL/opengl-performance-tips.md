---
title: OpenGL-Leistungs Tipps
description: OpenGL-Leistungs Tipps
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, Tipps zur Leistung
- OpenGL, bewährte Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e5b6fa33f8d6841d0fd47d1a655ef99facc84e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710595"
---
# <a name="opengl-performance-tips"></a>OpenGL-Leistungs Tipps

Diese Programmierverfahren optimieren die Leistung Ihrer Anwendung:

-   Verwenden Sie [**glcolormaterial**](glcolormaterial.md) , wenn nur eine einzelne Materialeigenschaft schnell geändert wird (z. b. bei jedem Scheitelpunkt). Verwenden Sie " [**glmaterial**](glmaterial-functions.md) " für seltene Änderungen oder wenn mehr als eine einzelne Materialeigenschaft schnell unterschiedlich ist.
-   Verwenden Sie " [**glLoadIdentity**](glloadidentity.md) ", um eine Matrix zu initialisieren, anstatt eine eigene Kopie der Identitätsmatrix zu laden.
-   Verwenden Sie bestimmte Matrix Aufrufe, wie z. b. [**glrotation**](glrotate.md), [**gltranslate**](gltranslate.md)und [**glscale**](glscale.md), anstatt eigene Dreh-, Übersetzungs-und Skalierungs Matrizen zu erstellen und [**glmultmatrix**](glmultmatrix.md)aufzurufen.
-   Verwenden Sie zum Speichern und Wiederherstellen von Zustands Werten [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) . Verwenden Sie Abfragefunktionen nur, wenn Ihre Anwendung die Zustands Werte für Ihre eigenen Berechnungen erfordert.
-   Verwenden Sie anzeigen Listen, um potenziell speicherintensive Zustandsänderungen zu kapseln. Fügen Sie z. b. alle " [**glteximage**](glteximage1d.md) "-Aufrufe ein, die erforderlich sind, um eine Textur (und möglicherweise auch die zugehörigen " [**gltexparameter**](gltexparameter-functions.md)", " [**glpixelstore**](glpixelstore-functions.md)" und " [**glpixeltransfer**](glpixeltransfer.md) ") vollständig in einer einzigen Anzeigeliste anzugeben Diese Anzeigeliste aufrufen, um die Textur auszuwählen.
-   Verwenden Sie anzeigen Listen, um die renderingaufrufe von starren Objekten zu kapseln, die wiederholt gezeichnet werden.
-   Um die Netzwerkbandbreite in Client-/Server-Umgebungen zu minimieren, verwenden Sie Evaluatoren auch für einfache Oberflächen Mosaik.
-   Wenn möglich, um den Aufwand von GL \_ normalize zu vermeiden, stellen Sie normale mit Einheiten Längen bereit. Da für [**glscale**](glscale.md) fast immer die Aktivierung von GL \_ normalize erforderlich ist, sollten Sie die Verwendung von **glscale** bei der Beleuchtung vermeiden.
-   Wenn eine Smooth-Schattierung nicht erforderlich ist, legen Sie [**glshademodel**](glshademodel.md) auf GL \_ Flat fest.
-   Verwenden Sie nach Möglichkeit einen einzelnen [**glClear**](glclear.md) -Rückruf pro Frame. Verwenden Sie " **glClear** " nicht, um kleine Unterbereiche der Puffer zu löschen. Verwenden Sie es nur, um den Puffer vollständig oder fast vollständig zu löschen.
-   Wenn Sie mehrere unabhängige Dreiecke zeichnen möchten, verwenden Sie anstelle mehrerer Aufrufe von [**glBegin**](glbegin.md) (GL \_ Dreiecke) oder eines Aufrufs von **glBegin** (GL Polygon) einen einzigen Aufruf \_ . Ähnliche Weise

    Zum Zeichnen eines einzelnen Dreiecks verwenden Sie GL- \_ Dreiecke anstelle von GL- \_ Polygon.

    Verwenden Sie einen einzelnen Aufruf von [**glBegin**](glbegin.md) (GL \_ QUADS), anstatt wiederholt **glBegin** (GL \_ Polygon) aufzurufen.

    Verwenden Sie einen einzelnen Aufruf von [**glBegin**](glbegin.md) (GL \_ Lines), um mehrere unabhängige Liniensegmente zu zeichnen, anstatt **glBegin** (GL \_ Lines) mehrmals aufzurufen.

-   Verwenden Sie im Allgemeinen die Vektorformen von Befehlen, um vorab berechnete Daten zu übergeben, und verwenden Sie die skalaren Formen von Befehlen, um Werte zu übergeben, die in der Nähe der Aufruf Zeit berechnet werden.
-   Vermeiden Sie das vornehmen von Änderungen im redundanten Modus, z. b. das Festlegen der Farbe auf denselben Wert zwischen den einzelnen Scheitel Punkten eines flachen Polygons.
-   Wenn Sie Bilder zeichnen oder kopieren, deaktivieren Sie die rasterisierung und die Vorgänge pro Fragment, um die Ressourcen zu optimieren. OpenGL kann Texturen auf Pixelbilder anwenden.

 

 




