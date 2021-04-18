---
description: Wenn Sie nicht mit einem Vertex-Shader oder einem Pixelshader Leuchten, können Sie die Beleuchtungs-Engine in der Laufzeit verwenden.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Beleuchtungs Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339646"
---
# <a name="lighting-state-direct3d-9"></a>Beleuchtungs Zustand (Direct3D 9)

Wenn Sie nicht mit einem Vertex-Shader oder einem Pixelshader Leuchten, können Sie die Beleuchtungs-Engine in der Laufzeit verwenden. Die Beleuchtungs-Engine erfordert, dass die Vertex-Daten pro-vertexnormale enthalten. Vertices ohne normale Daten generieren in allen Beleuchtungsberechnungen ein Punktprodukt von NULL. Die Beleuchtungsberechnungen werden in der [Mathematik der Beleuchtung ausführlicher behandelt (Direct3D 9)](mathematics-of-lighting.md).

Verwenden Sie zum Aktivieren der Beleuchtungs-Engine Folgendes:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 



