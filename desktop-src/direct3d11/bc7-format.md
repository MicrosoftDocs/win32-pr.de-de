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
# <a name="bc7-format"></a>Bzw bc7-Format

Das bzw bc7-Format ist ein Textur Komprimierungs Format, das für die hochwertige Komprimierung von RGB-und RGBA-Daten verwendet wird.

-   [Informationen zum bzw bc7/DXGI- \_ Format \_ bzw bc7](/windows)
-   [Bzw bc7-Implementierung](#bc7-implementation)
-   [Decodieren des bzw bc7-Formats](#decoding-the-bc7-format)
-   [Zugehörige Themen](#related-topics)

Informationen zu den Block Modi des bzw bc7-Formats finden Sie unter [bzw bc7 formatmode Reference](bc7-format-mode-reference.md).

## <a name="about-bc7dxgi_format_bc7"></a>Informationen zum bzw bc7/DXGI- \_ Format \_ bzw bc7

Bzw bc7 wird durch die folgenden DXGI- \_ formatenumerationswerte angegeben:

-   **DXGI \_ Format \_ bzw bc7 \_ typlose Formatierung**.
-   **DXGI \_ Formatieren Sie \_ bzw bc7 \_ unorm**.
-   **DXGI \_ Format \_ bzw bc7 \_ unorm \_ sRGB**.

Das bzw bc7-Format kann für die Textur Ressourcen [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (einschließlich Arrays), Texture3D oder texturecube (einschließlich Arrays) verwendet werden. Ebenso gilt dieses Format für alle mit diesen Ressourcen verknüpften MIP-Map-Oberflächen.

Bzw bc7 verwendet eine fester Blockgröße von 16 Bytes (128 Bits) und eine fixierte Kachel Größe von 4 x 4 texeln. Wie bei früheren BC-Formaten werden Textur Bilder, die größer als die unterstützte Kachel Größe (4X4) sind, mithilfe mehrerer Blöcke komprimiert. Diese Adressierungs Identität gilt auch für dreidimensionale Bilder und MIP-Maps, Cubemaps und Textur Arrays. Alle Bildkacheln müssen das gleiche Format aufweisen.

Bzw bc7 komprimiert sowohl Daten Abbilder mit drei Kanälen (RGB) als auch mit vier Kanälen (RGBA). Normalerweise handelt es sich bei den Quelldaten um 8 Bits pro Farbkomponente (Channel), obwohl das Format Quelldaten mit einer höheren Bits pro Color-Komponente codieren kann. Alle Bildkacheln müssen das gleiche Format aufweisen.

Der bzw bc7-Decoder führt vor dem Anwenden der Textur Filterung eine Komprimierung durch.

Bzw bc7-Komprimierungs Hardware muss etwas genau sein. Das heißt, dass die Hardware Ergebnisse zurückgeben muss, die mit den Ergebnissen identisch sind, die von dem in diesem Dokument beschriebenen Decoder zurückgegeben werden.

## <a name="bc7-implementation"></a>Bzw bc7-Implementierung

Eine bzw bc7-Implementierung kann einen von 8 Modi angeben, wobei der Modus im unwichtigsten Bit des 16-Byte-Blocks (128 Bit) angegeben wird. Der-Modus wird von 0 (null) oder mehr Bits mit einem Wert von 0 (null) gefolgt von einem 1 codiert.

Ein bzw bc7-Block kann mehrere Endpunkt Paare enthalten. Im Rahmen dieser Dokumentation kann der Satz von Indizes, die einem Endpunkt paar entsprechen, als "Teilmenge" bezeichnet werden. Außerdem wird die Endpunkt Darstellung in einigen Block Modi in einem Formular codiert, das für die Zwecke dieser Dokumentation wieder als "rbgp" bezeichnet wird. Hierbei steht das "P"-Bit für die Farbkomponenten des Endpunkts für ein gemeinsam genutztes Bit. Wenn die Endpunkt Darstellung für das Format z. b. "RGB 5.5.5.1" ist, wird der Endpunkt als RGB 6.6.6-Wert interpretiert, wobei der Status des P-Bits das unwichtigste Bit der einzelnen Komponenten definiert. Ebenso gilt für Quelldaten mit einem Alphakanal, wenn die Darstellung im Format "rgbap 5.5.5.5.1" ist, der Endpunkt als RGBA 6.6.6.6. Abhängig vom Block Modus können Sie das gemeinsame, unwichtigste Bit entweder für beide Endpunkte einer Teilmenge einzeln (2 p-Bits pro Teilmenge) oder für die gemeinsame Nutzung zwischen Endpunkten einer Teilmenge (1 p-Bit pro Teilmenge) angeben.

Für bzw bc7-Blöcke, die die Alpha Komponente nicht explizit codieren, besteht ein bzw bc7-Block aus modusbits, Partitions Bits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen P-Bit. In diesen Blöcken verfügen die Endpunkte über eine nur-RGB-Darstellung, und die Alpha Komponente wird als 1,0 für alle texeln in den Quelldaten decodiert.

Für bzw bc7-Blöcke mit kombinierten Farben und Alpha Komponenten besteht ein Block aus modusbits, komprimierten Endpunkten, komprimierten Indizes und optionalen Partitions Bits und einem P-Bit. In diesen Blöcken werden die Endpunkt Farben im RGBA-Format ausgedrückt, und Alpha Komponentenwerte werden zusammen mit den Farbkomponenten Werten interpoliert.

Für bzw bc7-Blöcke mit separaten Farb-und Alpha Komponenten besteht ein-Block aus modusbits, Rotations Bits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen indexselektor-Bit. Diese Blöcke verfügen über einen effektiven RGB \[ -Vektor R, G, B \] und einen skalaren Alphakanal, der \[ \] separat codiert ist.

In der folgenden Tabelle sind die Komponenten der einzelnen Blocktypen aufgeführt.



| Bzw bc7-Block enthält...     | modusbits | Drehungs Bits | Index Auswahl Bit | Partitions Bits | komprimierte Endpunkte | P-Bit    | komprimierte Indizes |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| nur Farbkomponenten     | required  | –           | –                | required       | required             | Optional | required           |
| Farbe + Alpha, kombiniert    | required  | –           | –                | Optional       | required             | Optional | required           |
| Farbe und Alpha getrennt | required  | required      | Optional           | –            | required             | –      | required           |



 

Bzw bc7 definiert eine Palette von Farben in einer ungefähren Linie zwischen zwei Endpunkten. Der Mode-Wert bestimmt die Anzahl der interinterpolenden Endpunkt-Paare pro Block. Bzw bc7 speichert einen Palettenindex pro Texel.

Für jede Teilmenge von Indizes, die einem Paar von Endpunkten entspricht, korrigiert der Encoder den Zustand der komprimierten Indexdaten für diese Teilmenge. Dies geschieht, indem eine Endpunkt Reihenfolge ausgewählt wird, die es dem Index für den festgelegten "Fixup"-Index ermöglicht, das signifikanteste Bit auf 0 festzulegen, und das dann verworfen werden kann, wobei ein Bit pro Teilmenge gespeichert wird. Bei Block Modi mit nur einer einzelnen Teilmenge ist der fixupindex immer Index 0.

## <a name="decoding-the-bc7-format"></a>Decodieren des bzw bc7-Formats

Der folgende Pseudo Code beschreibt die Schritte zum Dekomprimieren des Pixels bei (x, y), wenn der 16-Byte-bzw bc7-Block angegeben wird.

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

Der folgende Pseudo Code beschreibt die Schritte zum vollständigen Decodieren der Endpunktfarbe und der Alpha Komponenten für jede Teilmenge, wenn ein 16-Byte-bzw bc7-Block angegeben wird.

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

Verwenden Sie den folgenden Algorithmus, um jede interpoliert Komponente für jede Teilmenge zu generieren: Let "c" ist die Komponente, die generiert werden soll. "E0" ist die Komponente von Endpunkt 0 der Teilmenge. und lassen Sie "E1" als Komponente von Endpunkt 1 der Teilmenge fest.

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

Der folgende Pseudo Code veranschaulicht, wie Indizes und Bitwerte für die Farb-und Alpha Komponenten extrahiert werden. Blöcke mit separater Farbe und Alpha haben ebenfalls zwei Sätze von Indexdaten: eine für den Vektor Kanal und eine für den skalaren Kanal. Für Modus 4 sind diese Indizes von unterschiedlichen breiten (2 oder 3 Bits), und es gibt eine Einbit-Auswahl, die angibt, ob der Vektor oder die skalaren Daten die 3-Bit-Indizes verwenden. (Das Extrahieren der Alpha Bitzahl ähnelt dem Extrahieren der farbbit-Anzahl, aber mit umgekehrtem Verhalten auf der Grundlage des **idxmode** -Bits.)

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

[Textur Block Komprimierung in Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 