---
description: Wenn Sie nicht mit einem Scheitelpunkt-Shader oder einem Pixel-Shader lichten, können Sie die Beleuchtungs-Engine in der Runtime verwenden.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Beleuchtungszustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5935590c46776c621535968f4d457f3738d83d02342ffddf832cbf0278bbd9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674270"
---
# <a name="lighting-state-direct3d-9"></a>Beleuchtungszustand (Direct3D 9)

Wenn Sie nicht mit einem Scheitelpunkt-Shader oder einem Pixel-Shader lichten, können Sie die Beleuchtungs-Engine in der Runtime verwenden. Das Beleuchtungsmodul erfordert, dass die Scheitelpunktdaten pro Scheitelpunkt normal sind. Scheitelpunkte ohne normale Daten generieren in allen Beleuchtungsberechnungen ein Punktprodukt von 0 (null). Die Beleuchtungsberechnungen werden unter [Mathematik der Beleuchtung (Direct3D 9)](mathematics-of-lighting.md)ausführlicher behandelt.

Verwenden Sie Folgendes, um die Beleuchtungsmaschine zu aktivieren:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 



