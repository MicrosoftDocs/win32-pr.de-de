---
title: Unterteilung von Texture3D-Unterressourcen
description: Diese Tabelle zeigt, wie Texture3D-unter Ressourcen nebeneinander angeordnet werden.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993606"
---
# <a name="texture3d-subresource-tiling"></a><span data-ttu-id="a0470-103">Unterteilung von Texture3D-Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="a0470-103">Texture3D subresource tiling</span></span>

<span data-ttu-id="a0470-104">Diese Tabelle zeigt, wie [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) -unter Ressourcen nebeneinander angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a0470-104">This table shows how [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) subresources are tiled.</span></span> <span data-ttu-id="a0470-105">Die Werte in dieser Tabelle zählen nicht zum Ende der MIP-Verpackung.</span><span class="sxs-lookup"><span data-stu-id="a0470-105">The values in this table don't count tail mip packing.</span></span>

<span data-ttu-id="a0470-106">In dieser Tabelle wird das [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) -tichen berücksichtigt, und die x/y-Dimensionen werden um 4 dividiert, und es werden 16 Ebenen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a0470-106">This table takes the [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) tiling and divides the x/y dimensions by 4 each and adds 16 layers of depth.</span></span> <span data-ttu-id="a0470-107">Alle Kacheln für die erste Ebene (2D-Ebene der Kacheln, die die ersten 16 Ebenen der Tiefe definieren) werden vor den nachfolgenden Ebenen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0470-107">All the tiles for the first plane (2D plane of tiles defining the first 16 layers of depth) appear before the subsequent planes.</span></span>

> [!Note]  
> <span data-ttu-id="a0470-108">Die [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) -Unterstützung in gekachelten Ressourcen wird in der ersten Implementierung von gekachelten Ressourcen nicht verfügbar gemacht, die gewünschten Kachel Formen werden hier jedoch aufgeführt, da die Unterstützung in einer zukünftigen Version möglicherweise berücksichtigt</span><span class="sxs-lookup"><span data-stu-id="a0470-108">[**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) support in tiled resources isn't exposed in the initial implementation of tiled resources, but the desired tile shapes are listed here because support might be consideration in a future release.</span></span>

 



| <span data-ttu-id="a0470-109">Bits/Pixel (1 Stichprobe/Pixel)</span><span class="sxs-lookup"><span data-stu-id="a0470-109">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="a0470-110">Kachel Dimensionen (Pixel, WxHxD)</span><span class="sxs-lookup"><span data-stu-id="a0470-110">Tile Dimensions (Pixels, WxHxD)</span></span> |
|-----------------------------|---------------------------------|
| <span data-ttu-id="a0470-111">8</span><span class="sxs-lookup"><span data-stu-id="a0470-111">8</span></span>                           | <span data-ttu-id="a0470-112">64x32x32</span><span class="sxs-lookup"><span data-stu-id="a0470-112">64x32x32</span></span>                        |
| <span data-ttu-id="a0470-113">16</span><span class="sxs-lookup"><span data-stu-id="a0470-113">16</span></span>                          | <span data-ttu-id="a0470-114">32x32x32</span><span class="sxs-lookup"><span data-stu-id="a0470-114">32x32x32</span></span>                        |
| <span data-ttu-id="a0470-115">32</span><span class="sxs-lookup"><span data-stu-id="a0470-115">32</span></span>                          | <span data-ttu-id="a0470-116">32x32x16</span><span class="sxs-lookup"><span data-stu-id="a0470-116">32x32x16</span></span>                        |
| <span data-ttu-id="a0470-117">64</span><span class="sxs-lookup"><span data-stu-id="a0470-117">64</span></span>                          | <span data-ttu-id="a0470-118">32x16x16</span><span class="sxs-lookup"><span data-stu-id="a0470-118">32x16x16</span></span>                        |
| <span data-ttu-id="a0470-119">128</span><span class="sxs-lookup"><span data-stu-id="a0470-119">128</span></span>                         | <span data-ttu-id="a0470-120">16x16x16</span><span class="sxs-lookup"><span data-stu-id="a0470-120">16x16x16</span></span>                        |
| <span data-ttu-id="a0470-121">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="a0470-121">BC1,4</span></span>                       | <span data-ttu-id="a0470-122">128 x 64x16</span><span class="sxs-lookup"><span data-stu-id="a0470-122">128x64x16</span></span>                       |
| <span data-ttu-id="a0470-123">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="a0470-123">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="a0470-124">64x64x16</span><span class="sxs-lookup"><span data-stu-id="a0470-124">64x64x16</span></span>                        |



 

<span data-ttu-id="a0470-125">Die von den Kachel Ressourcen nicht unterstützten Formatbit-Zahlen sind 96 bpp-Formate, Videoformate, DXGI- \_ Format \_ R1 \_ unorm, DXGI- \_ Format \_ R8G8 \_ B8G8 \_ unorm und DXGI- \_ Format \_ R8R8 \_ G8B8 \_ unorm.</span><span class="sxs-lookup"><span data-stu-id="a0470-125">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0470-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0470-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0470-127">Kacheln eines gekachelten Ressourcenbereichs</span><span class="sxs-lookup"><span data-stu-id="a0470-127">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 