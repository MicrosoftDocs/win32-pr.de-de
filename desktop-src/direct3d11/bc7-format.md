---
title: Bzw bc7-Format
description: Das bzw bc7-Format ist ein Textur Komprimierungs Format, das für die hochwertige Komprimierung von RGB-und RGBA-Daten verwendet wird.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390814"
---
# <a name="bc7-format"></a><span data-ttu-id="fa229-103">Bzw bc7-Format</span><span class="sxs-lookup"><span data-stu-id="fa229-103">BC7 Format</span></span>

<span data-ttu-id="fa229-104">Das bzw bc7-Format ist ein Textur Komprimierungs Format, das für die hochwertige Komprimierung von RGB-und RGBA-Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa229-104">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span>

-   [<span data-ttu-id="fa229-105">Informationen zum bzw bc7/DXGI- \_ Format \_ bzw bc7</span><span class="sxs-lookup"><span data-stu-id="fa229-105">About BC7/DXGI\_FORMAT\_BC7</span></span>](/windows)
-   [<span data-ttu-id="fa229-106">Bzw bc7-Implementierung</span><span class="sxs-lookup"><span data-stu-id="fa229-106">BC7 Implementation</span></span>](#bc7-implementation)
-   [<span data-ttu-id="fa229-107">Decodieren des bzw bc7-Formats</span><span class="sxs-lookup"><span data-stu-id="fa229-107">Decoding the BC7 Format</span></span>](#decoding-the-bc7-format)
-   [<span data-ttu-id="fa229-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa229-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="fa229-109">Informationen zu den Block Modi des bzw bc7-Formats finden Sie unter [bzw bc7 formatmode Reference](bc7-format-mode-reference.md).</span><span class="sxs-lookup"><span data-stu-id="fa229-109">For info about the block modes of the BC7 format, see [BC7 Format Mode Reference](bc7-format-mode-reference.md).</span></span>

## <a name="about-bc7dxgi_format_bc7"></a><span data-ttu-id="fa229-110">Informationen zum bzw bc7/DXGI- \_ Format \_ bzw bc7</span><span class="sxs-lookup"><span data-stu-id="fa229-110">About BC7/DXGI\_FORMAT\_BC7</span></span>

<span data-ttu-id="fa229-111">Bzw bc7 wird durch die folgenden DXGI- \_ formatenumerationswerte angegeben:</span><span class="sxs-lookup"><span data-stu-id="fa229-111">BC7 is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="fa229-112">**DXGI \_ Format \_ bzw bc7 \_ typlose Formatierung**.</span><span class="sxs-lookup"><span data-stu-id="fa229-112">**DXGI\_FORMAT\_BC7\_TYPELESS**.</span></span>
-   <span data-ttu-id="fa229-113">**DXGI \_ Formatieren Sie \_ bzw bc7 \_ unorm**.</span><span class="sxs-lookup"><span data-stu-id="fa229-113">**DXGI\_FORMAT\_BC7\_UNORM**.</span></span>
-   <span data-ttu-id="fa229-114">**DXGI \_ Format \_ bzw bc7 \_ unorm \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="fa229-114">**DXGI\_FORMAT\_BC7\_UNORM\_SRGB**.</span></span>

<span data-ttu-id="fa229-115">Das bzw bc7-Format kann für die Textur Ressourcen [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (einschließlich Arrays), Texture3D oder texturecube (einschließlich Arrays) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa229-115">The BC7 format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="fa229-116">Ebenso gilt dieses Format für alle mit diesen Ressourcen verknüpften MIP-Map-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="fa229-116">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="fa229-117">Bzw bc7 verwendet eine fester Blockgröße von 16 Bytes (128 Bits) und eine fixierte Kachel Größe von 4 x 4 texeln.</span><span class="sxs-lookup"><span data-stu-id="fa229-117">BC7 uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="fa229-118">Wie bei früheren BC-Formaten werden Textur Bilder, die größer als die unterstützte Kachel Größe (4X4) sind, mithilfe mehrerer Blöcke komprimiert.</span><span class="sxs-lookup"><span data-stu-id="fa229-118">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="fa229-119">Diese Adressierungs Identität gilt auch für dreidimensionale Bilder und MIP-Maps, Cubemaps und Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="fa229-119">This addressing identity also applies to three-dimensional images and MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="fa229-120">Alle Bildkacheln müssen das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fa229-120">All image tiles must be of the same format.</span></span>

<span data-ttu-id="fa229-121">Bzw bc7 komprimiert sowohl Daten Abbilder mit drei Kanälen (RGB) als auch mit vier Kanälen (RGBA).</span><span class="sxs-lookup"><span data-stu-id="fa229-121">BC7 compresses both three-channel (RGB) and four-channel (RGBA) fixed-point data images.</span></span> <span data-ttu-id="fa229-122">Normalerweise handelt es sich bei den Quelldaten um 8 Bits pro Farbkomponente (Channel), obwohl das Format Quelldaten mit einer höheren Bits pro Color-Komponente codieren kann.</span><span class="sxs-lookup"><span data-stu-id="fa229-122">Typically, source data is 8 bits per color component (channel), although the format is capable of encoding source data with higher bits per color component.</span></span> <span data-ttu-id="fa229-123">Alle Bildkacheln müssen das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fa229-123">All image tiles must be of the same format.</span></span>

<span data-ttu-id="fa229-124">Der bzw bc7-Decoder führt vor dem Anwenden der Textur Filterung eine Komprimierung durch.</span><span class="sxs-lookup"><span data-stu-id="fa229-124">The BC7 decoder performs decompression before texture filtering is applied.</span></span>

<span data-ttu-id="fa229-125">Bzw bc7-Komprimierungs Hardware muss etwas genau sein. Das heißt, dass die Hardware Ergebnisse zurückgeben muss, die mit den Ergebnissen identisch sind, die von dem in diesem Dokument beschriebenen Decoder zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fa229-125">BC7 decompression hardware must be bit accurate; that is, the hardware must return results that are identical to the results returned by the decoder described in this document.</span></span>

## <a name="bc7-implementation"></a><span data-ttu-id="fa229-126">Bzw bc7-Implementierung</span><span class="sxs-lookup"><span data-stu-id="fa229-126">BC7 Implementation</span></span>

<span data-ttu-id="fa229-127">Eine bzw bc7-Implementierung kann einen von 8 Modi angeben, wobei der Modus im unwichtigsten Bit des 16-Byte-Blocks (128 Bit) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa229-127">A BC7 implementation can specify one of 8 modes, with the mode specified in the least significant bit of the 16 byte (128 bit) block.</span></span> <span data-ttu-id="fa229-128">Der-Modus wird von 0 (null) oder mehr Bits mit einem Wert von 0 (null) gefolgt von einem 1 codiert.</span><span class="sxs-lookup"><span data-stu-id="fa229-128">The mode is encoded by zero or more bits with a value of 0 followed by a 1.</span></span>

<span data-ttu-id="fa229-129">Ein bzw bc7-Block kann mehrere Endpunkt Paare enthalten.</span><span class="sxs-lookup"><span data-stu-id="fa229-129">A BC7 block can contain multiple endpoint pairs.</span></span> <span data-ttu-id="fa229-130">Im Rahmen dieser Dokumentation kann der Satz von Indizes, die einem Endpunkt paar entsprechen, als "Teilmenge" bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="fa229-130">For the purposes of this documentation, the set of indices that correspond to an endpoint pair may be referred to as a "subset."</span></span> <span data-ttu-id="fa229-131">Außerdem wird die Endpunkt Darstellung in einigen Block Modi in einem Formular codiert, das für die Zwecke dieser Dokumentation wieder als "rbgp" bezeichnet wird. Hierbei steht das "P"-Bit für die Farbkomponenten des Endpunkts für ein gemeinsam genutztes Bit.</span><span class="sxs-lookup"><span data-stu-id="fa229-131">Also, in some block modes, the endpoint representation is encoded in a form that -- again, for the purposes of this documentation -- shall be referred to as "RBGP," where the "P" bit represents a shared least significant bit for the color components of the endpoint.</span></span> <span data-ttu-id="fa229-132">Wenn die Endpunkt Darstellung für das Format z. b. "RGB 5.5.5.1" ist, wird der Endpunkt als RGB 6.6.6-Wert interpretiert, wobei der Status des P-Bits das unwichtigste Bit der einzelnen Komponenten definiert.</span><span class="sxs-lookup"><span data-stu-id="fa229-132">For example, if the endpoint representation for the format is "RGB 5.5.5.1," then the endpoint is interpreted as an RGB 6.6.6 value, where the state of the P-bit defines the least significant bit of each component.</span></span> <span data-ttu-id="fa229-133">Ebenso gilt für Quelldaten mit einem Alphakanal, wenn die Darstellung im Format "rgbap 5.5.5.5.1" ist, der Endpunkt als RGBA 6.6.6.6.</span><span class="sxs-lookup"><span data-stu-id="fa229-133">Similarly, for source data with an alpha channel, if the representation for the format is "RGBAP 5.5.5.5.1," then the endpoint is interepreted as RGBA 6.6.6.6.</span></span> <span data-ttu-id="fa229-134">Abhängig vom Block Modus können Sie das gemeinsame, unwichtigste Bit entweder für beide Endpunkte einer Teilmenge einzeln (2 p-Bits pro Teilmenge) oder für die gemeinsame Nutzung zwischen Endpunkten einer Teilmenge (1 p-Bit pro Teilmenge) angeben.</span><span class="sxs-lookup"><span data-stu-id="fa229-134">Depending on the block mode, you can specify the shared least significant bit for either both endpoints of a subset individually (2 P-bits per subset), or shared between endpoints of a subset (1 P-bit per subset).</span></span>

<span data-ttu-id="fa229-135">Für bzw bc7-Blöcke, die die Alpha Komponente nicht explizit codieren, besteht ein bzw bc7-Block aus modusbits, Partitions Bits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen P-Bit.</span><span class="sxs-lookup"><span data-stu-id="fa229-135">For BC7 blocks that don't explicitly encode the alpha component, a BC7 block consists of mode bits, partition bits, compressed endpoints, compressed indices, and an optional P-bit.</span></span> <span data-ttu-id="fa229-136">In diesen Blöcken verfügen die Endpunkte über eine nur-RGB-Darstellung, und die Alpha Komponente wird als 1,0 für alle texeln in den Quelldaten decodiert.</span><span class="sxs-lookup"><span data-stu-id="fa229-136">In these blocks the endpoints have an RGB-only representation and the alpha component is decoded as 1.0 for all texels in the source data.</span></span>

<span data-ttu-id="fa229-137">Für bzw bc7-Blöcke mit kombinierten Farben und Alpha Komponenten besteht ein Block aus modusbits, komprimierten Endpunkten, komprimierten Indizes und optionalen Partitions Bits und einem P-Bit.</span><span class="sxs-lookup"><span data-stu-id="fa229-137">For BC7 blocks that have combined color and alpha components, a block consists of mode bits, compressed endpoints, compressed indices, and optional partition bits and a P-bit.</span></span> <span data-ttu-id="fa229-138">In diesen Blöcken werden die Endpunkt Farben im RGBA-Format ausgedrückt, und Alpha Komponentenwerte werden zusammen mit den Farbkomponenten Werten interpoliert.</span><span class="sxs-lookup"><span data-stu-id="fa229-138">In these blocks, the endpoint colors are expressed in RGBA format, and alpha component values are interpolated alongside the color component values.</span></span>

<span data-ttu-id="fa229-139">Für bzw bc7-Blöcke mit separaten Farb-und Alpha Komponenten besteht ein-Block aus modusbits, Rotations Bits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen indexselektor-Bit.</span><span class="sxs-lookup"><span data-stu-id="fa229-139">For BC7 blocks that have separate color and alpha components, a block consists of mode bits, rotation bits, compressed endpoints, compressed indices, and an optional index selector bit.</span></span> <span data-ttu-id="fa229-140">Diese Blöcke verfügen über einen effektiven RGB \[ -Vektor R, G, B \] und einen skalaren Alphakanal, der \[ \] separat codiert ist.</span><span class="sxs-lookup"><span data-stu-id="fa229-140">These blocks have an effective RGB vector \[R, G, B\] and a scalar alpha channel \[A\] separately encoded.</span></span>

<span data-ttu-id="fa229-141">In der folgenden Tabelle sind die Komponenten der einzelnen Blocktypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa229-141">The following table lists the components of each block type.</span></span>



| <span data-ttu-id="fa229-142">Bzw bc7-Block enthält...</span><span class="sxs-lookup"><span data-stu-id="fa229-142">BC7 block contains...</span></span>     | <span data-ttu-id="fa229-143">modusbits</span><span class="sxs-lookup"><span data-stu-id="fa229-143">mode bits</span></span> | <span data-ttu-id="fa229-144">Drehungs Bits</span><span class="sxs-lookup"><span data-stu-id="fa229-144">rotation bits</span></span> | <span data-ttu-id="fa229-145">Index Auswahl Bit</span><span class="sxs-lookup"><span data-stu-id="fa229-145">index selector bit</span></span> | <span data-ttu-id="fa229-146">Partitions Bits</span><span class="sxs-lookup"><span data-stu-id="fa229-146">partition bits</span></span> | <span data-ttu-id="fa229-147">komprimierte Endpunkte</span><span class="sxs-lookup"><span data-stu-id="fa229-147">compressed endpoints</span></span> | <span data-ttu-id="fa229-148">P-Bit</span><span class="sxs-lookup"><span data-stu-id="fa229-148">P-bit</span></span>    | <span data-ttu-id="fa229-149">komprimierte Indizes</span><span class="sxs-lookup"><span data-stu-id="fa229-149">compressed indices</span></span> |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| <span data-ttu-id="fa229-150">nur Farbkomponenten</span><span class="sxs-lookup"><span data-stu-id="fa229-150">color components only</span></span>     | <span data-ttu-id="fa229-151">required</span><span class="sxs-lookup"><span data-stu-id="fa229-151">required</span></span>  | <span data-ttu-id="fa229-152">–</span><span class="sxs-lookup"><span data-stu-id="fa229-152">N/A</span></span>           | <span data-ttu-id="fa229-153">–</span><span class="sxs-lookup"><span data-stu-id="fa229-153">N/A</span></span>                | <span data-ttu-id="fa229-154">required</span><span class="sxs-lookup"><span data-stu-id="fa229-154">required</span></span>       | <span data-ttu-id="fa229-155">required</span><span class="sxs-lookup"><span data-stu-id="fa229-155">required</span></span>             | <span data-ttu-id="fa229-156">Optional</span><span class="sxs-lookup"><span data-stu-id="fa229-156">optional</span></span> | <span data-ttu-id="fa229-157">required</span><span class="sxs-lookup"><span data-stu-id="fa229-157">required</span></span>           |
| <span data-ttu-id="fa229-158">Farbe + Alpha, kombiniert</span><span class="sxs-lookup"><span data-stu-id="fa229-158">color + alpha combined</span></span>    | <span data-ttu-id="fa229-159">required</span><span class="sxs-lookup"><span data-stu-id="fa229-159">required</span></span>  | <span data-ttu-id="fa229-160">–</span><span class="sxs-lookup"><span data-stu-id="fa229-160">N/A</span></span>           | <span data-ttu-id="fa229-161">–</span><span class="sxs-lookup"><span data-stu-id="fa229-161">N/A</span></span>                | <span data-ttu-id="fa229-162">Optional</span><span class="sxs-lookup"><span data-stu-id="fa229-162">optional</span></span>       | <span data-ttu-id="fa229-163">required</span><span class="sxs-lookup"><span data-stu-id="fa229-163">required</span></span>             | <span data-ttu-id="fa229-164">Optional</span><span class="sxs-lookup"><span data-stu-id="fa229-164">optional</span></span> | <span data-ttu-id="fa229-165">required</span><span class="sxs-lookup"><span data-stu-id="fa229-165">required</span></span>           |
| <span data-ttu-id="fa229-166">Farbe und Alpha getrennt</span><span class="sxs-lookup"><span data-stu-id="fa229-166">color and alpha separated</span></span> | <span data-ttu-id="fa229-167">required</span><span class="sxs-lookup"><span data-stu-id="fa229-167">required</span></span>  | <span data-ttu-id="fa229-168">required</span><span class="sxs-lookup"><span data-stu-id="fa229-168">required</span></span>      | <span data-ttu-id="fa229-169">Optional</span><span class="sxs-lookup"><span data-stu-id="fa229-169">optional</span></span>           | <span data-ttu-id="fa229-170">–</span><span class="sxs-lookup"><span data-stu-id="fa229-170">N/A</span></span>            | <span data-ttu-id="fa229-171">required</span><span class="sxs-lookup"><span data-stu-id="fa229-171">required</span></span>             | <span data-ttu-id="fa229-172">–</span><span class="sxs-lookup"><span data-stu-id="fa229-172">N/A</span></span>      | <span data-ttu-id="fa229-173">required</span><span class="sxs-lookup"><span data-stu-id="fa229-173">required</span></span>           |



 

<span data-ttu-id="fa229-174">Bzw bc7 definiert eine Palette von Farben in einer ungefähren Linie zwischen zwei Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="fa229-174">BC7 defines a palette of colors on an approximate line between two endpoints.</span></span> <span data-ttu-id="fa229-175">Der Mode-Wert bestimmt die Anzahl der interinterpolenden Endpunkt-Paare pro Block.</span><span class="sxs-lookup"><span data-stu-id="fa229-175">The mode value determines the number of interpolating endpoint pairs per block.</span></span> <span data-ttu-id="fa229-176">Bzw bc7 speichert einen Palettenindex pro Texel.</span><span class="sxs-lookup"><span data-stu-id="fa229-176">BC7 stores one palette index per texel.</span></span>

<span data-ttu-id="fa229-177">Für jede Teilmenge von Indizes, die einem Paar von Endpunkten entspricht, korrigiert der Encoder den Zustand der komprimierten Indexdaten für diese Teilmenge.</span><span class="sxs-lookup"><span data-stu-id="fa229-177">For each subset of indices that corresponds to a pair of endpoints, the encoder fixes the state of one bit of the compressed index data for that subset.</span></span> <span data-ttu-id="fa229-178">Dies geschieht, indem eine Endpunkt Reihenfolge ausgewählt wird, die es dem Index für den festgelegten "Fixup"-Index ermöglicht, das signifikanteste Bit auf 0 festzulegen, und das dann verworfen werden kann, wobei ein Bit pro Teilmenge gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="fa229-178">It does so by choosing an endpoint order that allows the index for the designated "fix-up" index to set its most significant bit to 0, and which can then be discarded, saving one bit per subset.</span></span> <span data-ttu-id="fa229-179">Bei Block Modi mit nur einer einzelnen Teilmenge ist der fixupindex immer Index 0.</span><span class="sxs-lookup"><span data-stu-id="fa229-179">For block modes with only a single subset, the fix-up index is always index 0.</span></span>

## <a name="decoding-the-bc7-format"></a><span data-ttu-id="fa229-180">Decodieren des bzw bc7-Formats</span><span class="sxs-lookup"><span data-stu-id="fa229-180">Decoding the BC7 Format</span></span>

<span data-ttu-id="fa229-181">Der folgende Pseudo Code beschreibt die Schritte zum Dekomprimieren des Pixels bei (x, y), wenn der 16-Byte-bzw bc7-Block angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa229-181">The following pseudocode outlines the steps to decompress the pixel at (x,y) given the 16 byte BC7 block.</span></span>

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

<span data-ttu-id="fa229-182">Der folgende Pseudo Code beschreibt die Schritte zum vollständigen Decodieren der Endpunktfarbe und der Alpha Komponenten für jede Teilmenge, wenn ein 16-Byte-bzw bc7-Block angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa229-182">The followoing pseudocode outlines the steps to fully decode endpoint color and alpha components for each subset given a 16-byte BC7 block.</span></span>

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

<span data-ttu-id="fa229-183">Verwenden Sie den folgenden Algorithmus, um jede interpoliert Komponente für jede Teilmenge zu generieren: Let "c" ist die Komponente, die generiert werden soll. "E0" ist die Komponente von Endpunkt 0 der Teilmenge. und lassen Sie "E1" als Komponente von Endpunkt 1 der Teilmenge fest.</span><span class="sxs-lookup"><span data-stu-id="fa229-183">To generate each interpolated component for each subset, use the following algorithm: let "c" be the component to generate; let "e0" be that component of endpoint 0 of the subset; and let "e1" be that component of endpoint 1 of the subset.</span></span>

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

<span data-ttu-id="fa229-184">Der folgende Pseudo Code veranschaulicht, wie Indizes und Bitwerte für die Farb-und Alpha Komponenten extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="fa229-184">The following pseudocode illustrates how to extract indices and bit counts for color and alpha components.</span></span> <span data-ttu-id="fa229-185">Blöcke mit separater Farbe und Alpha haben ebenfalls zwei Sätze von Indexdaten: eine für den Vektor Kanal und eine für den skalaren Kanal.</span><span class="sxs-lookup"><span data-stu-id="fa229-185">Blocks with separate color and alpha also have two sets of index data: one for the vector channel, and one for the scalar channel.</span></span> <span data-ttu-id="fa229-186">Für Modus 4 sind diese Indizes von unterschiedlichen breiten (2 oder 3 Bits), und es gibt eine Einbit-Auswahl, die angibt, ob der Vektor oder die skalaren Daten die 3-Bit-Indizes verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa229-186">For Mode 4, these indices are of differing widths (2 or 3 bits), and there is a one-bit selector which specifies whether the vector or scalar data uses the 3-bit indices.</span></span> <span data-ttu-id="fa229-187">(Das Extrahieren der Alpha Bitzahl ähnelt dem Extrahieren der farbbit-Anzahl, aber mit umgekehrtem Verhalten auf der Grundlage des **idxmode** -Bits.)</span><span class="sxs-lookup"><span data-stu-id="fa229-187">(Extracting the alpha bit count is similar to extracting color bit count but with inverse behavior based on the **idxMode** bit.)</span></span>

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a><span data-ttu-id="fa229-188">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa229-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa229-189">Textur Block Komprimierung in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="fa229-189">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 