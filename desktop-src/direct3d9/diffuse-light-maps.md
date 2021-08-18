---
description: Wenn sie von einer Lichtquelle gespiegelt werden, zeigen matte Oberflächen diffuse Lichtlektion an.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Diffuse Light Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fc2b5054a30bf8df703941b3cedf0810c378a5fb459d8c5783bb295ff9abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044448"
---
# <a name="diffuse-light-maps-direct3d-9"></a>Diffuse Light Karten (Direct3D 9)

Wenn sie von einer Lichtquelle gespiegelt werden, zeigen matte Oberflächen diffuse Lichtlektion an. Die Helligkeit des diffusen Lichts hängt vom Abstand von der Lichtquelle und dem Winkel zwischen der Oberflächennormale und dem Lichtquellenrichtungsvektor ab. Die von Beleuchtungsberechnungen simulierten diffusen Beleuchtungseffekte erzeugen nur allgemeine Effekte.

Ihre Anwendung kann komplexere diffuse Beleuchtung mit Texturlichtkarten simulieren. Fügen Sie hierzu der Basistextur die diffuse Lichtkarte hinzu, wie im folgenden C++-Codebeispiel gezeigt.


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

[Light Mapping with Textures](light-mapping-with-textures.md)
</dt> </dl>

 

 



