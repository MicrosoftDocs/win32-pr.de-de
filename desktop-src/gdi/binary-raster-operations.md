---
description: In diesem Abschnitt werden die binären Raster Vorgangs Codes aufgelistet, die von den GetROP2-und SetROP2-Funktionen verwendet werden. Raster-Vorgangs Codes definieren, wie GDI die Bits aus dem ausgewählten Stift mit den Bits in der Ziel Bitmap kombiniert.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Binäre Raster Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130856"
---
# <a name="binary-raster-operations"></a><span data-ttu-id="20464-104">Binäre Raster Vorgänge</span><span class="sxs-lookup"><span data-stu-id="20464-104">Binary Raster Operations</span></span>

<span data-ttu-id="20464-105">In diesem Abschnitt werden die binären Raster Vorgangs Codes aufgelistet, die von den [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) -und [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) -Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20464-105">This section lists the binary raster-operation codes used by the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) and [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) functions.</span></span> <span data-ttu-id="20464-106">Raster-Vorgangs Codes definieren, wie GDI die Bits aus dem ausgewählten Stift mit den Bits in der Ziel Bitmap kombiniert.</span><span class="sxs-lookup"><span data-stu-id="20464-106">Raster-operation codes define how GDI combines the bits from the selected pen with the bits in the destination bitmap.</span></span>

<span data-ttu-id="20464-107">Jeder Raster Vorgangs Code stellt einen booleschen Vorgang dar, in dem die Werte der Pixel im ausgewählten Stift und die Ziel Bitmap kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="20464-107">Each raster-operation code represents a Boolean operation in which the values of the pixels in the selected pen and the destination bitmap are combined.</span></span> <span data-ttu-id="20464-108">Die folgenden beiden Operanden werden in diesen Vorgängen verwendet.</span><span class="sxs-lookup"><span data-stu-id="20464-108">The following are the two operands used in these operations.</span></span>



| <span data-ttu-id="20464-109">Operand</span><span class="sxs-lookup"><span data-stu-id="20464-109">Operand</span></span> | <span data-ttu-id="20464-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="20464-110">Meaning</span></span>            |
|---------|--------------------|
| <span data-ttu-id="20464-111">P</span><span class="sxs-lookup"><span data-stu-id="20464-111">P</span></span>       | <span data-ttu-id="20464-112">Ausgewählter Stift</span><span class="sxs-lookup"><span data-stu-id="20464-112">Selected pen</span></span>       |
| <span data-ttu-id="20464-113">D</span><span class="sxs-lookup"><span data-stu-id="20464-113">D</span></span>       | <span data-ttu-id="20464-114">Ziel Bitmap</span><span class="sxs-lookup"><span data-stu-id="20464-114">Destination bitmap</span></span> |



 

<span data-ttu-id="20464-115">Die in diesen Vorgängen verwendeten booleschen Operatoren folgen.</span><span class="sxs-lookup"><span data-stu-id="20464-115">The Boolean operators used in these operations follow.</span></span>



| <span data-ttu-id="20464-116">Operator</span><span class="sxs-lookup"><span data-stu-id="20464-116">Operator</span></span> | <span data-ttu-id="20464-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="20464-117">Meaning</span></span>                    |
|----------|----------------------------|
| <span data-ttu-id="20464-118">a</span><span class="sxs-lookup"><span data-stu-id="20464-118">a</span></span>        | <span data-ttu-id="20464-119">Bitweises AND</span><span class="sxs-lookup"><span data-stu-id="20464-119">Bitwise AND</span></span>                |
| <span data-ttu-id="20464-120">n</span><span class="sxs-lookup"><span data-stu-id="20464-120">n</span></span>        | <span data-ttu-id="20464-121">Bitweises NOT (inversen)</span><span class="sxs-lookup"><span data-stu-id="20464-121">Bitwise NOT (inverse)</span></span>      |
| <span data-ttu-id="20464-122">o</span><span class="sxs-lookup"><span data-stu-id="20464-122">o</span></span>        | <span data-ttu-id="20464-123">Bitweises OR</span><span class="sxs-lookup"><span data-stu-id="20464-123">Bitwise OR</span></span>                 |
| <span data-ttu-id="20464-124">x</span><span class="sxs-lookup"><span data-stu-id="20464-124">x</span></span>        | <span data-ttu-id="20464-125">Bitweises exklusives OR (XOR)</span><span class="sxs-lookup"><span data-stu-id="20464-125">Bitwise exclusive OR (XOR)</span></span> |



 

