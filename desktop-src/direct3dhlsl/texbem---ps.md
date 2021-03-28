---
title: texbem-PS
description: Anwenden einer gefälschten Bump Environment-Map-Transformation. Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV) und einer 2D-Bump-Umgebungs Matrix geändert werden.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976696"
---
# <a name="texbem---ps"></a><span data-ttu-id="7a6ce-104">texbem-PS</span><span class="sxs-lookup"><span data-stu-id="7a6ce-104">texbem - ps</span></span>

<span data-ttu-id="7a6ce-105">Anwenden einer gefälschten Bump Environment-Map-Transformation.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-105">Apply a fake bump environment-map transform.</span></span> <span data-ttu-id="7a6ce-106">Dies wird erreicht, indem die Textur Adressdaten des Ziel Registers mithilfe von Adress Erstellungs Daten (du, DV) und einer 2D-Bump-Umgebungs Matrix geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), and a 2D bump environment matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a6ce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a6ce-107">Syntax</span></span>



| <span data-ttu-id="7a6ce-108">texbem DST, src</span><span class="sxs-lookup"><span data-stu-id="7a6ce-108">texbem dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="7a6ce-109">where</span><span class="sxs-lookup"><span data-stu-id="7a6ce-109">where</span></span>

-   <span data-ttu-id="7a6ce-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-110">dst is the destination register.</span></span>
-   <span data-ttu-id="7a6ce-111">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a6ce-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a6ce-112">Remarks</span></span>



| <span data-ttu-id="7a6ce-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="7a6ce-113">Pixel shader versions</span></span> | <span data-ttu-id="7a6ce-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="7a6ce-114">1\_1</span></span> | <span data-ttu-id="7a6ce-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="7a6ce-115">1\_2</span></span> | <span data-ttu-id="7a6ce-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7a6ce-116">1\_3</span></span> | <span data-ttu-id="7a6ce-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="7a6ce-117">1\_4</span></span> | <span data-ttu-id="7a6ce-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a6ce-118">2\_0</span></span> | <span data-ttu-id="7a6ce-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7a6ce-119">2\_x</span></span> | <span data-ttu-id="7a6ce-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a6ce-120">2\_sw</span></span> | <span data-ttu-id="7a6ce-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a6ce-121">3\_0</span></span> | <span data-ttu-id="7a6ce-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a6ce-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7a6ce-123">texbem</span><span class="sxs-lookup"><span data-stu-id="7a6ce-123">texbem</span></span>                | <span data-ttu-id="7a6ce-124">x</span><span class="sxs-lookup"><span data-stu-id="7a6ce-124">x</span></span>    | <span data-ttu-id="7a6ce-125">x</span><span class="sxs-lookup"><span data-stu-id="7a6ce-125">x</span></span>    | <span data-ttu-id="7a6ce-126">x</span><span class="sxs-lookup"><span data-stu-id="7a6ce-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="7a6ce-127">Die roten und grünen Farbdaten im src-Register werden als Perturbation-Daten (du, DV) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span>

<span data-ttu-id="7a6ce-128">Diese Anweisung transformiert rote und grüne Komponenten im Quell Register mithilfe der 2D-Bump-Umgebungs mappingmatrix.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-128">This instruction transforms red and green components in the source register using the 2D bump environment-mapping matrix.</span></span> <span data-ttu-id="7a6ce-129">Das Ergebnis wird dem Texturkoordinaten Satz hinzugefügt, der der Ziel Registernummer entspricht, und wird zum Beispiel für die aktuelle Textur Phase verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-129">The result is added to the texture coordinate set corresponding to the destination register number, and is used to sample the current texture stage.</span></span>

