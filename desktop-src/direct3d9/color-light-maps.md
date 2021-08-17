---
description: Ihre Anwendung rendert 3D-Szenen in der Regel realistischer, wenn sie farbige Lichtkarten verwendet. Eine farbige Lichtkarte verwendet die RGB-Daten in der Lichtkarte für ihre Beleuchtungsinformationen.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Color Light Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbff9fe246131fc90bda8ac9b5f1c49cd2413c412a7b3da5c013b1e936aa6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989300"
---
# <a name="color-light-maps-direct3d-9"></a>Color Light Karten (Direct3D 9)

Ihre Anwendung rendert 3D-Szenen in der Regel realistischer, wenn sie farbige Lichtkarten verwendet. Eine farbige Lichtkarte verwendet die RGB-Daten in der Lichtkarte für ihre Beleuchtungsinformationen.

Im folgenden C++-Codebeispiel wird die Lichtzuordnung mit RGB-Farbdaten veranschaulicht.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



In diesem Beispiel wird die Lichtkarte als erste Textur festgelegt. Anschließend wird der Zustand der ersten Mischungsphase festgelegt, um die eingehenden Texturdaten zu modulieren. Sie verwendet die erste Textur und die aktuelle Farbe des Primitiven als Argumente für den Modulierenvorgang.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lichtzuordnung mit Texturen](light-mapping-with-textures.md)
</dt> </dl>

 

 