<span data-ttu-id="20464-126">Alle booleschen Vorgänge werden in umgekehrter polnischer Schreibweise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="20464-126">All Boolean operations are presented in reverse Polish notation.</span></span> <span data-ttu-id="20464-127">Der folgende Vorgang ersetzt z. b. die Werte der Pixel in der Ziel Bitmap durch eine Kombination der Pixelwerte des Stifts und des ausgewählten Pinsels:</span><span class="sxs-lookup"><span data-stu-id="20464-127">For example, the following operation replaces the values of the pixels in the destination bitmap with a combination of the pixel values of the pen and the selected brush:</span></span>


```C++
DPo 
```



<span data-ttu-id="20464-128">Jeder Raster Vorgangs Code ist eine 32-Bit-Ganzzahl, deren hohes Wort ein boolescher Vorgangs Index ist und dessen niedriges Wort der Vorgangs Code ist.</span><span class="sxs-lookup"><span data-stu-id="20464-128">Each raster-operation code is a 32-bit integer whose high-order word is a Boolean operation index and whose low-order word is the operation code.</span></span> <span data-ttu-id="20464-129">Bei dem 16-Bit-Vorgangs Index handelt es sich um einen 8-Bit-Wert mit 0 (null), der alle möglichen Ergebnisse darstellt, die sich aus der booleschen Operation für zwei Parameter ergeben (in diesem Fall der Stift-und Zielwert).</span><span class="sxs-lookup"><span data-stu-id="20464-129">The 16-bit operation index is a zero-extended 8-bit value that represents all possible outcomes resulting from the Boolean operation on two parameters (in this case, the pen and destination values).</span></span> <span data-ttu-id="20464-130">Die Vorgangs Indizes für die DPO-und DPAN-Vorgänge werden z. b. in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20464-130">For example, the operation indexes for the DPo and DPan operations are shown in the following list.</span></span>



| <span data-ttu-id="20464-131">P</span><span class="sxs-lookup"><span data-stu-id="20464-131">P</span></span>   | <span data-ttu-id="20464-132">D</span><span class="sxs-lookup"><span data-stu-id="20464-132">D</span></span>   | <span data-ttu-id="20464-133">DPO</span><span class="sxs-lookup"><span data-stu-id="20464-133">DPo</span></span> | <span data-ttu-id="20464-134">DPAN</span><span class="sxs-lookup"><span data-stu-id="20464-134">Dpan</span></span> |
|-----|-----|-----|------|
| <span data-ttu-id="20464-135">0</span><span class="sxs-lookup"><span data-stu-id="20464-135">0</span></span>   | <span data-ttu-id="20464-136">0</span><span class="sxs-lookup"><span data-stu-id="20464-136">0</span></span>   | <span data-ttu-id="20464-137">0</span><span class="sxs-lookup"><span data-stu-id="20464-137">0</span></span>   | <span data-ttu-id="20464-138">1</span><span class="sxs-lookup"><span data-stu-id="20464-138">1</span></span>    |
| <span data-ttu-id="20464-139">0</span><span class="sxs-lookup"><span data-stu-id="20464-139">0</span></span>   | <span data-ttu-id="20464-140">1</span><span class="sxs-lookup"><span data-stu-id="20464-140">1</span></span>   | <span data-ttu-id="20464-141">1</span><span class="sxs-lookup"><span data-stu-id="20464-141">1</span></span>   | <span data-ttu-id="20464-142">1</span><span class="sxs-lookup"><span data-stu-id="20464-142">1</span></span>    |
| <span data-ttu-id="20464-143">1</span><span class="sxs-lookup"><span data-stu-id="20464-143">1</span></span>   | <span data-ttu-id="20464-144">0</span><span class="sxs-lookup"><span data-stu-id="20464-144">0</span></span>   | <span data-ttu-id="20464-145">1</span><span class="sxs-lookup"><span data-stu-id="20464-145">1</span></span>   | <span data-ttu-id="20464-146">1</span><span class="sxs-lookup"><span data-stu-id="20464-146">1</span></span>    |
| <span data-ttu-id="20464-147">1</span><span class="sxs-lookup"><span data-stu-id="20464-147">1</span></span>   | <span data-ttu-id="20464-148">1</span><span class="sxs-lookup"><span data-stu-id="20464-148">1</span></span>   | <span data-ttu-id="20464-149">1</span><span class="sxs-lookup"><span data-stu-id="20464-149">1</span></span>   | <span data-ttu-id="20464-150">0</span><span class="sxs-lookup"><span data-stu-id="20464-150">0</span></span>    |



 

