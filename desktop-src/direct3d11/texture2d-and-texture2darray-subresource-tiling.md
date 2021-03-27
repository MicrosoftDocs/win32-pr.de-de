---
title: Unterteilung von Texture2D- und Texture2DArray-Unterressourcen
description: Diese Tabellen zeigen, wie Texture2D und Texture2DArray-unter Ressourcen nebeneinander angeordnet werden.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390644"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a><span data-ttu-id="b8358-103">Unterteilung von Texture2D- und Texture2DArray-Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="b8358-103">Texture2D and Texture2DArray subresource tiling</span></span>

<span data-ttu-id="b8358-104">Diese Tabellen zeigen, wie [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) -unter Ressourcen nebeneinander angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8358-104">These tables show how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources are tiled.</span></span> <span data-ttu-id="b8358-105">Die Werte in diesen Tabellen zählen nicht zum Ende der MIP-Verpackung.</span><span class="sxs-lookup"><span data-stu-id="b8358-105">The values in these tables don't count tail mip packing.</span></span>

<span data-ttu-id="b8358-106">Diese Tabelle zeigt, wie die unter Ressourcen [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) mit der Multisampling-Anzahl 1 nebeneinander dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8358-106">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with multisample counts of 1 are tiled.</span></span>



| <span data-ttu-id="b8358-107">Bits/Pixel (1 Stichprobe/Pixel)</span><span class="sxs-lookup"><span data-stu-id="b8358-107">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="b8358-108">Kachel Dimensionen (Pixel, WxH)</span><span class="sxs-lookup"><span data-stu-id="b8358-108">Tile Dimensions (Pixels, WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="b8358-109">8</span><span class="sxs-lookup"><span data-stu-id="b8358-109">8</span></span>                           | <span data-ttu-id="b8358-110">256x256</span><span class="sxs-lookup"><span data-stu-id="b8358-110">256x256</span></span>                       |
| <span data-ttu-id="b8358-111">16</span><span class="sxs-lookup"><span data-stu-id="b8358-111">16</span></span>                          | <span data-ttu-id="b8358-112">Größe 256x128</span><span class="sxs-lookup"><span data-stu-id="b8358-112">256x128</span></span>                       |
| <span data-ttu-id="b8358-113">32</span><span class="sxs-lookup"><span data-stu-id="b8358-113">32</span></span>                          | <span data-ttu-id="b8358-114">128x128</span><span class="sxs-lookup"><span data-stu-id="b8358-114">128x128</span></span>                       |
| <span data-ttu-id="b8358-115">64</span><span class="sxs-lookup"><span data-stu-id="b8358-115">64</span></span>                          | <span data-ttu-id="b8358-116">128 x 64</span><span class="sxs-lookup"><span data-stu-id="b8358-116">128x64</span></span>                        |
| <span data-ttu-id="b8358-117">128</span><span class="sxs-lookup"><span data-stu-id="b8358-117">128</span></span>                         | <span data-ttu-id="b8358-118">64 x 64</span><span class="sxs-lookup"><span data-stu-id="b8358-118">64x64</span></span>                         |
| <span data-ttu-id="b8358-119">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="b8358-119">BC1,4</span></span>                       | <span data-ttu-id="b8358-120">512 x 256</span><span class="sxs-lookup"><span data-stu-id="b8358-120">512x256</span></span>                       |
| <span data-ttu-id="b8358-121">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="b8358-121">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="b8358-122">256x256</span><span class="sxs-lookup"><span data-stu-id="b8358-122">256x256</span></span>                       |



 

<span data-ttu-id="b8358-123">Die von den Kachel Ressourcen nicht unterstützten Formatbit-Zahlen sind 96 bpp-Formate, Videoformate, DXGI- \_ Format \_ R1 \_ unorm, DXGI- \_ Format \_ R8G8 \_ B8G8 \_ unorm und DXGI- \_ Format \_ R8R8 \_ G8B8 \_ unorm.</span><span class="sxs-lookup"><span data-stu-id="b8358-123">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="b8358-124">Diese Tabelle zeigt, wie [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) -unter Ressourcen mit verschiedenen Multisampling-Zählungen nebeneinander angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8358-124">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with various multisample counts are tiled.</span></span>



| <span data-ttu-id="b8358-125">Anzahl von mehreren Stichproben</span><span class="sxs-lookup"><span data-stu-id="b8358-125">Multisample Count</span></span>           | <span data-ttu-id="b8358-126">Aufteilen von Kachel Dimensionen oberhalb durch (WxH)</span><span class="sxs-lookup"><span data-stu-id="b8358-126">Divide Tile Dimensions Above by (WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="b8358-127">1</span><span class="sxs-lookup"><span data-stu-id="b8358-127">1</span></span>                           | <span data-ttu-id="b8358-128">1x1</span><span class="sxs-lookup"><span data-stu-id="b8358-128">1x1</span></span>                           |
| <span data-ttu-id="b8358-129">2</span><span class="sxs-lookup"><span data-stu-id="b8358-129">2</span></span>                           | <span data-ttu-id="b8358-130">2x1</span><span class="sxs-lookup"><span data-stu-id="b8358-130">2x1</span></span>                           |
| <span data-ttu-id="b8358-131">4</span><span class="sxs-lookup"><span data-stu-id="b8358-131">4</span></span>                           | <span data-ttu-id="b8358-132">2 x 2</span><span class="sxs-lookup"><span data-stu-id="b8358-132">2x2</span></span>                           |
| <span data-ttu-id="b8358-133">8</span><span class="sxs-lookup"><span data-stu-id="b8358-133">8</span></span>                           | <span data-ttu-id="b8358-134">4x2</span><span class="sxs-lookup"><span data-stu-id="b8358-134">4x2</span></span>                           |
| <span data-ttu-id="b8358-135">16</span><span class="sxs-lookup"><span data-stu-id="b8358-135">16</span></span>                          | <span data-ttu-id="b8358-136">4x4</span><span class="sxs-lookup"><span data-stu-id="b8358-136">4x4</span></span>                           |



 

<span data-ttu-id="b8358-137">Nur die Stichproben Anzahl 1 und 4 sind erforderlich (und zulässig), damit Sie mit gekachelten Ressourcen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b8358-137">Only sample counts 1 and 4 are required (and allowed) to be supported with tiled resources.</span></span> <span data-ttu-id="b8358-138">Gekachelte Ressourcen unterstützen derzeit nicht 2, 8 und 16, obwohl Sie angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8358-138">Tiled resources don't currently support 2, 8, and 16 even though they are shown.</span></span>

<span data-ttu-id="b8358-139">Implementierungen können für nicht gekachelte Ressourcen zwei, 8 und/oder 16 Sample Multisampling Antialiasing (MSAA)-Modus unterstützen, auch wenn Sie von einer gekachelten Ressource nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b8358-139">Implementations can choose to support 2, 8, and/or 16 sample multisample antialiasing (MSAA) mode for non-tiled resources even though tiled resource don't support them.</span></span>

<span data-ttu-id="b8358-140">Gekachelte Ressourcen mit Stichproben Anzahl größer als 1 können 128 bpp-Formate nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8358-140">Tiled resources with sample counts larger than 1 can't use 128 bpp formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8358-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8358-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8358-142">Kacheln eines gekachelten Ressourcenbereichs</span><span class="sxs-lookup"><span data-stu-id="b8358-142">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 