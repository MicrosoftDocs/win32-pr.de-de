---
description: Textur Format DXT1 ist für Texturen, die nicht transparent sind oder eine einzelne transparente Farbe aufweisen.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Undurchsichtige und 1-Bit-Alpha Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104553148"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a><span data-ttu-id="8c73d-103">Undurchsichtige und 1-Bit-Alpha Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8c73d-103">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>

<span data-ttu-id="8c73d-104">Textur Format DXT1 ist für Texturen, die nicht transparent sind oder eine einzelne transparente Farbe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8c73d-104">Texture format DXT1 is for textures that are opaque or have a single transparent color.</span></span>

<span data-ttu-id="8c73d-105">Für jeden opaken oder 1-Bit-Alpha Block werden 2 16-Bit-Werte (RGB 5:6:5-Format) und eine 4X4-Bitmap mit 2 Bits pro Pixel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8c73d-105">For each opaque or 1-bit alpha block, two 16-bit values (RGB 5:6:5 format) and a 4x4 bitmap with 2 bits per pixel are stored.</span></span> <span data-ttu-id="8c73d-106">Dies ergibt 64 Bits für 16 texeln oder vier Bits pro textteln.</span><span class="sxs-lookup"><span data-stu-id="8c73d-106">This totals 64 bits for 16 texels, or four bits per texel.</span></span> <span data-ttu-id="8c73d-107">In der Block Bitmap gibt es zwei Bits pro Texttypen, die zwischen den vier Farben ausgewählt werden sollen, von denen zwei in den codierten Daten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8c73d-107">In the block bitmap, there are 2 bits per texel to select between the four colors, two of which are stored in the encoded data.</span></span> <span data-ttu-id="8c73d-108">Die anderen beiden Farben werden von diesen gespeicherten Farben durch lineare Interpolationen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8c73d-108">The other two colors are derived from these stored colors by linear interpolation.</span></span> <span data-ttu-id="8c73d-109">Dieses Layout ist im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8c73d-109">This layout is shown in the following diagram.</span></span>

![Diagramm des Bitmap-Layouts](images/colors1.png)

<span data-ttu-id="8c73d-111">Das 1-Bit-Alpha Format unterscheidet sich vom nicht transparenten Format durch Vergleichen der im-Block gespeicherten 2 16-Bit-Farbwerte.</span><span class="sxs-lookup"><span data-stu-id="8c73d-111">The 1-bit alpha format is distinguished from the opaque format by comparing the two 16-bit color values stored in the block.</span></span> <span data-ttu-id="8c73d-112">Sie werden als ganze Zahlen ohne Vorzeichen behandelt.</span><span class="sxs-lookup"><span data-stu-id="8c73d-112">They are treated as unsigned integers.</span></span> <span data-ttu-id="8c73d-113">Wenn die erste Farbe größer als die zweite ist, bedeutet dies, dass nur nicht transparente texeln definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c73d-113">If the first color is greater than the second, it implies that only opaque texels are defined.</span></span> <span data-ttu-id="8c73d-114">Dies bedeutet, dass vier Farben zur Darstellung der Texels verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c73d-114">This means four colors are used to represent the texels.</span></span> <span data-ttu-id="8c73d-115">Bei der vierfarbigen Codierung gibt es zwei abgeleitete Farben, und alle vier Farben sind gleichmäßig im RGB-Farbraum verteilt.</span><span class="sxs-lookup"><span data-stu-id="8c73d-115">In four-color encoding, there are two derived colors and all four colors are equally distributed in RGB color space.</span></span> <span data-ttu-id="8c73d-116">Dieses Format entspricht dem RGB-5:6:5-Format.</span><span class="sxs-lookup"><span data-stu-id="8c73d-116">This format is analogous to RGB 5:6:5 format.</span></span> <span data-ttu-id="8c73d-117">Andernfalls werden für eine 1-Bit-Alpha Transparenz drei Farben verwendet, und die vierte ist für die Darstellung transparenter texeln reserviert.</span><span class="sxs-lookup"><span data-stu-id="8c73d-117">Otherwise, for 1-bit alpha transparency, three colors are used and the fourth is reserved to represent transparent texels.</span></span>

