---
description: Einige ältere 3D-Zugriffstasten bieten keine Unterstützung für Textur Mischungen mithilfe des Alphawerts des Zielpixels.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Monochrome helle Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346183"
---
# <a name="monochrome-light-maps-direct3d-9"></a><span data-ttu-id="15ce8-103">Monochrome helle Karten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="15ce8-103">Monochrome Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="15ce8-104">Einige ältere 3D-Zugriffstasten bieten keine Unterstützung für Textur Mischungen mithilfe des Alphawerts des Zielpixels.</span><span class="sxs-lookup"><span data-stu-id="15ce8-104">Some older 3D accelerator boards do not support texture blending using the alpha value of the destination pixel.</span></span> <span data-ttu-id="15ce8-105">Weitere Informationen finden Sie unter [Alpha Textur blending (Direct3D 9)](alpha-texture-blending.md) .</span><span class="sxs-lookup"><span data-stu-id="15ce8-105">See [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) for more information.</span></span> <span data-ttu-id="15ce8-106">Diese Adapter unterstützen in der Regel auch keine mehrfach Textur Mischung.</span><span class="sxs-lookup"><span data-stu-id="15ce8-106">These adapters also generally do not support multiple texture blending.</span></span> <span data-ttu-id="15ce8-107">Wenn die Anwendung auf einem Adapter wie diesem ausgeführt wird, kann Sie Multipass-Textur Mischungs Vorgänge verwenden, um eine monochrome einfache Zuordnung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="15ce8-107">If your application is running on an adapter such as this, it can use multipass texture blending to perform monochrome light mapping.</span></span>

<span data-ttu-id="15ce8-108">Zum Durchführen einer Monochrom-Licht Zuordnung speichert eine Anwendung die Beleuchtungs Informationen in den Alpha Daten ihrer hellen Karten Texturen.</span><span class="sxs-lookup"><span data-stu-id="15ce8-108">To perform monochrome light mapping, an application stores the lighting information in the alpha data of its light map textures.</span></span> <span data-ttu-id="15ce8-109">Die Anwendung verwendet die Textur Filterungs Funktionen von Direct3D, um eine Zuordnung von jedem Pixel im primitiven Bild zu einem entsprechenden Texel in der lichtkarte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="15ce8-109">The application uses the texture filtering capabilities of Direct3D to perform a mapping from each pixel in the primitive's image to a corresponding texel in the light map.</span></span> <span data-ttu-id="15ce8-110">Der quellmischungs Faktor wird auf den Alpha Wert des entsprechenden Texttyps festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15ce8-110">It sets the source blending factor to the alpha value of the corresponding texel.</span></span>

<span data-ttu-id="15ce8-111">Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung eine Textur als monochrome Light map verwenden kann:</span><span class="sxs-lookup"><span data-stu-id="15ce8-111">The following example illustrates how an application can use a texture as a monochrome light map:</span></span>


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



<span data-ttu-id="15ce8-112">Da Anzeige Adapter, die keine Ziel-Alpha-Blending unterstützen, in der Regel nicht mehrere Textur Mischungen unterstützen, wird in diesem Beispiel die helle Karte als erste Textur festgelegt, die auf allen 3D-Zugriffs Karten verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="15ce8-112">Because display adapters that do not support destination alpha blending usually do not support multiple texture blending, this example sets the light map as the first texture, which is available on all 3D accelerator cards.</span></span> <span data-ttu-id="15ce8-113">Im Beispielcode wird der Farb Vorgang für die Mischungs Phase der Textur festgelegt, um die Textur Daten mit der vorhandenen Farbe des Primitivs zu vermischen.</span><span class="sxs-lookup"><span data-stu-id="15ce8-113">The sample code sets the color operation for the texture's blending stage to blend the texture data with the primitive's existing color.</span></span> <span data-ttu-id="15ce8-114">Anschließend werden die erste Textur und die vorhandene Farbe des primitiven als Eingabedaten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="15ce8-114">It then selects the first texture and the primitive's existing color as the input data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15ce8-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15ce8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15ce8-116">Einfache Zuordnung mit Texturen</span><span class="sxs-lookup"><span data-stu-id="15ce8-116">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