<span data-ttu-id="20464-151">In der folgenden Liste werden die Zeichnungs Modi und die booleschen Operationen beschrieben, die Sie darstellen.</span><span class="sxs-lookup"><span data-stu-id="20464-151">The following list outlines the drawing modes and the Boolean operations that they represent.</span></span>



| <span data-ttu-id="20464-152">Raster Vorgang</span><span class="sxs-lookup"><span data-stu-id="20464-152">Raster operation</span></span> | <span data-ttu-id="20464-153">Boolescher Vorgang</span><span class="sxs-lookup"><span data-stu-id="20464-153">Boolean operation</span></span> |
|------------------|-------------------|
| <span data-ttu-id="20464-154">R2 \_ schwarz</span><span class="sxs-lookup"><span data-stu-id="20464-154">R2\_BLACK</span></span>        | <span data-ttu-id="20464-155">0</span><span class="sxs-lookup"><span data-stu-id="20464-155">0</span></span>                 |
| <span data-ttu-id="20464-156">R2- \_ CopyPen</span><span class="sxs-lookup"><span data-stu-id="20464-156">R2\_COPYPEN</span></span>      | <span data-ttu-id="20464-157">P</span><span class="sxs-lookup"><span data-stu-id="20464-157">P</span></span>                 |
| <span data-ttu-id="20464-158">R2 \_ masklotpen</span><span class="sxs-lookup"><span data-stu-id="20464-158">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="20464-159">DPNA</span><span class="sxs-lookup"><span data-stu-id="20464-159">DPna</span></span>              |
| <span data-ttu-id="20464-160">R2- \_ MaskPen</span><span class="sxs-lookup"><span data-stu-id="20464-160">R2\_MASKPEN</span></span>      | <span data-ttu-id="20464-161">DPa</span><span class="sxs-lookup"><span data-stu-id="20464-161">DPa</span></span>               |
| <span data-ttu-id="20464-162">R2 \_ maskpnot</span><span class="sxs-lookup"><span data-stu-id="20464-162">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="20464-163">Pdna</span><span class="sxs-lookup"><span data-stu-id="20464-163">PDna</span></span>              |
| <span data-ttu-id="20464-164">R2 \_ mergenotpen</span><span class="sxs-lookup"><span data-stu-id="20464-164">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="20464-165">Dpno</span><span class="sxs-lookup"><span data-stu-id="20464-165">DPno</span></span>              |
| <span data-ttu-id="20464-166">R2- \_ MergePen</span><span class="sxs-lookup"><span data-stu-id="20464-166">R2\_MERGEPEN</span></span>     | <span data-ttu-id="20464-167">DPO</span><span class="sxs-lookup"><span data-stu-id="20464-167">DPo</span></span>               |
| <span data-ttu-id="20464-168">R2 \_ mergepnot</span><span class="sxs-lookup"><span data-stu-id="20464-168">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="20464-169">Pdno</span><span class="sxs-lookup"><span data-stu-id="20464-169">PDno</span></span>              |
| <span data-ttu-id="20464-170">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="20464-170">R2\_NOP</span></span>          | <span data-ttu-id="20464-171">D</span><span class="sxs-lookup"><span data-stu-id="20464-171">D</span></span>                 |
| <span data-ttu-id="20464-172">R2 \_ nicht</span><span class="sxs-lookup"><span data-stu-id="20464-172">R2\_NOT</span></span>          | <span data-ttu-id="20464-173">Dn</span><span class="sxs-lookup"><span data-stu-id="20464-173">Dn</span></span>                |
| <span data-ttu-id="20464-174">R2- \_ notcopypen</span><span class="sxs-lookup"><span data-stu-id="20464-174">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="20464-175">PN</span><span class="sxs-lookup"><span data-stu-id="20464-175">Pn</span></span>                |
| <span data-ttu-id="20464-176">R2 \_ notmaskpen</span><span class="sxs-lookup"><span data-stu-id="20464-176">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="20464-177">DPAN</span><span class="sxs-lookup"><span data-stu-id="20464-177">DPan</span></span>              |
| <span data-ttu-id="20464-178">R2 \_ NotMergePen</span><span class="sxs-lookup"><span data-stu-id="20464-178">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="20464-179">Dpon</span><span class="sxs-lookup"><span data-stu-id="20464-179">DPon</span></span>              |
| <span data-ttu-id="20464-180">R2- \_ NotXorPen</span><span class="sxs-lookup"><span data-stu-id="20464-180">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="20464-181">Dpxn</span><span class="sxs-lookup"><span data-stu-id="20464-181">DPxn</span></span>              |
| <span data-ttu-id="20464-182">R2 \_ weiß</span><span class="sxs-lookup"><span data-stu-id="20464-182">R2\_WHITE</span></span>        | <span data-ttu-id="20464-183">1</span><span class="sxs-lookup"><span data-stu-id="20464-183">1</span></span>                 |
| <span data-ttu-id="20464-184">R2- \_ XOrPen</span><span class="sxs-lookup"><span data-stu-id="20464-184">R2\_XORPEN</span></span>       | <span data-ttu-id="20464-185">DPX</span><span class="sxs-lookup"><span data-stu-id="20464-185">DPx</span></span>               |



 