<span data-ttu-id="7a6ce-130">Mit diesem Vorgang werden du und DV immer als signierte Mengen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-130">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="7a6ce-131">Für die Versionen 1 \_ 0 und 1 \_ 1 ist der Eingabe Modifizierer für die [Quell Registrierung mit signierter Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ bx2) für das Eingabe Argument nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-131">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="7a6ce-132">Diese Anweisung erzeugt definierte Ergebnisse, wenn Eingabe Texturen signierte Formatierungsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-132">This instruction produces defined results when input textures contain signed format data.</span></span> <span data-ttu-id="7a6ce-133">Daten im gemischten Format funktionieren nur, wenn die ersten beiden Kanäle signierte Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-133">Mixed format data works only if the first two channels contain signed data.</span></span> <span data-ttu-id="7a6ce-134">Weitere Informationen zu Oberflächen Formaten finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="7a6ce-134">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

<span data-ttu-id="7a6ce-135">Dies kann für eine Vielzahl von Techniken verwendet werden, die auf der Adress Umgebung basieren, einschließlich gefälschter Umgebungs Zuordnung pro Pixel und diffuses Beleuchtung (Bump-Zuordnung).</span><span class="sxs-lookup"><span data-stu-id="7a6ce-135">This can be used for a variety of techniques based on address perturbation, including fake per-pixel environment mapping and diffuse lighting (bump mapping).</span></span>

<span data-ttu-id="7a6ce-136">Bei der Verwendung dieser Anweisung müssen Textur Register der folgenden Sequenz folgen.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-136">When using this instruction, texture registers must follow the following sequence.</span></span>


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



<span data-ttu-id="7a6ce-137">Die Berechnungen in der Anweisung sind unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-137">The calculations done within the instruction are shown below.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



<span data-ttu-id="7a6ce-138">u ' = TextureCoordinates (Stufe m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (Phase m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (Phase m) \* t (n)<sub>G</sub> v ' = TextureCoordinates (Phase m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (Stufe m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (Phase m) \* t (n)<sub>G</sub> t (m)<sub>RGBA</sub> = texturesample (Stufe m)</span><span class="sxs-lookup"><span data-stu-id="7a6ce-138">u' = TextureCoordinates(stage m)<sub>u</sub> + D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub> v' = TextureCoordinates(stage m)<sub>v</sub> + D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub> t(m)<sub>RGBA</sub> = TextureSample(stage m)</span></span>

<span data-ttu-id="7a6ce-139">Verwenden von (u ', v ') als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="7a6ce-139">// using (u',v') as coordinates</span></span>

<span data-ttu-id="7a6ce-140">Das Registrieren von Daten, die von einer texbem-PS [-oder texbeml-PS-](texbeml---ps.md) Anweisung gelesen wurden, kann später nicht mehr gelesen werden, außer von anderen texbem-PS oder texbeml-PS.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-140">Register data that has been read by a texbem - ps or [texbeml - ps](texbeml---ps.md) instruction cannot be read later, except by another texbem - ps or texbeml - ps.</span></span>


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="7a6ce-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a6ce-141">Examples</span></span>

<span data-ttu-id="7a6ce-142">Hier ist ein Beispiel-Shader mit den identifizierten Textur Zuordnungen und den identifizierten Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-142">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="7a6ce-143">texbem erfordert die folgenden Texturen in den folgenden Textur Phasen.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-143">texbem requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="7a6ce-144">Phase 0 wird eine Bump Map mit (du-, DV-) perturingdaten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-144">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="7a6ce-145">Phase 1 verwendet eine Textur Zuordnung mit Farbdaten.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-145">Stage 1 uses a texture map with color data.</span></span>
-   <span data-ttu-id="7a6ce-146">Diese Anweisung legt die Matrix Daten auf der Textur Stufe fest, für die ein Sampling durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-146">This instruction sets the matrix data on the texture stage that is sampled.</span></span>
-   <span data-ttu-id="7a6ce-147">Dies unterscheidet sich von der Funktionalität der Fixed-Funktions Pipeline, bei der die Leistungsdaten und Matrizen dieselbe Textur Phase belegen.</span><span class="sxs-lookup"><span data-stu-id="7a6ce-147">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a6ce-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a6ce-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a6ce-149">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="7a6ce-149">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 