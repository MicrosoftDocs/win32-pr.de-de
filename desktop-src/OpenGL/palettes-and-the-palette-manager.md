---
title: Paletten und der Palette-Manager
description: Der Windows-palettenmanager, der Teil des GDI ist, zielt speziell auf 8-Bit-Anzeige Adapter mit einer Hardware Palette von 256-Farb Einträgen ab.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL unter Windows, Palette Manager
- OpenGL unter Windows, Hardware Paletten
- Palette-Manager OpenGL
- Hardware Paletten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341855"
---
# <a name="palettes-and-the-palette-manager"></a>Paletten und der Palette-Manager

Der Windows-palettenmanager, der Teil des GDI ist, zielt speziell auf 8-Bit-Anzeige Adapter mit einer *Hardware Palette* von 256-Farb Einträgen ab. Pixel auf dem Bildschirm werden als 8-Bit-Index in der Hardware Palette gespeichert. Jeder Eintrag in der Hardware Palette definiert in der Regel eine 24-Bit-Farbe (8 von rot, grün und blau).

Der Palette-Manager verwaltet eine *Systempalette* , bei der es sich um eine Kopie der Hardware Palette handelt. Die Systempalette ist in zwei Abschnitte unterteilt: 20 reservierte Farben und die restlichen 236-Farben, die Sie mit dem palettenmanager festlegen können.

Eine standardmäßige, 20-farbige, *logische Palette* wird ausgewählt und in einem Gerätekontext realisiert. Sie können eine neue logische Palette erstellen und verwenden. Wählen Sie die logische Palette aus, die Sie erstellt haben, um die Systempalette zu ändern.

Wahrscheinlich erstellen Sie eine logische Palette, um die Farben anzugeben, die Sie in ihrer OpenGL-Anwendung anzeigen möchten. Mit bestimmten GDI-aufrufen können Sie den größten Teil der Systempalette temporär durch eine logische Palette ersetzen. Mithilfe einer logischen Palette können Sie Pixel Farben für das GDI mithilfe des RGBA-oder des Farb Index Modus definieren. Die maximale Größe einer logischen Palette beträgt 256 Farben für 8-Bit-Geräte und 4.096-Farben auf einem echten Farbgerät (16, 24 und 32 Bits).

Weitere Informationen zu den Modi RGBA und Color-Index finden Sie unter [RGBA-Modus und Windows-Palettenverwaltung](rgba-mode-and-windows-palette-management.md) und [OpenGL-Farbmodi und Windows-Palettenverwaltung](opengl-color-modes-and-windows-palette-management.md).

 

 