<span data-ttu-id="8c73d-118">Bei der drei-Farben-Codierung gibt es eine abgeleitete Farbe, und der vierte 2-Bit-Code ist für die Angabe einer transparenten Texttyp (Alpha Information) reserviert.</span><span class="sxs-lookup"><span data-stu-id="8c73d-118">In three-color encoding, there is one derived color and the fourth 2-bit code is reserved to indicate a transparent texel (alpha information).</span></span> <span data-ttu-id="8c73d-119">Dieses Format entspricht RGBA 5:5:5:1, wobei das abschließende Bit zum Codieren der Alpha Maske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c73d-119">This format is analogous to RGBA 5:5:5:1, where the final bit is used for encoding the alpha mask.</span></span>

<span data-ttu-id="8c73d-120">Das folgende Codebeispiel veranschaulicht den Algorithmus für die Entscheidung, ob drei-oder vierfarbige Codierungen ausgewählt sind:</span><span class="sxs-lookup"><span data-stu-id="8c73d-120">The following code example illustrates the algorithm for deciding whether three- or four-color encoding is selected:</span></span>


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



<span data-ttu-id="8c73d-121">Es wird empfohlen, vor dem mischen die RGBA-Komponenten des Transparenz Pixels auf 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8c73d-121">It is recommended that you set the RGBA components of the transparency pixel to zero before blending.</span></span>

<span data-ttu-id="8c73d-122">In den folgenden Tabellen wird das Speicher Layout für den 8-Byte-Block angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c73d-122">The following tables show the memory layout for the 8-byte block.</span></span> <span data-ttu-id="8c73d-123">Es wird davon ausgegangen, dass der erste Index der y-Koordinate entspricht und der zweite der x-Koordinate entspricht.</span><span class="sxs-lookup"><span data-stu-id="8c73d-123">It is assumed that the first index corresponds to the y-coordinate and the second corresponds to the x-coordinate.</span></span> <span data-ttu-id="8c73d-124">Beispielsweise verweist Texel \[ 1 \] \[ 2 \] auf das Textur Karten Pixel bei (x, y) = (2, 1).</span><span class="sxs-lookup"><span data-stu-id="8c73d-124">For example, Texel\[1\]\[2\] refers to the texture map pixel at (x,y) = (2,1).</span></span>

<span data-ttu-id="8c73d-125">Diese Tabelle enthält das Speicher Layout für den 8-Byte-Block (64 Bit).</span><span class="sxs-lookup"><span data-stu-id="8c73d-125">This table contains the memory layout for the 8-byte (64-bit) block.</span></span>



| <span data-ttu-id="8c73d-126">Word-Adresse</span><span class="sxs-lookup"><span data-stu-id="8c73d-126">Word address</span></span> | <span data-ttu-id="8c73d-127">16-Bit-Wort</span><span class="sxs-lookup"><span data-stu-id="8c73d-127">16-bit word</span></span>    |
|--------------|----------------|
| <span data-ttu-id="8c73d-128">0</span><span class="sxs-lookup"><span data-stu-id="8c73d-128">0</span></span>            | <span data-ttu-id="8c73d-129">Farbe \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c73d-129">Color\_0</span></span>       |
| <span data-ttu-id="8c73d-130">1</span><span class="sxs-lookup"><span data-stu-id="8c73d-130">1</span></span>            | <span data-ttu-id="8c73d-131">Farbe \_ 1</span><span class="sxs-lookup"><span data-stu-id="8c73d-131">Color\_1</span></span>       |
| <span data-ttu-id="8c73d-132">2</span><span class="sxs-lookup"><span data-stu-id="8c73d-132">2</span></span>            | <span data-ttu-id="8c73d-133">Bitmap Wort \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c73d-133">Bitmap Word\_0</span></span> |
| <span data-ttu-id="8c73d-134">3</span><span class="sxs-lookup"><span data-stu-id="8c73d-134">3</span></span>            | <span data-ttu-id="8c73d-135">Bitmap Word \_ 1</span><span class="sxs-lookup"><span data-stu-id="8c73d-135">Bitmap Word\_1</span></span> |



 

