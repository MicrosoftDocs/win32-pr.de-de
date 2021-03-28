---
title: texm3x3vspec-PS
description: Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche auszuführen.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948325"
---
# <a name="texm3x3vspec---ps"></a><span data-ttu-id="3ac7c-103">texm3x3vspec-PS</span><span class="sxs-lookup"><span data-stu-id="3ac7c-103">texm3x3vspec - ps</span></span>

<span data-ttu-id="3ac7c-104">Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-104">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="3ac7c-105">Dies kann für Glanz Reflektion und Umgebungs Zuordnung verwendet werden, bei denen der Eye-Ray-Vektor nicht konstant ist.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-105">This can be used for specular reflection and environment mapping where the eye-ray vector is not constant.</span></span> <span data-ttu-id="3ac7c-106">texm3x3vspec muss in Verbindung mit zwei [texm3x3pad-PS-](texm3x3pad---ps.md) Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-106">texm3x3vspec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span> <span data-ttu-id="3ac7c-107">Wenn der Augen Strahl Vektor konstant ist, führt die [texm3x3spec-PS-](texm3x3spec---ps.md) Anweisung die gleiche Matrix Multiplikation und Textur Suche aus.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-107">If the eye-ray vector is constant, the [texm3x3spec - ps](texm3x3spec---ps.md) instruction will perform the same matrix multiply and texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac7c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ac7c-108">Syntax</span></span>



| <span data-ttu-id="3ac7c-109">texm3x3vspec DST, src</span><span class="sxs-lookup"><span data-stu-id="3ac7c-109">texm3x3vspec dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="3ac7c-110">where</span><span class="sxs-lookup"><span data-stu-id="3ac7c-110">where</span></span>

-   <span data-ttu-id="3ac7c-111">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-111">dst is the destination register.</span></span>
-   <span data-ttu-id="3ac7c-112">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-112">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac7c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ac7c-113">Remarks</span></span>



| <span data-ttu-id="3ac7c-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="3ac7c-114">Pixel shader versions</span></span> | <span data-ttu-id="3ac7c-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="3ac7c-115">1\_1</span></span> | <span data-ttu-id="3ac7c-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="3ac7c-116">1\_2</span></span> | <span data-ttu-id="3ac7c-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3ac7c-117">1\_3</span></span> | <span data-ttu-id="3ac7c-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="3ac7c-118">1\_4</span></span> | <span data-ttu-id="3ac7c-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3ac7c-119">2\_0</span></span> | <span data-ttu-id="3ac7c-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3ac7c-120">2\_x</span></span> | <span data-ttu-id="3ac7c-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3ac7c-121">2\_sw</span></span> | <span data-ttu-id="3ac7c-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3ac7c-122">3\_0</span></span> | <span data-ttu-id="3ac7c-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3ac7c-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3ac7c-124">texm3x3vspec</span><span class="sxs-lookup"><span data-stu-id="3ac7c-124">texm3x3vspec</span></span>          | <span data-ttu-id="3ac7c-125">x</span><span class="sxs-lookup"><span data-stu-id="3ac7c-125">x</span></span>    | <span data-ttu-id="3ac7c-126">x</span><span class="sxs-lookup"><span data-stu-id="3ac7c-126">x</span></span>    | <span data-ttu-id="3ac7c-127">x</span><span class="sxs-lookup"><span data-stu-id="3ac7c-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="3ac7c-128">Diese Anweisung führt die letzte Zeile eines 3X3-Matrix Multiplikations Vorgangs aus, interpretiert den resultierenden Vektor als normalen Vektor, um einen Augen Strahl Vektor widerzuspiegeln, und verwendet dann den reflektierten Vektor als Textur Adresse für eine Textur Suche.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-128">This instruction performs the final row of a 3x3 matrix multiply operation, interprets the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector as a texture address for a texture lookup.</span></span> <span data-ttu-id="3ac7c-129">Es funktioniert genauso wie [texm3x3spec-PS](texm3x3spec---ps.md), mit dem Unterschied, dass der Augen Strahl Vektor aus der vierten Komponente der Texturkoordinaten entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-129">It works just like [texm3x3spec - ps](texm3x3spec---ps.md), except that the eye-ray vector is taken from the fourth component of the texture coordinates.</span></span> <span data-ttu-id="3ac7c-130">Die 3X3-Matrix Multiplikation ist in der Regel hilfreich, um einen normalen Vektor auf den richtigen Tangenten Raum für die zu rendernde Oberfläche zu ausrichten.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-130">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="3ac7c-131">Die 3X3-Matrix besteht aus den Texturkoordinaten der dritten Textur Phase und den beiden vorangehenden Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-131">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="3ac7c-132">Der resultierende postreflection Vector (UVW) wird verwendet, um eine Stichprobe der Textur in Phase 3 durchführen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-132">The resulting post-reflection vector (UVW) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="3ac7c-133">Jede Textur, die den vorherigen zwei Textur Stufen zugewiesen ist, wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-133">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="3ac7c-134">Diese Anweisung muss mit der texm3x3pad-Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-134">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="3ac7c-135">Textur Register müssen die folgende Sequenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-135">Texture registers must use the following sequence.</span></span>


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



