---
title: OpenGL-Tipps zur Richtigkeit
description: OpenGL-Tipps zur Richtigkeit
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, Tipps zur Richtigkeit
- OpenGL, bewährte Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388171"
---
# <a name="opengl-correctness-tips"></a>OpenGL-Tipps zur Richtigkeit

Befolgen Sie diese Richtlinien, um OpenGL-Anwendungen zu erstellen, die Sie wie beabsichtigt ausführen:

-   Angenommen, das Fehler Verhalten im Rahmen einer OpenGL-Implementierung kann sich in einer zukünftigen Version von OpenGL ändern. Die OpenGL-Fehler Semantik kann sich in zukünftigen Revisionen ändern.
-   Verwenden Sie die Projektions Matrix, um die gesamte Geometrie auf eine einzelne Ebene zu reduzieren. Wenn die Modelview-Matrix verwendet wird, können OpenGL-Funktionen, die in Augen Koordinaten (z. b. Beleuchtung und Anwendungs definierte Clippingebenen) betrieben werden, fehlschlagen.
-   Nehmen Sie keine ausführlichen Änderungen an einer einzelnen Matrix vor. Animieren Sie z. b. eine Drehung nicht durch kontinuierliches Aufrufen von [**glrotation**](glrotate.md) mit einem inkrementellen Winkel. Verwenden Sie stattdessen " [**glLoadIdentity**](glloadidentity.md) ", um die angegebene Matrix für jeden Frame zu initialisieren, und nennen Sie dann " **glrotation** " mit dem gewünschten, kompletten Winkel für diesen Frame.
-   Gehen Sie davon aus, dass mehrere Durchgänge durch eine renderdatenbank nur die gleichen Pixel Fragmente generieren, wenn dieses Verhalten durch die für eine kompatible OpenGL-Implementierung eingerichteten Invarianz Regeln gewährleistet ist. Andernfalls können mehrere Durchgänge unterschiedliche Sätze von Fragmenten generieren.
-   Es wird nicht erwartet, dass Fehler gemeldet werden, während eine Anzeigeliste definiert wird. Die Befehle in einer Anzeigeliste generieren nur dann Fehler, wenn die Liste ausgeführt wird.
-   Um den Vorgang des tiefen Puffers zu optimieren, platzieren Sie die Near Frustum-Ebene so weit wie möglich vom Standpunkt aus.
-   Ruft " [**glflush**](glflush.md) " auf, um die Ausführung aller vorherigen OpenGL-Befehle zu erzwingen. Verwenden [**Sie nicht, um**](glisenabled.md) den renderingstream [**zu leeren**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . Abfrage Befehle leeren den Datenstrom, der zum Zurückgeben gültiger Daten erforderlich ist, aber nicht notwendigerweise alle ausstehenden renderingbefehle vervollständigen.
-   Deaktivieren Sie Dithering beim Rendern von Vorhersage Bildern (z. b. Wenn [**glcopypixels**](glcopypixels.md) aufgerufen wird).
-   Verwenden Sie den gesamten Bereich des Akkumulations Puffers. Wenn z. b. vier Bilder gesammelt werden, Skalieren Sie jedes Quartal um ein Quartal, wenn es akkumuliert wird.
-   Zum Abrufen der exakten zweidimensionalen rasterisierung müssen Sie sowohl die orthografische Projektion als auch die Scheitel Punkte der primitiven angeben, die rasterisiert werden sollen. Geben Sie die orthografische Projektion mit ganzzahligen Koordinaten an, wie im folgenden Beispiel gezeigt.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    Die Parameter " *Width* " und " *height* " sind die Abmessungen des Viewports. Platzieren Sie bei dieser Projektions Matrix Polygon Scheitel Punkte und Pixel Bild Positionen an ganzzahligen Koordinaten, um vorhersagbare Raster zu erhalten. Beispielsweise füllt [glrecti](glrect-functions.md)(0, 0, 1, 1) zuverlässig das untere linke Pixel des Viewports aus, und [glRasterPos2i](glrasterpos-functions.md)(0,0) positioniert ein unzoombild zuverlässig am unteren linken Pixel des Viewports. Punkt Scheitel Punkte, Zeilen Scheitel Punkte und bitmappositionen sollten jedoch an der Hälfte der ganzzahligen Standorte platziert werden. Beispielsweise wird eine von (*x* (1), 0,5) bis (*x* (2), 0,5) gezeichnete Linie zuverlässig entlang der untersten Zeile der Pixel im Viewport gerendert, und ein Punkt, der bei (0,5, 0,5) gezeichnet wird, wird das gleiche Pixel wie glrecti (0, 0, 1, 1) zuverlässig ausfüllen.

    Ein optimaler Kompromiss, bei dem alle primitiven an *ganzzahligen* Positionen angegeben werden können, während gleichzeitig die vorhersagbare rasterisierung sichergestellt wird, ist das Konvertieren von *x* und y durch 0,375, wie im folgenden Codebeispiel gezeigt. Eine solche Übersetzung sorgt dafür, dass Polygon-und Pixel Bildkanten sicher aus den Mittelpunkten der Pixel entfernt werden, während Zeilen Scheitel Punkte in den Pixel Centern nah beieinander verschoben werden.

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

-   Vermeiden Sie die Verwendung negativer *w* -Scheitelpunkt Koordinaten und negativer *q* -Texturkoordinaten. Bei OpenGL werden solche Koordinaten möglicherweise nicht ordnungsgemäß durchlaufen, und es können Interpolations Fehler auftreten, wenn Schattierungs primitive durch solche Koordinaten definiert werden.

 

 




