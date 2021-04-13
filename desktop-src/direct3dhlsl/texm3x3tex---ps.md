---
title: texm3x3tex-PS
description: Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen. texm3x3tex muss mit zwei texm3x3pad-PS-Anweisungen verwendet werden.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389610"
---
# <a name="texm3x3tex---ps"></a><span data-ttu-id="c5a0f-104">texm3x3tex-PS</span><span class="sxs-lookup"><span data-stu-id="c5a0f-104">texm3x3tex - ps</span></span>

<span data-ttu-id="c5a0f-105">Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-105">Performs a 3x3 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="c5a0f-106">texm3x3tex muss mit zwei [texm3x3pad-PS-](texm3x3pad---ps.md) Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-106">texm3x3tex must be used with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a0f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5a0f-107">Syntax</span></span>



| <span data-ttu-id="c5a0f-108">texm3x3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="c5a0f-108">texm3x3tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="c5a0f-109">where</span><span class="sxs-lookup"><span data-stu-id="c5a0f-109">where</span></span>

-   <span data-ttu-id="c5a0f-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-110">dst is the destination register.</span></span>
-   <span data-ttu-id="c5a0f-111">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a0f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5a0f-112">Remarks</span></span>



| <span data-ttu-id="c5a0f-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="c5a0f-113">Pixel shader versions</span></span> | <span data-ttu-id="c5a0f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c5a0f-114">1\_1</span></span> | <span data-ttu-id="c5a0f-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c5a0f-115">1\_2</span></span> | <span data-ttu-id="c5a0f-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c5a0f-116">1\_3</span></span> | <span data-ttu-id="c5a0f-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c5a0f-117">1\_4</span></span> | <span data-ttu-id="c5a0f-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5a0f-118">2\_0</span></span> | <span data-ttu-id="c5a0f-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c5a0f-119">2\_x</span></span> | <span data-ttu-id="c5a0f-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c5a0f-120">2\_sw</span></span> | <span data-ttu-id="c5a0f-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5a0f-121">3\_0</span></span> | <span data-ttu-id="c5a0f-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c5a0f-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c5a0f-123">texm3x3tex</span><span class="sxs-lookup"><span data-stu-id="c5a0f-123">texm3x3tex</span></span>            | <span data-ttu-id="c5a0f-124">x</span><span class="sxs-lookup"><span data-stu-id="c5a0f-124">x</span></span>    | <span data-ttu-id="c5a0f-125">x</span><span class="sxs-lookup"><span data-stu-id="c5a0f-125">x</span></span>    | <span data-ttu-id="c5a0f-126">x</span><span class="sxs-lookup"><span data-stu-id="c5a0f-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="c5a0f-127">Diese Anweisung wird als letzte von drei Anweisungen verwendet, die einen 3X3-Matrix Multiplikations Vorgang darstellen, gefolgt von einer Textur Suche.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-127">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation, followed by a texture lookup.</span></span> <span data-ttu-id="c5a0f-128">Die 3X3-Matrix besteht aus den Texturkoordinaten der dritten Textur Phase und den beiden vorangehenden Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-128">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="c5a0f-129">Der resultierende Vektor mit drei Komponenten (u, v, w) wird verwendet, um eine Stichprobe der Textur in Phase 3 durchführen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-129">The resulting three-component vector (u,v,w) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="c5a0f-130">Jede Textur, die den vorherigen zwei Textur Stufen zugewiesen ist, wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-130">Any texture assigned to the preceding two texture stages is ignored.</span></span> <span data-ttu-id="c5a0f-131">Die 3X3-Matrix Multiplikation ist in der Regel hilfreich, um einen normalen Vektor auf den richtigen Tangenten Raum für die zu rendernde Oberfläche zu ausrichten.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="c5a0f-132">Diese Anweisung muss mit der texm3x3pad-Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-132">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="c5a0f-133">Textur Register müssen die folgende Sequenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-133">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



<span data-ttu-id="c5a0f-134">Hier finden Sie weitere Details dazu, wie die 3X3-Multiplikation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-134">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="c5a0f-135">Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-135">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="c5a0f-136">u<sup>'</sup> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="c5a0f-136">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="c5a0f-137">Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-137">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="c5a0f-138">v<sup>'</sup> = TextureCoordinates (Stufe m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="c5a0f-138">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="c5a0f-139">Die texm3x3spec-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-139">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="c5a0f-140">w<sup>'</sup> = TextureCoordinates (Stufe m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="c5a0f-140">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="c5a0f-141">Schließlich wird die texm3x3tex-Anweisung mit t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) und das Ergebnis in t (m + 2) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-141">Lastly, the texm3x3tex instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="c5a0f-142">t (m + 2)<sub>RGBA</sub> = texturesample (Phase m + 2)<sub>RGBA</sub> mithilfe von (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) als Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-142">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates.</span></span>

## <a name="examples"></a><span data-ttu-id="c5a0f-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5a0f-143">Examples</span></span>

<span data-ttu-id="c5a0f-144">Hier ist ein Beispiel-Shader mit den identifizierten Textur Zuordnungen und den identifizierten Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-144">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



<span data-ttu-id="c5a0f-145">Für dieses Beispiel ist die folgende Textur Stufen Einrichtung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-145">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="c5a0f-146">Phase 0 wird eine Textur Zuordnung mit normalen Daten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-146">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="c5a0f-147">Dies wird häufig als Bump Map bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-147">This is often referred to as a bump map.</span></span> <span data-ttu-id="c5a0f-148">Bei den Daten handelt es sich um (XYZ) normale für jedes texaus.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-148">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="c5a0f-149">Texturkoordinaten Satz 0 definiert, wie diese normale Karte Stichprobe ist.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-149">Texture coordinate set 0 defines how to sample this normal map.</span></span>
-   <span data-ttu-id="c5a0f-150">Der Texturkoordinaten Satz 1 wird Zeile 1 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-150">Texture coordinate set 1 is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="c5a0f-151">Alle der Phase 1 zugewiesenen Textur werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-151">Any texture assigned to stage 1 is ignored.</span></span>
-   <span data-ttu-id="c5a0f-152">Der Texturkoordinaten Satz 2 wird Zeile 2 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-152">Texture coordinate set 2 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="c5a0f-153">Alle der Phase 2 zugewiesenen Textur werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-153">Any texture assigned to stage 2 is ignored.</span></span>
-   <span data-ttu-id="c5a0f-154">Der Texturkoordinaten Satz 3 wird Zeile 3 der 3X3-Matrix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-154">Texture coordinate set 3 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="c5a0f-155">Ein Volume oder eine cubetextur sollte für die Suche nach dem transformierten 3D-Vektor auf Phase 3 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c5a0f-155">A volume or cube texture should be set to stage 3 for lookup by the transformed 3D vector.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5a0f-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5a0f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5a0f-157">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="c5a0f-157">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




