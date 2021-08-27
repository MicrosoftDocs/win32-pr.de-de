---
title: Front-, Back- und Andere Puffer
description: OpenGL speichert und bearbeitet Pixeldaten in einem Framepuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL für Windows,Buffers
- framebuffers OpenGL
- Farbpuffer OpenGL
- Tiefenpuffer OpenGL
- Akkumulationspuffer OpenGL
- Schablonenpuffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd64f980aad1df8576accd8c37d19521a5368e1fe295393d54c2836f2db8566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082320"
---
# <a name="front-back-and-other-buffers"></a>Front-, Back- und Andere Puffer

OpenGL speichert und bearbeitet Pixeldaten in einem Framepuffer. Der Framepuffer besteht aus einem Satz logischer Puffer: Farb-, Tiefen-, Akkumulations- und Schablonenpuffer. Der Farbpuffer selbst besteht aus einem Satz logischer Puffer. Diese Gruppe kann eine front-left-, eine front-right-, eine back-left-, eine back-right- und einige Anzahl von Hilfspuffern enthalten. Ein bestimmtes Pixelformat oder eine OpenGL-Implementierung stellen möglicherweise nicht alle diese Puffer zur Verfügung. Beispielsweise unterstützt die aktuelle Version der Microsoft-Implementierung von OpenGL in Windows keine Stereobilder, sodass ein Pixelformat keine linken und rechten Farbpuffer aufweisen kann. Darüber hinaus unterstützt die aktuelle Version keine zusätzlichen Puffer. Weitere Informationen zu OpenGL-Puffern und den Damit betriebenen OpenGL-Funktionen finden Sie im *OpenGL-Referenzhandbuch* und im *OpenGL-Programmierhandbuch.*

Die Microsoft-Implementierung von OpenGL in Windows unterstützt die doppelte Pufferung von Bildern. Dies ist eine Technik, bei der eine Anwendung Pixel in einen Off-Screen-Puffer zeichnet und dann, wenn dieses Bild für die Anzeige bereit ist, den Inhalt des Off-Screen-Puffers in einen Bildschirmpuffer kopiert. Die doppelte Pufferung ermöglicht reibungslose Bildänderungen, die besonders wichtig für animierte Bilder sind.

Zwei Farbpuffer sind für Anwendungen verfügbar, die doppelte Pufferung verwenden: einen Frontpuffer und einen Backpuffer. Standardmäßig werden Zeichnungsbefehle an den Hintergrundpuffer (den Off-Screen-Puffer) weitergeleitet, während der Frontpuffer auf dem Bildschirm angezeigt wird. Wenn der Off-Screen-Puffer für die Anzeige bereit ist, rufen Sie [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)auf, und Windows kopiert den Inhalt des Off-Screen-Puffers in den Bildschirmpuffer.

Die generische Implementierung verwendet eine geräteunabhängige Bitmap (DIB) als Hintergrundpuffer und die Bildschirmanzeige als Frontpuffer. Hardwaregeräte und deren Treiber können unterschiedliche Ansätze verwenden.

Die doppelte Pufferung ist eine Eigenschaft im Pixelformat. Um eine doppelte Pufferung für ein Pixelformat anzufordern, legen Sie das PFD \_ DOUBLEBUFFER-Flag in der [**PIXELFORMATDESCRIPTOR-Datenstruktur**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) in einem Aufruf auf [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)fest.

Die OpenGL-Kernfunktion [**glDrawBuffer**](gldrawbuffer.md)wählt Puffer zum Schreiben und Löschen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pufferfunktionen](buffer-functions.md)
</dt> </dl>

 

 




