---
title: Front, Back und andere Puffer
description: OpenGL speichert und manipuliert Pixeldaten in einem Framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL unter Windows, Puffer
- Framebuffers OpenGL
- Farb Puffer OpenGL
- tiefen Puffer OpenGL
- Akkumulations Puffer OpenGL
- Schablonen Puffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388442"
---
# <a name="front-back-and-other-buffers"></a>Front, Back und andere Puffer

OpenGL speichert und manipuliert Pixeldaten in einem Framebuffer. Der Frame Puffer besteht aus einem Satz logischer Puffer: Farb-, tiefen-, Akkumulations-und Schablonen Puffer. Der Farb Puffer selbst besteht aus einem Satz logischer Puffer. Diese Menge kann ein Front-Left-, ein Front-Right-, ein-Links-, ein-Rechts-und eine bestimmte Anzahl von zusätzlichen Puffern enthalten. In einer bestimmten Pixel Format-oder OpenGL-Implementierung werden möglicherweise nicht alle diese Puffer bereitgestellt. Beispielsweise unterstützt die aktuelle Version der Microsoft-Implementierung von OpenGL in Windows keine Stereotyp-Bilder, sodass ein Pixel Format keine linken und rechten Farb Puffer aufweisen kann. Außerdem werden zusätzliche Puffer von der aktuellen Version nicht unterstützt. Weitere Informationen zu OpenGL-Puffern und den OpenGL-Funktionen, die darauf angewendet werden, finden Sie im *OpenGL-Referenzhandbuch* und im *OpenGL-Programmier* Handbuch.

Die Microsoft-Implementierung von OpenGL in Windows unterstützt die doppelte Pufferung von Bildern. Dabei handelt es sich um eine Technik, bei der eine Anwendung Pixel auf einen Offscreen-Puffer zeichnet und dann, wenn dieses Bild bereit für die Anzeige ist, den Inhalt des Offscreen-Puffers in einen Bildschirm Puffer kopiert. Die doppelte Pufferung ermöglicht Smooth-Abbild Änderungen, die für animierte Bilder besonders wichtig sind.

Für Anwendungen, die doppelte Pufferung verwenden, sind zwei Farb Puffer verfügbar: ein Front-und ein Hintergrund Puffer. Standardmäßig werden Zeichnungs Befehle an den Hintergrund Puffer (den Offscreen-Puffer) umgeleitet, während der Front-Puffer auf dem Bildschirm angezeigt wird. Wenn der Offscreen-Puffer für die Anzeige bereit ist, wird " [**Swap Buffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)" aufgerufen, und Windows kopiert den Inhalt des Offscreen-Puffers in den Bildschirm Puffer.

Die generische Implementierung verwendet eine geräteunabhängige Bitmap (DIB) als Hintergrund Puffer und die Bildschirm Anzeige als Vorder-Puffer. Hardware Geräte und deren Treiber können unterschiedliche Ansätze verwenden.

Die doppelte Pufferung ist eine Eigenschaft im Pixel Format. Um die doppelte Pufferung für ein Pixel Format anzufordern, legen Sie das PFD- \_ Double Buffer-Flag in der Datenstruktur " [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) " in einem aufzurufenden " [**choosepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)" fest.

Die OpenGL-Kernfunktion, [**gldrawbuffer**](gldrawbuffer.md), wählt Puffer zum Schreiben und löschen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pufferfunktionen](buffer-functions.md)
</dt> </dl>

 

 




