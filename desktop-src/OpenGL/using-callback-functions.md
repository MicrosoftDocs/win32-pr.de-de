---
title: Verwenden von Rückruf Funktionen
description: Die glu-Rückruf Funktionen "glubeginpolygon", "glutess Vertex", "glunextcontour" und "gluendpolygon" ähneln den OpenGL-Polygon Funktionen.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- OpenGL-Hilfsprogramm (GLU), Rückruf Funktionen
- GLU (OpenGL-Hilfsprogramm), Rückruf Funktionen
- OpenGL-Hilfsprogramm (GLU), Mosaik
- GLU (OpenGL-Hilfsprogramm), Mosaik
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855819"
---
# <a name="using-callback-functions"></a>Verwenden von Rückruf Funktionen

Die glu-Rückruf Funktionen " [**glubeginpolygon**](glubeginpolygon.md)", " [**glutess Vertex**](glutessvertex.md)", " [**glunextcontour**](glunextcontour.md)" und " [**gluendpolygon**](gluendpolygon.md)" ähneln den OpenGL-Polygon Funktionen.

In der Regel speichern Sie die Daten für die Dreiecke, Dreiecksnetze und Dreiecks Lüfter in benutzerdefinierten Datenstrukturen oder in OpenGL-Anzeigelisten. Um die Polygone zu rendieren, durchläuft anderer Code die Datenstrukturen oder ruft die Anzeigelisten auf. Obwohl die Rückruf Funktionen OpenGL-Funktionen aufrufen können, um Polygone direkt anzuzeigen, wird dies in der Regel nicht durchgeführt, da das Mosaik Rechenressourcen intensiv sein kann. Es empfiehlt sich, die Daten zu speichern, wenn Sie die Möglichkeit haben, Sie erneut anzuzeigen. Es ist garantiert, dass die glu-Mosaik Funktionen keine neuen Scheitel Punkte zurückgeben, sodass keine interpolung von Scheitel Punkten, Texturkoordinaten oder Farben erforderlich ist.

 

 




