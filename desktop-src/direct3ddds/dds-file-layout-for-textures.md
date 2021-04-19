---
title: Beispiel für DDS-Textur
description: Verwenden Sie für eine nicht komprimierte Textur die ddsd \_ -und ddpf- \_ RGB-Flags. verwenden Sie für eine komprimierte Textur die ddsd \_ -Informationen linearsize und ddpf \_ FourCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342278"
---
# <a name="dds-texture-example"></a><span data-ttu-id="cff8b-103">Beispiel für DDS-Textur</span><span class="sxs-lookup"><span data-stu-id="cff8b-103">DDS Texture Example</span></span>

<span data-ttu-id="cff8b-104">Verwenden Sie für eine nicht komprimierte Textur die ddsd \_ -und ddpf- \_ RGB-Flags. verwenden Sie für eine komprimierte Textur die ddsd \_ -Informationen linearsize und ddpf \_ FourCC.</span><span class="sxs-lookup"><span data-stu-id="cff8b-104">For an uncompressed texture, use the DDSD\_PITCH and DDPF\_RGB flags; for a compressed texture, use the DDSD\_LINEARSIZE and DDPF\_FOURCC flags.</span></span> <span data-ttu-id="cff8b-105">Verwenden Sie für eine mipzugeordnete Textur die \_ komplexen Flags ddsd mipmapcount, DDSCAPS \_ MIPMAP und DDSCAPS sowie \_ das Element MIPMAP count.</span><span class="sxs-lookup"><span data-stu-id="cff8b-105">For a mipmapped texture, use the DDSD\_MIPMAPCOUNT, DDSCAPS\_MIPMAP, and DDSCAPS\_COMPLEX flags also as well as the mipmap count member.</span></span> <span data-ttu-id="cff8b-106">Wenn Mipmaps generiert werden, werden alle Ebenen, die bis zu 1 bis 1 liegen, in der Regel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="cff8b-106">If mipmaps are generated, all levels down to 1-by-1 are usually written.</span></span>

<span data-ttu-id="cff8b-107">Bei einer komprimierten Textur ist die Größe jedes Bilds auf MipMap-Ebene in der Regel eine vierte der Größe des vorherigen Bilds, mit mindestens 8 (DXT1) oder 16 (DXT2-5) Bytes (für quadratische Texturen).</span><span class="sxs-lookup"><span data-stu-id="cff8b-107">For a compressed texture, the size of each mipmap level image is typically one-fourth the size of the previous, with a minimum of 8 (DXT1) or 16 (DXT2-5) bytes (for square textures).</span></span> <span data-ttu-id="cff8b-108">Verwenden Sie die folgende Formel, um die Größe der einzelnen Ebenen für eine nicht quadratische Textur zu berechnen:</span><span class="sxs-lookup"><span data-stu-id="cff8b-108">Use the following formula to calculate the size of each level for a non-square texture:</span></span>


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



<span data-ttu-id="cff8b-109">In dieser Tabelle wird der von jeder Schicht benötigte Speicherplatz für eine 256-by-256 R8G8B8-Textur ohne Komprimierung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cff8b-109">This table lists the amount of space taken up by each layer for a 256-by-256 R8G8B8 texture, without using compression.</span></span>



