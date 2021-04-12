---
description: Die Anwendung wird in der Regel 3D-Szenen realistischer darstellen, wenn farbige Licht Karten verwendet werden. In einer farbigen lichtkarte werden die RGB-Daten in der lichtkarte für die Beleuchtungs Informationen verwendet.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Farb hellen Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483174"
---
# <a name="color-light-maps-direct3d-9"></a>Farb hellen Karten (Direct3D 9)

Die Anwendung wird in der Regel 3D-Szenen realistischer darstellen, wenn farbige Licht Karten verwendet werden. In einer farbigen lichtkarte werden die RGB-Daten in der lichtkarte für die Beleuchtungs Informationen verwendet.

Im folgenden C++-Codebeispiel wird die einfache Zuordnung mit RGB-Farbdaten veranschaulicht.


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



In diesem Beispiel wird die helle Map als erste Textur festgelegt. Anschließend wird der Zustand der ersten Mischungs Phase festgelegt, um die eingehenden Textur Daten zu modulieren. Dabei werden die erste Textur und die aktuelle Farbe des primitiven als Argumente für den modulieren-Vorgang verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einfache Zuordnung mit Texturen](light-mapping-with-textures.md)
</dt> </dl>

 

 



