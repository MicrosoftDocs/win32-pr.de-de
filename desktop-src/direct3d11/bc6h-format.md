---
title: BC6H-Format
description: Das BC6H-Format ist ein Textur Komprimierungs Format, das für die Unterstützung von HDR-Farbräumen (High Dynamic Range) in Quelldaten konzipiert ist.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed4b934df742a4d2c99e20b52b7172b64e598dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039347"
---
# <a name="bc6h-format"></a><span data-ttu-id="85188-105">BC6H-Format</span><span class="sxs-lookup"><span data-stu-id="85188-105">BC6H Format</span></span>

<span data-ttu-id="85188-106">Das BC6H-Format ist ein Textur Komprimierungs Format, das für die Unterstützung von HDR-Farbräumen (High Dynamic Range) in Quelldaten konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="85188-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="85188-107">Informationen zum BC6H/DXGI- \_ Format \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="85188-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="85188-108">BC6H-Implementierung</span><span class="sxs-lookup"><span data-stu-id="85188-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="85188-109">Decodieren des BC6H-Formats</span><span class="sxs-lookup"><span data-stu-id="85188-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="85188-110">BC6H-komprimiertes Endpunkt Format</span><span class="sxs-lookup"><span data-stu-id="85188-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="85188-111">Signieren der Erweiterung für Endpunkt Werte</span><span class="sxs-lookup"><span data-stu-id="85188-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="85188-112">Inversion für Endpunkt Werte transformieren</span><span class="sxs-lookup"><span data-stu-id="85188-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="85188-113">Unquantifization von Farb Endpunkten</span><span class="sxs-lookup"><span data-stu-id="85188-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="85188-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85188-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="85188-115">Informationen zum BC6H/DXGI- \_ Format \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="85188-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="85188-116">Das BC6H-Format bietet hochwertige Komprimierung für Bilder, die drei HDR-Farbkanäle verwenden, mit einem 16-Bit-Wert für jeden Farbkanal des Werts (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="85188-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="85188-117">Es gibt keine Unterstützung für einen Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="85188-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="85188-118">BC6H wird durch die folgenden DXGI- \_ formatenumerationswerte angegeben:</span><span class="sxs-lookup"><span data-stu-id="85188-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="85188-119">**DXGI \_ Format \_ BC6H \_ typlose Formatierung**.</span><span class="sxs-lookup"><span data-stu-id="85188-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="85188-120">**DXGI \_ Format \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="85188-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="85188-121">Dieses BC6H-Format verwendet kein Signier Bit in den 16-Bit-Farb Kanal Werten für Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="85188-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="85188-122">**DXGI \_ Format \_ BC6H \_ SF16**. Dieses BC6H-Format verwendet ein Signier Bit in den 16-Bit-Farb Kanal Werten für Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="85188-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="85188-123">Das 16-Bit-Gleit Komma Format für Farbkanäle wird häufig als "halb"-Gleit Komma Format bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="85188-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="85188-124">Dieses Format weist das folgende bitlayout auf:</span><span class="sxs-lookup"><span data-stu-id="85188-124">This format has the following bit layout:</span></span>
>
> |                       |                                                 |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="85188-125">UF16 (unsigned float)</span><span class="sxs-lookup"><span data-stu-id="85188-125">UF16 (unsigned float)</span></span> | <span data-ttu-id="85188-126">5 Exponent Bits + 11 Mantisse Bits</span><span class="sxs-lookup"><span data-stu-id="85188-126">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="85188-127">SF16 (mit Vorzeichen signiert)</span><span class="sxs-lookup"><span data-stu-id="85188-127">SF16 (signed float)</span></span>   | <span data-ttu-id="85188-128">1 Vorzeichen Bit + 5 Exponent Bits + 10 Mantisse Bits</span><span class="sxs-lookup"><span data-stu-id="85188-128">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="85188-129">Das BC6H-Format kann für die Textur Ressourcen [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (einschließlich Arrays), Texture3D oder texturecube (einschließlich Arrays) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85188-129">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="85188-130">Ebenso gilt dieses Format für alle mit diesen Ressourcen verknüpften MIP-Map-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="85188-130">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="85188-131">BC6H verwendet eine fester Blockgröße von 16 Bytes (128 Bits) und eine fixierte Kachel Größe von 4 x 4 texeln.</span><span class="sxs-lookup"><span data-stu-id="85188-131">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="85188-132">Wie bei früheren BC-Formaten werden Textur Bilder, die größer als die unterstützte Kachel Größe (4X4) sind, mithilfe mehrerer Blöcke komprimiert.</span><span class="sxs-lookup"><span data-stu-id="85188-132">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="85188-133">Diese Adressierungs Identität gilt auch für dreidimensionale Bilder, MIP-Maps, Cubemaps und Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="85188-133">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="85188-134">Alle Bildkacheln müssen das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="85188-134">All image tiles must be of the same format.</span></span>

<span data-ttu-id="85188-135">Einige wichtige Hinweise zum BC6H-Format:</span><span class="sxs-lookup"><span data-stu-id="85188-135">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="85188-136">BC6H unterstützt die Floating-Point-Denormalisierung, unterstützt jedoch nicht inf (unendlich) und NaN (keine Zahl).</span><span class="sxs-lookup"><span data-stu-id="85188-136">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="85188-137">Die Ausnahme ist der signierte Modus von BC6H (DXGI \_ Format \_ BC6H \_ SF16), der-INF unterstützt (minus unendlich).</span><span class="sxs-lookup"><span data-stu-id="85188-137">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="85188-138">Beachten Sie, dass diese Unterstützung für-INF lediglich ein Element des Formats selbst ist und nicht explizit von Encodern für dieses Format unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="85188-138">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="85188-139">Im Allgemeinen sollten \\ diese Daten in den maximal zulässigen nicht-INF-Darstellungs Wert konvertiert werden, wenn die Encoder inf-(positive oder negative) oder NaN-Eingabedaten begegnen.</span><span class="sxs-lookup"><span data-stu-id="85188-139">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="85188-140">BC6H unterstützt keinen Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="85188-140">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="85188-141">Der BC6H-Decoder führt die Komprimierung aus, bevor die Textur Filterung durchführt.</span><span class="sxs-lookup"><span data-stu-id="85188-141">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="85188-142">Die BC6H-decokomprimierung muss etwas genau sein. Das heißt, dass die Hardware Ergebnisse zurückgeben muss, die mit dem in dieser Dokumentation beschriebenen Decoder identisch sind.</span><span class="sxs-lookup"><span data-stu-id="85188-142">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="85188-143">BC6H-Implementierung</span><span class="sxs-lookup"><span data-stu-id="85188-143">BC6H Implementation</span></span>

<span data-ttu-id="85188-144">Ein BC6H-Block besteht aus modusbits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen Partitions Index.</span><span class="sxs-lookup"><span data-stu-id="85188-144">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="85188-145">Dieses Format gibt 14 verschiedene Modi an.</span><span class="sxs-lookup"><span data-stu-id="85188-145">This format specifies 14 different modes.</span></span>

<span data-ttu-id="85188-146">Eine Endpunktfarbe wird als RGB-Dreieck gespeichert.</span><span class="sxs-lookup"><span data-stu-id="85188-146">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="85188-147">BC6H definiert eine Palette von Farben in einer ungefähren Linie für eine Reihe definierter Farb Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="85188-147">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="85188-148">Abhängig vom Modus kann eine Kachel auch in zwei Bereiche aufgeteilt oder als eine einzelne Region behandelt werden, in der eine Kachel mit zwei Regionen über einen separaten Satz von Farb Endpunkten für jede Region verfügt.</span><span class="sxs-lookup"><span data-stu-id="85188-148">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="85188-149">BC6H speichert einen Palettenindex pro Texel.</span><span class="sxs-lookup"><span data-stu-id="85188-149">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="85188-150">Im Fall von zwei Regionen gibt es 32 mögliche Partitionen.</span><span class="sxs-lookup"><span data-stu-id="85188-150">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="85188-151">Decodieren des BC6H-Formats</span><span class="sxs-lookup"><span data-stu-id="85188-151">Decoding the BC6H Format</span></span>

<span data-ttu-id="85188-152">Der folgende Pseudo Code zeigt die Schritte zum Dekomprimieren des Pixels bei (x, y), wenn der 16-Byte-BC6H-Block angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85188-152">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

<span data-ttu-id="85188-153">Die folgende Tabelle enthält die Bitanzahl und die Werte für jedes der 14 möglichen Formate für BC6H-Blöcke.</span><span class="sxs-lookup"><span data-stu-id="85188-153">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="85188-154">Modus</span><span class="sxs-lookup"><span data-stu-id="85188-154">Mode</span></span> | <span data-ttu-id="85188-155">Partitions Indizes</span><span class="sxs-lookup"><span data-stu-id="85188-155">Partition Indices</span></span> | <span data-ttu-id="85188-156">Partition</span><span class="sxs-lookup"><span data-stu-id="85188-156">Partition</span></span> | <span data-ttu-id="85188-157">Farb Endpunkte</span><span class="sxs-lookup"><span data-stu-id="85188-157">Color Endpoints</span></span>                  | <span data-ttu-id="85188-158">Modusbits</span><span class="sxs-lookup"><span data-stu-id="85188-158">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="85188-159">1</span><span class="sxs-lookup"><span data-stu-id="85188-159">1</span></span>    | <span data-ttu-id="85188-160">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-160">46 bits</span></span>           | <span data-ttu-id="85188-161">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-161">5 bits</span></span>    | <span data-ttu-id="85188-162">75 Bits (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="85188-162">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="85188-163">2 Bits (00)</span><span class="sxs-lookup"><span data-stu-id="85188-163">2 bits (00)</span></span>    |
| <span data-ttu-id="85188-164">2</span><span class="sxs-lookup"><span data-stu-id="85188-164">2</span></span>    | <span data-ttu-id="85188-165">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-165">46 bits</span></span>           | <span data-ttu-id="85188-166">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-166">5 bits</span></span>    | <span data-ttu-id="85188-167">75 Bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="85188-167">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="85188-168">2 Bits (01)</span><span class="sxs-lookup"><span data-stu-id="85188-168">2 bits (01)</span></span>    |
| <span data-ttu-id="85188-169">3</span><span class="sxs-lookup"><span data-stu-id="85188-169">3</span></span>    | <span data-ttu-id="85188-170">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-170">46 bits</span></span>           | <span data-ttu-id="85188-171">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-171">5 bits</span></span>    | <span data-ttu-id="85188-172">72 Bits (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="85188-172">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="85188-173">5 Bits (00010)</span><span class="sxs-lookup"><span data-stu-id="85188-173">5 bits (00010)</span></span> |
| <span data-ttu-id="85188-174">4</span><span class="sxs-lookup"><span data-stu-id="85188-174">4</span></span>    | <span data-ttu-id="85188-175">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-175">46 bits</span></span>           | <span data-ttu-id="85188-176">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-176">5 bits</span></span>    | <span data-ttu-id="85188-177">72 Bits (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="85188-177">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="85188-178">5 Bits (00110)</span><span class="sxs-lookup"><span data-stu-id="85188-178">5 bits (00110)</span></span> |
| <span data-ttu-id="85188-179">5</span><span class="sxs-lookup"><span data-stu-id="85188-179">5</span></span>    | <span data-ttu-id="85188-180">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-180">46 bits</span></span>           | <span data-ttu-id="85188-181">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-181">5 bits</span></span>    | <span data-ttu-id="85188-182">72 Bits (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="85188-182">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="85188-183">5 Bits (01010)</span><span class="sxs-lookup"><span data-stu-id="85188-183">5 bits (01010)</span></span> |
| <span data-ttu-id="85188-184">6</span><span class="sxs-lookup"><span data-stu-id="85188-184">6</span></span>    | <span data-ttu-id="85188-185">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-185">46 bits</span></span>           | <span data-ttu-id="85188-186">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-186">5 bits</span></span>    | <span data-ttu-id="85188-187">72 Bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="85188-187">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="85188-188">5 Bits (01110)</span><span class="sxs-lookup"><span data-stu-id="85188-188">5 bits (01110)</span></span> |
| <span data-ttu-id="85188-189">7</span><span class="sxs-lookup"><span data-stu-id="85188-189">7</span></span>    | <span data-ttu-id="85188-190">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-190">46 bits</span></span>           | <span data-ttu-id="85188-191">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-191">5 bits</span></span>    | <span data-ttu-id="85188-192">72 Bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="85188-192">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="85188-193">5 Bits (10010)</span><span class="sxs-lookup"><span data-stu-id="85188-193">5 bits (10010)</span></span> |
| <span data-ttu-id="85188-194">8</span><span class="sxs-lookup"><span data-stu-id="85188-194">8</span></span>    | <span data-ttu-id="85188-195">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-195">46 bits</span></span>           | <span data-ttu-id="85188-196">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-196">5 bits</span></span>    | <span data-ttu-id="85188-197">72 Bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="85188-197">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="85188-198">5 Bits (10110)</span><span class="sxs-lookup"><span data-stu-id="85188-198">5 bits (10110)</span></span> |
| <span data-ttu-id="85188-199">9</span><span class="sxs-lookup"><span data-stu-id="85188-199">9</span></span>    | <span data-ttu-id="85188-200">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-200">46 bits</span></span>           | <span data-ttu-id="85188-201">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-201">5 bits</span></span>    | <span data-ttu-id="85188-202">72 Bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="85188-202">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="85188-203">5 Bits (11010)</span><span class="sxs-lookup"><span data-stu-id="85188-203">5 bits (11010)</span></span> |
| <span data-ttu-id="85188-204">10</span><span class="sxs-lookup"><span data-stu-id="85188-204">10</span></span>   | <span data-ttu-id="85188-205">46 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-205">46 bits</span></span>           | <span data-ttu-id="85188-206">5 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-206">5 bits</span></span>    | <span data-ttu-id="85188-207">72 Bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="85188-207">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="85188-208">5 Bits (11110)</span><span class="sxs-lookup"><span data-stu-id="85188-208">5 bits (11110)</span></span> |
| <span data-ttu-id="85188-209">11</span><span class="sxs-lookup"><span data-stu-id="85188-209">11</span></span>   | <span data-ttu-id="85188-210">63 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-210">63 bits</span></span>           | <span data-ttu-id="85188-211">0 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-211">0 bits</span></span>    | <span data-ttu-id="85188-212">60 Bits (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="85188-212">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="85188-213">5 Bits (00011)</span><span class="sxs-lookup"><span data-stu-id="85188-213">5 bits (00011)</span></span> |
| <span data-ttu-id="85188-214">12</span><span class="sxs-lookup"><span data-stu-id="85188-214">12</span></span>   | <span data-ttu-id="85188-215">63 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-215">63 bits</span></span>           | <span data-ttu-id="85188-216">0 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-216">0 bits</span></span>    | <span data-ttu-id="85188-217">60 Bits (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="85188-217">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="85188-218">5 Bits (00111)</span><span class="sxs-lookup"><span data-stu-id="85188-218">5 bits (00111)</span></span> |
| <span data-ttu-id="85188-219">13</span><span class="sxs-lookup"><span data-stu-id="85188-219">13</span></span>   | <span data-ttu-id="85188-220">63 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-220">63 bits</span></span>           | <span data-ttu-id="85188-221">0 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-221">0 bits</span></span>    | <span data-ttu-id="85188-222">60 Bits (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="85188-222">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="85188-223">5 Bits (01011)</span><span class="sxs-lookup"><span data-stu-id="85188-223">5 bits (01011)</span></span> |
| <span data-ttu-id="85188-224">14</span><span class="sxs-lookup"><span data-stu-id="85188-224">14</span></span>   | <span data-ttu-id="85188-225">63 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-225">63 bits</span></span>           | <span data-ttu-id="85188-226">0 Bits</span><span class="sxs-lookup"><span data-stu-id="85188-226">0 bits</span></span>    | <span data-ttu-id="85188-227">60 Bits (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="85188-227">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="85188-228">5 Bits (01111)</span><span class="sxs-lookup"><span data-stu-id="85188-228">5 bits (01111)</span></span> |



 

<span data-ttu-id="85188-229">Jedes Format in dieser Tabelle kann durch die modusbits eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="85188-229">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="85188-230">Die ersten zehn Modi werden für Kacheln mit zwei Regionen verwendet, und das Bitfeld des Modus kann entweder zwei oder fünf Bits lang sein.</span><span class="sxs-lookup"><span data-stu-id="85188-230">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="85188-231">Diese Blöcke verfügen auch über Felder für die komprimierten Farb Endpunkte (72 oder 75 Bits), die Partition (5 Bits) und die Partitions Indizes (46 Bits).</span><span class="sxs-lookup"><span data-stu-id="85188-231">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="85188-232">Für die komprimierten Farb Endpunkte notieren die Werte in der obigen Tabelle die Genauigkeit der gespeicherten RGB-Endpunkte und die Anzahl der Bits, die für die einzelnen Farbwerte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85188-232">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="85188-233">Beispielsweise gibt Modus 3 eine farbend Punktgenauigkeit von 11 und die Anzahl der Bits an, die zum Speichern der Delta Werte der transformierten Endpunkte für die Farben rot, blau und grün (5, 4 bzw. 4) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85188-233">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="85188-234">Der Modus 10 verwendet keine Delta Komprimierung und speichert stattdessen alle vier Farb Endpunkte explizit.</span><span class="sxs-lookup"><span data-stu-id="85188-234">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="85188-235">Die letzten vier Block Modi werden für Kacheln der einzelnen Regionen verwendet, wobei das Feld Modus 5 Bits ist.</span><span class="sxs-lookup"><span data-stu-id="85188-235">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="85188-236">Diese Blöcke verfügen über Felder für die Endpunkte (60 Bits) und die komprimierten Indizes (63 Bits).</span><span class="sxs-lookup"><span data-stu-id="85188-236">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="85188-237">Der Modus 11 (z. b. Modus 10) verwendet keine Delta Komprimierung, sondern speichert beide Farb Endpunkte explizit.</span><span class="sxs-lookup"><span data-stu-id="85188-237">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="85188-238">Die Modi 10011, 10111, 11011 und 11111 (nicht angezeigt) sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="85188-238">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="85188-239">Verwenden Sie diese nicht im Encoder.</span><span class="sxs-lookup"><span data-stu-id="85188-239">Do not use these in your encoder.</span></span> <span data-ttu-id="85188-240">Wenn die Hardware Blöcke mit einem dieser Modi überschritten werden, muss der resultierende dekomprimierte Block alle Nullen in allen Kanälen mit Ausnahme des Alphakanals enthalten.</span><span class="sxs-lookup"><span data-stu-id="85188-240">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="85188-241">Bei BC6H muss der Alphakanal unabhängig vom Modus immer 1,0 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="85188-241">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="85188-242">BC6H-Partitions Satz</span><span class="sxs-lookup"><span data-stu-id="85188-242">BC6H Partition Set</span></span>

<span data-ttu-id="85188-243">Es gibt 32 mögliche Partitions Sätze für eine Kachel mit zwei Regionen, die in der folgenden Tabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="85188-243">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="85188-244">Jeder 4X4-Block stellt eine einzelne Form dar.</span><span class="sxs-lookup"><span data-stu-id="85188-244">Each 4x4 block represents a single shape.</span></span>

![Tabelle von bc6h-Partitions Sätzen](images/bc6h-partition-sets.png)

<span data-ttu-id="85188-246">In dieser Tabelle mit Partitions Sätzen ist der fett formatierten und unterstrichene Eintrag der Speicherort des fixupindex für die Teilmenge 1 (die mit einem geringeren Bit angegeben wird).</span><span class="sxs-lookup"><span data-stu-id="85188-246">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="85188-247">Der fixupindex für Teilmenge 0 ist immer Index 0, da die Partitionierung immer so angeordnet ist, dass Index 0 immer in der Teilmenge 0 ist.</span><span class="sxs-lookup"><span data-stu-id="85188-247">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="85188-248">Die Partitions Reihenfolge wechselt von oben links nach unten rechts, von links nach rechts und von oben nach unten.</span><span class="sxs-lookup"><span data-stu-id="85188-248">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="85188-249">BC6H-komprimiertes Endpunkt Format</span><span class="sxs-lookup"><span data-stu-id="85188-249">BC6H Compressed Endpoint Format</span></span>

![Bitfelder für bc6h-komprimierte Endpunkt Formate](images/bc6h-headers-med.png)

<span data-ttu-id="85188-251">Diese Tabelle zeigt die Bitfelder für die komprimierten Endpunkte als Funktion des Endpunkt Formats an, wobei jede Spalte eine Codierung und jede Zeile, die ein Bitfeld angibt, angibt.</span><span class="sxs-lookup"><span data-stu-id="85188-251">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="85188-252">Bei diesem Ansatz werden 82 Bits für Kacheln mit zwei Regionen und 65 Bits für Kacheln der einzelnen Regionen benötigt.</span><span class="sxs-lookup"><span data-stu-id="85188-252">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="85188-253">Beispielsweise sind die ersten 5 Bits für die oben genannte 1-Region \[ 16 4- \] Codierung (insbesondere die Spalte ganz rechts) Bits m \[ 4:0 \] , die nächsten 10 Bits sind Bits RW \[ 9:0 \] , usw. mit den letzten 6 Bits, die BW 10:15 enthalten \[ \] .</span><span class="sxs-lookup"><span data-stu-id="85188-253">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="85188-254">Die Feldnamen in der obigen Tabelle sind wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="85188-254">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="85188-255">Feld</span><span class="sxs-lookup"><span data-stu-id="85188-255">Field</span></span> | <span data-ttu-id="85188-256">Variable</span><span class="sxs-lookup"><span data-stu-id="85188-256">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="85188-257">m</span><span class="sxs-lookup"><span data-stu-id="85188-257">m</span></span>     | <span data-ttu-id="85188-258">Modus</span><span class="sxs-lookup"><span data-stu-id="85188-258">mode</span></span>              |
| <span data-ttu-id="85188-259">d</span><span class="sxs-lookup"><span data-stu-id="85188-259">d</span></span>     | <span data-ttu-id="85188-260">Shape-Index</span><span class="sxs-lookup"><span data-stu-id="85188-260">shape index</span></span>       |
| <span data-ttu-id="85188-261">RW</span><span class="sxs-lookup"><span data-stu-id="85188-261">rw</span></span>    | <span data-ttu-id="85188-262">Endpt \[ 0 \] . Ein \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="85188-262">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="85188-263">RX</span><span class="sxs-lookup"><span data-stu-id="85188-263">rx</span></span>    | <span data-ttu-id="85188-264">Endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="85188-264">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="85188-265">Wahn</span><span class="sxs-lookup"><span data-stu-id="85188-265">ry</span></span>    | <span data-ttu-id="85188-266">Endpt \[ 1 \] . Ein \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="85188-266">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="85188-267">RZ</span><span class="sxs-lookup"><span data-stu-id="85188-267">rz</span></span>    | <span data-ttu-id="85188-268">Endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="85188-268">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="85188-269">GW</span><span class="sxs-lookup"><span data-stu-id="85188-269">gw</span></span>    | <span data-ttu-id="85188-270">Endpt \[ 0 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="85188-270">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="85188-271">GX</span><span class="sxs-lookup"><span data-stu-id="85188-271">gx</span></span>    | <span data-ttu-id="85188-272">Endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="85188-272">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="85188-273">schlank</span><span class="sxs-lookup"><span data-stu-id="85188-273">gy</span></span>    | <span data-ttu-id="85188-274">Endpt \[ 1 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="85188-274">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="85188-275">gz</span><span class="sxs-lookup"><span data-stu-id="85188-275">gz</span></span>    | <span data-ttu-id="85188-276">Endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="85188-276">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="85188-277">BW</span><span class="sxs-lookup"><span data-stu-id="85188-277">bw</span></span>    | <span data-ttu-id="85188-278">Endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="85188-278">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="85188-279">BX</span><span class="sxs-lookup"><span data-stu-id="85188-279">bx</span></span>    | <span data-ttu-id="85188-280">Endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="85188-280">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="85188-281">by</span><span class="sxs-lookup"><span data-stu-id="85188-281">by</span></span>    | <span data-ttu-id="85188-282">Endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="85188-282">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="85188-283">BZ</span><span class="sxs-lookup"><span data-stu-id="85188-283">bz</span></span>    | <span data-ttu-id="85188-284">Endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="85188-284">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="85188-285">"Endpt \[ i" \] , wobei "0" oder "1" ist, bezieht sich auf den bzw. den jeweils ersten Satz von Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="85188-285">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="85188-286">Signieren der Erweiterung für Endpunkt Werte</span><span class="sxs-lookup"><span data-stu-id="85188-286">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="85188-287">Für Kacheln mit zwei Regionen gibt es vier Endpunkt Werte, für die das Vorzeichen erweitert werden kann.</span><span class="sxs-lookup"><span data-stu-id="85188-287">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="85188-288">Endpt \[ 0 \] . Ein wird nur signiert, wenn das Format ein signiertes Format ist. die anderen Endpunkte werden nur signiert, wenn der Endpunkt transformiert wurde, oder, wenn das Format ein signiertes Format ist.</span><span class="sxs-lookup"><span data-stu-id="85188-288">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="85188-289">Der folgende Code veranschaulicht den Algorithmus zum Erweitern des Vorzeichen von Endpunkt Werten mit zwei Regionen.</span><span class="sxs-lookup"><span data-stu-id="85188-289">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

<span data-ttu-id="85188-290">Bei Kacheln der einzelnen Regionen ist das Verhalten identisch, nur wenn Endpt \[ 1 \] entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="85188-290">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="85188-291">Inversion für Endpunkt Werte transformieren</span><span class="sxs-lookup"><span data-stu-id="85188-291">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="85188-292">Bei Kacheln mit zwei Regionen wendet die Transformation die Umkehrung der Differenz Codierung an und fügt den Basiswert bei Endpt \[ 0 hinzu \] . Eine zu den drei anderen Einträgen für insgesamt 9 Add-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="85188-292">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="85188-293">In der folgenden Abbildung wird der Basiswert als "a0" dargestellt und verfügt über die höchste Gleit Komma Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="85188-293">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="85188-294">"A1", "B0" und "B1" sind alle Deltas, die aus dem Anker Wert berechnet werden, und diese Delta Werte werden mit niedrigerer Genauigkeit dargestellt.</span><span class="sxs-lookup"><span data-stu-id="85188-294">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="85188-295">(A0 entspricht Endpt \[ 0 \] . A, B0 entspricht Endpt \[ 0 \] . B, a1 entspricht Endpt \[ 1 \] . A und B1 entsprechen Endpt \[ 1 \] . B.)</span><span class="sxs-lookup"><span data-stu-id="85188-295">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![Berechnung der Endpunkt Werte der Transformations Umkehrung](images/bc6h-transform-inverse.png)

<span data-ttu-id="85188-297">Für Kacheln der 1-Region gibt es nur einen Delta Offset und somit nur drei Add-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="85188-297">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="85188-298">Der-Debug muss sicherstellen, dass die Ergebnisse der umgekehrten Transformation nicht die Genauigkeit von Endpt \[ 0 \] . a überlaufen.</span><span class="sxs-lookup"><span data-stu-id="85188-298">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="85188-299">Im Fall eines Überlaufs müssen die Werte, die sich aus der umgekehrten Transformation ergeben, innerhalb der gleichen Anzahl von Bits umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="85188-299">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="85188-300">Wenn die Genauigkeit von a0 "p" ist, lautet der Transformations Algorithmus wie folgt:</span><span class="sxs-lookup"><span data-stu-id="85188-300">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="85188-301">Bei signierten Formaten müssen die Ergebnisse der Delta Berechnung ebenfalls mit Vorzeichen erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="85188-301">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="85188-302">Wenn beim Vorgang zum Signieren der Signierung beide Zeichen erweitert werden, wobei 0 positiv und 1 negativ ist, wird die oben genannte Klammer durch die Signierungs Erweiterung 0 übernommen.</span><span class="sxs-lookup"><span data-stu-id="85188-302">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="85188-303">Gleichwertig, nach der obigen Klammer, muss nur der Wert 1 (negativ) mit Extended signiert werden.</span><span class="sxs-lookup"><span data-stu-id="85188-303">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="85188-304">Unquantifization von Farb Endpunkten</span><span class="sxs-lookup"><span data-stu-id="85188-304">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="85188-305">Bei den nicht komprimierten Endpunkten ist der nächste Schritt das Ausführen einer anfänglichen unquantisierung der Farb Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="85188-305">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="85188-306">Dies umfasst drei Schritte:</span><span class="sxs-lookup"><span data-stu-id="85188-306">This involves three steps:</span></span>

-   <span data-ttu-id="85188-307">Eine unquantisierung der Farbpaletten.</span><span class="sxs-lookup"><span data-stu-id="85188-307">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="85188-308">Interpolations der Paletten</span><span class="sxs-lookup"><span data-stu-id="85188-308">Interpolation of the palettes</span></span>
-   <span data-ttu-id="85188-309">Beendigung der nicht quantifialisierung</span><span class="sxs-lookup"><span data-stu-id="85188-309">Unquantization finalization</span></span>

<span data-ttu-id="85188-310">Wenn Sie den unquantisierungsprozess in zwei Teile aufteilen (vor Interpolations-und abschließende unquantisierung nach der interpolung), wird die Anzahl der Multiplikations Vorgänge verringert, die im Vergleich zu einem vollständigen unquantisierungsprozess vor der paletteninterpolung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="85188-310">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="85188-311">Der folgende Code veranschaulicht den Prozess zum Abrufen von Schätzungen der ursprünglichen 16-Bit-Farbwerte und verwendet dann die angegebenen Gewichtungswerte, um der Palette 6 zusätzliche Farbwerte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="85188-311">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="85188-312">Der gleiche Vorgang wird für jeden Kanal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85188-312">The same operation is performed on each channel.</span></span>

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

<span data-ttu-id="85188-313">Im nächsten Codebeispiel wird der Interpolations Prozess mit den folgenden Beobachtungen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="85188-313">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="85188-314">Da der vollständige Bereich von Farbwerten für die **unquantifize** -Funktion (unten) zwischen-32768 und 65535 liegt, wird der interpolators mit einer 17-Bit-Arithmetik mit Vorzeichen implementiert.</span><span class="sxs-lookup"><span data-stu-id="85188-314">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="85188-315">Nach der interpolung werden die Werte an die Funktion zur Fertigstellung von **\_ unquantifize** (im dritten Beispiel in diesem Abschnitt beschrieben) weitergegeben, die die endgültige Skalierung anwendet.</span><span class="sxs-lookup"><span data-stu-id="85188-315">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="85188-316">Alle Hardware-Dekompressoren müssen mit diesen Funktionen bitgenaue Ergebnisse zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="85188-316">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

<span data-ttu-id="85188-317">**" \_ unquantize beenden** " wird nach der paletteninterpolung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="85188-317">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="85188-318">Die Funktion " **unquantifize** " verschiebt die Skalierung um 31/32 für "signiert", 31/64 für "unsigned".</span><span class="sxs-lookup"><span data-stu-id="85188-318">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="85188-319">Dieses Verhalten ist erforderlich, um den endgültigen Wert in einen gültigen halben Bereich (-0x7bff ~ 0x7bff) zu bringen, nachdem die paletteninterpolung abgeschlossen ist, um die Anzahl der erforderlichen Multiplikationen zu verringern.</span><span class="sxs-lookup"><span data-stu-id="85188-319">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="85188-320">**" \_ unquantize abschließen** " wendet die endgültige Skalierung an und gibt einen **kurzen Wert ohne** Vorzeichen zurück, der in eine **Hälfte** reinterpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="85188-320">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="85188-321">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85188-321">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85188-322">Textur Block Komprimierung in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="85188-322">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 