<span data-ttu-id="20464-186">Bei einem monochrome Gerät ordnet GDI den Wert 0 (null) und den Wert 1 weiß zu.</span><span class="sxs-lookup"><span data-stu-id="20464-186">For a monochrome device, GDI maps the value zero to black and the value 1 to white.</span></span> <span data-ttu-id="20464-187">Wenn eine Anwendung versucht, mit einem schwarzen Stift auf einem weißen Ziel mithilfe der verfügbaren binären Raster Vorgänge zu zeichnen, treten die folgenden Ergebnisse auf.</span><span class="sxs-lookup"><span data-stu-id="20464-187">If an application attempts to draw with a black pen on a white destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="20464-188">Raster Vorgang</span><span class="sxs-lookup"><span data-stu-id="20464-188">Raster operation</span></span> | <span data-ttu-id="20464-189">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="20464-189">Result</span></span>             |
|------------------|--------------------|
| <span data-ttu-id="20464-190">R2 \_ schwarz</span><span class="sxs-lookup"><span data-stu-id="20464-190">R2\_BLACK</span></span>        | <span data-ttu-id="20464-191">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-191">Visible black line</span></span> |
| <span data-ttu-id="20464-192">R2- \_ CopyPen</span><span class="sxs-lookup"><span data-stu-id="20464-192">R2\_COPYPEN</span></span>      | <span data-ttu-id="20464-193">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-193">Visible black line</span></span> |
| <span data-ttu-id="20464-194">R2 \_ masklotpen</span><span class="sxs-lookup"><span data-stu-id="20464-194">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="20464-195">Keine sichtbare Zeile</span><span class="sxs-lookup"><span data-stu-id="20464-195">No visible line</span></span>    |
| <span data-ttu-id="20464-196">R2- \_ MaskPen</span><span class="sxs-lookup"><span data-stu-id="20464-196">R2\_MASKPEN</span></span>      | <span data-ttu-id="20464-197">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-197">Visible black line</span></span> |
| <span data-ttu-id="20464-198">R2 \_ maskpnot</span><span class="sxs-lookup"><span data-stu-id="20464-198">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="20464-199">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-199">Visible black line</span></span> |
| <span data-ttu-id="20464-200">R2 \_ mergenotpen</span><span class="sxs-lookup"><span data-stu-id="20464-200">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="20464-201">Keine sichtbare Zeile</span><span class="sxs-lookup"><span data-stu-id="20464-201">No visible line</span></span>    |
| <span data-ttu-id="20464-202">R2- \_ MergePen</span><span class="sxs-lookup"><span data-stu-id="20464-202">R2\_MERGEPEN</span></span>     | <span data-ttu-id="20464-203">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-203">Visible black line</span></span> |
| <span data-ttu-id="20464-204">R2 \_ mergepnot</span><span class="sxs-lookup"><span data-stu-id="20464-204">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="20464-205">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-205">Visible black line</span></span> |
| <span data-ttu-id="20464-206">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="20464-206">R2\_NOP</span></span>          | <span data-ttu-id="20464-207">Keine sichtbare Zeile</span><span class="sxs-lookup"><span data-stu-id="20464-207">No visible line</span></span>    |
| <span data-ttu-id="20464-208">R2 \_ nicht</span><span class="sxs-lookup"><span data-stu-id="20464-208">R2\_NOT</span></span>          | <span data-ttu-id="20464-209">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-209">Visible black line</span></span> |
| <span data-ttu-id="20464-210">R2- \_ notcopypen</span><span class="sxs-lookup"><span data-stu-id="20464-210">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="20464-211">Keine sichtbare Zeile</span><span class="sxs-lookup"><span data-stu-id="20464-211">No visible line</span></span>    |
| <span data-ttu-id="20464-212">R2 \_ notmaskpen</span><span class="sxs-lookup"><span data-stu-id="20464-212">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="20464-213">Keine sichtbare Zeile</span><span class="sxs-lookup"><span data-stu-id="20464-213">No visible line</span></span>    |
| <span data-ttu-id="20464-214">R2 \_ NotMergePen</span><span class="sxs-lookup"><span data-stu-id="20464-214">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="20464-215">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-215">Visible black line</span></span> |
| <span data-ttu-id="20464-216">R2- \_ NotXorPen</span><span class="sxs-lookup"><span data-stu-id="20464-216">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="20464-217">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-217">Visible black line</span></span> |
| <span data-ttu-id="20464-218">R2 \_ weiß</span><span class="sxs-lookup"><span data-stu-id="20464-218">R2\_WHITE</span></span>        | <span data-ttu-id="20464-219">Keine sichtbare Zeile</span><span class="sxs-lookup"><span data-stu-id="20464-219">No visible line</span></span>    |
| <span data-ttu-id="20464-220">R2- \_ XOrPen</span><span class="sxs-lookup"><span data-stu-id="20464-220">R2\_XORPEN</span></span>       | <span data-ttu-id="20464-221">Keine sichtbare Zeile</span><span class="sxs-lookup"><span data-stu-id="20464-221">No visible line</span></span>    |



 