<span data-ttu-id="3ac7c-136">Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-136">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="3ac7c-137">u<sup>'</sup> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="3ac7c-137">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub></span></span>

<span data-ttu-id="3ac7c-138">Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-138">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="3ac7c-139">v<sup>'</sup> = TextureCoordinates (Stufe m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="3ac7c-139">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="3ac7c-140">Die texm3x3spec-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-140">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="3ac7c-141">w<sup>'</sup> = TextureCoordinates (Stufe m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="3ac7c-141">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="3ac7c-142">Die texm3x3vspec-Anweisung führt auch eine reflektionsanberechnung durch.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-142">The texm3x3vspec instruction also does a reflection calculation.</span></span>

<span data-ttu-id="3ac7c-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* )/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="3ac7c-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="3ac7c-144">Gibt an, wo der normale N von angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-144">// where the normal N is given by</span></span>

<span data-ttu-id="3ac7c-145">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="3ac7c-145">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="3ac7c-146">und der Augen Strahl Vektor E wird von</span><span class="sxs-lookup"><span data-stu-id="3ac7c-146">// and the eye-ray vector E is given by</span></span>

<span data-ttu-id="3ac7c-147">E = (TextureCoordinates (Stufe m)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="3ac7c-147">// E = (TextureCoordinates(stage m)<sub>Q</sub> ,</span></span>

<span data-ttu-id="3ac7c-148">TextureCoordinates (Phase m + 1)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="3ac7c-148">// TextureCoordinates(stage m+1)<sub>Q</sub> ,</span></span>

<span data-ttu-id="3ac7c-149">TextureCoordinates (Stufe m + 2)<sub>Q</sub> )</span><span class="sxs-lookup"><span data-stu-id="3ac7c-149">// TextureCoordinates(stage m+2)<sub>Q</sub> )</span></span>

<span data-ttu-id="3ac7c-150">Schließlich wird die texm3x3vspec-Anweisung mit t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) und das Ergebnis in t (m + 2) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-150">Lastly, the texm3x3vspec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>)and stores the result in t(m+2).</span></span>

<span data-ttu-id="3ac7c-151">t (m + 2)<sub>RGBA</sub> = texturesample (Phase m + 2)<sub>RGBA</sub> mithilfe von (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="3ac7c-151">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="3ac7c-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ac7c-152">Examples</span></span>

<span data-ttu-id="3ac7c-153">Hier ist ein Beispiel-Shader mit den identifizierten Textur Zuordnungen und den identifizierten Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-153">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



<span data-ttu-id="3ac7c-154">Für dieses Beispiel ist die folgende Textur Stufen Einrichtung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-154">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="3ac7c-155">Phase 0 wird eine Textur Zuordnung mit normalen Daten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-155">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="3ac7c-156">Dies wird häufig als Bump Map bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-156">This is often referred to as a bump map.</span></span> <span data-ttu-id="3ac7c-157">Bei den Daten handelt es sich um (XYZ) normale für jedes texaus.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-157">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="3ac7c-158">Texturkoordinaten in Phase n definieren, wie diese normale Karte als Stichprobe festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-158">Texture coordinates at stage n defines how to sample this normal map.</span></span>
-   <span data-ttu-id="3ac7c-159">Der Texturkoordinaten Satz m wird der Zeile 1 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-159">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="3ac7c-160">Alle der Phase m zugewiesenen Textur werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-160">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="3ac7c-161">Der Texturkoordinaten Satz m + 1 wird Zeile 2 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-161">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="3ac7c-162">Alle der Phase m + 1 zugewiesenen Textur werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-162">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="3ac7c-163">Der Texturkoordinaten Satz m + 2 wird Zeile 3 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-163">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="3ac7c-164">Phase m + 2 wird ein Volume oder eine cubetexturmap zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-164">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="3ac7c-165">Die Textur stellt Farbdaten (RGBA) bereit.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-165">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="3ac7c-166">Der Eye-Ray-Vektor E wird an die Anweisung in der vierten Komponente (q) der Texturkoordinaten Daten in den Phasen m, m + 1 und m + 2 geleitet.</span><span class="sxs-lookup"><span data-stu-id="3ac7c-166">The eye-ray vector E is passed into the instruction in the fourth component (q) of the texture coordinate data at stages m, m+1, and m+2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ac7c-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ac7c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ac7c-168">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="3ac7c-168">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




