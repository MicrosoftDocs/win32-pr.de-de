---
title: texm3x3spec-PS
description: Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche auszuführen. Dies kann für die Glanz Reflektion und die Umgebungs Zuordnung verwendet werden. texm3x3spec muss in Verbindung mit zwei texm3x3pad-PS-Anweisungen verwendet werden.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389522"
---
# <a name="texm3x3spec---ps"></a><span data-ttu-id="bf8aa-105">texm3x3spec-PS</span><span class="sxs-lookup"><span data-stu-id="bf8aa-105">texm3x3spec - ps</span></span>

<span data-ttu-id="bf8aa-106">Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-106">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="bf8aa-107">Dies kann für die Glanz Reflektion und die Umgebungs Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-107">This can be used for specular reflection and environment mapping.</span></span> <span data-ttu-id="bf8aa-108">texm3x3spec muss in Verbindung mit zwei [texm3x3pad-PS-](texm3x3pad---ps.md) Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-108">texm3x3spec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8aa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf8aa-109">Syntax</span></span>



| <span data-ttu-id="bf8aa-110">texm3x3spec DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="bf8aa-110">texm3x3spec dst, src0, src1</span></span> |
|-----------------------------|



 

<span data-ttu-id="bf8aa-111">where</span><span class="sxs-lookup"><span data-stu-id="bf8aa-111">where</span></span>

-   <span data-ttu-id="bf8aa-112">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-112">dst is the destination register.</span></span>
-   <span data-ttu-id="bf8aa-113">src0 und Quelle1 sind Quell Register.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-113">src0 and src1 are source registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8aa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf8aa-114">Remarks</span></span>



| <span data-ttu-id="bf8aa-115">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="bf8aa-115">Pixel shader versions</span></span> | <span data-ttu-id="bf8aa-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="bf8aa-116">1\_1</span></span> | <span data-ttu-id="bf8aa-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="bf8aa-117">1\_2</span></span> | <span data-ttu-id="bf8aa-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bf8aa-118">1\_3</span></span> | <span data-ttu-id="bf8aa-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="bf8aa-119">1\_4</span></span> | <span data-ttu-id="bf8aa-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf8aa-120">2\_0</span></span> | <span data-ttu-id="bf8aa-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bf8aa-121">2\_x</span></span> | <span data-ttu-id="bf8aa-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf8aa-122">2\_sw</span></span> | <span data-ttu-id="bf8aa-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf8aa-123">3\_0</span></span> | <span data-ttu-id="bf8aa-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf8aa-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bf8aa-125">texm3x3spec</span><span class="sxs-lookup"><span data-stu-id="bf8aa-125">texm3x3spec</span></span>           | <span data-ttu-id="bf8aa-126">x</span><span class="sxs-lookup"><span data-stu-id="bf8aa-126">x</span></span>    | <span data-ttu-id="bf8aa-127">x</span><span class="sxs-lookup"><span data-stu-id="bf8aa-127">x</span></span>    | <span data-ttu-id="bf8aa-128">x</span><span class="sxs-lookup"><span data-stu-id="bf8aa-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="bf8aa-129">Diese Anweisung führt die letzte Zeile einer 3X3-Matrix Multiplikation aus, verwendet den resultierenden Vektor als normalen Vektor, um einen Augen Strahl Vektor widerzuspiegeln, und verwendet dann den reflektierten Vektor, um eine Textur Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-129">This instruction performs the final row of a 3x3 matrix multiply, uses the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector to perform a texture lookup.</span></span> <span data-ttu-id="bf8aa-130">Der Shader liest den Augen Strahl Vektor aus einem konstanten Register.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-130">The shader reads the eye-ray vector from a constant register.</span></span> <span data-ttu-id="bf8aa-131">Die 3X3-Matrix Multiplikation ist in der Regel hilfreich, um einen normalen Vektor auf den richtigen Tangenten Raum für die zu rendernde Oberfläche zu ausrichten.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="bf8aa-132">Die 3X3-Matrix besteht aus den Texturkoordinaten der dritten Textur Phase und den beiden vorangehenden Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-132">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="bf8aa-133">Der resultierende postreflection Vector (u, v, w) wird verwendet, um die Textur auf der abschließenden Textur Phase zu testen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-133">The resulting post reflection vector (u,v,w) is used to sample the texture on the final texture stage.</span></span> <span data-ttu-id="bf8aa-134">Jede Textur, die den vorherigen zwei Textur Stufen zugewiesen ist, wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-134">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="bf8aa-135">Diese Anweisung muss mit zwei texm3x3pad-Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-135">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="bf8aa-136">Textur Register müssen die folgende Sequenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-136">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



