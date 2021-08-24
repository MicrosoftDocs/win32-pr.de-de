---
title: BC7-Format
description: Das BC7-Format ist ein Texturkomprimierungsformat, das für die hochwertige Komprimierung von RGB- und RGBA-Daten verwendet wird.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd48826cc0c02be6d15a837c272442c0931e9660f507a90cb491acf4d5820ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858220"
---
# <a name="bc7-format"></a>BC7-Format

Das BC7-Format ist ein Texturkomprimierungsformat, das für die hochwertige Komprimierung von RGB- und RGBA-Daten verwendet wird.

-   [Informationen zum BC7/DXGI-FORMAT \_ \_ BC7](/windows)
-   [BC7-Implementierung](#bc7-implementation)
-   [Decodieren des BC7-Formats](#decoding-the-bc7-format)
-   [Zugehörige Themen](#related-topics)

Informationen zu den Blockmodi des BC7-Formats finden Sie in der [Referenz zum BC7-Formatmodus.](bc7-format-mode-reference.md)

## <a name="about-bc7dxgi_format_bc7"></a>Informationen zum BC7/DXGI-FORMAT \_ \_ BC7

BC7 wird durch die folgenden DXGI \_ FORMAT-Enumerationswerte angegeben:

-   **DXGI \_ FORMAT \_ BC7 \_ TYPELESS**.
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM**.
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM \_ SRGB**.

Das BC7-Format kann für Texturressourcen von [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (einschließlich Arrays), Texture3D oder TextureCube (einschließlich Arrays) verwendet werden. Ebenso gilt dieses Format für alle MIP-Kartenoberflächen, die diesen Ressourcen zugeordnet sind.

BC7 verwendet eine feste Blockgröße von 16 Bytes (128 Bits) und eine feste Kachelgröße von 4x4 Texels. Wie bei vorherigen BC-Formaten werden Texturbilder, die größer als die unterstützte Kachelgröße (4 x 4) sind, mithilfe mehrerer Blöcke komprimiert. Diese Adressierungsidentität gilt auch für dreidimensionale Bilder und MIP-Zuordnungen, Cubemaps und Texturarrays. Alle Bildkacheln müssen das gleiche Format haben.

BC7 komprimiert sowohl RGB-Datenbilder (Dreikanal) als auch RGBA-Festpunktdatenbilder(4-Kanal). In der Regel sind Quelldaten 8 Bits pro Farbkomponente (Kanal), obwohl das Format Quelldaten mit höheren Bits pro Farbkomponente codieren kann. Alle Bildkacheln müssen das gleiche Format haben.

Der BC7-Decoder führt eine Dekomprimierung durch, bevor Texturfilterung angewendet wird.

BC7-Dekomprimierungshardware muss bitgenau sein. Das heißt, die Hardware muss Ergebnisse zurückgeben, die mit den Ergebnissen identisch sind, die vom in diesem Dokument beschriebenen Decoder zurückgegeben werden.

## <a name="bc7-implementation"></a>BC7-Implementierung

Eine BC7-Implementierung kann einen von acht Modi angeben, bei dem der Modus im am wenigsten signifikanten Bit des 16-Byte-Blocks (128 Bit) angegeben ist. Der Modus wird durch null oder mehr Bits mit dem Wert 0 gefolgt von 1 codiert.

Ein BC7-Block kann mehrere Endpunktpaare enthalten. Im Rahmen dieser Dokumentation kann der Satz von Indizes, die einem Endpunktpaar entsprechen, als "Teilmenge" bezeichnet werden. Außerdem wird die Endpunktdarstellung in einigen Blockmodi in einer Form codiert, die – auch hier im Rahmen dieser Dokumentation – als "RBGP" bezeichnet wird, wobei das "P"-Bit ein gemeinsam genutztes, am wenigsten signifikantes Bit für die Farbkomponenten des Endpunkts darstellt. Wenn die Endpunktdarstellung für das Format beispielsweise "RGB 5.5.5.1" ist, wird der Endpunkt als RGB 6.6.6-Wert interpretiert, wobei der Zustand des P-Bit das am wenigsten signifikante Bit jeder Komponente definiert. Wenn für Quelldaten mit einem Alphakanal die Darstellung für das Format "RGBAP 5.5.5.5.1" ist, wird der Endpunkt als RGBA 6.6.6.6 interpretiert. Abhängig vom Blockmodus können Sie das am wenigsten signifikante Bit für beide Endpunkte einer Teilmenge einzeln (2 P-Bits pro Teilmenge) oder für Endpunkte einer Teilmenge (1 P-Bit pro Teilmenge) angeben.

Bei BC7-Blöcken, die die Alphakomponente nicht explizit codieren, besteht ein BC7-Block aus Modusbits, Partitionsbits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen P-Bit. In diesen Blöcken verfügen die Endpunkte über eine ausschließliche RGB-Darstellung, und die Alphakomponente wird für alle Texel in den Quelldaten als 1.0 decodiert.

Bei BC7-Blöcken mit kombinierten Farb- und Alphakomponenten besteht ein Block aus Modusbits, komprimierten Endpunkten, komprimierten Indizes und optionalen Partitionsbits und einem P-Bit. In diesen Blöcken werden die Endpunktfarben im RGBA-Format ausgedrückt, und Alphakomponentenwerte werden zusammen mit den Farbkomponentenwerten interpoliert.

Bei BC7-Blöcken mit separaten Farb- und Alphakomponenten besteht ein Block aus Modusbits, Drehungsbits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen Indexauswahlbit. Diese Blöcke verfügen über einen effektiven \[ RGB-Vektor R, G, B und \] einen skalaren Alphakanal \[ A separat \] codiert.

In der folgenden Tabelle sind die Komponenten der einzelnen Blocktypen aufgeführt.



| BC7-Block enthält...     | Modusbits | Drehungsbits | Indexauswahlbit | Partitionsbits | Komprimierte Endpunkte | P-Bit    | Komprimierte Indizes |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| Nur Farbkomponenten     | Erforderlich  | Nicht zutreffend           | Nicht zutreffend                | Erforderlich       | Erforderlich             | optional | Erforderlich           |
| Color + Alpha kombiniert    | Erforderlich  | Nicht zutreffend           | Nicht zutreffend                | optional       | Erforderlich             | optional | Erforderlich           |
| Farbe und Alpha getrennt | Erforderlich  | Erforderlich      | optional           | Nicht zutreffend            | Erforderlich             | Nicht zutreffend      | Erforderlich           |



 

BC7 definiert eine Palette von Farben auf einer ungefähren Linie zwischen zwei Endpunkten. Der Moduswert bestimmt die Anzahl der interpolierenden Endpunktpaare pro Block. BC7 speichert einen Palettenindex pro Texel.

Für jede Teilmenge von Indizes, die einem Endpunktpaar entspricht, korrigiert der Encoder den Zustand eines Bits der komprimierten Indexdaten für diese Teilmenge. Wählen Sie dazu eine Endpunkt reihenfolge aus, die es dem Index für den festgelegten "Fix up"-Index ermöglicht, das wichtigste Bit auf 0 zu setzen, und die dann verworfen werden kann, wodurch ein Bit pro Teilmenge spart. Bei Blockmodi mit nur einer Teilmenge ist der Fix up-Index immer Index 0.

## <a name="decoding-the-bc7-format"></a>Decodieren des BC7-Formats

Der folgende Pseudocode beschreibt die Schritte zum Dekomprimieren des Pixels bei (x,y) unter 16 Byte BC7-Block.

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

Der folgende Pseudocode beschreibt die Schritte zum vollständigen Decodieren von Endpunktfarbe und Alphakomponenten für jede Teilmenge mit einem BC7-Block mit 16 Byte.

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

Um jede interpolierte Komponente für jede Teilmenge zu generieren, verwenden Sie den folgenden Algorithmus: "c" soll die zu generierende Komponente sein. "e0" ist die Komponente von Endpunkt 0 der Teilmenge; und lassen Sie "e1" die Komponente von Endpunkt 1 der Teilmenge sein.

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

Der folgende Pseudocode veranschaulicht, wie Indizes und Bitanzahlen für Farb- und Alphakomponenten extrahiert werden. Blöcke mit separater Farbe und Alpha verfügen ebenfalls über zwei Sätze von Indexdaten: einen für den Vektorkanal und einen für den Skalarkanal. Für Modus 4 haben diese Indizes unterschiedliche Breiten (2 oder 3 Bits), und es gibt einen Ein-Bit-Selektor, der angibt, ob die Vektor- oder Skalardaten die 3-Bit-Indizes verwenden. (Das Extrahieren der Alphabitanzahl ähnelt dem Extrahieren der Anzahl von Farbbits, jedoch mit umgekehrten Verhalten, das auf dem **idxMode-Bit** basiert.)

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

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturblockkomprimierung in Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 