---
description: Um die Renderingleistung zu verbessern, können Sie einen Primitiv, der gesichtert, von der Kamera entfernen (oder entfernen).
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Culling State (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bf9d8ed8ecea46dcfee146784dc97a38e42f0261b8f78bfc9d45ffaf99ddd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608030"
---
# <a name="culling-state-direct3d-9"></a>Culling State (Direct3D 9)

Um die Renderingleistung zu verbessern, können Sie einen Primitiv, der gesichtert, von der Kamera entfernen (oder entfernen). Bei einseitigen Primitiven spart dies Renderingzeit, da ein Back-Face nicht sichtbar ist. Um Culling zu aktivieren, müssen Sie die Wickelrichtung der Scheitelungen kennen (in der Regel gegen den Uhrzeigersinn). In diesem Beispiel werden alle Primitiven entfernt, deren Hintergesicht nach vorn gerichtet ist (bei einer gegen den Uhrzeigersinn gerichteten Windungsrichtung):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 



