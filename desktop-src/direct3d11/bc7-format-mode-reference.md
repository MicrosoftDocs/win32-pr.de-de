---
title: Bzw bc7-formatmodusverweis
description: Diese Dokumentation enthält eine Liste der 8 Block Modi und bitbelegungen für bzw bc7 Textur Komprimierungs-Format Blöcke.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2020
ms.locfileid: "104389727"
---
# <a name="bc7-format-mode-reference"></a><span data-ttu-id="18a4a-103">Bzw bc7-formatmodusverweis</span><span class="sxs-lookup"><span data-stu-id="18a4a-103">BC7 Format Mode Reference</span></span>

<span data-ttu-id="18a4a-104">Diese Dokumentation enthält eine Liste der 8 Block Modi und bitbelegungen für bzw bc7 Textur Komprimierungs-Format Blöcke.</span><span class="sxs-lookup"><span data-stu-id="18a4a-104">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span>

<span data-ttu-id="18a4a-105">Die Farben für jede Teilmenge innerhalb eines Blocks werden von zwei expliziten Endpunkt Farben und einem Satz interversierter Farben zwischen Ihnen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="18a4a-105">The colors for each subset within a block are represented by two explicit endpoint colors and a set of interpolated colors between them.</span></span> <span data-ttu-id="18a4a-106">Abhängig von der Index Genauigkeit des Blocks kann jede Teilmenge über 4, 8 oder 16 mögliche Farben verfügen.</span><span class="sxs-lookup"><span data-stu-id="18a4a-106">Depending on the block's index precision, each subset can have 4, 8 or 16 possible colors.</span></span>

