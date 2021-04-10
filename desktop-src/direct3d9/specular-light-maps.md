---
description: Bei der Beleuchtung durch eine Lichtquelle werden glänzende Objekte, die stark reflektierenden Materialien verwenden, Glanzlichter erhalten.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Glanzlichter Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55b4bf34baae0e73c2d072d62470533fc99827a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860247"
---
# <a name="specular-light-maps-direct3d-9"></a>Glanzlichter Karten (Direct3D 9)

Bei der Beleuchtung durch eine Lichtquelle werden glänzende Objekte, die stark reflektierenden Materialien verwenden, Glanzlichter erhalten. In einigen Fällen sind die Glanzlichter, die vom Beleuchtungs Modul erzeugt werden, nicht exakt. Um eine ansprechendere Hervorhebung zu schaffen, wenden viele Direct3D-Anwendungen Glanzlicht Zuordnungen auf primitive an.

Fügen Sie zum Durchführen einer Glanzlicht Zuordnung der Textur des primitiven die Glanz Karte hinzu, und führen Sie dann die RGB-lichtkarte modulieren (multipliziert mit) aus.

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

[Einfache Zuordnung mit Texturen](light-mapping-with-textures.md)
</dt> </dl>

 

 



