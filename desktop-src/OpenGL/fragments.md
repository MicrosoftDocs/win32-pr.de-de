---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL,Fragmente
- OpenGL-Verarbeitungspipeline, Fragmente
- Fragmente OpenGL
- framebuffers,fragments modifying pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab5d4124445455e518e4f091730e6e38e899442785b9f86ef73a230b99fbd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082410"
---
# <a name="fragments"></a>Fragments

Ein durch die Rasterung erzeugtes Fragment ändert das entsprechende Pixel im Framepuffer nur, wenn es die folgenden Tests besteht:

-   [Testen des Pixelbesitzes](pixel-ownership-test.md)
-   [Scissor-Test](scissor-test.md)
-   [Alphatest](alpha-test.md)
-   [Schablonentest](stencil-test.md)
-   [Tiefenpuffertest](depth-buffer-test.md)

Wenn sie übergeht, können die Daten des Fragments die vorhandenen Framepufferwerte ersetzen, oder Sie können sie je nach Zustand bestimmter Modi mit vorhandenen Daten im Framepuffer kombinieren. Sie können das Fragment mit Daten im Framepuffer kombinieren, indem Sie:

-   [Mischung](blending.md)
-   [Dithering](dithering.md)
-   [Logische Vorgänge](logical-operations.md)

 

 




