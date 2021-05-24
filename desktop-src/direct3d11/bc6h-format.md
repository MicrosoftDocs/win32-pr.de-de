---
title: BC6H-Format
description: Das BC6H-Format ist ein Texturkomprimierungsformat, das entwickelt wurde, um HDR-Farbräume (High Dynamic Range) in Quelldaten zu unterstützen.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ea15e0275bc478c0708ce08f531d8888a3c84d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335224"
---
# <a name="bc6h-format"></a><span data-ttu-id="00bcf-105">BC6H-Format</span><span class="sxs-lookup"><span data-stu-id="00bcf-105">BC6H Format</span></span>

<span data-ttu-id="00bcf-106">Das BC6H-Format ist ein Texturkomprimierungsformat, das entwickelt wurde, um HDR-Farbräume (High Dynamic Range) in Quelldaten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="00bcf-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="00bcf-107">Informationen zum BC6H-/DXGI-FORMAT \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="00bcf-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="00bcf-108">BC6H-Implementierung</span><span class="sxs-lookup"><span data-stu-id="00bcf-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="00bcf-109">Decodieren des BC6H-Formats</span><span class="sxs-lookup"><span data-stu-id="00bcf-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="00bcf-110">BC6H Compressed Endpoint Format</span><span class="sxs-lookup"><span data-stu-id="00bcf-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="00bcf-111">Signieren der Erweiterung für Endpunktwerte</span><span class="sxs-lookup"><span data-stu-id="00bcf-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="00bcf-112">Transformieren von Inversion für Endpunktwerte</span><span class="sxs-lookup"><span data-stu-id="00bcf-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="00bcf-113">Nichtquantisierung von Farbendpunkten</span><span class="sxs-lookup"><span data-stu-id="00bcf-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="00bcf-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="00bcf-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="00bcf-115">Informationen zum BC6H-/DXGI-FORMAT \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="00bcf-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="00bcf-116">Das BC6H-Format bietet eine hochwertige Komprimierung für Bilder, die drei HDR-Farbkanäle verwenden, mit einem 16-Bit-Wert für jeden Farbkanal des Werts (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="00bcf-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="00bcf-117">Es gibt keine Unterstützung für einen Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="00bcf-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="00bcf-118">BC6H wird durch die folgenden DXGI \_ FORMAT-Enumerationswerte angegeben:</span><span class="sxs-lookup"><span data-stu-id="00bcf-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="00bcf-119">**DXGI \_ FORMATIEREN SIE \_ BC6H \_ TYPELESS**.</span><span class="sxs-lookup"><span data-stu-id="00bcf-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="00bcf-120">**DXGI \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="00bcf-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="00bcf-121">Dieses BC6H-Format verwendet kein Vorzeichenbit in den 16-Bit-Gleitkommafarbkanalwerten.</span><span class="sxs-lookup"><span data-stu-id="00bcf-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="00bcf-122">**DXGI \_ FORMAT \_ BC6H \_ SF16**. Dieses BC6H-Format verwendet ein Vorzeichenbit in den 16-Bit-Gleitkommafarbkanalwerten.</span><span class="sxs-lookup"><span data-stu-id="00bcf-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="00bcf-123">Das 16-Bit-Gleitkommaformat für Farbkanäle wird häufig als "halb" Gleitkommaformat bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="00bcf-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="00bcf-124">Dieses Format hat das folgende Bitlayout:</span><span class="sxs-lookup"><span data-stu-id="00bcf-124">This format has the following bit layout:</span></span>
>
> |  <span data-ttu-id="00bcf-125">Format</span><span class="sxs-lookup"><span data-stu-id="00bcf-125">Format</span></span>                     | <span data-ttu-id="00bcf-126">Bitlayout</span><span class="sxs-lookup"><span data-stu-id="00bcf-126">Bit layout</span></span>                                                |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="00bcf-127">UF16 (float ohne Vorzeichen)</span><span class="sxs-lookup"><span data-stu-id="00bcf-127">UF16 (unsigned float)</span></span> | <span data-ttu-id="00bcf-128">5 Exponentenbits + 11 Mantissebits</span><span class="sxs-lookup"><span data-stu-id="00bcf-128">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="00bcf-129">SF16 (signed float)</span><span class="sxs-lookup"><span data-stu-id="00bcf-129">SF16 (signed float)</span></span>   | <span data-ttu-id="00bcf-130">1 Vorzeichenbit + 5 Exponentenbits + 10 Mantissebits</span><span class="sxs-lookup"><span data-stu-id="00bcf-130">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="00bcf-131">Das BC6H-Format kann für [Textur2D-Texturressourcen](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (einschließlich Arrays), Texture3D oder TextureCube (einschließlich Arrays) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00bcf-131">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="00bcf-132">Ebenso gilt dieses Format für alle MIP-Kartenoberflächen, die diesen Ressourcen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="00bcf-132">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="00bcf-133">BC6H verwendet eine feste Blockgröße von 16 Bytes (128 Bits) und eine feste Kachelgröße von 4x4 Texels.</span><span class="sxs-lookup"><span data-stu-id="00bcf-133">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="00bcf-134">Wie bei vorherigen BC-Formaten werden Texturbilder, die größer als die unterstützte Kachelgröße (4 x 4) sind, mithilfe mehrerer Blöcke komprimiert.</span><span class="sxs-lookup"><span data-stu-id="00bcf-134">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="00bcf-135">Diese Adressierungsidentität gilt auch für dreidimensionale Bilder, MIP-Karten, Cubemaps und Texturarrays.</span><span class="sxs-lookup"><span data-stu-id="00bcf-135">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="00bcf-136">Alle Bildkacheln müssen das gleiche Format haben.</span><span class="sxs-lookup"><span data-stu-id="00bcf-136">All image tiles must be of the same format.</span></span>

<span data-ttu-id="00bcf-137">Einige wichtige Hinweise zum BC6H-Format:</span><span class="sxs-lookup"><span data-stu-id="00bcf-137">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="00bcf-138">BC6H unterstützt die Gleitkommadenormalisierung, jedoch keine INF (unendlich) und NaN (keine Zahl).</span><span class="sxs-lookup"><span data-stu-id="00bcf-138">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="00bcf-139">Die Ausnahme ist der signierte Modus von BC6H (DXGI \_ FORMAT \_ BC6H \_ SF16), der -INF (negative Unendlichkeit) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00bcf-139">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="00bcf-140">Beachten Sie, dass diese Unterstützung für -INF lediglich ein Artefakt des Formats selbst ist und nicht speziell von Encodern für dieses Format unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="00bcf-140">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="00bcf-141">Wenn Encoder auf INF-Eingabedaten (positiv oder negativ) oder NaN-Eingabedaten stoßen, sollten sie diese Daten im Allgemeinen in den maximal zulässigen Nicht-INF-Darstellungswert konvertieren und NaN vor der Komprimierung \\ 0 zuordnen.</span><span class="sxs-lookup"><span data-stu-id="00bcf-141">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="00bcf-142">BC6H unterstützt keinen Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="00bcf-142">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="00bcf-143">Der BC6H-Decoder führt die Dekomprimierung durch, bevor er texturfiltert.</span><span class="sxs-lookup"><span data-stu-id="00bcf-143">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="00bcf-144">Die BC6H-Dekomprimierung muss bitgenau sein. Das heißt, die Hardware muss Ergebnisse zurückgeben, die mit dem in dieser Dokumentation beschriebenen Decoder identisch sind.</span><span class="sxs-lookup"><span data-stu-id="00bcf-144">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="00bcf-145">BC6H-Implementierung</span><span class="sxs-lookup"><span data-stu-id="00bcf-145">BC6H Implementation</span></span>

<span data-ttu-id="00bcf-146">Ein BC6H-Block besteht aus Modusbits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen Partitionsindex.</span><span class="sxs-lookup"><span data-stu-id="00bcf-146">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="00bcf-147">Dieses Format gibt 14 verschiedene Modi an.</span><span class="sxs-lookup"><span data-stu-id="00bcf-147">This format specifies 14 different modes.</span></span>

<span data-ttu-id="00bcf-148">Eine Endpunktfarbe wird als RGB-Triplet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="00bcf-148">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="00bcf-149">BC6H definiert eine Palette von Farben auf einer ungefähren Linie für eine Reihe von definierten Farbendpunkten.</span><span class="sxs-lookup"><span data-stu-id="00bcf-149">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="00bcf-150">Je nach Modus kann eine Kachel in zwei Regionen unterteilt oder als einzelne Region behandelt werden, wobei eine Kachel mit zwei Regionen einen separaten Satz von Farbendpunkten für jede Region aufwies.</span><span class="sxs-lookup"><span data-stu-id="00bcf-150">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="00bcf-151">BC6H speichert einen Palettenindex pro Texel.</span><span class="sxs-lookup"><span data-stu-id="00bcf-151">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="00bcf-152">Im Fall von zwei Regionen gibt es 32 mögliche Partitionen.</span><span class="sxs-lookup"><span data-stu-id="00bcf-152">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="00bcf-153">Decodieren des BC6H-Formats</span><span class="sxs-lookup"><span data-stu-id="00bcf-153">Decoding the BC6H Format</span></span>

<span data-ttu-id="00bcf-154">Der folgende Pseudocode zeigt die Schritte zum Dekomprimieren des Pixels bei (x,y) unter 16 Byte BC6H-Block.</span><span class="sxs-lookup"><span data-stu-id="00bcf-154">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

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

<span data-ttu-id="00bcf-155">Die folgende Tabelle enthält die Bitanzahl und die Werte für jedes der 14 möglichen Formate für BC6H-Blöcke.</span><span class="sxs-lookup"><span data-stu-id="00bcf-155">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="00bcf-156">Mode</span><span class="sxs-lookup"><span data-stu-id="00bcf-156">Mode</span></span> | <span data-ttu-id="00bcf-157">Partitionsindizes</span><span class="sxs-lookup"><span data-stu-id="00bcf-157">Partition Indices</span></span> | <span data-ttu-id="00bcf-158">Partition</span><span class="sxs-lookup"><span data-stu-id="00bcf-158">Partition</span></span> | <span data-ttu-id="00bcf-159">Farbendpunkte</span><span class="sxs-lookup"><span data-stu-id="00bcf-159">Color Endpoints</span></span>                  | <span data-ttu-id="00bcf-160">Modusbits</span><span class="sxs-lookup"><span data-stu-id="00bcf-160">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="00bcf-161">1</span><span class="sxs-lookup"><span data-stu-id="00bcf-161">1</span></span>    | <span data-ttu-id="00bcf-162">46 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-162">46 bits</span></span>           | <span data-ttu-id="00bcf-163">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-163">5 bits</span></span>    | <span data-ttu-id="00bcf-164">75 Bits (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="00bcf-164">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="00bcf-165">2 Bits (00)</span><span class="sxs-lookup"><span data-stu-id="00bcf-165">2 bits (00)</span></span>    |
| <span data-ttu-id="00bcf-166">2</span><span class="sxs-lookup"><span data-stu-id="00bcf-166">2</span></span>    | <span data-ttu-id="00bcf-167">46 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-167">46 bits</span></span>           | <span data-ttu-id="00bcf-168">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-168">5 bits</span></span>    | <span data-ttu-id="00bcf-169">75 Bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="00bcf-169">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="00bcf-170">2 Bits (01)</span><span class="sxs-lookup"><span data-stu-id="00bcf-170">2 bits (01)</span></span>    |
| <span data-ttu-id="00bcf-171">3</span><span class="sxs-lookup"><span data-stu-id="00bcf-171">3</span></span>    | <span data-ttu-id="00bcf-172">46 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-172">46 bits</span></span>           | <span data-ttu-id="00bcf-173">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-173">5 bits</span></span>    | <span data-ttu-id="00bcf-174">72 Bits (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="00bcf-174">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="00bcf-175">5 Bits (00010)</span><span class="sxs-lookup"><span data-stu-id="00bcf-175">5 bits (00010)</span></span> |
| <span data-ttu-id="00bcf-176">4</span><span class="sxs-lookup"><span data-stu-id="00bcf-176">4</span></span>    | <span data-ttu-id="00bcf-177">46 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-177">46 bits</span></span>           | <span data-ttu-id="00bcf-178">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-178">5 bits</span></span>    | <span data-ttu-id="00bcf-179">72 Bits (11.444, 11.555, 11.444)</span><span class="sxs-lookup"><span data-stu-id="00bcf-179">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="00bcf-180">5 Bits (00110)</span><span class="sxs-lookup"><span data-stu-id="00bcf-180">5 bits (00110)</span></span> |
| <span data-ttu-id="00bcf-181">5</span><span class="sxs-lookup"><span data-stu-id="00bcf-181">5</span></span>    | <span data-ttu-id="00bcf-182">46 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-182">46 bits</span></span>           | <span data-ttu-id="00bcf-183">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-183">5 bits</span></span>    | <span data-ttu-id="00bcf-184">72 Bits (11.444, 11.444, 11.555)</span><span class="sxs-lookup"><span data-stu-id="00bcf-184">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="00bcf-185">5 Bits (01010)</span><span class="sxs-lookup"><span data-stu-id="00bcf-185">5 bits (01010)</span></span> |
| <span data-ttu-id="00bcf-186">6</span><span class="sxs-lookup"><span data-stu-id="00bcf-186">6</span></span>    | <span data-ttu-id="00bcf-187">46 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-187">46 bits</span></span>           | <span data-ttu-id="00bcf-188">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-188">5 bits</span></span>    | <span data-ttu-id="00bcf-189">72 Bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="00bcf-189">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="00bcf-190">5 Bits (01110)</span><span class="sxs-lookup"><span data-stu-id="00bcf-190">5 bits (01110)</span></span> |
| <span data-ttu-id="00bcf-191">7</span><span class="sxs-lookup"><span data-stu-id="00bcf-191">7</span></span>    | <span data-ttu-id="00bcf-192">46 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-192">46 bits</span></span>           | <span data-ttu-id="00bcf-193">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-193">5 bits</span></span>    | <span data-ttu-id="00bcf-194">72 Bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="00bcf-194">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="00bcf-195">5 Bits (10010)</span><span class="sxs-lookup"><span data-stu-id="00bcf-195">5 bits (10010)</span></span> |
| <span data-ttu-id="00bcf-196">8</span><span class="sxs-lookup"><span data-stu-id="00bcf-196">8</span></span>    | <span data-ttu-id="00bcf-197">46 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-197">46 bits</span></span>           | <span data-ttu-id="00bcf-198">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-198">5 bits</span></span>    | <span data-ttu-id="00bcf-199">72 Bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="00bcf-199">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="00bcf-200">5 Bits (10110)</span><span class="sxs-lookup"><span data-stu-id="00bcf-200">5 bits (10110)</span></span> |
| <span data-ttu-id="00bcf-201">9</span><span class="sxs-lookup"><span data-stu-id="00bcf-201">9</span></span>    | <span data-ttu-id="00bcf-202">46 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-202">46 bits</span></span>           | <span data-ttu-id="00bcf-203">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-203">5 bits</span></span>    | <span data-ttu-id="00bcf-204">72 Bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="00bcf-204">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="00bcf-205">5 Bits (11010)</span><span class="sxs-lookup"><span data-stu-id="00bcf-205">5 bits (11010)</span></span> |
| <span data-ttu-id="00bcf-206">10</span><span class="sxs-lookup"><span data-stu-id="00bcf-206">10</span></span>   | <span data-ttu-id="00bcf-207">46 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-207">46 bits</span></span>           | <span data-ttu-id="00bcf-208">5 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-208">5 bits</span></span>    | <span data-ttu-id="00bcf-209">72 Bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="00bcf-209">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="00bcf-210">5 Bits (11110)</span><span class="sxs-lookup"><span data-stu-id="00bcf-210">5 bits (11110)</span></span> |
| <span data-ttu-id="00bcf-211">11</span><span class="sxs-lookup"><span data-stu-id="00bcf-211">11</span></span>   | <span data-ttu-id="00bcf-212">63 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-212">63 bits</span></span>           | <span data-ttu-id="00bcf-213">0 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-213">0 bits</span></span>    | <span data-ttu-id="00bcf-214">60 Bits (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="00bcf-214">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="00bcf-215">5 Bits (00011)</span><span class="sxs-lookup"><span data-stu-id="00bcf-215">5 bits (00011)</span></span> |
| <span data-ttu-id="00bcf-216">12</span><span class="sxs-lookup"><span data-stu-id="00bcf-216">12</span></span>   | <span data-ttu-id="00bcf-217">63 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-217">63 bits</span></span>           | <span data-ttu-id="00bcf-218">0 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-218">0 bits</span></span>    | <span data-ttu-id="00bcf-219">60 Bits (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="00bcf-219">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="00bcf-220">5 Bits (00111)</span><span class="sxs-lookup"><span data-stu-id="00bcf-220">5 bits (00111)</span></span> |
| <span data-ttu-id="00bcf-221">13</span><span class="sxs-lookup"><span data-stu-id="00bcf-221">13</span></span>   | <span data-ttu-id="00bcf-222">63 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-222">63 bits</span></span>           | <span data-ttu-id="00bcf-223">0 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-223">0 bits</span></span>    | <span data-ttu-id="00bcf-224">60 Bits (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="00bcf-224">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="00bcf-225">5 Bits (01011)</span><span class="sxs-lookup"><span data-stu-id="00bcf-225">5 bits (01011)</span></span> |
| <span data-ttu-id="00bcf-226">14</span><span class="sxs-lookup"><span data-stu-id="00bcf-226">14</span></span>   | <span data-ttu-id="00bcf-227">63 Bit</span><span class="sxs-lookup"><span data-stu-id="00bcf-227">63 bits</span></span>           | <span data-ttu-id="00bcf-228">0 Bits</span><span class="sxs-lookup"><span data-stu-id="00bcf-228">0 bits</span></span>    | <span data-ttu-id="00bcf-229">60 Bits (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="00bcf-229">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="00bcf-230">5 Bits (01111)</span><span class="sxs-lookup"><span data-stu-id="00bcf-230">5 bits (01111)</span></span> |



 

<span data-ttu-id="00bcf-231">Jedes Format in dieser Tabelle kann durch die Modusbits eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="00bcf-231">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="00bcf-232">Die ersten zehn Modi werden für Kacheln mit zwei Bereichen verwendet, und das Modusbitfeld kann zwei oder fünf Bits lang sein.</span><span class="sxs-lookup"><span data-stu-id="00bcf-232">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="00bcf-233">Diese Blöcke enthalten auch Felder für die komprimierten Farbendpunkte (72 oder 75 Bits), die Partition (5 Bits) und die Partitionsindizes (46 Bits).</span><span class="sxs-lookup"><span data-stu-id="00bcf-233">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="00bcf-234">Für die komprimierten Farbendpunkte notieren die Werte in der vorangehenden Tabelle die Genauigkeit der gespeicherten RGB-Endpunkte und die Anzahl der Bits, die für jeden Farbwert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00bcf-234">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="00bcf-235">Der Modus 3 gibt beispielsweise eine Genauigkeitsstufe des Farbendpunkts von 11 und die Anzahl der Bits an, die zum Speichern der Deltawerte der transformierten Endpunkte für die Rot-, Blau- und Grünfarben verwendet werden (5, 4 bzw. 4).</span><span class="sxs-lookup"><span data-stu-id="00bcf-235">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="00bcf-236">Modus 10 verwendet keine Deltakomprimierung und speichert stattdessen alle vier Farbendpunkte explizit.</span><span class="sxs-lookup"><span data-stu-id="00bcf-236">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="00bcf-237">Die letzten vier Blockmodi werden für Kacheln mit einem Bereich verwendet, wobei das Modusfeld 5 Bits beträgt.</span><span class="sxs-lookup"><span data-stu-id="00bcf-237">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="00bcf-238">Diese Blöcke enthalten Felder für die Endpunkte (60 Bits) und die komprimierten Indizes (63 Bits).</span><span class="sxs-lookup"><span data-stu-id="00bcf-238">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="00bcf-239">Modus 11 (wie Modus 10) verwendet keine Deltakomprimierung und speichert stattdessen beide Farbendpunkte explizit.</span><span class="sxs-lookup"><span data-stu-id="00bcf-239">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="00bcf-240">Die Modi 10011, 10111, 11011 und 11111 (nicht angezeigt) sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="00bcf-240">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="00bcf-241">Verwenden Sie diese nicht in Ihrem Encoder.</span><span class="sxs-lookup"><span data-stu-id="00bcf-241">Do not use these in your encoder.</span></span> <span data-ttu-id="00bcf-242">Wenn der Hardware Blöcke mit einem dieser Modi übergeben werden, muss der resultierende dekomprimierte Block alle Nullen in allen Kanälen mit Ausnahme des Alphakanals enthalten.</span><span class="sxs-lookup"><span data-stu-id="00bcf-242">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="00bcf-243">Für BC6H muss der Alphakanal unabhängig vom Modus immer 1.0 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="00bcf-243">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="00bcf-244">BC6H-Partitionssatz</span><span class="sxs-lookup"><span data-stu-id="00bcf-244">BC6H Partition Set</span></span>

<span data-ttu-id="00bcf-245">Es gibt 32 mögliche Partitionssätze für eine Kachel mit zwei Regionen, die in der folgenden Tabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="00bcf-245">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="00bcf-246">Jeder 4x4-Block stellt eine einzelne Form dar.</span><span class="sxs-lookup"><span data-stu-id="00bcf-246">Each 4x4 block represents a single shape.</span></span>

![Tabelle der bc6h-Partitionssätze](images/bc6h-partition-sets.png)

<span data-ttu-id="00bcf-248">In dieser Tabelle von Partitionssätzen ist der fett formatierte und unterstrichene Eintrag der Speicherort des Fix up-Index für Teilmenge 1 (der mit einem Bit weniger angegeben wird).</span><span class="sxs-lookup"><span data-stu-id="00bcf-248">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="00bcf-249">Der Fix up-Index für Teilmenge 0 ist immer Index 0, da die Partitionierung immer so angeordnet ist, dass Index 0 immer teilmenge 0 ist.</span><span class="sxs-lookup"><span data-stu-id="00bcf-249">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="00bcf-250">Die Partitionsreihenfolge verläuft von oben links nach unten rechts, von links nach rechts und dann von oben nach unten.</span><span class="sxs-lookup"><span data-stu-id="00bcf-250">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="00bcf-251">BC6H Compressed Endpoint Format</span><span class="sxs-lookup"><span data-stu-id="00bcf-251">BC6H Compressed Endpoint Format</span></span>

![Bitfelder für komprimierte bc6h-Endpunktformate](images/bc6h-headers-med.png)

<span data-ttu-id="00bcf-253">Diese Tabelle zeigt die Bitfelder für die komprimierten Endpunkte als Funktion des Endpunktformats, wobei jede Spalte eine Codierung und jede Zeile ein Bitfeld angibt.</span><span class="sxs-lookup"><span data-stu-id="00bcf-253">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="00bcf-254">Dieser Ansatz benötigt 82 Bits für Kacheln mit zwei Regionen und 65 Bits für Kacheln mit einer Region.</span><span class="sxs-lookup"><span data-stu-id="00bcf-254">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="00bcf-255">Als Beispiel sind die ersten 5 Bits für die \[ Codierung mit 1 Region 16 4 \] oben (insbesondere die spalte ganz rechts) Bits m \[ 4:0, \] die nächsten 10 Bits sind Bits rw \[ 9:0 \] usw. Mit den letzten 6 Bits, die bw \[ 10:15 \] enthalten.</span><span class="sxs-lookup"><span data-stu-id="00bcf-255">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="00bcf-256">Die Feldnamen in der obigen Tabelle sind wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="00bcf-256">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="00bcf-257">Feld</span><span class="sxs-lookup"><span data-stu-id="00bcf-257">Field</span></span> | <span data-ttu-id="00bcf-258">Variable</span><span class="sxs-lookup"><span data-stu-id="00bcf-258">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="00bcf-259">m</span><span class="sxs-lookup"><span data-stu-id="00bcf-259">m</span></span>     | <span data-ttu-id="00bcf-260">Modus</span><span class="sxs-lookup"><span data-stu-id="00bcf-260">mode</span></span>              |
| <span data-ttu-id="00bcf-261">d</span><span class="sxs-lookup"><span data-stu-id="00bcf-261">d</span></span>     | <span data-ttu-id="00bcf-262">Shape-Index</span><span class="sxs-lookup"><span data-stu-id="00bcf-262">shape index</span></span>       |
| <span data-ttu-id="00bcf-263">Rw</span><span class="sxs-lookup"><span data-stu-id="00bcf-263">rw</span></span>    | <span data-ttu-id="00bcf-264">endpt \[ 0 \] . A \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-264">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="00bcf-265">Rx</span><span class="sxs-lookup"><span data-stu-id="00bcf-265">rx</span></span>    | <span data-ttu-id="00bcf-266">endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-266">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="00bcf-267">Ry</span><span class="sxs-lookup"><span data-stu-id="00bcf-267">ry</span></span>    | <span data-ttu-id="00bcf-268">endpt \[ 1 \] . A \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-268">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="00bcf-269">Rz</span><span class="sxs-lookup"><span data-stu-id="00bcf-269">rz</span></span>    | <span data-ttu-id="00bcf-270">endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-270">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="00bcf-271">Gw</span><span class="sxs-lookup"><span data-stu-id="00bcf-271">gw</span></span>    | <span data-ttu-id="00bcf-272">endpt \[ 0 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-272">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="00bcf-273">Gx</span><span class="sxs-lookup"><span data-stu-id="00bcf-273">gx</span></span>    | <span data-ttu-id="00bcf-274">endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-274">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="00bcf-275">Gy</span><span class="sxs-lookup"><span data-stu-id="00bcf-275">gy</span></span>    | <span data-ttu-id="00bcf-276">endpt \[ 1 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-276">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="00bcf-277">gz</span><span class="sxs-lookup"><span data-stu-id="00bcf-277">gz</span></span>    | <span data-ttu-id="00bcf-278">endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-278">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="00bcf-279">Bw</span><span class="sxs-lookup"><span data-stu-id="00bcf-279">bw</span></span>    | <span data-ttu-id="00bcf-280">endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-280">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="00bcf-281">Bx</span><span class="sxs-lookup"><span data-stu-id="00bcf-281">bx</span></span>    | <span data-ttu-id="00bcf-282">endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-282">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="00bcf-283">by</span><span class="sxs-lookup"><span data-stu-id="00bcf-283">by</span></span>    | <span data-ttu-id="00bcf-284">endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-284">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="00bcf-285">Bz</span><span class="sxs-lookup"><span data-stu-id="00bcf-285">bz</span></span>    | <span data-ttu-id="00bcf-286">endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="00bcf-286">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="00bcf-287">Endpt \[ i , wobei i entweder \] 0 oder 1 ist, bezieht sich auf den 0. bzw. 1. Satz von Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="00bcf-287">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="00bcf-288">Signieren der Erweiterung für Endpunktwerte</span><span class="sxs-lookup"><span data-stu-id="00bcf-288">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="00bcf-289">Für Kacheln mit zwei Regionen gibt es vier Endpunktwerte, die erweitert werden können.</span><span class="sxs-lookup"><span data-stu-id="00bcf-289">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="00bcf-290">Endpt \[ 0 \] . Ein ist nur signiert, wenn das Format ein signiertes Format ist. die anderen Endpunkte werden nur signiert, wenn der Endpunkt transformiert wurde, oder wenn das Format ein signiertes Format ist.</span><span class="sxs-lookup"><span data-stu-id="00bcf-290">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="00bcf-291">Der folgende Code veranschaulicht den Algorithmus zum Erweitern des Vorzeichens von Endpunktwerten mit zwei Regionen.</span><span class="sxs-lookup"><span data-stu-id="00bcf-291">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

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

<span data-ttu-id="00bcf-292">Bei Kacheln mit einer Region ist das Verhalten identisch, nur wenn endpt \[ 1 \] entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="00bcf-292">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

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

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="00bcf-293">Transformieren von Inversion für Endpunktwerte</span><span class="sxs-lookup"><span data-stu-id="00bcf-293">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="00bcf-294">Bei Kacheln mit zwei Regionen wendet die Transformation die Umkehrung der Differenzcodierung an und fügt den Basiswert am Ende \[ von 0 \] hinzu. Ein zu den drei anderen Einträgen für insgesamt 9 Add-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="00bcf-294">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="00bcf-295">In der folgenden Abbildung wird der Basiswert als "A0" dargestellt und weist die höchste Gleitkommagenauigkeit auf.</span><span class="sxs-lookup"><span data-stu-id="00bcf-295">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="00bcf-296">"A1", "B0" und "B1" sind alle Deltas, die aus dem Ankerwert berechnet werden, und diese Deltawerte werden mit geringerer Genauigkeit dargestellt.</span><span class="sxs-lookup"><span data-stu-id="00bcf-296">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="00bcf-297">(A0 entspricht endpt \[ 0 \] . A, B0 entspricht endpt \[ 0 \] . B, A1 entspricht endpt \[ 1 \] . A und B1 entsprechen endpt \[ 1 \] .B.)</span><span class="sxs-lookup"><span data-stu-id="00bcf-297">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![Berechnung der Endpunktwerte für die Transformationsumkehr](images/bc6h-transform-inverse.png)

<span data-ttu-id="00bcf-299">Für Kacheln mit einer Region gibt es nur einen Deltaoffset und somit nur drei Add-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="00bcf-299">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="00bcf-300">Der Dekomprimierer muss sicherstellen, dass die Ergebnisse der inverse Transformation nicht die Genauigkeit von endpt \[ 0 \] .a überlaufen.</span><span class="sxs-lookup"><span data-stu-id="00bcf-300">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="00bcf-301">Bei einem Überlauf müssen die Werte, die sich aus der umgekehrten Transformation ergeben, innerhalb der gleichen Anzahl von Bits umbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="00bcf-301">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="00bcf-302">Wenn die Genauigkeit von A0 "p" Bits ist, lautet der Transformationsalgorithmus:</span><span class="sxs-lookup"><span data-stu-id="00bcf-302">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="00bcf-303">Bei Formaten mit Vorzeichen müssen die Ergebnisse der Deltaberechnung ebenfalls erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="00bcf-303">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="00bcf-304">Wenn der Vorgang der Vorzeichenerweiterung die Erweiterung beider Zeichen in Betracht zieht, wobei 0 positiv und 1 negativ ist, übernimmt die Vorzeichenerweiterung von 0 die obige Klammer.</span><span class="sxs-lookup"><span data-stu-id="00bcf-304">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="00bcf-305">Entsprechend muss nach der obigen Klammer nur der Wert 1 (negativ) erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="00bcf-305">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="00bcf-306">Unquantisierung von Farbendpunkten</span><span class="sxs-lookup"><span data-stu-id="00bcf-306">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="00bcf-307">Angesichts der nicht komprimierten Endpunkte besteht der nächste Schritt im Ausführen einer anfänglichen Unquantisierung der Farbendpunkte.</span><span class="sxs-lookup"><span data-stu-id="00bcf-307">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="00bcf-308">Dies umfasst drei Schritte:</span><span class="sxs-lookup"><span data-stu-id="00bcf-308">This involves three steps:</span></span>

-   <span data-ttu-id="00bcf-309">Eine Unquantisierung der Farbpaletten</span><span class="sxs-lookup"><span data-stu-id="00bcf-309">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="00bcf-310">Interpolation der Paletten</span><span class="sxs-lookup"><span data-stu-id="00bcf-310">Interpolation of the palettes</span></span>
-   <span data-ttu-id="00bcf-311">Unquantisierungs finalization</span><span class="sxs-lookup"><span data-stu-id="00bcf-311">Unquantization finalization</span></span>

<span data-ttu-id="00bcf-312">Durch die Trennung des Unquantisierungsprozesses in zwei Teile (Farbpaletten-Unquantisierung vor der Interpolation und endgültige Unquantisierung nach der Interpolation) wird die Anzahl von Multiplikationsvorgängen reduziert, die im Vergleich zu einem vollständigen Unquantisierungsprozess vor der Paletteninterpolation erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="00bcf-312">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="00bcf-313">Der folgende Code veranschaulicht den Prozess zum Abrufen von Schätzungen der ursprünglichen 16-Bit-Farbwerte und anschließendes Verwenden der angegebenen Gewichtungswerte, um der Palette sechs zusätzliche Farbwerte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="00bcf-313">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="00bcf-314">Der gleiche Vorgang wird auf jedem Kanal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00bcf-314">The same operation is performed on each channel.</span></span>

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

<span data-ttu-id="00bcf-315">Im nächsten Codebeispiel wird der Interpolationsprozess mit den folgenden Beobachtungen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="00bcf-315">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="00bcf-316">Da der vollständige Farbbereich für die **Unquantize-Funktion** (unten) zwischen -32768 und 65535 liegt, wird der Interpolator mithilfe einer 17-Bit-Arithmetik mit Vorsigniert implementiert.</span><span class="sxs-lookup"><span data-stu-id="00bcf-316">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="00bcf-317">Nach der Interpolation werden die Werte an die finish **\_ unquantize-Funktion** übergeben (im dritten Beispiel in diesem Abschnitt beschrieben), die die endgültige Skalierung an wendet.</span><span class="sxs-lookup"><span data-stu-id="00bcf-317">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="00bcf-318">Alle Hardwaredekompressoren sind erforderlich, um bitgenaue Ergebnisse mit diesen Funktionen zurück zu geben.</span><span class="sxs-lookup"><span data-stu-id="00bcf-318">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

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

<span data-ttu-id="00bcf-319">**finish \_ unquantize** wird nach der Paletteninterpolation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="00bcf-319">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="00bcf-320">Die **unquantize-Funktion** verschiebt die Skalierung für signed um 31/32 und für unsigned um 31/64.</span><span class="sxs-lookup"><span data-stu-id="00bcf-320">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="00bcf-321">Dieses Verhalten ist erforderlich, um den endgültigen Wert in einen gültigen Halbbereich (-0x7BFF ~ 0x7BFF) zu bekommen, nachdem die Paletteninterpolation abgeschlossen ist, um die Anzahl der erforderlichen Multiplikationen zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="00bcf-321">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="00bcf-322">**finish \_ unquantize wendet** die endgültige Skalierung an und gibt einen **unsignierten** short-Wert zurück, der in die Hälfte neu interpretiert **wird.**</span><span class="sxs-lookup"><span data-stu-id="00bcf-322">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="00bcf-323">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00bcf-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00bcf-324">Texturblockkomprimierung in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="00bcf-324">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 