---
description: Um die Renderingleistung zu verbessern, können Sie eine primitive, die von der Kamera entfernt ist, auslagern (oder entfernen).
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Status der Zertifizierungsstelle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127125"
---
# <a name="culling-state-direct3d-9"></a>Status der Zertifizierungsstelle (Direct3D 9)

Um die Renderingleistung zu verbessern, können Sie eine primitive, die von der Kamera entfernt ist, auslagern (oder entfernen). Bei einseitigen primitiven spart dies die Renderingzeit, da eine Backface nicht sichtbar ist. Um die Daten zu aktivieren, müssen Sie die Sortierreihenfolge der Scheitel Punkte kennen (in der Regel gegen den Uhrzeigersinn). In diesem Beispiel werden alle primitiven entfernt, deren Rückseite vorwärts geht (bei einer Sortierreihenfolge gegen den Uhrzeigersinn):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 