<span data-ttu-id="8c73d-136">Farbe \_ 0 und Farbe \_ 1, die Farben in den zwei extremen, werden wie folgt angeordnet:</span><span class="sxs-lookup"><span data-stu-id="8c73d-136">Color\_0 and Color\_1, the colors at the two extremes, are laid out as follows:</span></span>



| <span data-ttu-id="8c73d-137">Bits</span><span class="sxs-lookup"><span data-stu-id="8c73d-137">Bits</span></span>        | <span data-ttu-id="8c73d-138">Color</span><span class="sxs-lookup"><span data-stu-id="8c73d-138">Color</span></span>                 |
|-------------|-----------------------|
| <span data-ttu-id="8c73d-139">4:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="8c73d-139">4:0 (LSB\*)</span></span> | <span data-ttu-id="8c73d-140">Blaue Farbkomponente</span><span class="sxs-lookup"><span data-stu-id="8c73d-140">Blue color component</span></span>  |
| <span data-ttu-id="8c73d-141">10:5</span><span class="sxs-lookup"><span data-stu-id="8c73d-141">10:5</span></span>        | <span data-ttu-id="8c73d-142">Grüne Farbkomponente</span><span class="sxs-lookup"><span data-stu-id="8c73d-142">Green color component</span></span> |
| <span data-ttu-id="8c73d-143">15:11</span><span class="sxs-lookup"><span data-stu-id="8c73d-143">15:11</span></span>       | <span data-ttu-id="8c73d-144">Rote Farbkomponente</span><span class="sxs-lookup"><span data-stu-id="8c73d-144">Red color component</span></span>   |



 

<span data-ttu-id="8c73d-145">\*unbedeutsames Bit</span><span class="sxs-lookup"><span data-stu-id="8c73d-145">\*least-significant bit</span></span>

<span data-ttu-id="8c73d-146">Das Bitmap-Wort \_ 0 wird wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="8c73d-146">Bitmap Word\_0 is laid out as follows:</span></span>



