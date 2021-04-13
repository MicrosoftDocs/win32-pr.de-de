---
title: Portieren von Dreiecken
description: Sie können drei Arten von Dreiecken in OpenGL zeichnen, indem Sie die Dreiecke, Dreiecks Streifen und Dreiecks Lüfter trennen.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- IRIS GL portieren, Dreiecke
- Portieren von IRIS GL, Dreiecke
- Portieren auf OpenGL von IRIS GL, Dreiecke
- OpenGL-Portierung von IRIS GL, Dreiecke
- Zeichnungsfunktionen, Dreiecke
- Dreiecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310535"
---
# <a name="porting-triangles"></a>Portieren von Dreiecken

Sie können drei Arten von Dreiecken in OpenGL zeichnen: separate Dreiecke, Dreiecks Streifen und Dreiecks Lüfter.

OpenGL hat keine Entsprechung für die Iris **GL-** Funktion "". Sie können denselben Effekt erzielen, indem Sie eine Kombination aus Dreiecke, Dreiecks Streifen und Dreiecks Lüfter verwenden.

In der folgenden Tabelle sind die Iris GL-Funktionen zum Zeichnen von Dreiecken und ihre entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion           | Äquivalenter glBegin-Parameter | Bedeutung                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | GL- \_ Dreiecke                | Die als Dreiecke interpretierten Scheitel Punkte. |
| **bgntmesh**, **endtmesh** | GL- \_ Dreiecks \_ Streifen          | Verknüpfte Streifen von Dreiecken.                   |
|                            | GL- \_ Dreiecks \_ Lüfter            | Verknüpfte Fans von Dreiecken.                     |



 

??

 

 




