---
description: Es gibt zwei Möglichkeiten, Textur Karten zu codieren, die komplexere Transparenz aufweisen.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Texturen mit Alpha Kanälen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104560981"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a><span data-ttu-id="2ed8d-103">Texturen mit Alpha Kanälen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-103">Textures with Alpha Channels (Direct3D 9)</span></span>

<span data-ttu-id="2ed8d-104">Es gibt zwei Möglichkeiten, Textur Karten zu codieren, die komplexere Transparenz aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-104">There are two ways to encode texture maps that exhibit more complex transparency.</span></span> <span data-ttu-id="2ed8d-105">In jedem Fall wird ein-Block, der die Transparenz vor dem 64-Bit-Block beschreibt, bereits beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-105">In each case, a block that describes the transparency precedes the 64-bit block already described.</span></span> <span data-ttu-id="2ed8d-106">Die Transparenz wird entweder als 4 x 4-Bitmap mit 4 Bits pro Pixel (explizite Codierung) oder mit weniger Bits und linearer Interpolationen dargestellt, die analog zu den für die Farbcodierung verwendeten Funktionen sind.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-106">The transparency is either represented as a 4x4 bitmap with 4 bits per pixel (explicit encoding), or with fewer bits and linear interpolation that is analogous to what is used for color encoding.</span></span>

<span data-ttu-id="2ed8d-107">Der Transparenz Block und der Farbblock werden wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-107">The transparency block and the color block are arranged as shown in the following table.</span></span>



| <span data-ttu-id="2ed8d-108">Word-Adresse</span><span class="sxs-lookup"><span data-stu-id="2ed8d-108">Word address</span></span> | <span data-ttu-id="2ed8d-109">64-Bit-Block</span><span class="sxs-lookup"><span data-stu-id="2ed8d-109">64-bit block</span></span>                      |
|--------------|-----------------------------------|
| <span data-ttu-id="2ed8d-110">3:0</span><span class="sxs-lookup"><span data-stu-id="2ed8d-110">3:0</span></span>          | <span data-ttu-id="2ed8d-111">Transparenz Block</span><span class="sxs-lookup"><span data-stu-id="2ed8d-111">Transparency block</span></span>                |
| <span data-ttu-id="2ed8d-112">7:4</span><span class="sxs-lookup"><span data-stu-id="2ed8d-112">7:4</span></span>          | <span data-ttu-id="2ed8d-113">Zuvor beschriebene 64-Bit-Block</span><span class="sxs-lookup"><span data-stu-id="2ed8d-113">Previously described 64-bit block</span></span> |



 

## <a name="explicit-texture-encoding"></a><span data-ttu-id="2ed8d-114">Explizite Textur Codierung</span><span class="sxs-lookup"><span data-stu-id="2ed8d-114">Explicit Texture Encoding</span></span>

<span data-ttu-id="2ed8d-115">Bei expliziten Textur Codierungen (DXT2-und DXT3-Format) werden die Alpha Komponenten der texeln, die Transparenz beschreiben, in einer 4 x 4-Bitmap mit 4 Bits pro Textteile codiert.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-115">For explicit texture encoding (DXT2 and DXT3 formats), the alpha components of the texels that describe transparency are encoded in a 4x4 bitmap with 4 bits per texel.</span></span> <span data-ttu-id="2ed8d-116">Diese vier Bits können durch eine Vielzahl von Methoden erreicht werden, wie z. b. das Dithering oder die Verwendung der vier wichtigsten Bits der Alpha Daten.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-116">These four bits can be achieved through a variety of means such as dithering or by using the four most significant bits of the alpha data.</span></span> <span data-ttu-id="2ed8d-117">Sie werden jedoch erstellt, Sie werden genauso wie Sie verwendet, ohne dass eine Interpolations Form vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-117">However they are produced, they are used just as they are, without any form of interpolation.</span></span>