| <span data-ttu-id="cff8b-110">DDS-Komponenten</span><span class="sxs-lookup"><span data-stu-id="cff8b-110">DDS Components</span></span>          | <span data-ttu-id="cff8b-111">\# Satz</span><span class="sxs-lookup"><span data-stu-id="cff8b-111">\# Bytes</span></span> |
|-------------------------|----------|
| <span data-ttu-id="cff8b-112">header</span><span class="sxs-lookup"><span data-stu-id="cff8b-112">header</span></span>                  | <span data-ttu-id="cff8b-113">128</span><span class="sxs-lookup"><span data-stu-id="cff8b-113">128</span></span>      |
| <span data-ttu-id="cff8b-114">256-bis 256-Haupt Abbild</span><span class="sxs-lookup"><span data-stu-id="cff8b-114">256-by-256 main image</span></span>   | <span data-ttu-id="cff8b-115">196608</span><span class="sxs-lookup"><span data-stu-id="cff8b-115">196608</span></span>   |
| <span data-ttu-id="cff8b-116">128-nach-128-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-116">128-by-128 mipmap image</span></span> | <span data-ttu-id="cff8b-117">49152</span><span class="sxs-lookup"><span data-stu-id="cff8b-117">49152</span></span>    |
| <span data-ttu-id="cff8b-118">64-nach-64-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-118">64-by-64 mipmap image</span></span>   | <span data-ttu-id="cff8b-119">12288</span><span class="sxs-lookup"><span data-stu-id="cff8b-119">12288</span></span>    |
| <span data-ttu-id="cff8b-120">32-nach-32-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-120">32-by-32 mipmap image</span></span>   | <span data-ttu-id="cff8b-121">3072</span><span class="sxs-lookup"><span data-stu-id="cff8b-121">3072</span></span>     |
| <span data-ttu-id="cff8b-122">16-by-16-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-122">16-by-16 mipmap image</span></span>   | <span data-ttu-id="cff8b-123">768</span><span class="sxs-lookup"><span data-stu-id="cff8b-123">768</span></span>      |
| <span data-ttu-id="cff8b-124">8-bis-8-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-124">8-by-8 mipmap image</span></span>     | <span data-ttu-id="cff8b-125">192</span><span class="sxs-lookup"><span data-stu-id="cff8b-125">192</span></span>      |
| <span data-ttu-id="cff8b-126">4 x 4-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-126">4-by-4 mipmap image</span></span>     | <span data-ttu-id="cff8b-127">48</span><span class="sxs-lookup"><span data-stu-id="cff8b-127">48</span></span>       |
| <span data-ttu-id="cff8b-128">Bild von 2 x 2 MipMap</span><span class="sxs-lookup"><span data-stu-id="cff8b-128">2-by-2 mipmap image</span></span>     | <span data-ttu-id="cff8b-129">12</span><span class="sxs-lookup"><span data-stu-id="cff8b-129">12</span></span>       |
| <span data-ttu-id="cff8b-130">1:1-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-130">1-by-1 mipmap image</span></span>     | <span data-ttu-id="cff8b-131">3</span><span class="sxs-lookup"><span data-stu-id="cff8b-131">3</span></span>        |



 

<span data-ttu-id="cff8b-132">In dieser Tabelle wird der von jeder Ebene benötigte Speicherplatz für die gleiche Textur mithilfe von Komprimierung (DXT1) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cff8b-132">This table lists the amount of space taken up by each layer for the same texture using compression (DXT1).</span></span>



| <span data-ttu-id="cff8b-133">DDS-Komponenten</span><span class="sxs-lookup"><span data-stu-id="cff8b-133">DDS Components</span></span>         | <span data-ttu-id="cff8b-134">\# Satz</span><span class="sxs-lookup"><span data-stu-id="cff8b-134">\# Bytes</span></span> |
|------------------------|----------|
| <span data-ttu-id="cff8b-135">header</span><span class="sxs-lookup"><span data-stu-id="cff8b-135">header</span></span>                 | <span data-ttu-id="cff8b-136">128</span><span class="sxs-lookup"><span data-stu-id="cff8b-136">128</span></span>      |
| <span data-ttu-id="cff8b-137">256-bis 64-Haupt Abbild</span><span class="sxs-lookup"><span data-stu-id="cff8b-137">256-by-64 main image</span></span>   | <span data-ttu-id="cff8b-138">8192</span><span class="sxs-lookup"><span data-stu-id="cff8b-138">8192</span></span>     |
| <span data-ttu-id="cff8b-139">128-nach-32-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-139">128-by-32 mipmap image</span></span> | <span data-ttu-id="cff8b-140">2048</span><span class="sxs-lookup"><span data-stu-id="cff8b-140">2048</span></span>     |
| <span data-ttu-id="cff8b-141">64-x-16-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-141">64-by-16 mipmap image</span></span>  | <span data-ttu-id="cff8b-142">512</span><span class="sxs-lookup"><span data-stu-id="cff8b-142">512</span></span>      |
| <span data-ttu-id="cff8b-143">32-x-8-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-143">32-by-8 mipmap image</span></span>   | <span data-ttu-id="cff8b-144">128</span><span class="sxs-lookup"><span data-stu-id="cff8b-144">128</span></span>      |
| <span data-ttu-id="cff8b-145">16-x-4-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-145">16-by-4 mipmap image</span></span>   | <span data-ttu-id="cff8b-146">32</span><span class="sxs-lookup"><span data-stu-id="cff8b-146">32</span></span>       |
| <span data-ttu-id="cff8b-147">8-x-2-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-147">8-by-2 mipmap image</span></span>    | <span data-ttu-id="cff8b-148">16</span><span class="sxs-lookup"><span data-stu-id="cff8b-148">16</span></span>       |
| <span data-ttu-id="cff8b-149">4-x-1-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-149">4-by-1 mipmap image</span></span>    | <span data-ttu-id="cff8b-150">8</span><span class="sxs-lookup"><span data-stu-id="cff8b-150">8</span></span>        |
| <span data-ttu-id="cff8b-151">2:1 MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-151">2-by-1 mipmap image</span></span>    | <span data-ttu-id="cff8b-152">8</span><span class="sxs-lookup"><span data-stu-id="cff8b-152">8</span></span>        |
| <span data-ttu-id="cff8b-153">1:1-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-153">1-by-1 mipmap image</span></span>    | <span data-ttu-id="cff8b-154">8</span><span class="sxs-lookup"><span data-stu-id="cff8b-154">8</span></span>        |



 

