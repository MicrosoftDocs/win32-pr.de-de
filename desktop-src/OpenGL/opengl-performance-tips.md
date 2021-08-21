---
title: OpenGL Performance Tipps
description: OpenGL Performance Tipps
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, Leistungstipps
- OpenGL, bewährte Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe91602d4a30767ed1e66e62d33445bf37152ede2cf9f8450e056f577cb3045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936830"
---
# <a name="opengl-performance-tips"></a>OpenGL Performance Tipps

Diese Programmiermethoden optimieren die Leistung Ihrer Anwendung:

-   Verwenden [**Sie glColorMaterial,**](glcolormaterial.md) wenn nur eine einzelne Materialeigenschaft schnell variiert wird (z. B. an jedem Scheitelpunkt). Verwenden [**Sie glMaterial**](glmaterial-functions.md) für selten auftretende Änderungen oder wenn sich mehr als eine material-Eigenschaft schnell ändert.
-   Verwenden [**Sie glLoadIdentity,**](glloadidentity.md) um eine Matrix zu initialisieren, anstatt Ihre eigene Kopie der Identitätsmatrix zu laden.
-   Verwenden Sie bestimmte Matrixaufrufe wie [**glRotate,**](glrotate.md) [**glTranslate**](gltranslate.md)und [**glScale,**](glscale.md)anstatt Ihre eigenen Drehungs-, Übersetzungs- und Skalierungsmatrizen zu erstellen und [**glMultMatrix auf zu rufen.**](glmultmatrix.md)
-   Verwenden [**Sie glPushAttrib und**](glpushattrib.md) [**glPopAttrib,**](glpopattrib.md) um Zustandswerte zu speichern und wiederherzustellen. Verwenden Sie Abfragefunktionen nur, wenn Ihre Anwendung die Zustandswerte für ihre eigenen Berechnungen erfordert.
-   Verwenden Sie Anzeigelisten, um potenziell speicherintensive Zustandsänderungen zu kapseln. Platzieren Sie beispielsweise alle [**glTexImage-Aufrufe,**](glteximage1d.md) die zum vollständigen Angeben einer Textur erforderlich sind (und möglicherweise auch die zugeordneten [**Aufrufe glTexParameter**](gltexparameter-functions.md), [**glPixelStore**](glpixelstore-functions.md)und [**glPixelTransfer)**](glpixeltransfer.md) in einer einzigen Anzeigeliste. Rufen Sie diese Anzeigeliste auf, um die Textur auszuwählen.
-   Verwenden Sie Anzeigelisten, um die Renderingaufrufe von festen Objekten zu kapseln, die wiederholt gezeichnet werden.
-   Um die Netzwerkbandbreite in Client-/Serverumgebungen zu minimieren, verwenden Sie Auswertungen auch für einfache Oberflächensessellationen.
-   Um den Mehraufwand von GL NORMALIZE zu vermeiden, geben Sie nach Möglichkeit Normal \_ normaler Einheitenlänge an. Da [**glScale fast**](glscale.md) immer die Aktivierung von GL \_ NORMALIZE erfordert, vermeiden Sie die Verwendung von **glScale** bei der Beleuchtung.
-   Wenn keine gleichmäßige Schattierung erforderlich ist, legen Sie [**glShadeModel**](glshademodel.md) auf GL \_ FLAT fest.
-   Verwenden Sie nach Möglichkeit [**einen einzelnen glClear-Aufruf**](glclear.md) pro Frame. Verwenden Sie **glClear nicht,** um kleine Teilregionen der Puffer zu löschen. Verwenden Sie ihn nur, um den Puffer vollständig oder fast vollständig zu löschen.
-   Um mehrere unabhängige Dreiecke zu zeichnen, verwenden Sie einen einzelnen Aufruf anstelle mehrerer Aufrufe von [**glBegin**](glbegin.md) ( GL TRIANGLES ) oder einen Aufruf \_ von **glBegin** ( GL \_ POLYGON ). Ähnlich:

    Um ein einzelnes Dreieck zu zeichnen, verwenden Sie GL \_ TRIANGLES anstelle von GL \_ POLYGON.

    Verwenden Sie einen einzelnen Aufruf von [**glBegin**](glbegin.md) ( GL \_ QUADS ), anstatt **glBegin** ( GL \_ POLYGON ) wiederholt auf aufruft.

    Verwenden Sie einen einzelnen Aufruf von [**glBegin**](glbegin.md) ( GL LINES ), um mehrere unabhängige Liniensegmente zu zeichnen, anstatt \_ **glBegin** ( GL \_ LINES ) mehrmals auf aufruft.

-   Verwenden Sie im Allgemeinen die Vektorformen von Befehlen, um vorausberechnte Daten zu übergeben, und verwenden Sie die Skalarformen von Befehlen, um Werte zu übergeben, die in der Nähe der Aufrufzeit berechnet werden.
-   Vermeiden Sie redundante Modusänderungen, z. B. das Festlegen der Farbe auf denselben Wert zwischen jedem Scheitelpunkt eines flach schattierten Polygons.
-   Deaktivieren Sie beim Zeichnen oder Kopieren von Bildern rasterization- und per-fragment-Vorgänge, um Ressourcen zu optimieren. OpenGL kann Texturen auf Pixelbilder anwenden.

 

 