<span data-ttu-id="2ed8d-118">Das folgende Diagramm zeigt einen 64-Bit-Transparenz Block.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-118">The following diagram shows a 64-bit transparency block.</span></span>

![Diagramm eines 64-Bit-Transparenz Blocks](images/colors4.png)

> [!Note]  
> <span data-ttu-id="2ed8d-120">Bei der Komprimierungs Methode von Direct3D werden die vier signifikantesten Bits verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-120">The compression method of Direct3D uses the four most significant bits.</span></span>

 

<span data-ttu-id="2ed8d-121">Die folgenden Tabellen veranschaulichen, wie die Alpha Informationen für jedes 16-Bit-Wort im Arbeitsspeicher angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-121">The following tables illustrate how the alpha information is laid out in memory, for each 16-bit word.</span></span>

<span data-ttu-id="2ed8d-122">Diese Tabelle enthält das Layout für Word 0.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-122">This table contains the layout for word 0.</span></span>



| <span data-ttu-id="2ed8d-123">Bits</span><span class="sxs-lookup"><span data-stu-id="2ed8d-123">Bits</span></span>          | <span data-ttu-id="2ed8d-124">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ed8d-124">Alpha</span></span>      |
|---------------|------------|
| <span data-ttu-id="2ed8d-125">3:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="2ed8d-125">3:0 (LSB\*)</span></span>   | <span data-ttu-id="2ed8d-126">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-126">\[0\]\[0\]</span></span> |
| <span data-ttu-id="2ed8d-127">7:4</span><span class="sxs-lookup"><span data-stu-id="2ed8d-127">7:4</span></span>           | <span data-ttu-id="2ed8d-128">\[0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-128">\[0\]\[1\]</span></span> |
| <span data-ttu-id="2ed8d-129">11:8</span><span class="sxs-lookup"><span data-stu-id="2ed8d-129">11:8</span></span>          | <span data-ttu-id="2ed8d-130">\[0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-130">\[0\]\[2\]</span></span> |
| <span data-ttu-id="2ed8d-131">15:12 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="2ed8d-131">15:12 (MSB\*)</span></span> | <span data-ttu-id="2ed8d-132">\[0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-132">\[0\]\[3\]</span></span> |



 

<span data-ttu-id="2ed8d-133">\*am wenigsten signifikantes Bit, höchst wichtiges Bit (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-133">\*least-significant bit, most significant bit (MSB)</span></span>

<span data-ttu-id="2ed8d-134">Diese Tabelle enthält das Layout für Word 1.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-134">This table contains the layout for word 1.</span></span>



| <span data-ttu-id="2ed8d-135">Bits</span><span class="sxs-lookup"><span data-stu-id="2ed8d-135">Bits</span></span>        | <span data-ttu-id="2ed8d-136">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ed8d-136">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="2ed8d-137">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-137">3:0 (LSB)</span></span>   | <span data-ttu-id="2ed8d-138">\[1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-138">\[1\]\[0\]</span></span> |
| <span data-ttu-id="2ed8d-139">7:4</span><span class="sxs-lookup"><span data-stu-id="2ed8d-139">7:4</span></span>         | <span data-ttu-id="2ed8d-140">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-140">\[1\]\[1\]</span></span> |
| <span data-ttu-id="2ed8d-141">11:8</span><span class="sxs-lookup"><span data-stu-id="2ed8d-141">11:8</span></span>        | <span data-ttu-id="2ed8d-142">\[1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-142">\[1\]\[2\]</span></span> |
| <span data-ttu-id="2ed8d-143">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-143">15:12 (MSB)</span></span> | <span data-ttu-id="2ed8d-144">\[1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-144">\[1\]\[3\]</span></span> |



 

<span data-ttu-id="2ed8d-145">Diese Tabelle enthält das Layout für Word 2.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-145">This table contains the layout for word 2.</span></span>



| <span data-ttu-id="2ed8d-146">Bits</span><span class="sxs-lookup"><span data-stu-id="2ed8d-146">Bits</span></span>        | <span data-ttu-id="2ed8d-147">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ed8d-147">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="2ed8d-148">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-148">3:0 (LSB)</span></span>   | <span data-ttu-id="2ed8d-149">\[2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-149">\[2\]\[0\]</span></span> |
| <span data-ttu-id="2ed8d-150">7:4</span><span class="sxs-lookup"><span data-stu-id="2ed8d-150">7:4</span></span>         | <span data-ttu-id="2ed8d-151">\[2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-151">\[2\]\[1\]</span></span> |
| <span data-ttu-id="2ed8d-152">11:8</span><span class="sxs-lookup"><span data-stu-id="2ed8d-152">11:8</span></span>        | <span data-ttu-id="2ed8d-153">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-153">\[2\]\[2\]</span></span> |
| <span data-ttu-id="2ed8d-154">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-154">15:12 (MSB)</span></span> | <span data-ttu-id="2ed8d-155">\[2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-155">\[2\]\[3\]</span></span> |



 

<span data-ttu-id="2ed8d-156">Diese Tabelle enthält das Layout für Word 3.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-156">This table contains the layout for word 3.</span></span>



| <span data-ttu-id="2ed8d-157">Bits</span><span class="sxs-lookup"><span data-stu-id="2ed8d-157">Bits</span></span>        | <span data-ttu-id="2ed8d-158">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ed8d-158">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="2ed8d-159">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-159">3:0 (LSB)</span></span>   | <span data-ttu-id="2ed8d-160">\[3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-160">\[3\]\[0\]</span></span> |
| <span data-ttu-id="2ed8d-161">7:4</span><span class="sxs-lookup"><span data-stu-id="2ed8d-161">7:4</span></span>         | <span data-ttu-id="2ed8d-162">\[3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-162">\[3\]\[1\]</span></span> |
| <span data-ttu-id="2ed8d-163">11:8</span><span class="sxs-lookup"><span data-stu-id="2ed8d-163">11:8</span></span>        | <span data-ttu-id="2ed8d-164">\[3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-164">\[3\]\[2\]</span></span> |
| <span data-ttu-id="2ed8d-165">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-165">15:12 (MSB)</span></span> | <span data-ttu-id="2ed8d-166">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-166">\[3\]\[3\]</span></span> |



 

<span data-ttu-id="2ed8d-167">Der Unterschied zwischen DXT2 und DXT3 besteht darin, dass im DXT2-Format angenommen wird, dass die Farbdaten mit Alpha multipliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-167">The difference between DXT2 and DXT3 are that, in the DXT2 format, it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="2ed8d-168">Im Format "DXT3" wird davon ausgegangen, dass die Farbe nicht mit Alpha multipliziert ist.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-168">In the DXT3 format, it is assumed that the color is not premultiplied by alpha.</span></span> <span data-ttu-id="2ed8d-169">Diese beiden Formate sind erforderlich, da in den meisten Fällen bis zur Zeit, in der eine Textur verwendet wird, die Untersuchung der Daten nicht ausreicht, um zu ermitteln, ob die Farbwerte mit Alpha multipliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-169">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="2ed8d-170">Da diese Informationen zur Laufzeit benötigt werden, werden die beiden FOURCC-Codes verwendet, um diese Fälle zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-170">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="2ed8d-171">Die für diese beiden Formate verwendeten Daten-und Interpolations Methoden sind jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-171">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="2ed8d-172">Der Farbvergleich, der in DXT1 verwendet wird, um zu bestimmen, ob der Texel transparent ist, wird in diesem Format nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-172">The color compare used in DXT1 to determine if the texel is transparent is not used in this format.</span></span> <span data-ttu-id="2ed8d-173">Es wird davon ausgegangen, dass die Farbdaten ohne den Farbvergleich immer so behandelt werden, als wären Sie im 4-Farben-Modus.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-173">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="2ed8d-174">Anders ausgedrückt: die if-Anweisung am Anfang des DXT1-Codes sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="2ed8d-174">In other words, the if statement at the top of the DXT1 code should be the following:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a><span data-ttu-id="2ed8d-175">Three-Bit Lineare Alpha interpolung</span><span class="sxs-lookup"><span data-stu-id="2ed8d-175">Three-Bit Linear Alpha Interpolation</span></span>

<span data-ttu-id="2ed8d-176">Die Codierung der Transparenz für die Formate DXT4 und DXT5 basiert auf einem Konzept, das der für Farbe verwendeten linearen Codierung ähnelt.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-176">The encoding of transparency for the DXT4 and DXT5 formats is based on a concept similar to the linear encoding used for color.</span></span> <span data-ttu-id="2ed8d-177">2 8-Bit-Alpha Werte und eine 4X4-Bitmap mit drei Bits pro Pixel werden in den ersten acht Bytes des Blocks gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-177">Two 8-bit alpha values and a 4x4 bitmap with three bits per pixel are stored in the first eight bytes of the block.</span></span> <span data-ttu-id="2ed8d-178">Die repräsentativen Alpha Werte werden zum interpolieren von zwischen Alpha Werten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-178">The representative alpha values are used to interpolate intermediate alpha values.</span></span> <span data-ttu-id="2ed8d-179">Weitere Informationen finden Sie in der Art und Weise, in der die beiden Alpha Werte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-179">Additional information is available in the way the two alpha values are stored.</span></span> <span data-ttu-id="2ed8d-180">Wenn Alpha \_ 0 größer als Alpha \_ 1 ist, werden sechs zwischen Alpha Werte von der Interpolations Zeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-180">If alpha\_0 is greater than alpha\_1, then six intermediate alpha values are created by the interpolation.</span></span> <span data-ttu-id="2ed8d-181">Andernfalls werden vier zwischenalpha Werte zwischen den angegebenen Alpha extremen interpoliert.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-181">Otherwise, four intermediate alpha values are interpolated between the specified alpha extremes.</span></span> <span data-ttu-id="2ed8d-182">Die zwei zusätzlichen impliziten Alpha Werte sind 0 (vollständig transparent) und 255 (vollständig deckend).</span><span class="sxs-lookup"><span data-stu-id="2ed8d-182">The two additional implicit alpha values are 0 (fully transparent) and 255 (fully opaque).</span></span>

<span data-ttu-id="2ed8d-183">Im folgenden Codebeispiel wird dieser Algorithmus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-183">The following code example illustrates this algorithm.</span></span>


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



<span data-ttu-id="2ed8d-184">Das Speicher Layout des Alpha-Blocks lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ed8d-184">The memory layout of the alpha block is as follows:</span></span>



| <span data-ttu-id="2ed8d-185">Byte</span><span class="sxs-lookup"><span data-stu-id="2ed8d-185">Byte</span></span> | <span data-ttu-id="2ed8d-186">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ed8d-186">Alpha</span></span>                                                          |
|------|----------------------------------------------------------------|
| <span data-ttu-id="2ed8d-187">0</span><span class="sxs-lookup"><span data-stu-id="2ed8d-187">0</span></span>    | <span data-ttu-id="2ed8d-188">Alpha \_ 0</span><span class="sxs-lookup"><span data-stu-id="2ed8d-188">Alpha\_0</span></span>                                                       |
| <span data-ttu-id="2ed8d-189">1</span><span class="sxs-lookup"><span data-stu-id="2ed8d-189">1</span></span>    | <span data-ttu-id="2ed8d-190">Alpha \_ 1</span><span class="sxs-lookup"><span data-stu-id="2ed8d-190">Alpha\_1</span></span>                                                       |
| <span data-ttu-id="2ed8d-191">2</span><span class="sxs-lookup"><span data-stu-id="2ed8d-191">2</span></span>    | <span data-ttu-id="2ed8d-192">\[0 \] \[ 2 \] (2 MSSB), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-192">\[0\]\[2\] (2 MSBs), \[0\]\[1\], \[0\]\[0\]</span></span>                    |
| <span data-ttu-id="2ed8d-193">3</span><span class="sxs-lookup"><span data-stu-id="2ed8d-193">3</span></span>    | <span data-ttu-id="2ed8d-194">\[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-194">\[1\]\[1\] (1 MSB), \[1\]\[0\], \[0\]\[3\], \[0\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="2ed8d-195">4</span><span class="sxs-lookup"><span data-stu-id="2ed8d-195">4</span></span>    | <span data-ttu-id="2ed8d-196">\[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 lssb)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-196">\[1\]\[3\], \[1\]\[2\], \[1\]\[1\] (2 LSBs)</span></span>                    |
| <span data-ttu-id="2ed8d-197">5</span><span class="sxs-lookup"><span data-stu-id="2ed8d-197">5</span></span>    | <span data-ttu-id="2ed8d-198">\[2 \] \[ 2 \] (2 MSSB), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-198">\[2\]\[2\] (2 MSBs), \[2\]\[1\], \[2\]\[0\]</span></span>                    |
| <span data-ttu-id="2ed8d-199">6</span><span class="sxs-lookup"><span data-stu-id="2ed8d-199">6</span></span>    | <span data-ttu-id="2ed8d-200">\[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-200">\[3\]\[1\] (1 MSB), \[3\]\[0\], \[2\]\[3\], \[2\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="2ed8d-201">7</span><span class="sxs-lookup"><span data-stu-id="2ed8d-201">7</span></span>    | <span data-ttu-id="2ed8d-202">\[3 3 \] \[ \] , \[ 3, \] \[ \] \[ 3 \] \[ 1 \] (2 lssb)</span><span class="sxs-lookup"><span data-stu-id="2ed8d-202">\[3\]\[3\], \[3\]\[2\], \[3\]\[1\] (2 LSBs)</span></span>                    |



 

<span data-ttu-id="2ed8d-203">Der Unterschied zwischen DXT4 und DXT5 besteht darin, dass im DXT4-Format angenommen wird, dass die Farbdaten mit Alpha multipliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-203">The difference between DXT4 and DXT5 is that in the DXT4 format it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="2ed8d-204">Im Format "DXT5" wird davon ausgegangen, dass die Farbe nicht mit Alpha aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-204">In the DXT5 format, it is assumed the color is not premultiplied by alpha.</span></span> <span data-ttu-id="2ed8d-205">Diese beiden Formate sind erforderlich, da in den meisten Fällen bis zur Zeit, in der eine Textur verwendet wird, die Untersuchung der Daten nicht ausreicht, um zu ermitteln, ob die Farbwerte mit Alpha multipliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-205">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="2ed8d-206">Da diese Informationen zur Laufzeit benötigt werden, werden die beiden FOURCC-Codes verwendet, um diese Fälle zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-206">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="2ed8d-207">Die für diese beiden Formate verwendeten Daten-und Interpolations Methoden sind jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-207">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="2ed8d-208">Der Farbvergleich, der in DXT1 verwendet wird, um zu bestimmen, ob der Texel transparent ist, wird in diesen Formaten nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-208">The color compare used in DXT1 to determine if the texel is transparent is not used with these formats.</span></span> <span data-ttu-id="2ed8d-209">Es wird davon ausgegangen, dass die Farbdaten ohne den Farbvergleich immer so behandelt werden, als wären Sie im 4-Farben-Modus.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-209">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="2ed8d-210">Anders ausgedrückt: die if-Anweisung am Anfang des DXT1-Codes sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="2ed8d-210">In other words, the if statement at the top of the DXT1 code should be:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a><span data-ttu-id="2ed8d-211">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ed8d-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed8d-212">Komprimierte Textur Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2ed8d-212">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



