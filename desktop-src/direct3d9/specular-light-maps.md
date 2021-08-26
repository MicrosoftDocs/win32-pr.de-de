---
description: Wenn sie von einer Lichtquelle gespiegelt werden, erhalten helle Objekte – diejenigen, die stark reflektierende Materialien verwenden – Glanzlichter.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Specular Light Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05362eb4c0b79ebb980a6c0acb1607713765a446c0ef27823ae0e648cef88d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026100"
---
# <a name="specular-light-maps-direct3d-9"></a>Specular Light Karten (Direct3D 9)

Wenn sie von einer Lichtquelle gespiegelt werden, erhalten helle Objekte – diejenigen, die stark reflektierende Materialien verwenden – Glanzlichter. In einigen Fällen sind die vom Beleuchtungsmodul erzeugten Glanzlichter nicht genau. Um eine ansprechendere Hervorhebung zu erzeugen, wenden viele Direct3D-Anwendungen Glanzlichtzuordnungen auf Primitive an.

Fügen Sie zum Durchführen der Specular Light Mapping (Lichtkartierung mit Specular) der Textur des Primitivs die Lichtkarte hinzu, und modulieren Sie dann die RGB-Lichtkarte (multiplizieren Sie das Ergebnis mit ).

Im folgenden Codebeispiel wird dieser Prozess in C++ veranschaulicht.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Light Mapping with Textures](light-mapping-with-textures.md)
</dt> </dl>

 

 



