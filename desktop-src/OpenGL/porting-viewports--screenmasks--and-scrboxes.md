---
title: Portieren von Viewports, screenmasken und scrboxes
description: Die folgenden IRIS GL-viewportfunktionen haben keine OpenGL-Entsprechung.
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- IRIS GL Porting, Viewport-Funktionen
- Portieren von IRIS GL, Viewport-Funktionen
- Portieren auf OpenGL von IRIS GL, Viewport-Funktionen
- OpenGL-Portierung von IRIS GL, Viewport-Funktionen
- Viewport-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337149"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Portieren von Viewports, screenmasken und scrboxes

Die folgenden IRIS GL-viewportfunktionen haben keine OpenGL-Entsprechung:

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Mit der Iris GL **Viewport** -Funktion geben Sie die x-Koordinaten (in Pixel) für den linken und rechten Rand eines Viewportrechtecks und die y-Koordinaten für den oberen und unteren Rand an. Mit der OpenGL-Funktion " [**glViewport**](glviewport.md) " geben Sie jedoch die x-und y-Koordinaten (in Pixel) der unteren linken Ecke des Viewportrechtecks zusammen mit der Breite und Höhe an.

In der folgenden Tabelle sind die Funktionen von IRIS GL Viewport und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion                          | OpenGL-Funktion                                                                                         | Bedeutung                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **Viewport** (Links, rechts, unten, oben) | [**glViewport**](glviewport.md) (x, y, Breite, Höhe)                                                | Legt den Viewport fest.           |
| **popviewportpushviewport**<br/>    | [**glpopatpub**](glpopattrib.md)[**glpushatkarb**](glpushattrib.md) (GL- \_ \_ viewportbit)<br/> | Überträgt den Stapel und zeigt ihn an.   |
| **getviewport**                           | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Viewport)               | Gibt viewportdimensionen zurück. |



 

??

 

 