<span data-ttu-id="20464-222">Bei einem Farbgerät verwendet GDI RGB-Werte, um die Farben des Stifts und des Ziels darzustellen.</span><span class="sxs-lookup"><span data-stu-id="20464-222">For a color device, GDI uses RGB values to represent the colors of the pen and the destination.</span></span> <span data-ttu-id="20464-223">Ein RGB-Farbwert ist eine lange ganze Zahl, die ein rotes, grünes und blaues Farbfeld enthält, das jeweils die Intensität der angegebenen Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="20464-223">An RGB color value is a long integer that contains a red, a green, and a blue color field, each specifying the intensity of the specified color.</span></span> <span data-ttu-id="20464-224">Die Intensitäten liegen zwischen 0 und 255.</span><span class="sxs-lookup"><span data-stu-id="20464-224">Intensities range from 0 through 255.</span></span> <span data-ttu-id="20464-225">Die Werte werden in die drei nieder wertigen Bytes der Long-Ganzzahl gepackt.</span><span class="sxs-lookup"><span data-stu-id="20464-225">The values are packed in the three low-order bytes of the long integer.</span></span> <span data-ttu-id="20464-226">Die Farbe eines Stifts ist immer eine voll Tonfarbe, aber die Farbe des Ziels kann eine Mischung aus zwei oder drei Farben sein.</span><span class="sxs-lookup"><span data-stu-id="20464-226">The color of a pen is always a solid color, but the color of the destination may be a mixture of any two or three colors.</span></span> <span data-ttu-id="20464-227">Wenn eine Anwendung versucht, mit einem weißen Stift auf einem blauen Ziel mithilfe der verfügbaren binären Raster Vorgänge zu zeichnen, treten die folgenden Ergebnisse auf.</span><span class="sxs-lookup"><span data-stu-id="20464-227">If an application attempts to draw with a white pen on a blue destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="20464-228">Raster Vorgang</span><span class="sxs-lookup"><span data-stu-id="20464-228">Raster operation</span></span> | <span data-ttu-id="20464-229">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="20464-229">Result</span></span>                 |
|------------------|------------------------|
| <span data-ttu-id="20464-230">R2 \_ schwarz</span><span class="sxs-lookup"><span data-stu-id="20464-230">R2\_BLACK</span></span>        | <span data-ttu-id="20464-231">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-231">Visible black line</span></span>     |
| <span data-ttu-id="20464-232">R2- \_ CopyPen</span><span class="sxs-lookup"><span data-stu-id="20464-232">R2\_COPYPEN</span></span>      | <span data-ttu-id="20464-233">Sichtbare weiße Linie</span><span class="sxs-lookup"><span data-stu-id="20464-233">Visible white line</span></span>     |
| <span data-ttu-id="20464-234">R2 \_ masklotpen</span><span class="sxs-lookup"><span data-stu-id="20464-234">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="20464-235">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-235">Visible black line</span></span>     |
| <span data-ttu-id="20464-236">R2- \_ MaskPen</span><span class="sxs-lookup"><span data-stu-id="20464-236">R2\_MASKPEN</span></span>      | <span data-ttu-id="20464-237">Unsichtbare blaue Linie</span><span class="sxs-lookup"><span data-stu-id="20464-237">Invisible blue line</span></span>    |
| <span data-ttu-id="20464-238">R2 \_ maskpnot</span><span class="sxs-lookup"><span data-stu-id="20464-238">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="20464-239">Sichtbare rote/grüne Linie</span><span class="sxs-lookup"><span data-stu-id="20464-239">Visible red/green line</span></span> |
| <span data-ttu-id="20464-240">R2 \_ mergenotpen</span><span class="sxs-lookup"><span data-stu-id="20464-240">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="20464-241">Unsichtbare blaue Linie</span><span class="sxs-lookup"><span data-stu-id="20464-241">Invisible blue line</span></span>    |
| <span data-ttu-id="20464-242">R2- \_ MergePen</span><span class="sxs-lookup"><span data-stu-id="20464-242">R2\_MERGEPEN</span></span>     | <span data-ttu-id="20464-243">Sichtbare weiße Linie</span><span class="sxs-lookup"><span data-stu-id="20464-243">Visible white line</span></span>     |
| <span data-ttu-id="20464-244">R2 \_ mergepnot</span><span class="sxs-lookup"><span data-stu-id="20464-244">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="20464-245">Sichtbare weiße Linie</span><span class="sxs-lookup"><span data-stu-id="20464-245">Visible white line</span></span>     |
| <span data-ttu-id="20464-246">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="20464-246">R2\_NOP</span></span>          | <span data-ttu-id="20464-247">Unsichtbare blaue Linie</span><span class="sxs-lookup"><span data-stu-id="20464-247">Invisible blue line</span></span>    |
| <span data-ttu-id="20464-248">R2 \_ nicht</span><span class="sxs-lookup"><span data-stu-id="20464-248">R2\_NOT</span></span>          | <span data-ttu-id="20464-249">Sichtbare rote/grüne Linie</span><span class="sxs-lookup"><span data-stu-id="20464-249">Visible red/green line</span></span> |
| <span data-ttu-id="20464-250">R2- \_ notcopypen</span><span class="sxs-lookup"><span data-stu-id="20464-250">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="20464-251">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-251">Visible black line</span></span>     |
| <span data-ttu-id="20464-252">R2 \_ notmaskpen</span><span class="sxs-lookup"><span data-stu-id="20464-252">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="20464-253">Sichtbare rote/grüne Linie</span><span class="sxs-lookup"><span data-stu-id="20464-253">Visible red/green line</span></span> |
| <span data-ttu-id="20464-254">R2 \_ NotMergePen</span><span class="sxs-lookup"><span data-stu-id="20464-254">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="20464-255">Sichtbare schwarze Linie</span><span class="sxs-lookup"><span data-stu-id="20464-255">Visible black line</span></span>     |
| <span data-ttu-id="20464-256">R2- \_ NotXorPen</span><span class="sxs-lookup"><span data-stu-id="20464-256">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="20464-257">Unsichtbare blaue Linie</span><span class="sxs-lookup"><span data-stu-id="20464-257">Invisible blue line</span></span>    |
| <span data-ttu-id="20464-258">R2 \_ weiß</span><span class="sxs-lookup"><span data-stu-id="20464-258">R2\_WHITE</span></span>        | <span data-ttu-id="20464-259">Sichtbare weiße Linie</span><span class="sxs-lookup"><span data-stu-id="20464-259">Visible white line</span></span>     |
| <span data-ttu-id="20464-260">R2- \_ XOrPen</span><span class="sxs-lookup"><span data-stu-id="20464-260">R2\_XORPEN</span></span>       | <span data-ttu-id="20464-261">Sichtbare rote/grüne Linie</span><span class="sxs-lookup"><span data-stu-id="20464-261">Visible red/green line</span></span> |



 

 

 



