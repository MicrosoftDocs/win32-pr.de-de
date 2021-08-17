---
description: Einige ältere 3D-Acceleratorboards unterstützen keine Texturmischung mit dem Alphawert des Zielpixels.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Monocolore Light Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac6f62aaba08ac6c8e1116a0bc5059fed3dea19da51d83b034bfae79653ed5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728237"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Monocolore Light Karten (Direct3D 9)

Einige ältere 3D-Acceleratorboards unterstützen keine Texturmischung mit dem Alphawert des Zielpixels. Weitere Informationen finden Sie unter [AlphaTexturmischung (Direct3D 9).](alpha-texture-blending.md) Diese Adapter unterstützen in der Regel auch keine mehrfache Texturmischung. Wenn Ihre Anwendung auf einem Adapter wie diesem ausgeführt wird, kann sie multipass texture blending verwenden, um monocolore Lichtzuordnungen durchzuführen.

Um monocolore Lichtzuordnungen durchzuführen, speichert eine Anwendung die Beleuchtungsinformationen in den Alphadaten ihrer Lichtkartentexturen. Die Anwendung verwendet die Texturfilterfunktionen von Direct3D, um eine Zuordnung von jedem Pixel im Bild des Primitiven zu einem entsprechenden Texel in der Lichtkarte durchzuführen. Der Quellmischungsfaktor wird auf den Alphawert des entsprechenden Texels festgelegt.

Das folgende Beispiel veranschaulicht, wie eine Anwendung eine Textur als monocolore Lichtkarte verwenden kann:


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



Da Anzeigeadapter, die das Alphablending des Ziels nicht unterstützen, in der Regel keine mehrfache Texturmischung unterstützen, wird in diesem Beispiel die Lichtkarte als erste Textur festgelegt, die auf allen 3D-Zugriffstastenkarten verfügbar ist. Der Beispielcode legt den Farbvorgang für die Mischungsphase der Textur fest, um die Texturdaten mit der vorhandenen Farbe des Primitiven zu mischen. Anschließend werden die erste Textur und die vorhandene Farbe des Primitivs als Eingabedaten ausgewählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lichtzuordnung mit Texturen](light-mapping-with-textures.md)
</dt> </dl>

 

 



