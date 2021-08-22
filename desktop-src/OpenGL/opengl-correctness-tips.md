---
title: OpenGL Correctness Tipps
description: OpenGL Correctness Tipps
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, Tipps zur Korrektheit
- OpenGL, bewährte Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588cb53ca9e096eb768c4ce448c0bb7badae6f01e7b8d7e16c31a631ebcafb47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486400"
---
# <a name="opengl-correctness-tips"></a>OpenGL Correctness Tipps

Befolgen Sie diese Richtlinien, um OpenGL-Anwendungen zu erstellen, die wie beabsichtigt arbeiten:

-   Angenommen, das Fehlerverhalten einer OpenGL-Implementierung kann sich in einer zukünftigen Version von OpenGL ändern. Die OpenGL-Fehlersemantik kann sich in zukünftigen Revisionen ändern.
-   Verwenden Sie die Projektionsmatrix, um die gesamte Geometrie auf eine einzelne Ebene zu reduzieren. Wenn die ModelView-Matrix verwendet wird, können OpenGL-Features, die in Augenkoordinaten arbeiten (z. B. Beleuchtung und anwendungsdefinierte Clippingebenen), fehlschlagen.
-   Nehmen Sie keine umfangreichen Änderungen an einer einzelnen Matrix vor. Animieren Sie beispielsweise keine Drehung, indem Sie [**glRotate kontinuierlich mit**](glrotate.md) einem inkrementellen Winkel aufrufen. Verwenden Sie stattdessen [**glLoadIdentity,**](glloadidentity.md) um die gegebene Matrix für jeden Frame zu initialisieren, und rufen Sie **dann glRotate** mit dem gewünschten vollständigen Winkel für diesen Frame auf.
-   Erwarten Sie, dass mehrere Durchläufe durch eine Renderingdatenbank nur dann dieselben Pixelfragmente generieren, wenn dieses Verhalten durch die Invarianzregeln garantiert wird, die für eine konforme OpenGL-Implementierung eingerichtet wurden. Andernfalls können mehrere Durchläufe unterschiedliche Sätze von Fragmenten generieren.
-   Erwarten Sie nicht, dass Fehler gemeldet werden, während eine Anzeigeliste definiert wird. Die Befehle in einer Anzeigeliste generieren nur dann Fehler, wenn die Liste ausgeführt wird.
-   Um den Betrieb des Tiefenpuffers zu optimieren, platzieren Sie die nahe Frustumebene so weit wie möglich vom Standpunkt entfernt.
-   Rufen [**Sie glFlush auf,**](glflush.md) um die Ausführung aller vorherigen OpenGL-Befehle zu erzwingen. Zählen Sie nicht auf [**glGet oder**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) [**glIsEnabled,**](glisenabled.md) um den Renderingstream zu leeren. Abfragebefehle leeren so viel des Streams, wie erforderlich ist, um gültige Daten zurück zu geben, aber nicht notwendigerweise alle ausstehenden Renderingbefehle abschließen.
-   Deaktivieren Sie das Dithering beim Rendern von vordefinierten Bildern (z. B. wenn [**glCopyPixels**](glcopypixels.md) aufgerufen wird).
-   Nutzen Sie den gesamten Bereich des Akkumulationspuffers. Wenn Sie beispielsweise vier Bilder akkumulieren, skalieren Sie jedes um ein Quartal, während es akkumuliert wird.
-   Um eine exakte zweidimensionale Rasterung zu erhalten, geben Sie sorgfältig sowohl die orthografische Projektion als auch die Scheitelungen der Primitive an, die rastert werden sollen. Geben Sie die orthografische Projektion mit ganzzahligen Koordinaten an, wie im folgenden Beispiel gezeigt.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    Die *Parameterbreite* und *-höhe* sind die Dimensionen des Viewports. Platzieren Sie angesichts dieser Projektionsmatrix Polygonvertices und Pixelbildpositionen an ganzzahligen Koordinaten, um vorhersagbar zu rastern. Beispielsweise füllt [glRecti](glrect-functions.md)( 0, 0, 1, 1 ) zuverlässig das untere linke Pixel des Viewports aus, und [glRasterPos2i](glrasterpos-functions.md)( 0, 0 ) positioniert zuverlässig ein nichtzoombasiertes Bild am unteren linken Pixel des Viewports. Punktvertices, Linienvertices und Bitmappositionen sollten jedoch an Stellen mit halber Ganzzahl platziert werden. Beispielsweise wird eine Linie, die von (*x* (1) , 0,5) bis (*x* (2) , 0,5) gezeichnet wird, zuverlässig entlang der unteren Pixelzeile im Viewport gerendert, und ein Punkt, der bei (0,5, 0,5) gezeichnet wird, füllt zuverlässig das gleiche Pixel wie glRecti( 0, 0, 1, 1 ).

    Eine optimale Kompromittierung, die es ermöglicht, alle Primitive an ganzzahligen Positionen anzugeben und gleichzeitig eine vorhersagbare Rasterung sicherzustellen, besteht in der Übersetzung von *x* und *y* um 0,375, wie im folgenden Codebeispiel gezeigt. Eine solche Übersetzung sorgt dafür, dass Polygon- und Pixelbildränder sicher von den Pixelcentern entfernt werden, während Linienvertices nahe genug an den Pixelcentern bewegt werden.

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   Vermeiden Sie die Verwendung von negativen W-Scheitelpunktkoordinaten und negativen  *q-Texturkoordinaten.* OpenGL beschneidet solche Koordinaten möglicherweise nicht ordnungsgemäß und kann Interpolationsfehler verursachen, wenn primitive Typen schattiert werden, die durch solche Koordinaten definiert sind.

 

 




