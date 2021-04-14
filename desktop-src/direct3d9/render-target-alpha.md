---
description: Der Frame Puffer Blender kann nun Alphakanäle unabhängig von der Farb Kanal Mischung bei renderzielen vermischen. Dieses Steuerelement wird mit einem neuen Rendering-Zustand aktiviert, D3DRS \_ separatealphablendenable.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Renderziel Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520475"
---
# <a name="render-target-alpha-direct3d-9"></a>Renderziel Alpha (Direct3D 9)

Der Frame Puffer Blender kann nun Alphakanäle unabhängig von der Farb Kanal Mischung bei renderzielen vermischen. Dieses Steuerelement wird mit einem neuen Rendering-Zustand aktiviert, D3DRS \_ separatealphablendenable.

Wenn D3DRS \_ separatealphablendenable auf **false** festgelegt ist (Dies ist die Standard Bedingung), sind die auf Alpha angewendeten Mischungs Ziel Faktoren und-Vorgänge identisch mit denen, die für das Mischen von Farbkanälen definiert sind. Ein Treiber muss das Limit von D3DPMISCCAPS \_ separatealphablend festlegen, um anzugeben, dass es das Mischen von renderzielalpha unterstützen kann. Stellen Sie sicher, dass Sie D3DRS \_ AlphaBlend aktivieren, um der Pipeline mitzuteilen, dass Alpha Blending benötigt wird.

Um die Faktoren im Alphakanal der Renderer des Renderziels zu steuern, werden zwei neue renderzustände wie folgt definiert:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Wie D3DRS \_ srcblend und D3DRS \_ destblend können diese auf einen der Werte in der [**D3DBLEND**](./d3dblend.md) -Enumeration festgelegt werden. Die Blend-Einstellungen für Quelle und Ziel können auf verschiedene Arten kombiniert werden, abhängig von den Einstellungen in den srcblendcaps-und destblendcaps-Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

Die Alpha Mischung erfolgt wie folgt:

rendertargetalpha = (Alpha<sub>in</sub> \* srcblendop) blendop (Alpha<sub>RT</sub> \* destblendop)

Hierbei gilt:

-   Alpha<sub>in</sub> ist der eingabealphawert.
-   srcblendop ist einer der Blend-Faktoren in [**D3DBLEND**](./d3dblend.md).
-   Blendop ist einer der Blend-Faktoren in [**D3DBLENDOP**](./d3dblendop.md).
-   Alpha<sub>RT</sub> ist der Wert für den Renderziel-Alpha Wert.
-   destblendop ist einer der Blend-Faktoren in [**D3DBLEND**](./d3dblend.md).
-   rendertargetalpha ist der abschließende gemischte Alpha-Wert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 
