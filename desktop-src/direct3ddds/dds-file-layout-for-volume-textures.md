---
title: Beispiel für DDS-volumetextur
description: Verwenden Sie für eine volumetextur die DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, ddsd \_ -Tiefe, Flags und Set und dwtiefe. Eine volumetextur ist eine Erweiterung einer Standard Textur für Direct3D 9; eine volumetextur kann mit oder ohne Mipmaps definiert werden.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338194"
---
# <a name="dds-volume-texture-example"></a><span data-ttu-id="07bb2-104">Beispiel für DDS-volumetextur</span><span class="sxs-lookup"><span data-stu-id="07bb2-104">DDS Volume Texture Example</span></span>

<span data-ttu-id="07bb2-105">Verwenden Sie für eine volumetextur die DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, ddsd \_ -Tiefe, Flags und Set und dwtiefe.</span><span class="sxs-lookup"><span data-stu-id="07bb2-105">For a volume texture, use the DDSCAPS\_COMPLEX, DDSCAPS2\_VOLUME, DDSD\_DEPTH, flags and set and dwDepth.</span></span> <span data-ttu-id="07bb2-106">Eine volumetextur ist eine Erweiterung einer Standard Textur für Direct3D 9; eine volumetextur kann mit oder ohne Mipmaps definiert werden.</span><span class="sxs-lookup"><span data-stu-id="07bb2-106">A volume texture is an extension of a standard texture for Direct3D 9; a volume texture is can be defined with or without mipmaps.</span></span>

<span data-ttu-id="07bb2-107">Für Volumes ohne Mipmaps wird jedes tiefen Slice in der richtigen Reihenfolge in die Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="07bb2-107">For volumes without mipmaps, each depth slice is written to the file in order.</span></span> <span data-ttu-id="07bb2-108">Wenn Mipmaps eingeschlossen werden, werden alle tiefen Slices für eine bestimmte MipMap-Ebene miteinander geschrieben, wobei jede Ebene die Hälfte so viele Slices wie die vorherige Ebene mit einem Mindestwert von 1 enthält.</span><span class="sxs-lookup"><span data-stu-id="07bb2-108">If mipmaps are included, all depth slices for a given mipmap level are written together, with each level containing half as many slices as the previous level with a minimum of 1.</span></span>

<span data-ttu-id="07bb2-109">Beispielsweise würde eine 64-by-64 von-4-volumekarte, die das Pixel Format R8G8B8 (3 Bytes pro Pixel) mit allen MipMap-Ebenen verwendet, Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="07bb2-109">For example, a 64-by-64-by-4 volume map using a pixel format of R8G8B8 (3 bytes per pixel) with all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="07bb2-110">DDS-Komponenten</span><span class="sxs-lookup"><span data-stu-id="07bb2-110">DDS Components</span></span>                      | <span data-ttu-id="07bb2-111">\# Satz</span><span class="sxs-lookup"><span data-stu-id="07bb2-111">\# Bytes</span></span>    |
|-------------------------------------|-------------|
| <span data-ttu-id="07bb2-112">header</span><span class="sxs-lookup"><span data-stu-id="07bb2-112">header</span></span>                              | <span data-ttu-id="07bb2-113">128 Bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-113">128 bytes</span></span>   |
| <span data-ttu-id="07bb2-114">64-bis-64 Slice 1 von 4 Hauptbild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-114">64-by-64 slice 1 of 4 main image.</span></span>   | <span data-ttu-id="07bb2-115">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-115">12288 bytes</span></span> |
| <span data-ttu-id="07bb2-116">64-bis-64 Slice 2 von 4 Hauptbild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-116">64-by-64 slice 2 of 4 main image.</span></span>   | <span data-ttu-id="07bb2-117">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-117">12288 bytes</span></span> |
| <span data-ttu-id="07bb2-118">64-bis-64 Slice 3 von 4 Hauptbild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-118">64-by-64 slice 3 of 4 main image.</span></span>   | <span data-ttu-id="07bb2-119">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-119">12288 bytes</span></span> |
| <span data-ttu-id="07bb2-120">64-bis-64 Slice 4 von 4 Hauptbild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-120">64-by-64 slice 4 of 4 main image.</span></span>   | <span data-ttu-id="07bb2-121">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-121">12288 bytes</span></span> |
| <span data-ttu-id="07bb2-122">32-bis-32 Slice 1 von 2 MipMap-Bild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-122">32-by-32 slice 1 of 2 mipmap image.</span></span> | <span data-ttu-id="07bb2-123">3072 bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-123">3072 bytes</span></span>  |
| <span data-ttu-id="07bb2-124">32-bis-32 Slice 2 von 2 MipMap-Bild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-124">32-by-32 slice 2 of 2 mipmap image.</span></span> | <span data-ttu-id="07bb2-125">3072 bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-125">3072 bytes</span></span>  |
| <span data-ttu-id="07bb2-126">16-bis-16-Slice 1 von 1 MipMap-Bild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-126">16-by-16 slice 1 of 1 mipmap image.</span></span> | <span data-ttu-id="07bb2-127">768 Bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-127">768 bytes</span></span>   |
| <span data-ttu-id="07bb2-128">8 x 8 Slice 1 von 1 MipMap-Bild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-128">8-by-8 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="07bb2-129">192 Bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-129">192 bytes</span></span>   |
| <span data-ttu-id="07bb2-130">4 x 4 Slice 1 von 1 MipMap-Bild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-130">4-by-4 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="07bb2-131">48 Bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-131">48 bytes</span></span>    |
| <span data-ttu-id="07bb2-132">2:2 Slice 1 von 1 MipMap-Bild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-132">2-by-2 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="07bb2-133">12 Bytes</span><span class="sxs-lookup"><span data-stu-id="07bb2-133">12 bytes</span></span>    |
| <span data-ttu-id="07bb2-134">1 bis 1 Slice 1 von 1 MipMap-Bild.</span><span class="sxs-lookup"><span data-stu-id="07bb2-134">1-by-1 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="07bb2-135">3 Byte</span><span class="sxs-lookup"><span data-stu-id="07bb2-135">3 bytes</span></span>     |



 

<span data-ttu-id="07bb2-136">Beachten Sie, dass die kleinste MipMap-Ebene nur 3 Bytes beträgt, da die Bitzahl 24 beträgt und auf dieser Ebene keine Komprimierung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="07bb2-136">Note that the smallest mipmap level is only 3 bytes because the bitcount is 24 and there is no added compression at this level.</span></span>

<span data-ttu-id="07bb2-137">Unterstützung für Volumentexturen wurde in DirectX 8 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="07bb2-137">Support for volume textures was added in DirectX 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07bb2-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07bb2-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07bb2-139">Programmier Handbuch für DDS</span><span class="sxs-lookup"><span data-stu-id="07bb2-139">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




