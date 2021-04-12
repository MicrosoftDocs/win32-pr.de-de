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
# <a name="color-light-maps-direct3d-9"></a><span data-ttu-id="432fb-104">Farb hellen Karten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="432fb-104">Color Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="432fb-105">Die Anwendung wird in der Regel 3D-Szenen realistischer darstellen, wenn farbige Licht Karten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="432fb-105">Your application will usually render 3D scenes more realistically if it uses colored light maps.</span></span> <span data-ttu-id="432fb-106">In einer farbigen lichtkarte werden die RGB-Daten in der lichtkarte für die Beleuchtungs Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="432fb-106">A colored light map uses the RGB data in the light map for its lighting information.</span></span>

<span data-ttu-id="432fb-107">Im folgenden C++-Codebeispiel wird die einfache Zuordnung mit RGB-Farbdaten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="432fb-107">The following C++ code example demonstrates light mapping with RGB color data.</span></span>


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



<span data-ttu-id="432fb-108">In diesem Beispiel wird die helle Map als erste Textur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="432fb-108">This example sets the light map as the first texture.</span></span> <span data-ttu-id="432fb-109">Anschließend wird der Zustand der ersten Mischungs Phase festgelegt, um die eingehenden Textur Daten zu modulieren.</span><span class="sxs-lookup"><span data-stu-id="432fb-109">It then sets the state of the first blending stage to modulate the incoming texture data.</span></span> <span data-ttu-id="432fb-110">Dabei werden die erste Textur und die aktuelle Farbe des primitiven als Argumente für den modulieren-Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="432fb-110">It uses the first texture and the current color of the primitive as the arguments to the modulate operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="432fb-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="432fb-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="432fb-112">Einfache Zuordnung mit Texturen</span><span class="sxs-lookup"><span data-stu-id="432fb-112">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



