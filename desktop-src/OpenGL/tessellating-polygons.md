---
title: Mosaik von Polygonen
description: Mosaik von Polygonen
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- OpenGL-Hilfsprogramm (GLU), Mosaik
- GLU (OpenGL-Hilfsprogramm), Mosaik
- OpenGL-Hilfsprogramm (GLU), einfache Polygone
- GLU (OpenGL-Hilfsprogramm), einfache Polygone
- einfache Polygone OpenGL
- OpenGL-Hilfsprogramm (GLU), komplexe Polygone
- GLU (OpenGL-Hilfsprogramm), komplexe Polygone
- komplexe Polygone OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341674"
---
# <a name="tessellating-polygons"></a>Mosaik von Polygonen

OpenGL kann direkt nur einfache, konforme Polygone anzeigen. Ein Polygon ist einfach, wenn Folgendes gilt:

-   Die Ränder schneiden sich nur bei Scheitel Punkten ab.
-   Es sind keine doppelten Vertices vorhanden.
-   An jedem Scheitelpunkt werden genau zwei Ränder angezeigt.

Um einfache, nicht konvexe Polygone oder einfache Polygone mit Löchern anzuzeigen, müssen Sie zunächst die Polygone auslagern (unterteilen Sie Sie in konvexe Polygone). Diese Unterteilung *wird als Mosaik* bezeichnet. Glu bietet eine Auflistung von Funktionen, die Mosaik Vorgänge durchführen. Beachten Sie, dass die glu-Mosaik Funktionen nicht einfache Polygone verarbeiten können. Es gibt keine standardmäßige OpenGL-Methode, um solche Polygone zu verarbeiten.

Da das Mosaik häufig benötigt wird und ziemlich schwierig sein kann, werden die Funktionen der Funktionen in diesem Abschnitt ausführlich beschrieben. Diese Funktionen akzeptieren beliebige einfache Polygone als Eingabe, die möglicherweise Löcher enthalten, und Sie geben eine Kombination von Dreiecken, Dreiecksnetzen und Dreiecks Lüfter zurück. Wenn Sie keine Netzen oder Lüfter behandeln möchten, können Sie angeben, dass die Mosaik Funktionen nur Dreiecke zurückgeben. Mesh-und Lüfter-Informationen verbessern jedoch die Leistung. Die Polygon-Mosaik Funktionen unterliegen einem konkaven Polygon mit mindestens einer Kontur.

**So verwenden Sie das Polygon-Mosaik**

1.  Erstellen Sie ein Mosaik Objekt mit [**glunewtess**](glunewtess.md).
2.  Verwenden Sie " [*glutesscallback*](glutess.md) ", um Rückruf Funktionen zu definieren, die Sie verwenden, um die vom Mosaik Prozess generierten Dreiecke zu verarbeiten.
3.  Geben Sie mit " [**glubeginpolygon**](glubeginpolygon.md)", " [**glutess Vertex**](glutessvertex.md)", " [**glunextcontour**](glunextcontour.md)" und " [**gluendpolygon**](gluendpolygon.md)" das Polygon mit Löchern oder dem konkaven Polygon an, das im Mosaik Prozess verwendet werden soll.

    Wenn die Polygon Beschreibung vollständig ist, ruft die Mosaik Funktion die Rückruf Funktionen nach Bedarf auf.

    Sie können nicht benötigte Mosaik Objekte mit " [**gludeletetess**](gludeletetess.md)" zerstören.

Weitere Informationen zum Speichern der Mosaik Daten finden [Sie unter Verwenden von Rückruf Funktionen](using-callback-functions.md).

 

 




