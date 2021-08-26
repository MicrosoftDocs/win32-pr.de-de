---
title: Mosaikpolygone
description: Mosaikpolygone
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- OpenGL Utility (GLU),Mosaik
- GLU (OpenGL Utility),Mosaik
- OpenGL Utility (GLU), einfache Polygone
- GLU (OpenGL Utility), einfache Polygone
- Einfache Polygone OpenGL
- OpenGL Utility (GLU), komplexe Polygone
- GLU (OpenGL Utility), komplexe Polygone
- Komplexe Polygone OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948e0669348404af763883f7ff713212d52f6f0d79312812552c0e5053041627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034512"
---
# <a name="tessellating-polygons"></a>Mosaikpolygone

OpenGL kann nur einfache konvexe Polygone direkt anzeigen. Ein Polygon ist einfach, wenn:

-   Die Kanten überschneiden sich nur bei Scheitelpunkten.
-   Es gibt keine doppelten Scheitelpunkte.
-   Genau zwei Kanten treffen an jedem Scheitelpunkt aufeinander.

Um einfache Nichtkonvexpolygone oder einfache Polygone mit Löchern anzuzeigen, müssen Sie zuerst die Polygone triangulieren (in konvexe Polygone unterteilen). Eine solche Unterteilung wird als *Mosaik* bezeichnet. GLU stellt eine Auflistung von Funktionen bereit, die Mosaiken ausführen. Beachten Sie, dass die GLU-Mosaikfunktionen keine nicht einfachen Polygone verarbeiten können. Es gibt keine OpenGL-Standardmethode, um solche Polygone zu verarbeiten.

Da das Mosaik häufig erforderlich ist und recht kompliziert sein kann, werden in diesem Abschnitt die GLU-Mosaikfunktionen ausführlich beschrieben. Diese Funktionen nehmen beliebige einfache Polygone als Eingabe an, die Löcher enthalten können, und geben eine Kombination aus Dreiecken, Dreiecksgittern und Dreiecksfächern zurück. Wenn Sie sich nicht mit Gitternetzen oder Lüftern befassen möchten, können Sie angeben, dass die Mosaikfunktionen nur Dreiecke zurückgeben. Mesh- und Lüfterinformationen verbessern jedoch die Leistung. Die Polygon-Mosaikfunktionen triangulieren ein konkaves Polygon mit einer oder mehreren Konturen.

**So verwenden Sie Polygon-Mosaik**

1.  Erstellen Sie mit [**gluNewTess**](glunewtess.md)ein Mosaikobjekt.
2.  Verwenden Sie [*gluTessCallBack,*](glutess.md) um Rückruffunktionen zu definieren, mit deren Hilfe Sie die vom Mosaikator generierten Dreiecke verarbeiten.
3.  Geben Sie mit [**gluBeginPolygon,**](glubeginpolygon.md) [**gluTessVertex,**](glutessvertex.md) [**gluNextContour**](glunextcontour.md)und [**gluEndPolygon**](gluendpolygon.md)das Polygon mit Löchern oder das konkave Polygon an, für das ein Mosaik erfolgen soll.

    Wenn die Polygonbeschreibung abgeschlossen ist, ruft die Mosaikfunktion Ihre Rückruffunktionen nach Bedarf auf.

    Sie können nicht benötigte Mosaikobjekte mit [**gluDeleteTess**](gludeletetess.md)zerstören.

Weitere Informationen zum Speichern der Mosaikdaten finden Sie unter [Verwenden von Rückruffunktionen.](using-callback-functions.md)

 

 




