---
title: Portcode, der eine aktuelle Grafikposition benötigt
description: OpenGL verwaltet keine aktuelle Grafikposition. IRIS GL-Funktionen, die von der aktuellen Grafikposition abhängen, z. B. Move, Draw und rmv, weisen keine Entsprechungen in OpenGL auf.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- IRIS GL-Portierung, aktuelle Grafikposition
- Portieren von IRIS GL, aktuelle Grafikposition
- Portieren von IRIS GL zu OpenGL, aktuelle Grafikposition
- OpenGL-Portierung von IRIS GL, aktuelle Grafikposition
- Aktuelle Grafikposition
- Rasterpositionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2354264ed5ad022c0657c95a31007ad33df2882d3c9ab2c44cfafeea99b53d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485790"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Portcode, der eine aktuelle Grafikposition benötigt

OpenGL verwaltet keine aktuelle Grafikposition. IRIS GL-Funktionen, die von der aktuellen Grafikposition abhängen, z. B. **move**, **draw** und **rmv,** weisen keine Entsprechungen in OpenGL auf.

Ältere Versionen von IRIS GL enthielten Zeichnungsbefehle, die auf der aktuellen Grafikposition beruhten, obwohl von ihrer Verwendung abgeraten wurde. Sie müssen Ihren Code umschreiben, wenn Sie sich auf die aktuelle Grafikposition verlassen oder eine der folgenden Routinen verwendet haben:

-   **Zeichnen** und **Verschieben**
-   **pmv,** **pdr** und **pclos**
-   **rdr,** **rmv,** **rpdr** und **rpmv**
-   **getgpos**

OpenGL verfügt über ein Konzept der Rasterposition, das der aktuellen Zeichenposition von IRIS GL entspricht. Weitere Informationen zur Rasterpositionierung finden Sie unter [Portieren von Pixelvorgängen.](porting-pixel-operations.md)

Dieses Thema enthält Informationen zu folgendem Thema.

-   [Befehle zum Portieren von Bildschirmen und Pufferbereinigungen](porting-screen-and-buffer-clearing-commands.md)
-   [Portieren von Matrix- und Transformationsfunktionen](porting-matrix-and-transformation-functions.md)
-   [Portieren von MSINGLE-Moduscode](porting-msingle-mode-code.md)
-   [Portieren von Funktionen zum Abrufen von Matrizen und Transformationen](porting-functions-that-get-matrices-and-transformations.md)
-   [Portieren von Viewports, Bildschirmmasken und Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Portieren von Clippingebenen](porting-clipping-planes.md)

 

 




