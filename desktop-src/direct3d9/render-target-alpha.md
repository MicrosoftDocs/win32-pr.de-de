---
description: Der Framepufferblender kann jetzt Alphakanäle unabhängig von Farbkanalblending auf Renderzielen mischen. Dieses Steuerelement wird mit dem neuen Renderzustand D3DRS \_ SEPARATEALPHABLENDENABLE aktiviert.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Renderziel alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5d4701b2d09334d605cf2c90ef0e03b06ea7886ea875ce8ec8ff9cbc428ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797935"
---
# <a name="render-target-alpha-direct3d-9"></a>Renderziel alpha (Direct3D 9)

Der Framepufferblender kann jetzt Alphakanäle unabhängig von Farbkanalblending auf Renderzielen mischen. Dieses Steuerelement wird mit dem neuen Renderzustand D3DRS \_ SEPARATEALPHABLENDENABLE aktiviert.

Wenn D3DRS \_ SEPARATEALPHABLENDENABLE auf **FALSE** festgelegt ist (dies ist die Standardbedingung), sind die auf Alpha angewendeten Renderingzielmischungsfaktoren und -vorgänge identisch mit denen, die für das Mischen von Farbkanälen definiert sind. Ein Treiber muss die D3DPMISCCAPS \_ SEPARATEALPHABLEND-Kapselung festlegen, um anzugeben, dass das Renderziel-Alphablending unterstützt werden kann. Stellen Sie sicher, dass Sie D3DRS \_ ALPHABLEND aktivieren, um der Pipeline mitzuteilen, dass Alphamischung erforderlich ist.

Um die Faktoren im Alphakanal der Renderzielblender zu steuern, werden zwei neue Renderzustände wie folgt definiert:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Wie D3DRS \_ SRCBLEND und D3DRS \_ DESTBLEND können diese auf einen der Werte in der [**D3DBLEND-Enumeration**](./d3dblend.md) festgelegt werden. Die Quell- und Zielmischungseinstellungen können auf verschiedene Weise kombiniert werden, abhängig von den Einstellungen in den Membern SrcBlendCaps und DestBlendCaps von [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

Die Alphamischung erfolgt wie folgt:

renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)

Hierbei gilt:

-   alpha<sub>in</sub> ist der Alpha-Eingabewert.
-   srcBlendOp ist einer der Mischungsfaktoren in [**D3DBLEND**](./d3dblend.md).
-   BlendOp ist einer der Mischungsfaktoren in [**D3DBLENDOP.**](./d3dblendop.md)
-   alpha<sub>rt</sub> ist der Alphawert des Renderziels.
-   destBlendOp ist einer der Mischungsfaktoren in [**D3DBLEND**](./d3dblend.md).
-   renderTargetAlpha ist der endgültige gemischte Alphawert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alphablending](alpha-blending.md)
</dt> </dl>

 

 
