---
description: Bei der Beleuchtung durch eine Lichtquelle zeigen Matte Oberflächen diffuses lichtreflektion an.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Diffuses Licht Maps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab6a85fb93bc1ebcc15735431c1d54be4482a1f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481542"
---
# <a name="diffuse-light-maps-direct3d-9"></a>Diffuses Licht Maps (Direct3D 9)

Bei der Beleuchtung durch eine Lichtquelle zeigen Matte Oberflächen diffuses lichtreflektion an. Die Helligkeit von diffuses Licht hängt von der Entfernung von der Lichtquelle und vom Winkel zwischen der Oberflächen normalen und dem Lichtquellen-Vektor ab. Die durch Beleuchtungsberechnungen simulierten diffusen Beleuchtungseffekte ergeben nur allgemeine Auswirkungen.

Die Anwendung kann komplexere diffuses Beleuchtung mit Textur hellen Karten simulieren. Fügen Sie hierzu der Basis Textur das diffuses Licht Map hinzu, wie im folgenden C++-Codebeispiel gezeigt.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einfache Zuordnung mit Texturen](light-mapping-with-textures.md)
</dt> </dl>

 

 