-   [<span data-ttu-id="18a4a-107">Modus 0</span><span class="sxs-lookup"><span data-stu-id="18a4a-107">Mode 0</span></span>](#mode-0)
-   [<span data-ttu-id="18a4a-108">Modus 1</span><span class="sxs-lookup"><span data-stu-id="18a4a-108">Mode 1</span></span>](#mode-1)
-   [<span data-ttu-id="18a4a-109">Modus 2</span><span class="sxs-lookup"><span data-stu-id="18a4a-109">Mode 2</span></span>](#mode-2)
-   [<span data-ttu-id="18a4a-110">Modus 3</span><span class="sxs-lookup"><span data-stu-id="18a4a-110">Mode 3</span></span>](#mode-3)
-   [<span data-ttu-id="18a4a-111">Modus 4</span><span class="sxs-lookup"><span data-stu-id="18a4a-111">Mode 4</span></span>](#mode-4)
-   [<span data-ttu-id="18a4a-112">Modus 5</span><span class="sxs-lookup"><span data-stu-id="18a4a-112">Mode 5</span></span>](#mode-5)
-   [<span data-ttu-id="18a4a-113">Modus 6</span><span class="sxs-lookup"><span data-stu-id="18a4a-113">Mode 6</span></span>](#mode-6)
-   [<span data-ttu-id="18a4a-114">Modus 7</span><span class="sxs-lookup"><span data-stu-id="18a4a-114">Mode 7</span></span>](#mode-7)
-   [<span data-ttu-id="18a4a-115">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="18a4a-115">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="18a4a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18a4a-116">Related topics</span></span>](#related-topics)

## <a name="mode-0"></a><span data-ttu-id="18a4a-117">Modus 0</span><span class="sxs-lookup"><span data-stu-id="18a4a-117">Mode 0</span></span>

<span data-ttu-id="18a4a-118">Bzw bc7 Mode 0 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-118">BC7 Mode 0 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-119">Nur Farbkomponenten (kein Alpha)</span><span class="sxs-lookup"><span data-stu-id="18a4a-119">Color components only (no alpha)</span></span>
-   <span data-ttu-id="18a4a-120">3 Teilmengen pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-120">3 subsets per block</span></span>
-   <span data-ttu-id="18a4a-121">Rgbp 4.4.4.1 Endpunkte mit einem eindeutigen P-Bit pro Endpunkt</span><span class="sxs-lookup"><span data-stu-id="18a4a-121">RGBP 4.4.4.1 endpoints with a unique P-bit per endpoint</span></span>
-   <span data-ttu-id="18a4a-122">3-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-122">3-bit indices</span></span>
-   <span data-ttu-id="18a4a-123">16 Partitionen</span><span class="sxs-lookup"><span data-stu-id="18a4a-123">16 partitions</span></span>

![Mode 0-bitlayout](images/bc7-mode0.png)

## <a name="mode-1"></a><span data-ttu-id="18a4a-125">Modus 1</span><span class="sxs-lookup"><span data-stu-id="18a4a-125">Mode 1</span></span>

<span data-ttu-id="18a4a-126">Bzw bc7 Mode 1 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-126">BC7 Mode 1 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-127">Nur Farbkomponenten (kein Alpha)</span><span class="sxs-lookup"><span data-stu-id="18a4a-127">Color components only (no alpha)</span></span>
-   <span data-ttu-id="18a4a-128">2 Teilmengen pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-128">2 subsets per block</span></span>
-   <span data-ttu-id="18a4a-129">Rgbp 6.6.6.1-Endpunkte mit einem freigegebenen P-Bit pro Teilmenge)</span><span class="sxs-lookup"><span data-stu-id="18a4a-129">RGBP 6.6.6.1 endpoints with a shared P-bit per subset)</span></span>
-   <span data-ttu-id="18a4a-130">3-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-130">3-bit indices</span></span>
-   <span data-ttu-id="18a4a-131">64 Partitionen</span><span class="sxs-lookup"><span data-stu-id="18a4a-131">64 partitions</span></span>

![Mode-1-Bit-Layout](images/bc7-mode1.png)

## <a name="mode-2"></a><span data-ttu-id="18a4a-133">Modus 2</span><span class="sxs-lookup"><span data-stu-id="18a4a-133">Mode 2</span></span>

<span data-ttu-id="18a4a-134">Bzw bc7 Mode 2 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-134">BC7 Mode 2 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-135">Nur Farbkomponenten (kein Alpha)</span><span class="sxs-lookup"><span data-stu-id="18a4a-135">Color components only (no alpha)</span></span>
-   <span data-ttu-id="18a4a-136">3 Teilmengen pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-136">3 subsets per block</span></span>
-   <span data-ttu-id="18a4a-137">RGB 5.5.5 Endpunkte</span><span class="sxs-lookup"><span data-stu-id="18a4a-137">RGB 5.5.5 endpoints</span></span>
-   <span data-ttu-id="18a4a-138">2-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-138">2-bit indices</span></span>
-   <span data-ttu-id="18a4a-139">64 Partitionen</span><span class="sxs-lookup"><span data-stu-id="18a4a-139">64 partitions</span></span>

![Modus 2 Bit Layout](images/bc7-mode2.png)

## <a name="mode-3"></a><span data-ttu-id="18a4a-141">Modus 3</span><span class="sxs-lookup"><span data-stu-id="18a4a-141">Mode 3</span></span>

<span data-ttu-id="18a4a-142">Bzw bc7 Mode 3 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-142">BC7 Mode 3 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-143">Nur Farbkomponenten (kein Alpha)</span><span class="sxs-lookup"><span data-stu-id="18a4a-143">Color components only (no alpha)</span></span>
-   <span data-ttu-id="18a4a-144">2 Teilmengen pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-144">2 subsets per block</span></span>
-   <span data-ttu-id="18a4a-145">Rgbp 7.7.7.1-Endpunkte mit einem eindeutigen P-Bit pro Teilmenge)</span><span class="sxs-lookup"><span data-stu-id="18a4a-145">RGBP 7.7.7.1 endpoints with a unique P-bit per subset)</span></span>
-   <span data-ttu-id="18a4a-146">2-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-146">2-bit indices</span></span>
-   <span data-ttu-id="18a4a-147">64 Partitionen</span><span class="sxs-lookup"><span data-stu-id="18a4a-147">64 partitions</span></span>

![Modus 3 Bit Layout](images/bc7-mode3.png)

## <a name="mode-4"></a><span data-ttu-id="18a4a-149">Modus 4</span><span class="sxs-lookup"><span data-stu-id="18a4a-149">Mode 4</span></span>

<span data-ttu-id="18a4a-150">Bzw bc7 Mode 4 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-150">BC7 Mode 4 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-151">Farbkomponenten mit separater Alpha Komponente</span><span class="sxs-lookup"><span data-stu-id="18a4a-151">Color components with separate alpha component</span></span>
-   <span data-ttu-id="18a4a-152">1 Teilmenge pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-152">1 subset per block</span></span>
-   <span data-ttu-id="18a4a-153">RGB 5.5.5 Farb Endpunkte</span><span class="sxs-lookup"><span data-stu-id="18a4a-153">RGB 5.5.5 color endpoints</span></span>
-   <span data-ttu-id="18a4a-154">6-Bit-Alpha-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="18a4a-154">6-bit alpha endpoints</span></span>
-   <span data-ttu-id="18a4a-155">16 x 2-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-155">16 x 2-bit indices</span></span>
-   <span data-ttu-id="18a4a-156">16 x 3-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-156">16 x 3-bit indices</span></span>
-   <span data-ttu-id="18a4a-157">2-Bit-Komponenten Drehung</span><span class="sxs-lookup"><span data-stu-id="18a4a-157">2-bit component rotation</span></span>
-   <span data-ttu-id="18a4a-158">1-Bit-indexselektor (unabhängig davon, ob die Indizes mit 2 oder 3 Bit verwendet werden)</span><span class="sxs-lookup"><span data-stu-id="18a4a-158">1-bit index selector (whether the 2- or 3-bit indices are used)</span></span>

![Modus 4 Bit Layout](images/bc7-mode4.png)

## <a name="mode-5"></a><span data-ttu-id="18a4a-160">Modus 5</span><span class="sxs-lookup"><span data-stu-id="18a4a-160">Mode 5</span></span>

<span data-ttu-id="18a4a-161">Bzw bc7 Mode 5 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-161">BC7 Mode 5 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-162">Farbkomponenten mit separater Alpha Komponente</span><span class="sxs-lookup"><span data-stu-id="18a4a-162">Color components with separate alpha component</span></span>
-   <span data-ttu-id="18a4a-163">1 Teilmenge pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-163">1 subset per block</span></span>
-   <span data-ttu-id="18a4a-164">RGB 7.7.7 Farb Endpunkte</span><span class="sxs-lookup"><span data-stu-id="18a4a-164">RGB 7.7.7 color endpoints</span></span>
-   <span data-ttu-id="18a4a-165">8-Bit-Alpha-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="18a4a-165">8-bit alpha endpoints</span></span>
-   <span data-ttu-id="18a4a-166">16 x 2-Bit-Farbindizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-166">16 x 2-bit color indices</span></span>
-   <span data-ttu-id="18a4a-167">16 x 2-Bit-Alpha Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-167">16 x 2-bit alpha indices</span></span>
-   <span data-ttu-id="18a4a-168">2-Bit-Komponenten Drehung</span><span class="sxs-lookup"><span data-stu-id="18a4a-168">2-bit component rotation</span></span>

![Layout des 5-Bit-Modus](images/bc7-mode5.png)

## <a name="mode-6"></a><span data-ttu-id="18a4a-170">Modus 6</span><span class="sxs-lookup"><span data-stu-id="18a4a-170">Mode 6</span></span>

<span data-ttu-id="18a4a-171">Bzw bc7 Mode 6 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-171">BC7 Mode 6 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-172">Kombinierte Farbe und Alpha Komponenten</span><span class="sxs-lookup"><span data-stu-id="18a4a-172">Combined color and alpha components</span></span>
-   <span data-ttu-id="18a4a-173">Eine Teilmenge pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-173">One subset per block</span></span>
-   <span data-ttu-id="18a4a-174">Rgbap 7.7.7.7.1 Farbe (und Alpha) Endpunkte (eindeutiges P-Bit pro Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="18a4a-174">RGBAP 7.7.7.7.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="18a4a-175">16 x 4-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-175">16 x 4-bit indices</span></span>

![Modus 6 Bit Layout](images/bc7-mode6.png)

## <a name="mode-7"></a><span data-ttu-id="18a4a-177">Modus 7</span><span class="sxs-lookup"><span data-stu-id="18a4a-177">Mode 7</span></span>

<span data-ttu-id="18a4a-178">Bzw bc7 Mode 7 weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="18a4a-178">BC7 Mode 7 has the following characteristics:</span></span>

-   <span data-ttu-id="18a4a-179">Kombinierte Farbe und Alpha Komponenten</span><span class="sxs-lookup"><span data-stu-id="18a4a-179">Combined color and alpha components</span></span>
-   <span data-ttu-id="18a4a-180">2 Teilmengen pro Block</span><span class="sxs-lookup"><span data-stu-id="18a4a-180">2 subsets per block</span></span>
-   <span data-ttu-id="18a4a-181">Rgbap 5.5.5.5.1 Farbe (und Alpha) Endpunkte (eindeutiges P-Bit pro Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="18a4a-181">RGBAP 5.5.5.5.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="18a4a-182">2-Bit-Indizes</span><span class="sxs-lookup"><span data-stu-id="18a4a-182">2-bit indices</span></span>
-   <span data-ttu-id="18a4a-183">64 Partitionen</span><span class="sxs-lookup"><span data-stu-id="18a4a-183">64 partitions</span></span>

![Modus 7 Bit Layout](images/bc7-mode7.png)

## <a name="remarks"></a><span data-ttu-id="18a4a-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18a4a-185">Remarks</span></span>

<span data-ttu-id="18a4a-186">Modus 8 (das am wenigsten signifikante Byte ist auf 0x00 festgelegt) ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="18a4a-186">Mode 8 (the least significant byte is set to 0x00) is reserved.</span></span> <span data-ttu-id="18a4a-187">Verwenden Sie Sie nicht in Ihrem Encoder.</span><span class="sxs-lookup"><span data-stu-id="18a4a-187">Don't use it in your encoder.</span></span> <span data-ttu-id="18a4a-188">Wenn Sie diesen Modus an die Hardware übergeben, wird ein Block zurückgegeben, der mit allen Nullen initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="18a4a-188">If you pass this mode to the hardware, a block initialized to all zeroes is returned.</span></span>

<span data-ttu-id="18a4a-189">In bzw bc7 können Sie die Alpha Komponente auf eine der folgenden Arten codieren:</span><span class="sxs-lookup"><span data-stu-id="18a4a-189">In BC7, you can encode the alpha component in one of the following ways:</span></span>

-   <span data-ttu-id="18a4a-190">Block Typen ohne explizite Alpha Komponenten Codierung.</span><span class="sxs-lookup"><span data-stu-id="18a4a-190">Block types without explicit alpha component encoding.</span></span> <span data-ttu-id="18a4a-191">In diesen Blöcken haben die Farb Endpunkte eine nur-RGB-Codierung, wobei die Alpha Komponente für alle Texels in 1,0 decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="18a4a-191">In these blocks, the color endpoints have an RGB-only encoding, with the alpha component decoded to 1.0 for all texels.</span></span>
-   <span data-ttu-id="18a4a-192">Block Typen mit kombinierten Farben und Alpha Komponenten.</span><span class="sxs-lookup"><span data-stu-id="18a4a-192">Block types with combined color and alpha components.</span></span> <span data-ttu-id="18a4a-193">In diesen Blöcken werden die endpunktfarbwerte im RGBA-Format angegeben, und die Alpha Komponenten Werte werden zusammen mit den Farbwerten interpoliert.</span><span class="sxs-lookup"><span data-stu-id="18a4a-193">In these blocks, the endpoint color values are specified in the RGBA format, and the alpha component values are interpolated along with the color values.</span></span>
-   <span data-ttu-id="18a4a-194">Block Typen mit getrennten Farben und Alpha Komponenten.</span><span class="sxs-lookup"><span data-stu-id="18a4a-194">Block types with separated color and alpha components.</span></span> <span data-ttu-id="18a4a-195">In diesen Blöcken werden die Werte für Farbe und Alpha separat angegeben, jeweils mit einem eigenen Satz von Indizes.</span><span class="sxs-lookup"><span data-stu-id="18a4a-195">In these blocks the color and alpha values are specified separately, each with their own set of indices.</span></span> <span data-ttu-id="18a4a-196">Demzufolge verfügen Sie über einen effektiven Vektor und einen skalarchannel, der separat codiert ist, wobei der Vektor häufig die Farbkanäle \[ R, G \] und B angibt und der Skalar den Alphakanal \[ a angibt \] .</span><span class="sxs-lookup"><span data-stu-id="18a4a-196">As a result, they have an effective vector and a scalar channel separately encoded, where the vector commonly specifies the color channels \[R, G, B\] and the scalar specifies the alpha channel \[A\].</span></span> <span data-ttu-id="18a4a-197">Zur Unterstützung dieses Ansatzes wird in der Codierung ein separates 2-Bit-Feld bereitgestellt, das die Angabe der separaten Kanalcodierung als Skalarwert ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="18a4a-197">To support this approach, a separate 2-bit field is provided in the encoding, which permits the specification of the separate channel encoding as a scalar value.</span></span> <span data-ttu-id="18a4a-198">Folglich kann der-Block eine der folgenden vier unterschiedlichen Darstellungen dieser Alpha Codierung aufweisen (wie durch das 2-Bit-Feld angegeben):</span><span class="sxs-lookup"><span data-stu-id="18a4a-198">As a result, the block can have one of the following four different representations of this alpha encoding (as indicated by the 2-bit field):</span></span>
    -   <span data-ttu-id="18a4a-199">RGB \| A: separater Alphakanal</span><span class="sxs-lookup"><span data-stu-id="18a4a-199">RGB\|A: alpha channel separate</span></span>
    -   <span data-ttu-id="18a4a-200">AGB \| R: "Roter" Farbkanal getrennt</span><span class="sxs-lookup"><span data-stu-id="18a4a-200">AGB\|R: "red" color channel separate</span></span>
    -   <span data-ttu-id="18a4a-201">Rab \| G: "grüner" Farbkanal getrennt</span><span class="sxs-lookup"><span data-stu-id="18a4a-201">RAB\|G: "green" color channel separate</span></span>
    -   <span data-ttu-id="18a4a-202">RGA \| B: "blauer" Farbkanal getrennt</span><span class="sxs-lookup"><span data-stu-id="18a4a-202">RGA\|B: "blue" color channel separate</span></span>

    <span data-ttu-id="18a4a-203">Der Decoder ordnet die Kanal Reihenfolge nach der Decodierung an RGBA zurück, sodass das interne Block Format für den Entwickler unsichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="18a4a-203">The decoder reorders the channel order back to RGBA after decoding, so the internal block format is invisible to the developer.</span></span> <span data-ttu-id="18a4a-204">Schwarze mit separaten Farb-und Alpha Komponenten verfügen auch über zwei Sätze von Indexdaten: einen für den Vektor Satz von Kanälen und einen für den skalaren Kanal.</span><span class="sxs-lookup"><span data-stu-id="18a4a-204">Blacks with separate color and alpha components also have two sets of index data: one for the vectored set of channels, and one for the scalar channel.</span></span> <span data-ttu-id="18a4a-205">(Im Fall von Modus 4 haben diese Indizes eine abweichende Breite von \[ 2 oder 3 Bits \] .</span><span class="sxs-lookup"><span data-stu-id="18a4a-205">(In the case of Mode 4, these indices are of differing widths \[2 or 3 bits\].</span></span> <span data-ttu-id="18a4a-206">In Modus 4 ist auch ein 1-Bit-Selektor enthalten, der angibt, ob der Vektor oder der skalare Kanal die 3-Bit-Indizes verwendet.)</span><span class="sxs-lookup"><span data-stu-id="18a4a-206">Mode 4 also contains a 1-bit selector that specifies whether the vector or the scalar channel uses the 3-bit indices.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="18a4a-207">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18a4a-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18a4a-208">Bzw bc7-Format</span><span class="sxs-lookup"><span data-stu-id="18a4a-208">BC7 Format</span></span>](bc7-format.md)
</dt> </dl>

 

 




