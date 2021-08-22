---
title: Überlagerungs-, Unter- und Hauptebenen
description: Sie können Hardwareebenenebenen (Überlagerungs- und Unterlagerungsebenen) in Ihren Anwendungen verwenden.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL auf Windows,Hardwareebenenebenen
- OpenGL-Hardwareebenen
- Überlagerungsebenen OpenGL
- Unterschichtebenen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b968a0ab028fd0a699e31ad3a3601d7140435e2b36d0188bef46c5dca7cbad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936489"
---
# <a name="overlay-underlay-and-main-planes"></a>Überlagerungs-, Unter- und Hauptebenen

Sie können Hardwareebenenebenen (Überlagerungs- und Unterlagerungsebenen) in Ihren Anwendungen verwenden. Mit Windows werden in Pixelformaten die Pixelkonfigurationen eines Grafikgeräts beschrieben. Jedes Pixelformat beschreibt die Tiefe und andere Merkmale der Hauptfarbpuffer und beschreibt zusätzliche Puffer (z. B. Tiefe, Akkumulation, Schablone und Hilfspuffer), die von der Hauptebene verwendet werden. Pixelformate werden jetzt um Überlagerungs- und Unterlagerungspuffer erweitert.

Ebenenebenen verfügen immer über einen Farbpuffer von vorn links und können auch Rechts- und Hintergrundfarbpuffer enthalten. Jede Ebenenebene verfügt über einen bestimmten Renderingkontext, der in die Ebenenpuffer gerendert werden soll. Sie können GDI-Zeichnungsfunktionen nicht in Ebenenebenen verwenden.

Ein Fenster verwaltet die Farbpuffer von Ebenenebenen auf ähnliche Weise wie die Verwaltung von Hauptebenen-Farbpuffern. Sie können mehrere Fenster mit Überlagerungs- und/oder Unterlagerungsebenen gleichzeitig anzeigen. Sie können keine frei schwebenden Überlagerungsfenster verwenden, die sich über ein beliebiges Fenster in der Hauptzeichnungsebene bewegen können. Darüber hinaus können Sie keine Hardware-Popupebenen verwenden, die keine transparente Farbe haben, da die zugrunde liegenden Ebenen in einem Fenster jederzeit verdeckt würden.

Jeder Ebenenebene in einem Fenster ist eine Palette zugeordnet. Sie können die Palette einer Farbindexebenenebene festlegen, aber die Palette einer RGBA-Farbebene ist fest. Sie müssen die entsprechende Palette erkennen, wenn sich ein Fenster im Vordergrund befindet. Ebenenebenen weisen eine transparente Pixelfarbe oder einen transparenten Index auf, mit der alle zugrunde liegenden Ebenenebenen angezeigt werden können.

Sie können den Zustand eines Renderingkontexts in einen anderen Renderingkontext auf einer separaten Ebenenebene kopieren. Sie können Anzeigelisten auch für Renderingkontexte auf verschiedenen Ebenenebenen freigeben.

Die folgenden Funktionen werden mit Ebenenebenen verwendet:

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