<span data-ttu-id="bf8aa-137">Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-137">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="bf8aa-138">u<sup>'</sup> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="bf8aa-138">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="bf8aa-139">Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-139">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="bf8aa-140">v<sup>'</sup> = TextureCoordinates (Stufe m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="bf8aa-140">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="bf8aa-141">Die texm3x3spec-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-141">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="bf8aa-142">w<sup>'</sup> = TextureCoordinates (Stufe m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="bf8aa-142">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="bf8aa-143">Die texm3x3spec-Anweisung führt dann eine reflektionsanberechnung durch.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-143">The texm3x3spec instruction then does a reflection calculation.</span></span>

<span data-ttu-id="bf8aa-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* )/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="bf8aa-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="bf8aa-145">Gibt an, wo der normale N von angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-145">// where the normal N is given by</span></span>

<span data-ttu-id="bf8aa-146">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="bf8aa-146">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="bf8aa-147">und der Eye-Ray-Vektor E wird durch das konstantenregister angegeben.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-147">// and the eye-ray vector E is given by the constant register</span></span>

<span data-ttu-id="bf8aa-148">E = c \# (beliebiges konstantes Register--C0, C1, C2 usw.--kann verwendet werden)</span><span class="sxs-lookup"><span data-stu-id="bf8aa-148">// E = c\# (Any constant register--c0, c1, c2, etc.--can be used)</span></span>

<span data-ttu-id="bf8aa-149">Schließlich wird die texm3x3spec-Anweisung mit t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) und das Ergebnis in t (m + 2) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-149">Lastly, the texm3x3spec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="bf8aa-150">t (m + 2)<sub>RGBA</sub> = texturesample (Phase m + 2)<sub>RGBA</sub> mithilfe von (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="bf8aa-150">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="bf8aa-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf8aa-151">Examples</span></span>

<span data-ttu-id="bf8aa-152">Hier ist ein Beispiel-Shader mit den Textur Maps und den identifizierten Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-152">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



<span data-ttu-id="bf8aa-153">Für dieses Beispiel ist die folgende Textur Stufen Einrichtung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-153">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="bf8aa-154">Phase 0 wird eine Textur Zuordnung mit normalen Daten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-154">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="bf8aa-155">Dies wird häufig als Bump Map bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-155">This is often referred to as a bump map.</span></span> <span data-ttu-id="bf8aa-156">Bei den Daten handelt es sich um (XYZ) normale für jedes texaus.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-156">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="bf8aa-157">Texturkoordinaten in Phase n definieren, wo diese normale Karte Stichproben gibt.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-157">Texture coordinates at stage n defines where to sample this normal map.</span></span>
-   <span data-ttu-id="bf8aa-158">Der Texturkoordinaten Satz m wird der Zeile 1 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-158">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="bf8aa-159">Alle der Phase m zugewiesenen Textur werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-159">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="bf8aa-160">Der Texturkoordinaten Satz m + 1 wird Zeile 2 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-160">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="bf8aa-161">Alle der Phase m + 1 zugewiesenen Textur werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-161">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="bf8aa-162">Der Texturkoordinaten Satz m + 2 wird Zeile 3 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-162">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="bf8aa-163">Phase m + 2 wird ein Volume oder eine cubetexturmap zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-163">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="bf8aa-164">Die Textur stellt Farbdaten (RGBA) bereit.</span><span class="sxs-lookup"><span data-stu-id="bf8aa-164">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="bf8aa-165">Der Augen Strahl Vektor e wird durch ein konstantes Register e = c angegeben \# .</span><span class="sxs-lookup"><span data-stu-id="bf8aa-165">The eye-ray vector E is given by a constant register E = c\#.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf8aa-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf8aa-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf8aa-167">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="bf8aa-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