| <span data-ttu-id="8c73d-147">Bits</span><span class="sxs-lookup"><span data-stu-id="8c73d-147">Bits</span></span>          | <span data-ttu-id="8c73d-148">Texel</span><span class="sxs-lookup"><span data-stu-id="8c73d-148">Texel</span></span>           |
|---------------|-----------------|
| <span data-ttu-id="8c73d-149">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="8c73d-149">1:0 (LSB)</span></span>     | <span data-ttu-id="8c73d-150">Texel \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-150">Texel\[0\]\[0\]</span></span> |
| <span data-ttu-id="8c73d-151">3:2</span><span class="sxs-lookup"><span data-stu-id="8c73d-151">3:2</span></span>           | <span data-ttu-id="8c73d-152">Texel \[ 0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-152">Texel\[0\]\[1\]</span></span> |
| <span data-ttu-id="8c73d-153">5:4</span><span class="sxs-lookup"><span data-stu-id="8c73d-153">5:4</span></span>           | <span data-ttu-id="8c73d-154">Texel \[ 0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-154">Texel\[0\]\[2\]</span></span> |
| <span data-ttu-id="8c73d-155">7:6</span><span class="sxs-lookup"><span data-stu-id="8c73d-155">7:6</span></span>           | <span data-ttu-id="8c73d-156">Texel \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-156">Texel\[0\]\[3\]</span></span> |
| <span data-ttu-id="8c73d-157">9:8</span><span class="sxs-lookup"><span data-stu-id="8c73d-157">9:8</span></span>           | <span data-ttu-id="8c73d-158">Texel \[ 1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-158">Texel\[1\]\[0\]</span></span> |
| <span data-ttu-id="8c73d-159">11:10</span><span class="sxs-lookup"><span data-stu-id="8c73d-159">11:10</span></span>         | <span data-ttu-id="8c73d-160">Texel \[ 1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-160">Texel\[1\]\[1\]</span></span> |
| <span data-ttu-id="8c73d-161">13:12</span><span class="sxs-lookup"><span data-stu-id="8c73d-161">13:12</span></span>         | <span data-ttu-id="8c73d-162">Texel \[ 1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-162">Texel\[1\]\[2\]</span></span> |
| <span data-ttu-id="8c73d-163">15:14 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="8c73d-163">15:14 (MSB\*)</span></span> | <span data-ttu-id="8c73d-164">Texel \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-164">Texel\[1\]\[3\]</span></span> |



 

<span data-ttu-id="8c73d-165">\*signifikantes Bit (MSB)</span><span class="sxs-lookup"><span data-stu-id="8c73d-165">\*most significant bit (MSB)</span></span>

<span data-ttu-id="8c73d-166">Bitmap Word \_ 1 wird wie folgt angeordnet:</span><span class="sxs-lookup"><span data-stu-id="8c73d-166">Bitmap Word\_1 is laid out as follows:</span></span>



| <span data-ttu-id="8c73d-167">Bits</span><span class="sxs-lookup"><span data-stu-id="8c73d-167">Bits</span></span>        | <span data-ttu-id="8c73d-168">Texel</span><span class="sxs-lookup"><span data-stu-id="8c73d-168">Texel</span></span>           |
|-------------|-----------------|
| <span data-ttu-id="8c73d-169">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="8c73d-169">1:0 (LSB)</span></span>   | <span data-ttu-id="8c73d-170">Texel \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-170">Texel\[2\]\[0\]</span></span> |
| <span data-ttu-id="8c73d-171">3:2</span><span class="sxs-lookup"><span data-stu-id="8c73d-171">3:2</span></span>         | <span data-ttu-id="8c73d-172">Texel \[ 2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-172">Texel\[2\]\[1\]</span></span> |
| <span data-ttu-id="8c73d-173">5:4</span><span class="sxs-lookup"><span data-stu-id="8c73d-173">5:4</span></span>         | <span data-ttu-id="8c73d-174">Texel \[ 2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-174">Texel\[2\]\[2\]</span></span> |
| <span data-ttu-id="8c73d-175">7:6</span><span class="sxs-lookup"><span data-stu-id="8c73d-175">7:6</span></span>         | <span data-ttu-id="8c73d-176">Texel \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-176">Texel\[2\]\[3\]</span></span> |
| <span data-ttu-id="8c73d-177">9:8</span><span class="sxs-lookup"><span data-stu-id="8c73d-177">9:8</span></span>         | <span data-ttu-id="8c73d-178">Texel \[ 3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-178">Texel\[3\]\[0\]</span></span> |
| <span data-ttu-id="8c73d-179">11:10</span><span class="sxs-lookup"><span data-stu-id="8c73d-179">11:10</span></span>       | <span data-ttu-id="8c73d-180">Texel \[ 3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-180">Texel\[3\]\[1\]</span></span> |
| <span data-ttu-id="8c73d-181">13:12</span><span class="sxs-lookup"><span data-stu-id="8c73d-181">13:12</span></span>       | <span data-ttu-id="8c73d-182">Texel \[ 3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-182">Texel\[3\]\[2\]</span></span> |
| <span data-ttu-id="8c73d-183">15:14 (MSB)</span><span class="sxs-lookup"><span data-stu-id="8c73d-183">15:14 (MSB)</span></span> | <span data-ttu-id="8c73d-184">Texel \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8c73d-184">Texel\[3\]\[3\]</span></span> |



 

## <a name="example-of-opaque-color-encoding"></a><span data-ttu-id="8c73d-185">Beispiel für nicht transparente Farbcodierung</span><span class="sxs-lookup"><span data-stu-id="8c73d-185">Example of Opaque Color Encoding</span></span>

<span data-ttu-id="8c73d-186">Nehmen Sie als Beispiel für die nicht transparente Codierung an, dass die Farben rot und schwarz die extreme sind.</span><span class="sxs-lookup"><span data-stu-id="8c73d-186">As an example of opaque encoding, assume that the colors red and black are at the extremes.</span></span> <span data-ttu-id="8c73d-187">Rot ist Farbe \_ 0, schwarz ist Farbe \_ 1.</span><span class="sxs-lookup"><span data-stu-id="8c73d-187">Red is color\_0, and black is color\_1.</span></span> <span data-ttu-id="8c73d-188">Es gibt vier interpoliert Farben, die den gleichmäßig verteilten Farbverlauf zwischen Ihnen bilden.</span><span class="sxs-lookup"><span data-stu-id="8c73d-188">There are four interpolated colors that form the uniformly distributed gradient between them.</span></span> <span data-ttu-id="8c73d-189">Zum Ermitteln der Werte für die 4X4-Bitmap werden die folgenden Berechnungen verwendet:</span><span class="sxs-lookup"><span data-stu-id="8c73d-189">To determine the values for the 4x4 bitmap, the following calculations are used:</span></span>


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



<span data-ttu-id="8c73d-190">Die Bitmap sieht dann wie im folgenden Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="8c73d-190">The bitmap then looks like the following diagram.</span></span>

![Diagramm, das das erweiterte bitmaplayout anzeigt.](images/colors2.png)

<span data-ttu-id="8c73d-192">Dies sieht wie die folgende veranschaulichte Reihe von Farben aus.</span><span class="sxs-lookup"><span data-stu-id="8c73d-192">This looks like the following illustrated series of colors.</span></span>

> [!Note]  
> <span data-ttu-id="8c73d-193">In einem Bild wird Pixel (0,0) oben links angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c73d-193">In an image, pixel (0,0) appears on the top left.</span></span>

 

![Abbildung eines opaken codierten Farbverlaufs](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a><span data-ttu-id="8c73d-195">Beispiel für 1-Bit-Alpha Codierung</span><span class="sxs-lookup"><span data-stu-id="8c73d-195">Example of 1-Bit Alpha Encoding</span></span>

<span data-ttu-id="8c73d-196">Dieses Format wird ausgewählt, wenn die 16-Bit-Ganzzahl ohne Vorzeichen (Farbe \_ 0) kleiner als die 16-Bit-Ganzzahl ohne Vorzeichen (Farbe 1) ist \_ .</span><span class="sxs-lookup"><span data-stu-id="8c73d-196">This format is selected when the unsigned 16-bit integer, color\_0, is less than the unsigned 16-bit integer, color\_1.</span></span> <span data-ttu-id="8c73d-197">Ein Beispiel für die Verwendung dieses Formats ist die Blätter in einer Struktur, die für einen blauen Himmel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8c73d-197">An example of where this format can be used is leaves on a tree, shown against a blue sky.</span></span> <span data-ttu-id="8c73d-198">Einige texeln können als transparent gekennzeichnet werden, während drei grüne Schattierungen weiterhin für die Blätter verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8c73d-198">Some texels can be marked as transparent while three shades of green are still available for the leaves.</span></span> <span data-ttu-id="8c73d-199">Zwei Farben korrigieren das Extreme, das dritte ist eine interinterpolierte Farbe.</span><span class="sxs-lookup"><span data-stu-id="8c73d-199">Two colors fix the extremes, and the third is an interpolated color.</span></span>

<span data-ttu-id="8c73d-200">In der folgenden Abbildung ist ein Beispiel für ein solches Bild dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8c73d-200">The following illustration is an example of such a picture.</span></span>

![Abbildung der 1-Bit-Alpha Codierung](images/greenthing.png)

<span data-ttu-id="8c73d-202">Beachten Sie, dass die textelist als transparent codiert werden, wenn das Bild als weiß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8c73d-202">Note that where the image is shown as white, the texel would be encoded as transparent.</span></span> <span data-ttu-id="8c73d-203">Beachten Sie auch, dass die RGBA-Komponenten der transparenten texeln vor dem Mischen auf 0 (null) festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c73d-203">Also note that the RGBA components of the transparent texels should be set to zero before blending.</span></span>

<span data-ttu-id="8c73d-204">Die Bitmap-Codierung für die Farben und Transparenz wird anhand der folgenden Berechnungen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8c73d-204">The bitmap encoding for the colors and the transparency is determined using the following calculations.</span></span>


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



<span data-ttu-id="8c73d-205">Die Bitmap sieht dann wie im folgenden Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="8c73d-205">The bitmap then looks like the following diagram.</span></span>

![Diagramm des erweiterten bitmaplayouts](images/colors3.png)

## <a name="related-topics"></a><span data-ttu-id="8c73d-207">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c73d-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c73d-208">Komprimierte Textur Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8c73d-208">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



