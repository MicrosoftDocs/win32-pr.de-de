---
title: Portieren von v-Funktionen
description: In IRIS GL verwenden Sie Variationen der v-Funktion, um Scheitelungen anzugeben. Die entsprechende OpenGL-Funktion ist glVertex Unten sind Beispiele für glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- IRIS GL-Portierung, Scheiteltices
- Portieren von IRIS GL,Scheiteltices
- Portieren von IRIS GL,Scheiteltices zu OpenGL
- OpenGL-Portierung von IRIS GL,Scheiteltices
- Zeichnungsfunktionen,Scheitelungen
- Vertices,porting from IRIS GL (Scheiteltices,Portieren von IRIS GL)
- IRIS GL-Portierung, v-Funktionen
- Portieren von IRIS GL,v-Funktionen
- Portieren von IRIS GL,v-Funktionen zu OpenGL
- OpenGL-Portierung über IRIS GL,v-Funktionen
- Zeichnungsfunktionen,v-Funktionen
- v-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e84fd5eb036afaf5291902ab00f91f3b155f7507d8fce7135dc8030323c1a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888070"
---
# <a name="porting-v-functions"></a>Portieren von v-Funktionen

In IRIS GL verwenden Sie Variationen der **v-Funktion,** um Scheitelungen anzugeben. Die entsprechende OpenGL-Funktion ist [glVertex:](glvertex-functions.md)Im Folgenden finden Sie Beispiele für **glVertex**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

Die **glVertex-Funktion** verwendet Suffixe auf die gleiche Weise wie andere OpenGL-Aufrufe. Die Vektorversionen des Aufrufs nehmen Arrays der richtigen Größe als Argumente an. In der 2D-Version z=0 und w=1. In der 3D-Version w=1.

 

 




