---
title: Überlagerung, Unterebene und Hauptebenen
description: Sie können in Ihren Anwendungen Hardware Ebenen (Überlagerung und Unterebene) verwenden.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL unter Windows, Hardware Ebenen-Ebenen
- Hardware Schicht-Flächen OpenGL
- über Lagerungs Ebenen OpenGL
- unterliegende Flächen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338990"
---
# <a name="overlay-underlay-and-main-planes"></a>Überlagerung, Unterebene und Hauptebenen

Sie können in Ihren Anwendungen Hardware Ebenen (Überlagerung und Unterebene) verwenden. Bei Windows beschreiben Pixel Formate die Pixel Konfigurationen eines Grafik Geräts. Jedes Pixel Format beschreibt die Tiefe und andere Merkmale der Haupt Farb Puffer und beschreibt zusätzliche Puffer (z. b. Tiefe, Kumulation, Schablone und Zusatz), die von der Hauptebene verwendet werden. Die Pixel Formate werden nun erweitert und umfassen Überlagerungs-und unterliegende Puffer.

Ebenenebenen verfügen immer über einen Farben Puffer in der Vorderseite und können auch Front-und Hintergrundfarben enthalten. Jede Ebenenebene verfügt über einen bestimmten renderingkontext zum Rendern in die ebenenpuffer. Sie können keine GDI-Zeichnungsfunktionen in ebenenebenen verwenden.

Ein Fenster verwaltet die Farb Puffer von ebenenflächen ähnlich der Art und Weise, wie Sie die Farben Puffer der Hauptebene verwaltet. Sie können mehrere Fenster gleichzeitig mit überlagern und/oder Unterebenen anzeigen. Sie können keine unverankerten über Lagerungs Fenster aufweisen, die über ein beliebiges Fenster in der hauptzeichnungs Ebene verschoben werden können. Darüber hinaus können Sie keine Hardware-Popup Flächen verwenden, die keine transparente Farbe aufweisen, da die zugrunde liegenden Flächen in einem Fenster jederzeit überladen werden.

Jede Ebenenebene in einem Fenster verfügt über eine zugeordnete Palette. Sie können die Palette einer Farb Index Ebene festlegen, aber die Palette einer RGBA-Farbebene ist fest. Sie müssen die entsprechende Palette erkennen, wenn sich ein Fenster im Vordergrund befindet. Ebenenebenen verfügen über eine transparente Pixelfarbe oder einen transparenten Index, mit dem alle zugrunde liegenden ebenenebenen durch angezeigt werden können.

Sie können den Zustand eines renderingkontexts in einen anderen renderingkontext auf einer separaten Ebenenebene kopieren. Sie können auch anzeigen Listen zwischen renderingkontexten in verschiedenen ebenenebenen freigeben.

Die folgenden Funktionen werden mit ebenenebenen verwendet:

-   [**wglcopycontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglkreatelayercontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wgldescribelayerplane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglgetlayerpaletteentries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglrealizelayerpalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglsetlayerpaletteentries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglswaplayerbuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




