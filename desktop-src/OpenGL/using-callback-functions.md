---
title: Verwenden von Rückruffunktionen
description: Die GLU-Rückruffunktionen gluBeginPolygon, gluTessVertex, gluNextContour und gluEndPolygon ähneln den OpenGL-Polygonfunktionen.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- OpenGL-Hilfsprogramm (GLU), Rückruffunktionen
- GLU (OpenGL Utility), Rückruffunktionen
- OpenGL Utility (GLU),Mosaik
- GLU (OpenGL Utility),Mosaik
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75556b8c366c83df5a5976c867e6fc5f68d520da65ed8f34609f312cbfebaa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932895"
---
# <a name="using-callback-functions"></a>Verwenden von Rückruffunktionen

Die GLU-Rückruffunktionen [**gluBeginPolygon,**](glubeginpolygon.md) [**gluTessVertex,**](glutessvertex.md) [**gluNextContour**](glunextcontour.md)und [**gluEndPolygon**](gluendpolygon.md)ähneln den OpenGL-Polygonfunktionen.

In der Regel speichern sie die Daten für die Dreiecke, Dreiecksgitternetze und Dreiecksfächer in benutzerdefinierten Datenstrukturen oder in OpenGL-Anzeigelisten. Um die Polygone zu rendern, durchläuft anderer Code die Datenstrukturen oder ruft die Anzeigelisten auf. Obwohl die Rückruffunktionen OpenGL-Funktionen aufrufen könnten, um Polygone direkt anzuzeigen, ist dies in der Regel nicht der Fall, da das Mosaik rechenintensiv sein kann. Es empfiehlt sich, die Daten zu speichern, wenn die Wahrscheinlichkeit besteht, dass Sie sie erneut anzeigen möchten. Die GLU-Mosaikfunktionen geben garantiert nie neue Scheitelpunkte zurück, sodass keine Interpolation von Scheitelpunkten, Texturkoordinaten oder Farben erforderlich ist.

 

 




