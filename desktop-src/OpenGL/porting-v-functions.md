---
title: Portieren von v-Funktionen
description: In IRIS GL verwenden Sie Variationen der v-Funktion, um Vertices anzugeben. Die entsprechende OpenGL-Funktion ist "glVertex" unten sind Beispiele für "glVertex".
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- IRIS GL portieren, Vertices
- Portieren von IRIS GL, Vertices
- Portieren auf OpenGL von IRIS GL, Vertices
- OpenGL-Portierung von IRIS GL, Vertices
- Zeichnungsfunktionen, Vertices
- Vertices, Portieren von IRIS GL
- IRIS GL Porting, v Functions
- Portieren von IRIS GL, v Functions
- Portieren auf OpenGL von IRIS GL, v Functions
- OpenGL-Portierung von IRIS GL, v Functions
- Zeichnungsfunktionen, v-Funktionen
- v-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309751"
---
# <a name="porting-v-functions"></a>Portieren von v-Funktionen

In IRIS GL verwenden Sie Variationen der **v** -Funktion, um Vertices anzugeben. Die entsprechende OpenGL-Funktion ist " [glVertex](glvertex-functions.md)": im folgenden finden Sie Beispiele für " **glVertex**".

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

Die **glVertex** -Funktion nimmt Suffixe auf dieselbe Weise wie andere OpenGL-Aufrufe auf. Die Vektor Versionen des Aufrufes übernehmen Arrays der richtigen Größe als Argumente. In der 2D-Version z = 0 und w = 1. In der 3D-Version ist w = 1.

 

 




