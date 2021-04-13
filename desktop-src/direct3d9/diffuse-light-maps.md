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
# <a name="diffuse-light-maps-direct3d-9"></a><span data-ttu-id="f43b4-103">Diffuses Licht Maps (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f43b4-103">Diffuse Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="f43b4-104">Bei der Beleuchtung durch eine Lichtquelle zeigen Matte Oberflächen diffuses lichtreflektion an.</span><span class="sxs-lookup"><span data-stu-id="f43b4-104">When illuminated by a light source, matte surfaces display diffuse light reflection.</span></span> <span data-ttu-id="f43b4-105">Die Helligkeit von diffuses Licht hängt von der Entfernung von der Lichtquelle und vom Winkel zwischen der Oberflächen normalen und dem Lichtquellen-Vektor ab.</span><span class="sxs-lookup"><span data-stu-id="f43b4-105">The brightness of diffuse light depends on the distance from the light source and the angle between the surface normal and the light source direction vector.</span></span> <span data-ttu-id="f43b4-106">Die durch Beleuchtungsberechnungen simulierten diffusen Beleuchtungseffekte ergeben nur allgemeine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="f43b4-106">The diffuse lighting effects simulated by lighting calculations produce only general effects.</span></span>

<span data-ttu-id="f43b4-107">Die Anwendung kann komplexere diffuses Beleuchtung mit Textur hellen Karten simulieren.</span><span class="sxs-lookup"><span data-stu-id="f43b4-107">Your application can simulate more complex diffuse lighting with texture light maps.</span></span> <span data-ttu-id="f43b4-108">Fügen Sie hierzu der Basis Textur das diffuses Licht Map hinzu, wie im folgenden C++-Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f43b4-108">Do this by adding the diffuse light map to the base texture, as shown in the following C++ code example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f43b4-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f43b4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f43b4-110">Einfache Zuordnung mit Texturen</span><span class="sxs-lookup"><span data-stu-id="f43b4-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



