---
title: Portieren von Viewports, Bildschirmmasken und Boxes
description: Die folgenden IRIS GL-Viewportfunktionen verfügen nicht über eine OpenGL-Entsprechung.
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- IRIS GL-Portierung, Viewportfunktionen
- Portieren von IRIS GL,Viewportfunktionen
- Portieren von IRIS GL,Viewportfunktionen zu OpenGL
- OpenGL-Portierung über IRIS GL,Viewportfunktionen
- Viewportfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb1a01cfb038faf87e48381856fe281bf2c935d13fedb78b79266e2af4fe15e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776910"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Portieren von Viewports, Bildschirmmasken und Boxes

Die folgenden IRIS GL-Viewportfunktionen verfügen nicht über ein OpenGL-Äquivalent:

-   **reshapeviewport**
-   **box**
-   **getscrbox**

Mit der **Viewportfunktion** IRIS GL geben Sie die x-Koordinaten (in Pixel) für die linke und rechte Seite eines Viewportrechtecks und die y-Koordinaten für den oberen und unteren Rand an. Bei der Funktion OpenGL [**glViewport**](glviewport.md) geben Sie jedoch die x- und y-Koordinaten (in Pixel) der unteren linken Ecke des Viewportrechtecks zusammen mit ihrer Breite und Höhe an.

In der folgenden Tabelle sind die IRIS GL-Viewportfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                          | OpenGL-Funktion                                                                                         | Bedeutung                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **viewport** ( left, right, bottom, top ) | [**glViewport**](glviewport.md) ( x, y, width, height )                                                | Legt den Viewport fest.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL \_ VIEWPORT BIT \_ )<br/> | Pusht den Stapel und popt ihn.   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ VIEWPORT )               | Gibt Viewportdimensionen zurück. |



 

??

 

 





