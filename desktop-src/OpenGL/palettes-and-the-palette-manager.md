---
title: Paletten und der Paletten-Manager
description: Der Windows Paletten-Manager, der Teil des GDI ist, ist speziell auf 8-Bit-Anzeigeadapter mit einer Hardwarepalette von 256 Farbeinträgen ausgerichtet.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL auf Windows,Paletten-Manager
- OpenGL auf Windows,Hardwarepaletten
- Paletten-Manager OpenGL
- Hardwarepaletten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58407a5ddafe862caa73edd498c4da529b0ac987880828177d0d0b284601efed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936276"
---
# <a name="palettes-and-the-palette-manager"></a>Paletten und der Paletten-Manager

Der Windows Paletten-Manager, der Teil des GDI ist, ist speziell auf 8-Bit-Anzeigeadapter mit einer *Hardwarepalette* von 256 Farbeinträgen ausgerichtet. Pixel auf dem Bildschirm werden als 8-Bit-Index in der Hardwarepalette gespeichert. Jeder Eintrag in der Hardwarepalette definiert in der Regel eine 24-Bit-Farbe (jeweils 8 rot, grün und blau).

Der Paletten-Manager verwaltet eine *Systempalette,* die eine Kopie der Hardwarepalette ist. Die Systempalette ist in zwei Abschnitte unterteilt: 20 reservierte Farben und die verbleibenden 236 Farben, die Sie mit dem Paletten-Manager festlegen können.

Eine *logische Standardpalette* mit 20 Farben wird ausgewählt und in einem Gerätekontext realisiert. Sie können eine neue logische Palette erstellen und verwenden. Um die Systempalette zu ändern, wählen Sie die erstellte logische Palette aus, und realisieren Sie sie.

Sie erstellen wahrscheinlich eine logische Palette, um die Farben anzugeben, die in Ihrer OpenGL-Anwendung angezeigt werden sollen. Mit bestimmten GDI-Aufrufen können Sie den Großteil der Systempalette vorübergehend durch eine logische Palette ersetzen. Mithilfe einer logischen Palette können Sie Pixelfarben für das GDI definieren, indem Sie entweder den RGBA- oder den Farbindexmodus verwenden. Die maximale Größe einer logischen Palette beträgt 256 Farben für 8-Bit-Geräte und 4.096 Farben auf einem echten Farbgerät (16, 24 und 32 Bits).

Weitere Informationen zum RGBA- und Farbindexmodus finden Sie unter [RGBA-Modus und Windows Palettenverwaltung](rgba-mode-and-windows-palette-management.md) und [OpenGL-Farbmodi und Windows Palettenverwaltung.](opengl-color-modes-and-windows-palette-management.md)

 

 