<span data-ttu-id="cff8b-155">In dieser Tabelle wird der von jeder Ebene benötigte Speicherplatz für die gleiche Textur mit einem DXGI-Komprimierungs Format (in diesem Fall BC3 \_ unorm) aufgelistet, das daher den erweiterten Header erfordert:</span><span class="sxs-lookup"><span data-stu-id="cff8b-155">This table lists the amount of space taken up by each layer for the same texture using a DXGI compression format (in this case BC3\_UNORM) that therefore requires the extended header:</span></span>



| <span data-ttu-id="cff8b-156">DDS-Komponenten</span><span class="sxs-lookup"><span data-stu-id="cff8b-156">DDS Components</span></span>                                                | <span data-ttu-id="cff8b-157">\# Satz</span><span class="sxs-lookup"><span data-stu-id="cff8b-157">\# Bytes</span></span> |
|---------------------------------------------------------------|----------|
| <span data-ttu-id="cff8b-158">Header (FourCC ist auf "DX10" festgelegt)</span><span class="sxs-lookup"><span data-stu-id="cff8b-158">header (FourCC set to "DX10")</span></span>                                 | <span data-ttu-id="cff8b-159">128</span><span class="sxs-lookup"><span data-stu-id="cff8b-159">128</span></span>      |
| <span data-ttu-id="cff8b-160">Extended-Header (DXGI-Format ist auf DXGI-Format festgelegt \_ \_ BC3 \_ unorm)</span><span class="sxs-lookup"><span data-stu-id="cff8b-160">extended header (DXGI format set to DXGI\_FORMAT\_BC3\_UNORM)</span></span> | <span data-ttu-id="cff8b-161">20</span><span class="sxs-lookup"><span data-stu-id="cff8b-161">20</span></span>       |
| <span data-ttu-id="cff8b-162">256-bis 64-Haupt Abbild</span><span class="sxs-lookup"><span data-stu-id="cff8b-162">256-by-64 main image</span></span>                                          | <span data-ttu-id="cff8b-163">16384</span><span class="sxs-lookup"><span data-stu-id="cff8b-163">16384</span></span>    |
| <span data-ttu-id="cff8b-164">128-nach-32-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-164">128-by-32 mipmap image</span></span>                                        | <span data-ttu-id="cff8b-165">4096</span><span class="sxs-lookup"><span data-stu-id="cff8b-165">4096</span></span>     |
| <span data-ttu-id="cff8b-166">64-x-16-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-166">64-by-16 mipmap image</span></span>                                         | <span data-ttu-id="cff8b-167">1024</span><span class="sxs-lookup"><span data-stu-id="cff8b-167">1024</span></span>     |
| <span data-ttu-id="cff8b-168">32-x-8-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-168">32-by-8 mipmap image</span></span>                                          | <span data-ttu-id="cff8b-169">256</span><span class="sxs-lookup"><span data-stu-id="cff8b-169">256</span></span>      |
| <span data-ttu-id="cff8b-170">16-x-4-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-170">16-by-4 mipmap image</span></span>                                          | <span data-ttu-id="cff8b-171">64</span><span class="sxs-lookup"><span data-stu-id="cff8b-171">64</span></span>       |
| <span data-ttu-id="cff8b-172">8-x-2-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-172">8-by-2 mipmap image</span></span>                                           | <span data-ttu-id="cff8b-173">32</span><span class="sxs-lookup"><span data-stu-id="cff8b-173">32</span></span>       |
| <span data-ttu-id="cff8b-174">4-x-1-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-174">4-by-1 mipmap image</span></span>                                           | <span data-ttu-id="cff8b-175">16</span><span class="sxs-lookup"><span data-stu-id="cff8b-175">16</span></span>       |
| <span data-ttu-id="cff8b-176">2:1 MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-176">2-by-1 mipmap image</span></span>                                           | <span data-ttu-id="cff8b-177">16</span><span class="sxs-lookup"><span data-stu-id="cff8b-177">16</span></span>       |
| <span data-ttu-id="cff8b-178">1:1-MipMap-Bild</span><span class="sxs-lookup"><span data-stu-id="cff8b-178">1-by-1 mipmap image</span></span>                                           | <span data-ttu-id="cff8b-179">16</span><span class="sxs-lookup"><span data-stu-id="cff8b-179">16</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="cff8b-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cff8b-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff8b-181">Programmier Handbuch für DDS</span><span class="sxs-lookup"><span data-stu-id="cff8b-181">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




