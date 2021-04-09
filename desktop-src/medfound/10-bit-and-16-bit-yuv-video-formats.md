---
description: In diesem Thema werden die 10-und 16-Bit-YUV-Formate beschrieben, die zum erfassen, verarbeiten und Anzeigen von Videos im Microsoft Windows-Betriebssystem empfohlen werden.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: 10-Bit-und 16-Bit-YUV-Video Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129560"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a><span data-ttu-id="46cec-103">10-Bit-und 16-Bit-YUV-Video Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-103">10-bit and 16-bit YUV Video Formats</span></span>

<span data-ttu-id="46cec-104">In diesem Thema werden die 10-und 16-Bit-YUV-Formate beschrieben, die zum erfassen, verarbeiten und Anzeigen von Videos im Microsoft Windows-Betriebssystem empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="46cec-104">This topic describes the 10- and 16-bit YUV formats that are recommended for capturing, processing, and displaying video in the Microsoft Windows operating system.</span></span>

<span data-ttu-id="46cec-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="46cec-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="46cec-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="46cec-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="46cec-107">FourCC Codes für 10-Bit-und 16-Bit-YUV</span><span class="sxs-lookup"><span data-stu-id="46cec-107">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [<span data-ttu-id="46cec-108">Oberflächen Definitionen</span><span class="sxs-lookup"><span data-stu-id="46cec-108">Surface Definitions</span></span>](#surface-definitions)
    -   [<span data-ttu-id="46cec-109">4:2:0 Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-109">4:2:0 Formats</span></span>](#420-formats)
    -   [<span data-ttu-id="46cec-110">4:2:2 Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-110">4:2:2 Formats</span></span>](#422-formats)
    -   [<span data-ttu-id="46cec-111">4:4:4 Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-111">4:4:4 Formats</span></span>](#444-formats)
-   [<span data-ttu-id="46cec-112">Bevorzugte YUV-Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-112">Preferred YUV Formats</span></span>](#preferred-yuv-formats)
-   [<span data-ttu-id="46cec-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46cec-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="46cec-114">Übersicht</span><span class="sxs-lookup"><span data-stu-id="46cec-114">Overview</span></span>

<span data-ttu-id="46cec-115">Diese Formate verwenden eine Fixed-Point-Darstellung für die Kanäle "Luma" und "Chroma" ("c" und "c").</span><span class="sxs-lookup"><span data-stu-id="46cec-115">These formats use a fixed-point representation for both the luma channel and the chroma (C'b and C'r) channels.</span></span> <span data-ttu-id="46cec-116">Beispiel Werte sind skalierte 8-Bit-Werte unter Verwendung eines Skalierungsfaktors von 2 ^ (n − 8), wobei n entweder 10 oder 16 ist, gemäß den Abschnitten 7.7-7.8 und 7.11-7.12 von SMPTE 274m.</span><span class="sxs-lookup"><span data-stu-id="46cec-116">Sample values are scaled 8-bit values, using a scaling factor of 2^(n − 8), where n is either 10 or 16, as per sections 7.7-7.8 and 7.11-7.12 of SMPTE 274M.</span></span> <span data-ttu-id="46cec-117">Genauigkeits Konvertierungen können mithilfe von einfachen Bitverschiebungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="46cec-117">Precision conversions can be performed using simple bit shifts.</span></span> <span data-ttu-id="46cec-118">Wenn der weiße Punkt eines 8-Bit-Formats z. b. 235 ist, hat das entsprechende 10-Bit-Format einen weißen Punkt bei 940 (235 × 4).</span><span class="sxs-lookup"><span data-stu-id="46cec-118">For example, if the white point of an 8-bit format is 235, the corresponding 10-bit format has a white point at 940 (235 × 4).</span></span>

<span data-ttu-id="46cec-119">In den hier beschriebenen 16-Bit-Darstellungen werden für jeden Kanal Little-Endian- **Wort** Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="46cec-119">The 16-bit representations described here use little-endian **WORD** values for each channel.</span></span> <span data-ttu-id="46cec-120">Die 10-Bit-Formate verwenden auch 16 Bits für jeden Kanal, wobei die niedrigsten 6 Bits auf 0 (null) festgelegt sind, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46cec-120">The 10-bit formats also use 16 bits for each channel, with the lowest 6 bits set to zero, as shown in the following diagram.</span></span>

![Diagramm mit 10-Bit-Darstellung](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

<span data-ttu-id="46cec-122">Da die 10-Bit-und die 16-Bit-Darstellung desselben YUV-Formats das gleiche Speicher Layout aufweisen, ist es möglich, eine 10-Bit-Darstellung ohne Genauigkeits Verlust in eine 16-Darstellung umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="46cec-122">Because the 10-bit and 16-bit representations of the same YUV format have the same memory layout, it is possible to cast a 10-bit representation to a 16-representation with no loss of precision.</span></span> <span data-ttu-id="46cec-123">Es ist auch möglich, eine 16-Bit-Darstellung in eine 10-Bit-Darstellung umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="46cec-123">It is also possible to cast a 16-bit representation down to a 10-bit representation.</span></span> <span data-ttu-id="46cec-124">(Bei den Formaten Y416 und Y410 handelt es sich jedoch um eine Ausnahme von dieser allgemeinen Regel, da Sie nicht das gleiche Speicher Layout haben.)</span><span class="sxs-lookup"><span data-stu-id="46cec-124">(The Y416 and Y410 formats are an exception to this general rule, however, because they do not share the same memory layout.)</span></span>

<span data-ttu-id="46cec-125">Wenn die Grafikhardware eine Oberfläche liest, die eine 10-Bit-Darstellung enthält, sollten die nieder wertigen 6 Bits der einzelnen Kanäle ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="46cec-125">When the graphics hardware reads a surface that contains a 10-bit representation, it should ignore the low-order 6 bits of each channel.</span></span> <span data-ttu-id="46cec-126">Wenn eine Oberfläche gültige 16-Bit-Daten enthält, sollte Sie jedoch als 16-Bit-Oberfläche identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="46cec-126">If a surface contains valid 16-bit data, however, it should be identified as a 16-bit surface.</span></span>

<span data-ttu-id="46cec-127">In den Formaten, die Alpha enthalten, weist ein vollständig transparentes Pixel einen Alpha-Wert von 0 (null) auf, und ein vollständig undurchsichtiges Pixel weist den Alpha-Wert (2 ^ n) – 1 auf, wobei n die Anzahl der Alpha Bits ist.</span><span class="sxs-lookup"><span data-stu-id="46cec-127">In the formats that contain alpha, a completely transparent pixel has an alpha value of zero, and a completely opaque pixel has an alpha value of (2^n) – 1, where n is the number of alpha bits.</span></span> <span data-ttu-id="46cec-128">Bei Alpha wird angenommen, dass es sich um einen linearen Wert handelt, der auf jede Komponente angewendet wird, nachdem die Komponente in die normalisierte lineare Form konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="46cec-128">Alpha is assumed to be a linear value that is applied to each component after the component has been converted into its normalized linear form.</span></span>

<span data-ttu-id="46cec-129">Bei Bildern im Videospeicher wählt der Grafiktreiber die Arbeitsspeicher Ausrichtung der Oberfläche aus.</span><span class="sxs-lookup"><span data-stu-id="46cec-129">For images in video memory, the graphics driver selects the memory alignment of the surface.</span></span> <span data-ttu-id="46cec-130">Die Oberfläche muss in **DWORD** ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="46cec-130">The surface must be **DWORD** aligned.</span></span> <span data-ttu-id="46cec-131">Das heißt, einzelne Zeilen innerhalb einer Oberfläche werden garantiert an einer 32-Bit-Grenze gestartet, obwohl die Ausrichtung größer als 32 Bits sein kann.</span><span class="sxs-lookup"><span data-stu-id="46cec-131">That is, individual lines within a surface are guaranteed to start at a 32-bit boundary, although the alignment can be larger than 32 bits.</span></span> <span data-ttu-id="46cec-132">Der Ursprung (0,0) ist immer die obere linke Ecke der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="46cec-132">The origin (0,0) is always the upper-left corner of the surface.</span></span>

<span data-ttu-id="46cec-133">Im Rahmen dieser Dokumentation entspricht der Begriff " *U* " dem Wert von " *CB*", und der Begriff " *V* " entspricht *CR*.</span><span class="sxs-lookup"><span data-stu-id="46cec-133">For the purposes of this documentation, the term *U* is equivalent to *Cb*, and the term *V* is equivalent to *Cr*.</span></span>

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a><span data-ttu-id="46cec-134">FourCC Codes für 10-Bit-und 16-Bit-YUV</span><span class="sxs-lookup"><span data-stu-id="46cec-134">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>

<span data-ttu-id="46cec-135">In den FourCC-Codes für die hier beschriebenen Formate wird die folgende Konvention verwendet:</span><span class="sxs-lookup"><span data-stu-id="46cec-135">The FOURCC codes for the formats described here use the following convention:</span></span>

-   <span data-ttu-id="46cec-136">Wenn das Format Planar ist, lautet das erste Zeichen im FourCC-Code "P".</span><span class="sxs-lookup"><span data-stu-id="46cec-136">If the format is planar, the first character in the FOURCC code is 'P'.</span></span> <span data-ttu-id="46cec-137">Wenn das Format gepackt ist, ist das erste Zeichen "Y".</span><span class="sxs-lookup"><span data-stu-id="46cec-137">If the format is packed, the first character is 'Y'.</span></span>
-   <span data-ttu-id="46cec-138">Das zweite Zeichen im FourCC-Code wird durch die Chroma-Stichprobenentnahme bestimmt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46cec-138">The second character in the FOURCC code is determined by the chroma sampling, as shown in the following table.</span></span>

    

    | <span data-ttu-id="46cec-139">Chroma-Sampling</span><span class="sxs-lookup"><span data-stu-id="46cec-139">Chroma sampling</span></span> | <span data-ttu-id="46cec-140">FourCC-Code Buchstabe</span><span class="sxs-lookup"><span data-stu-id="46cec-140">FOURCC code letter</span></span> |
    |-----------------|--------------------|
    | <span data-ttu-id="46cec-141">4:4:4</span><span class="sxs-lookup"><span data-stu-id="46cec-141">4:4:4</span></span>           | <span data-ttu-id="46cec-142">0:</span><span class="sxs-lookup"><span data-stu-id="46cec-142">'4'</span></span>                |
    | <span data-ttu-id="46cec-143">4:2:2</span><span class="sxs-lookup"><span data-stu-id="46cec-143">4:2:2</span></span>           | <span data-ttu-id="46cec-144">2,2</span><span class="sxs-lookup"><span data-stu-id="46cec-144">'2'</span></span>                |
    | <span data-ttu-id="46cec-145">4:2:1</span><span class="sxs-lookup"><span data-stu-id="46cec-145">4:2:1</span></span>           | <span data-ttu-id="46cec-146">'1'</span><span class="sxs-lookup"><span data-stu-id="46cec-146">'1'</span></span>                |
    | <span data-ttu-id="46cec-147">4:2:0</span><span class="sxs-lookup"><span data-stu-id="46cec-147">4:2:0</span></span>           | <span data-ttu-id="46cec-148">'0'</span><span class="sxs-lookup"><span data-stu-id="46cec-148">'0'</span></span>                |

    

     

-   <span data-ttu-id="46cec-149">Die letzten zwei Zeichen im FourCC geben die Anzahl der Bits pro Kanal an, entweder "16" für 16 Bits oder "10" für 10 Bits.</span><span class="sxs-lookup"><span data-stu-id="46cec-149">The final two characters in the FOURCC indicate the number of bits per channel, either '16' for 16 bits or '10' for 10 bits.</span></span>

<span data-ttu-id="46cec-150">Mithilfe dieses Schemas wurden die folgenden FOURCC-Codes definiert.</span><span class="sxs-lookup"><span data-stu-id="46cec-150">Using this scheme, the following FOURCC codes have been defined.</span></span> <span data-ttu-id="46cec-151">Zurzeit wurden keine 4:2:1-Formate für 10-Bit-oder 16-Bit-YUV definiert.</span><span class="sxs-lookup"><span data-stu-id="46cec-151">No 4:2:1 formats for 10-bit or 16-bit YUV have been defined at this time.</span></span>



| <span data-ttu-id="46cec-152">FOURCC</span><span class="sxs-lookup"><span data-stu-id="46cec-152">FOURCC</span></span> | <span data-ttu-id="46cec-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46cec-153">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="46cec-154">P016</span><span class="sxs-lookup"><span data-stu-id="46cec-154">P016</span></span>   | <span data-ttu-id="46cec-155">Planar, 4:2:0, 16-Bit.</span><span class="sxs-lookup"><span data-stu-id="46cec-155">Planar, 4:2:0, 16-bit.</span></span> |
| <span data-ttu-id="46cec-156">P010</span><span class="sxs-lookup"><span data-stu-id="46cec-156">P010</span></span>   | <span data-ttu-id="46cec-157">Planar, 4:2:0, 10-Bit.</span><span class="sxs-lookup"><span data-stu-id="46cec-157">Planar, 4:2:0, 10-bit.</span></span> |
| <span data-ttu-id="46cec-158">P216</span><span class="sxs-lookup"><span data-stu-id="46cec-158">P216</span></span>   | <span data-ttu-id="46cec-159">Planar, 4:2:2, 16-Bit.</span><span class="sxs-lookup"><span data-stu-id="46cec-159">Planar, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="46cec-160">P210</span><span class="sxs-lookup"><span data-stu-id="46cec-160">P210</span></span>   | <span data-ttu-id="46cec-161">Planar, 4:2:2, 10-Bit.</span><span class="sxs-lookup"><span data-stu-id="46cec-161">Planar, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="46cec-162">Y216</span><span class="sxs-lookup"><span data-stu-id="46cec-162">Y216</span></span>   | <span data-ttu-id="46cec-163">Gepackt, 4:2:2, 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="46cec-163">Packed, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="46cec-164">Y210</span><span class="sxs-lookup"><span data-stu-id="46cec-164">Y210</span></span>   | <span data-ttu-id="46cec-165">Gepackt, 4:2:2, 10-Bit.</span><span class="sxs-lookup"><span data-stu-id="46cec-165">Packed, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="46cec-166">Y416</span><span class="sxs-lookup"><span data-stu-id="46cec-166">Y416</span></span>   | <span data-ttu-id="46cec-167">Gepackt, 4:4:4, 16 Bit</span><span class="sxs-lookup"><span data-stu-id="46cec-167">Packed, 4:4:4, 16-bit</span></span>  |
| <span data-ttu-id="46cec-168">Y410</span><span class="sxs-lookup"><span data-stu-id="46cec-168">Y410</span></span>   | <span data-ttu-id="46cec-169">Gepackt, 4:4:4, 10-Bit.</span><span class="sxs-lookup"><span data-stu-id="46cec-169">Packed, 4:4:4, 10-bit.</span></span> |



 

<span data-ttu-id="46cec-170">Untertyp-GUIDs wurden auch aus diesen fourccs definiert. siehe [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="46cec-170">Subtype GUIDs have also been defined from these FOURCCs; see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="46cec-171">Oberflächen Definitionen</span><span class="sxs-lookup"><span data-stu-id="46cec-171">Surface Definitions</span></span>

<span data-ttu-id="46cec-172">In diesem Abschnitt wird das Speicher Layout der einzelnen Formate beschrieben.</span><span class="sxs-lookup"><span data-stu-id="46cec-172">This section describes the memory layout of each format.</span></span> <span data-ttu-id="46cec-173">In den folgenden Beschreibungen verweist der Begriff **Word** auf einen Little-Endian-16-Bit-Wert, und der Begriff **DWORD** verweist auf einen Little-Endian-32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="46cec-173">In the descriptions that follow, the term **WORD** refers to a little-endian 16-bit value, and the term **DWORD** refers to a little-endian 32-bit value.</span></span>

### <a name="420-formats"></a><span data-ttu-id="46cec-174">4:2:0 Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-174">4:2:0 Formats</span></span>

<span data-ttu-id="46cec-175">Es werden zwei 4:2:0-Formate mit den FourCC-Codes P016 und P010 definiert.</span><span class="sxs-lookup"><span data-stu-id="46cec-175">Two 4:2:0 formats are defined, with the FOURCC codes P016 and P010.</span></span> <span data-ttu-id="46cec-176">Sie verwenden dasselbe Speicher Layout, aber P016 verwendet 16 Bits pro Kanal und P010 verwendet 10 Bits pro Kanal.</span><span class="sxs-lookup"><span data-stu-id="46cec-176">They share the same memory layout, but P016 uses 16 bits per channel and P010 uses 10 bits per channel.</span></span>

### <a name="p016-and-p010"></a><span data-ttu-id="46cec-177">P016 und P010</span><span class="sxs-lookup"><span data-stu-id="46cec-177">P016 and P010</span></span>

<span data-ttu-id="46cec-178">In diesen beiden Formaten werden alle Y-Beispiele als erstes im Arbeitsspeicher als Array von **Word** s mit einer geraden Anzahl von Zeilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46cec-178">In these two formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="46cec-179">Der Oberflächen Schritt kann größer als die Breite der Y-Ebene sein.</span><span class="sxs-lookup"><span data-stu-id="46cec-179">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="46cec-180">Auf dieses Array folgt unmittelbar ein Array von **Word** s, das verschachtelte Sie-und V-Beispiele enthält, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46cec-180">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![Diagramm mit P016 und P010 Pixel Layout](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

<span data-ttu-id="46cec-182">Wenn das kombinierte U-V-Array als Array von **DWORD** adressiert wird, enthält das unwichtigste Wort (LSW) den U-Wert und das signifikanteste Wort (MSW) den V-Wert.</span><span class="sxs-lookup"><span data-stu-id="46cec-182">If the combined U-V array is addressed as an array of **DWORD** s, the least significant word (LSW) contains the U value and the most significant word (MSW) contains the V value.</span></span> <span data-ttu-id="46cec-183">Der Schritt der kombinierten U-V-Ebene entspricht dem STRIDE der Y-Ebene.</span><span class="sxs-lookup"><span data-stu-id="46cec-183">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="46cec-184">Die U-V-Ebene hat die Hälfte der Zeilen in der Y-Ebene.</span><span class="sxs-lookup"><span data-stu-id="46cec-184">The U-V plane has half as many lines as the Y plane.</span></span>

<span data-ttu-id="46cec-185">Diese beiden Formate sind die bevorzugten 4:2:0-planaren Pixel Formate für YUV-Darstellungen mit höherer Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="46cec-185">These two formats are the preferred 4:2:0 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="46cec-186">Es wird erwartet, dass es sich um eine zwischen Bedingung für DXVA-Accelerators (DirectX Video Acceleration) handelt, die 10-Bit-oder 16-Bit-4:2:0-Videos unterstützen.</span><span class="sxs-lookup"><span data-stu-id="46cec-186">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:0 video.</span></span>

### <a name="422-formats"></a><span data-ttu-id="46cec-187">4:2:2 Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-187">4:2:2 Formats</span></span>

<span data-ttu-id="46cec-188">Vier 4:2:2 Formate sind definiert, zwei planare und zwei gepackte.</span><span class="sxs-lookup"><span data-stu-id="46cec-188">Four 4:2:2 formats are defined, two planar and two packed.</span></span> <span data-ttu-id="46cec-189">Sie verfügen über die folgenden FOURCC-Codes:</span><span class="sxs-lookup"><span data-stu-id="46cec-189">They have the following FOURCC codes:</span></span>

-   <span data-ttu-id="46cec-190">P216</span><span class="sxs-lookup"><span data-stu-id="46cec-190">P216</span></span>
-   <span data-ttu-id="46cec-191">P210</span><span class="sxs-lookup"><span data-stu-id="46cec-191">P210</span></span>
-   <span data-ttu-id="46cec-192">Y216</span><span class="sxs-lookup"><span data-stu-id="46cec-192">Y216</span></span>
-   <span data-ttu-id="46cec-193">Y210</span><span class="sxs-lookup"><span data-stu-id="46cec-193">Y210</span></span>

### <a name="p216-and-p210"></a><span data-ttu-id="46cec-194">P216 und P210</span><span class="sxs-lookup"><span data-stu-id="46cec-194">P216 and P210</span></span>

<span data-ttu-id="46cec-195">In diesen beiden planaren Formaten werden alle Y-Beispiele als erstes im Arbeitsspeicher als Array von **Word** s mit einer geraden Anzahl von Zeilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46cec-195">In these two planar formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="46cec-196">Der Oberflächen Schritt kann größer als die Breite der Y-Ebene sein.</span><span class="sxs-lookup"><span data-stu-id="46cec-196">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="46cec-197">Auf dieses Array folgt unmittelbar ein Array von **Word** s, das verschachtelte Sie-und V-Beispiele enthält, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46cec-197">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![Diagramm mit P216 und P210 Pixel Layout](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

<span data-ttu-id="46cec-199">Wenn das kombinierte U-V-Array als ein Array von **DWORD** s adressiert wird, enthält der LSW den U-Wert, und der MSW enthält den V-Wert.</span><span class="sxs-lookup"><span data-stu-id="46cec-199">If the combined U-V array is addressed as an array of **DWORD** s, the LSW contains the U value and the MSW contains the V value.</span></span> <span data-ttu-id="46cec-200">Der Schritt der kombinierten U-V-Ebene entspricht dem STRIDE der Y-Ebene.</span><span class="sxs-lookup"><span data-stu-id="46cec-200">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="46cec-201">Die U-V-Ebene verfügt über die gleiche Anzahl von Zeilen wie die Y-Ebene.</span><span class="sxs-lookup"><span data-stu-id="46cec-201">The U-V plane has the same number of lines as the Y plane.</span></span>

<span data-ttu-id="46cec-202">Diese beiden Formate sind die bevorzugten 4:2:2-planaren Pixel Formate für YUV-Darstellungen mit höherer Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="46cec-202">These two formats are the preferred 4:2:2 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="46cec-203">Es wird erwartet, dass es sich um eine zwischen Bedingung für DXVA-Accelerators (DirectX Video Acceleration) handelt, die 10-Bit-oder 16-Bit-4:2:2-Videos unterstützen.</span><span class="sxs-lookup"><span data-stu-id="46cec-203">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:2 video.</span></span>

### <a name="y216-and-y210"></a><span data-ttu-id="46cec-204">Y216 und Y210</span><span class="sxs-lookup"><span data-stu-id="46cec-204">Y216 and Y210</span></span>

<span data-ttu-id="46cec-205">In diesen zwei verpackten Formaten wird jedes Pixel Paar als Array von vier **Wörtern** gespeichert, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46cec-205">In these two packed formats, each pair of pixels is stored as an array of four **WORD** s, as shown in the following illustration.</span></span>

![Diagramm, das das Pixel Layout y216 und y210 anzeigt.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

<span data-ttu-id="46cec-207">Das erste **Wort** im Array enthält das erste y-Beispiel im Paar, das zweite **Wort** enthält das U-Beispiel, das dritte **Wort** enthält das zweite y-Beispiel, und das vierte **Wort** enthält das V-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="46cec-207">The first **WORD** in the array contains the first Y sample in the pair, the second **WORD** contains the U sample, the third **WORD** contains the second Y sample, and the fourth **WORD** contains the V sample.</span></span>

<span data-ttu-id="46cec-208">Y210 ist mit Y216 identisch, mit dem Unterschied, dass jedes Beispiel nur 10 Bits signifikanter Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="46cec-208">Y210 is identical to Y216 except that each sample contains only 10 bits of significant data.</span></span> <span data-ttu-id="46cec-209">Die am wenigsten wichtigen 6 Bits werden auf 0 (null) festgelegt, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="46cec-209">The least significant 6 bits are set to zero, as described previously.</span></span>

### <a name="444-formats"></a><span data-ttu-id="46cec-210">4:4:4 Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-210">4:4:4 Formats</span></span>

<span data-ttu-id="46cec-211">Es werden zwei 4:4:4-Formate mit den FourCC-Codes Y410 und Y416 definiert.</span><span class="sxs-lookup"><span data-stu-id="46cec-211">Two 4:4:4 formats are defined, with the FOURCC codes Y410 and Y416.</span></span> <span data-ttu-id="46cec-212">Beide sind gepackte Formate.</span><span class="sxs-lookup"><span data-stu-id="46cec-212">Both are packed formats.</span></span>

### <a name="y410"></a><span data-ttu-id="46cec-213">Y410</span><span class="sxs-lookup"><span data-stu-id="46cec-213">Y410</span></span>

<span data-ttu-id="46cec-214">Dieses Format ist eine gepackte 10-Bit-Darstellung, die 2 Bits von Alpha enthält.</span><span class="sxs-lookup"><span data-stu-id="46cec-214">This format is a packed 10-bit representation that includes 2 bits of alpha.</span></span> <span data-ttu-id="46cec-215">Jedes Pixel wird als einzelnes **DWORD** mit dem im folgenden Diagramm dargestellten Arbeitsspeicher Layout codiert.</span><span class="sxs-lookup"><span data-stu-id="46cec-215">Each pixel is encoded as a single **DWORD** with the memory layout shown in the following diagram.</span></span>

![Diagramm, das das y410 Pixel Layout anzeigt.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

<span data-ttu-id="46cec-217">Bits 0-9 enthalten das U-Beispiel, Bits 10-19 enthalten das Y-Beispiel, Bits 20-29 das V-Beispiel und Bits 30-31 den Alpha-Wert.</span><span class="sxs-lookup"><span data-stu-id="46cec-217">Bits 0-9 contain the U sample, bits 10-19 contain the Y sample, bits 20-29 contain the V sample, and bits 30-31 contain the alpha value.</span></span> <span data-ttu-id="46cec-218">Um anzugeben, dass ein Pixel vollständig undurchsichtig ist, muss eine Anwendung die beiden Alpha Bits gleich 0x03 festlegen.</span><span class="sxs-lookup"><span data-stu-id="46cec-218">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0x03.</span></span>

### <a name="y416"></a><span data-ttu-id="46cec-219">Y416</span><span class="sxs-lookup"><span data-stu-id="46cec-219">Y416</span></span>

<span data-ttu-id="46cec-220">Dieses Format ist eine gepackte 16-Bit-Darstellung, die 16 Bits von Alpha enthält.</span><span class="sxs-lookup"><span data-stu-id="46cec-220">This format is a packed 16-bit representation that includes 16 bits of alpha.</span></span> <span data-ttu-id="46cec-221">Jedes Pixel wird als Paar von **DWORD** s codiert, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46cec-221">Each pixel is encoded as a pair of **DWORD** s, as shown in the following illustration.</span></span>

![Diagramm, das das y416 Pixel Layout anzeigt.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

<span data-ttu-id="46cec-223">Bits 0-15 enthalten das U-Beispiel, Bits 16-31 enthalten das Y-Beispiel, Bits 32-47 das V-Beispiel und Bits 48-63 den Alpha-Wert.</span><span class="sxs-lookup"><span data-stu-id="46cec-223">Bits 0-15 contain the U sample, bits 16-31 contain the Y sample, bits 32-47 contain the V sample, and bits 48-63 contain the alpha value.</span></span>

<span data-ttu-id="46cec-224">Um anzugeben, dass ein Pixel vollständig undurchsichtig ist, muss eine Anwendung die beiden Alpha Bits gleich 0xFFFF festlegen.</span><span class="sxs-lookup"><span data-stu-id="46cec-224">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0xFFFF.</span></span> <span data-ttu-id="46cec-225">Dieses Format dient primär als zwischen Format bei der Bildverarbeitung, um die Ansammlung von Fehlern zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="46cec-225">This format is intended primarily as an intermediate format during image processing to avoid the accumulation of errors.</span></span>

## <a name="preferred-yuv-formats"></a><span data-ttu-id="46cec-226">Bevorzugte YUV-Formate</span><span class="sxs-lookup"><span data-stu-id="46cec-226">Preferred YUV Formats</span></span>

<span data-ttu-id="46cec-227">In der folgenden Tabelle werden die bevorzugten YUV-Formate einschließlich 8-Bit-Formaten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="46cec-227">The following table lists the preferred YUV formats, including 8-bit formats.</span></span>



| <span data-ttu-id="46cec-228">Format</span><span class="sxs-lookup"><span data-stu-id="46cec-228">Format</span></span> | <span data-ttu-id="46cec-229">Chroma-Sampling</span><span class="sxs-lookup"><span data-stu-id="46cec-229">Chroma sampling</span></span> | <span data-ttu-id="46cec-230">Gepackt oder planare</span><span class="sxs-lookup"><span data-stu-id="46cec-230">Packed or planar</span></span> | <span data-ttu-id="46cec-231">Bits pro Kanal</span><span class="sxs-lookup"><span data-stu-id="46cec-231">Bits per channel</span></span> |
|--------|-----------------|------------------|------------------|
| <span data-ttu-id="46cec-232">Ayuv</span><span class="sxs-lookup"><span data-stu-id="46cec-232">AYUV</span></span>   | <span data-ttu-id="46cec-233">4:4:4</span><span class="sxs-lookup"><span data-stu-id="46cec-233">4:4:4</span></span>           | <span data-ttu-id="46cec-234">Stop</span><span class="sxs-lookup"><span data-stu-id="46cec-234">Packed</span></span>           | <span data-ttu-id="46cec-235">8</span><span class="sxs-lookup"><span data-stu-id="46cec-235">8</span></span>                |
| <span data-ttu-id="46cec-236">Y410</span><span class="sxs-lookup"><span data-stu-id="46cec-236">Y410</span></span>   | <span data-ttu-id="46cec-237">4:4:4</span><span class="sxs-lookup"><span data-stu-id="46cec-237">4:4:4</span></span>           | <span data-ttu-id="46cec-238">Stop</span><span class="sxs-lookup"><span data-stu-id="46cec-238">Packed</span></span>           | <span data-ttu-id="46cec-239">10</span><span class="sxs-lookup"><span data-stu-id="46cec-239">10</span></span>               |
| <span data-ttu-id="46cec-240">Y416</span><span class="sxs-lookup"><span data-stu-id="46cec-240">Y416</span></span>   | <span data-ttu-id="46cec-241">4:4:4</span><span class="sxs-lookup"><span data-stu-id="46cec-241">4:4:4</span></span>           | <span data-ttu-id="46cec-242">Stop</span><span class="sxs-lookup"><span data-stu-id="46cec-242">Packed</span></span>           | <span data-ttu-id="46cec-243">16</span><span class="sxs-lookup"><span data-stu-id="46cec-243">16</span></span>               |
| <span data-ttu-id="46cec-244">AI44</span><span class="sxs-lookup"><span data-stu-id="46cec-244">AI44</span></span>   | <span data-ttu-id="46cec-245">4:4:4</span><span class="sxs-lookup"><span data-stu-id="46cec-245">4:4:4</span></span>           | <span data-ttu-id="46cec-246">Stop</span><span class="sxs-lookup"><span data-stu-id="46cec-246">Packed</span></span>           | <span data-ttu-id="46cec-247">Das Paletten</span><span class="sxs-lookup"><span data-stu-id="46cec-247">Palettized</span></span>       |
| <span data-ttu-id="46cec-248">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="46cec-248">YUY2</span></span>   | <span data-ttu-id="46cec-249">4:2:2</span><span class="sxs-lookup"><span data-stu-id="46cec-249">4:2:2</span></span>           | <span data-ttu-id="46cec-250">Stop</span><span class="sxs-lookup"><span data-stu-id="46cec-250">Packed</span></span>           | <span data-ttu-id="46cec-251">8</span><span class="sxs-lookup"><span data-stu-id="46cec-251">8</span></span>                |
| <span data-ttu-id="46cec-252">Y210</span><span class="sxs-lookup"><span data-stu-id="46cec-252">Y210</span></span>   | <span data-ttu-id="46cec-253">4:2:2</span><span class="sxs-lookup"><span data-stu-id="46cec-253">4:2:2</span></span>           | <span data-ttu-id="46cec-254">Stop</span><span class="sxs-lookup"><span data-stu-id="46cec-254">Packed</span></span>           | <span data-ttu-id="46cec-255">10</span><span class="sxs-lookup"><span data-stu-id="46cec-255">10</span></span>               |
| <span data-ttu-id="46cec-256">Y216</span><span class="sxs-lookup"><span data-stu-id="46cec-256">Y216</span></span>   | <span data-ttu-id="46cec-257">4:2:2</span><span class="sxs-lookup"><span data-stu-id="46cec-257">4:2:2</span></span>           | <span data-ttu-id="46cec-258">Stop</span><span class="sxs-lookup"><span data-stu-id="46cec-258">Packed</span></span>           | <span data-ttu-id="46cec-259">16</span><span class="sxs-lookup"><span data-stu-id="46cec-259">16</span></span>               |
| <span data-ttu-id="46cec-260">P210</span><span class="sxs-lookup"><span data-stu-id="46cec-260">P210</span></span>   | <span data-ttu-id="46cec-261">4:2:2</span><span class="sxs-lookup"><span data-stu-id="46cec-261">4:2:2</span></span>           | <span data-ttu-id="46cec-262">Planare</span><span class="sxs-lookup"><span data-stu-id="46cec-262">Planar</span></span>           | <span data-ttu-id="46cec-263">10</span><span class="sxs-lookup"><span data-stu-id="46cec-263">10</span></span>               |
| <span data-ttu-id="46cec-264">P216</span><span class="sxs-lookup"><span data-stu-id="46cec-264">P216</span></span>   | <span data-ttu-id="46cec-265">4:2:2</span><span class="sxs-lookup"><span data-stu-id="46cec-265">4:2:2</span></span>           | <span data-ttu-id="46cec-266">Planare</span><span class="sxs-lookup"><span data-stu-id="46cec-266">Planar</span></span>           | <span data-ttu-id="46cec-267">16</span><span class="sxs-lookup"><span data-stu-id="46cec-267">16</span></span>               |
| <span data-ttu-id="46cec-268">NV12</span><span class="sxs-lookup"><span data-stu-id="46cec-268">NV12</span></span>   | <span data-ttu-id="46cec-269">4:2:0</span><span class="sxs-lookup"><span data-stu-id="46cec-269">4:2:0</span></span>           | <span data-ttu-id="46cec-270">Planare</span><span class="sxs-lookup"><span data-stu-id="46cec-270">Planar</span></span>           | <span data-ttu-id="46cec-271">8</span><span class="sxs-lookup"><span data-stu-id="46cec-271">8</span></span>                |
| <span data-ttu-id="46cec-272">P010</span><span class="sxs-lookup"><span data-stu-id="46cec-272">P010</span></span>   | <span data-ttu-id="46cec-273">4:2:0</span><span class="sxs-lookup"><span data-stu-id="46cec-273">4:2:0</span></span>           | <span data-ttu-id="46cec-274">Planare</span><span class="sxs-lookup"><span data-stu-id="46cec-274">Planar</span></span>           | <span data-ttu-id="46cec-275">10</span><span class="sxs-lookup"><span data-stu-id="46cec-275">10</span></span>               |
| <span data-ttu-id="46cec-276">P016</span><span class="sxs-lookup"><span data-stu-id="46cec-276">P016</span></span>   | <span data-ttu-id="46cec-277">4:2:0</span><span class="sxs-lookup"><span data-stu-id="46cec-277">4:2:0</span></span>           | <span data-ttu-id="46cec-278">Planare</span><span class="sxs-lookup"><span data-stu-id="46cec-278">Planar</span></span>           | <span data-ttu-id="46cec-279">16</span><span class="sxs-lookup"><span data-stu-id="46cec-279">16</span></span>               |
| <span data-ttu-id="46cec-280">NV11</span><span class="sxs-lookup"><span data-stu-id="46cec-280">NV11</span></span>   | <span data-ttu-id="46cec-281">4:1:1</span><span class="sxs-lookup"><span data-stu-id="46cec-281">4:1:1</span></span>           | <span data-ttu-id="46cec-282">Planare</span><span class="sxs-lookup"><span data-stu-id="46cec-282">Planar</span></span>           | <span data-ttu-id="46cec-283">8</span><span class="sxs-lookup"><span data-stu-id="46cec-283">8</span></span>                |



 

<span data-ttu-id="46cec-284">Es wird empfohlen, dass ein Objekt, das eine bestimmte Bittiefe und ein Chroma-Samplings unterstützt, die entsprechenden YUV-Formate unterstützt, die in dieser Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="46cec-284">It is recommended that if an object supports a given bit depth and chroma sampling scheme, it should support the corresponding YUV formats listed in this table.</span></span> <span data-ttu-id="46cec-285">(Objekte unterstützen möglicherweise zusätzliche Formate, die hier nicht aufgeführt sind.)</span><span class="sxs-lookup"><span data-stu-id="46cec-285">(Objects might support additional formats not listed here.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="46cec-286">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46cec-286">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46cec-287">Empfohlene 8-Bit-YUV-Formate für Video Rendering</span><span class="sxs-lookup"><span data-stu-id="46cec-287">Recommended 8-Bit YUV Formats for Video Rendering</span></span>](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[<span data-ttu-id="46cec-288">Video Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="46cec-288">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> <dt>

[<span data-ttu-id="46cec-289">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="46cec-289">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



