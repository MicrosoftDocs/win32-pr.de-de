---
title: texbeml-PS
description: Anwenden einer gefälschten Bump Environment-Map-Transformation mit Beleuchtungs Korrektur. Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV), einer 2D-Stoß Umgebungs Matrix und einer Leuchtkraft geändert werden.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949066"
---
# <a name="texbeml---ps"></a><span data-ttu-id="c8f8f-104">texbeml-PS</span><span class="sxs-lookup"><span data-stu-id="c8f8f-104">texbeml - ps</span></span>

<span data-ttu-id="c8f8f-105">Anwenden einer gefälschten Bump Environment-Map-Transformation mit Beleuchtungs Korrektur.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-105">Apply a fake bump environment-map transform with luminance correction.</span></span> <span data-ttu-id="c8f8f-106">Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV), einer 2D-Stoß Umgebungs Matrix und einer Leuchtkraft geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), a 2D bump environment matrix, and luminance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f8f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8f8f-107">Syntax</span></span>



| <span data-ttu-id="c8f8f-108">texbeml DST, src</span><span class="sxs-lookup"><span data-stu-id="c8f8f-108">texbeml dst, src</span></span> |
|------------------|



 

<span data-ttu-id="c8f8f-109">where</span><span class="sxs-lookup"><span data-stu-id="c8f8f-109">where</span></span>

-   <span data-ttu-id="c8f8f-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-110">dst is the destination register.</span></span>
-   <span data-ttu-id="c8f8f-111">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f8f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8f8f-112">Remarks</span></span>



| <span data-ttu-id="c8f8f-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="c8f8f-113">Pixel shader versions</span></span> | <span data-ttu-id="c8f8f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c8f8f-114">1\_1</span></span> | <span data-ttu-id="c8f8f-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c8f8f-115">1\_2</span></span> | <span data-ttu-id="c8f8f-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c8f8f-116">1\_3</span></span> | <span data-ttu-id="c8f8f-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c8f8f-117">1\_4</span></span> | <span data-ttu-id="c8f8f-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c8f8f-118">2\_0</span></span> | <span data-ttu-id="c8f8f-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c8f8f-119">2\_x</span></span> | <span data-ttu-id="c8f8f-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c8f8f-120">2\_sw</span></span> | <span data-ttu-id="c8f8f-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c8f8f-121">3\_0</span></span> | <span data-ttu-id="c8f8f-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c8f8f-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c8f8f-123">texbeml</span><span class="sxs-lookup"><span data-stu-id="c8f8f-123">texbeml</span></span>               | <span data-ttu-id="c8f8f-124">x</span><span class="sxs-lookup"><span data-stu-id="c8f8f-124">x</span></span>    | <span data-ttu-id="c8f8f-125">x</span><span class="sxs-lookup"><span data-stu-id="c8f8f-125">x</span></span>    | <span data-ttu-id="c8f8f-126">x</span><span class="sxs-lookup"><span data-stu-id="c8f8f-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="c8f8f-127">Die roten und grünen Farbdaten im src-Register werden als Perturbation-Daten (du, DV) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span> <span data-ttu-id="c8f8f-128">Die blauen Farbdaten im src-Register werden als Beleuchtungs Daten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-128">The blue color data in the src register is interpreted as the luminance data.</span></span>

<span data-ttu-id="c8f8f-129">Diese Anweisung transformiert die roten und grünen Komponenten im Quell Register mithilfe der 2D-Bump-Umgebungs mappingmatrix.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-129">This instruction transforms the red and green components in the source register using the 2D bump environment mapping matrix.</span></span> <span data-ttu-id="c8f8f-130">Das Ergebnis wird dem Texturkoordinaten Satz hinzugefügt, der der Ziel Registernummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-130">The result is added to the texture coordinate set corresponding to the destination register number.</span></span> <span data-ttu-id="c8f8f-131">Eine Leuchtkraft Korrektur wird mithilfe des Leuchtkraft Werts und der Bias-Textur Stufen Werte angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-131">A luminance correction is applied using the luminance value and the bias texture stage values.</span></span> <span data-ttu-id="c8f8f-132">Das Ergebnis wird verwendet, um eine Stichprobe der aktuellen Textur Phase durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-132">The result is used to sample the current texture stage.</span></span>

<span data-ttu-id="c8f8f-133">Dies kann für eine Vielzahl von Techniken verwendet werden, die auf der Adress Erfassung basieren, wie z. b. eine gefälschte Umgebungs Zuordnung pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-133">This can be used for a variety of techniques based on address perturbation such as fake per-pixel environment mapping.</span></span>

