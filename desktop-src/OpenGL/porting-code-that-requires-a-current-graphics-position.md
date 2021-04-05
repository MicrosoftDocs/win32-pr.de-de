---
title: Port Code, der eine aktuelle Grafik Position benötigt
description: OpenGL behält keine aktuelle Grafik Position bei. IRIS GL-Funktionen, die von der aktuellen Grafik Position abhängig sind, z. b. Move, Draw und RMV, haben keine Entsprechungen in OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- IRIS GL portieren, aktuelle Grafik Position
- Portieren von IRIS GL, aktuelle Grafik Position
- Portieren auf OpenGL von IRIS GL, aktueller Grafik Position
- OpenGL-Portierung von IRIS GL, aktuelle Grafik Position
- aktuelle Grafik Position
- Raster Positionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "103719596"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Port Code, der eine aktuelle Grafik Position benötigt

OpenGL behält keine aktuelle Grafik Position bei. IRIS GL-Funktionen, die von der aktuellen Grafik Position abhängig sind, z. b. **Move**, **Draw** und **RMV**, haben keine Entsprechungen in OpenGL.

Ältere Versionen von IRIS GL enthielten Zeichnungs Befehle, die auf der aktuellen Grafik Position beruhten, obwohl ihre Verwendung davon abgeraten ist. Sie müssen Ihren Code umschreiben, wenn Sie die aktuelle Grafik Position in irgendeiner Weise verwendet haben, oder eine der folgenden Routinen verwendet haben:

-   **Zeichnen** und **verschieben**
-   **pmv**, **PDR** und **PCLOS**
-   **rdr**, **RMV**, **rpdr** und **rpmv**
-   **getgpos**

OpenGL hat ein Konzept der Raster Position, das der aktuellen Zeichenposition von IRIS GL entspricht. Weitere Informationen zur Raster Positionierung finden Sie unter [Portieren von Pixel Vorgängen](porting-pixel-operations.md).

Dieses Thema enthält Informationen zu den folgenden Themen.

-   [Portieren von Bildschirm-und Puffer Lösch Befehlen](porting-screen-and-buffer-clearing-commands.md)
-   [Portieren von Matrix-und Transformations Funktionen](porting-matrix-and-transformation-functions.md)
-   [Portieren von Code im msingle-Modus](porting-msingle-mode-code.md)
-   [Portieren von Funktionen, die Matrizen und Transformationen erhalten](porting-functions-that-get-matrices-and-transformations.md)
-   [Portieren von Viewports, screenmasken und scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Portieren von Clippingebenen](porting-clipping-planes.md)

 

 




