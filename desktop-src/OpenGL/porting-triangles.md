---
title: Portierende Dreiecke
description: Sie können drei Arten von Dreiecken in separaten OpenGL-Dreiecken, Dreiecksstreifen und Dreiecksfächern zeichnen.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- IRIS GL-Portierung, Dreiecke
- Portieren von IRIS GL, Dreiecke
- Portieren von IRIS GL zu OpenGL, Dreiecke
- OpenGL-Portierung von IRIS GL,Dreiecke
- Zeichnungsfunktionen, Dreiecke
- Dreiecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85acc650a709650495b93cdd00176400f00168cc8fe6445a23505f12b332abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011998"
---
# <a name="porting-triangles"></a>Portierende Dreiecke

Sie können drei Arten von Dreiecken in OpenGL zeichnen: separate Dreiecke, Dreiecksstreifen und Dreiecksfächer.

OpenGL verfügt über keine Entsprechung für die IRIS GL **swaptmesh-Funktion.** Sie können den gleichen Effekt erzielen, indem Sie eine Kombination aus Dreiecken, Dreiecksstreifen und Dreiecksfächern verwenden.

In der folgenden Tabelle sind die IRIS GL-Funktionen zum Zeichnen von Dreiecken und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion           | Äquivalenter glBegin-Parameter | Bedeutung                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | GL \_ TRIANGLES                | Triples von Scheitelpunkten, die als Dreiecke interpretiert werden. |
| **bgntmesh**, **endtmesh** | GL \_ TRIANGLE \_ STRIP          | Verknüpfte Dreiecksstreifen.                   |
|                            | GL \_ TRIANGLE \_ FAN            | Verknüpfte Lüfter von Dreiecken.                     |



 

??

 

 