<span data-ttu-id="c8f8f-134">Mit diesem Vorgang werden du und DV immer als signierte Mengen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-134">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="c8f8f-135">Für die Versionen 1 \_ 0 und 1 \_ 1 ist der Eingabe Modifizierer für die [Quell Registrierung mit signierter Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ bx2) für das Eingabe Argument nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-135">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="c8f8f-136">Diese Anweisung erzeugt definierte Ergebnisse, wenn Eingabe Texturen gemischte Formatierungsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-136">This instruction produces defined results when input textures contain mixed format data.</span></span> <span data-ttu-id="c8f8f-137">Weitere Informationen zu Oberflächen Formaten finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="c8f8f-137">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



<span data-ttu-id="c8f8f-138">In diesem Beispiel werden die in der-Anweisung durchgeführten Berechnungen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-138">This example shows the calculations done within the instruction.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



<span data-ttu-id="c8f8f-139">u ' = TextureCoordinates (Stufe m)<sub>u</sub> +</span><span class="sxs-lookup"><span data-stu-id="c8f8f-139">u' = TextureCoordinates(stage m)<sub>u</sub> +</span></span>

<span data-ttu-id="c8f8f-140">D3DTSS \_ BUMPENVMAT00 (Stufe m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="c8f8f-140">D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="c8f8f-141">D3DTSS \_ BUMPENVMAT10 (Stufe m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="c8f8f-141">D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="c8f8f-142">v ' = TextureCoordinates (Stufe m)<sub>v</sub> +</span><span class="sxs-lookup"><span data-stu-id="c8f8f-142">v' = TextureCoordinates(stage m)<sub>v</sub> +</span></span>

<span data-ttu-id="c8f8f-143">D3DTSS \_ BUMPENVMAT01 (Stufe m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="c8f8f-143">D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="c8f8f-144">D3DTSS \_ BUMPENVMAT11 (Stufe m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="c8f8f-144">D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="c8f8f-145">t (m)<sub>RGBA</sub> = texturesample (Stufe m) mit (u ', v ') als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="c8f8f-145">t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates</span></span>

<span data-ttu-id="c8f8f-146">t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*</span><span class="sxs-lookup"><span data-stu-id="c8f8f-146">t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub> \*</span></span>

<span data-ttu-id="c8f8f-147">\[(t (n)<sub>B</sub> \* D3DTSS \_ bumpenvlscale (Stufe m) +</span><span class="sxs-lookup"><span data-stu-id="c8f8f-147">\[(t(n)<sub>B</sub> \* D3DTSS\_BUMPENVLSCALE(stage m)) +</span></span>

<span data-ttu-id="c8f8f-148">D3DTSS \_ bumpenvloffset (Stufe m)\]</span><span class="sxs-lookup"><span data-stu-id="c8f8f-148">D3DTSS\_BUMPENVLOFFSET(stage m)\]</span></span>

<span data-ttu-id="c8f8f-149">Das Registrieren von Daten, die von einer [texbem](texbem---ps.md) -oder texbeml-Anweisung gelesen wurden, kann später nicht mehr gelesen werden, mit Ausnahme von anderen texbem oder texbeml.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-149">Register data that has been read by a [texbem](texbem---ps.md) or texbeml instruction cannot be read later, except by another texbem or texbeml.</span></span>


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="c8f8f-150">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8f8f-150">Examples</span></span>

<span data-ttu-id="c8f8f-151">Hier ist ein Beispiel-Shader mit den identifizierten Textur Zuordnungen und den identifizierten Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-151">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="c8f8f-152">Für dieses Beispiel sind die folgenden Texturen in den folgenden Textur Phasen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-152">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="c8f8f-153">Phase 0 wird eine Bump Map mit (du-, DV-) perturingdaten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-153">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="c8f8f-154">Phase 1 wird eine Textur Zuordnung mit Farbdaten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-154">Stage 1 is assigned a texture map with color data.</span></span>
-   <span data-ttu-id="c8f8f-155">texbeml legt die Matrix Daten auf der Textur Stufe fest, für die ein Sampling durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-155">texbeml sets the matrix data on the texture stage that is sampled.</span></span> <span data-ttu-id="c8f8f-156">Dies unterscheidet sich von der Funktionalität der Fixed-Funktions Pipeline, bei der die Leistungsdaten und Matrizen dieselbe Textur Phase belegen.</span><span class="sxs-lookup"><span data-stu-id="c8f8f-156">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8f8f-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8f8f-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8f8f-158">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="c8f8f-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 