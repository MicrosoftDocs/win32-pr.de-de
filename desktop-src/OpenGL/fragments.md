---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, Fragmente
- OpenGL-Verarbeitungs Pipeline, Fragmente
- Fragmente OpenGL
- Framebuffers, Fragmente, die Pixel ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337375"
---
# <a name="fragments"></a>Fragments

Ein von Rasterung erstelltes Fragment ändert das entsprechende Pixel im Frame Puffer nur dann, wenn es die folgenden Tests übergibt:

-   [Pixel Besitz Test](pixel-ownership-test.md)
-   [Scissor-Test](scissor-test.md)
-   [Alpha-Test](alpha-test.md)
-   [Schablone-Test](stencil-test.md)
-   [Tiefen Puffer Test](depth-buffer-test.md)

Wenn Sie den Wert übergibt, können die Daten des Fragments die vorhandenen Frame Puffer-Werte ersetzen, oder Sie können Sie mit vorhandenen Daten im Frame Puffer kombinieren, abhängig vom Zustand bestimmter Modi. Sie können das Fragment mit Daten im Frame Puffer kombinieren, indem Sie Folgendes durchführen:

-   [Bänder](blending.md)
-   [Dithering](dithering.md)
-   [Logische Vorgänge](logical-operations.md)

 

 




