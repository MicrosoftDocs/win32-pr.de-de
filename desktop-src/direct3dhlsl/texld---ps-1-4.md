---
title: texld-ps_1_4
description: Lädt das Ziel Register mit Farbdaten (RGBA), wobei der Inhalt des Quell Registers als Texturkoordinaten verwendet wird. Die Stichproben Textur ist die Textur, die der Ziel Registernummer zugeordnet ist.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993143"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="a48db-104">texld-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a48db-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="a48db-105">Lädt das Ziel Register mit Farbdaten (RGBA), wobei der Inhalt des Quell Registers als Texturkoordinaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a48db-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="a48db-106">Die Stichproben Textur ist die Textur, die der Ziel Registernummer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a48db-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="a48db-107">texld DST, src</span><span class="sxs-lookup"><span data-stu-id="a48db-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="a48db-108">Register</span><span class="sxs-lookup"><span data-stu-id="a48db-108">Registers</span></span>



| <span data-ttu-id="a48db-109">Argument</span><span class="sxs-lookup"><span data-stu-id="a48db-109">Argument</span></span> | <span data-ttu-id="a48db-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a48db-110">Description</span></span>          | <span data-ttu-id="a48db-111">Register</span><span class="sxs-lookup"><span data-stu-id="a48db-111">Registers</span></span> |     |     |     | <span data-ttu-id="a48db-112">Version</span><span class="sxs-lookup"><span data-stu-id="a48db-112">Version</span></span>      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | <span data-ttu-id="a48db-113">VN</span><span class="sxs-lookup"><span data-stu-id="a48db-113">vₙ</span></span>        | <span data-ttu-id="a48db-114">2.300</span><span class="sxs-lookup"><span data-stu-id="a48db-114">cₙ</span></span>  | <span data-ttu-id="a48db-115">TN</span><span class="sxs-lookup"><span data-stu-id="a48db-115">tₙ</span></span>  | <span data-ttu-id="a48db-116">Mar</span><span class="sxs-lookup"><span data-stu-id="a48db-116">rₙ</span></span>  |              |
| <span data-ttu-id="a48db-117">DST</span><span class="sxs-lookup"><span data-stu-id="a48db-117">dst</span></span>      | <span data-ttu-id="a48db-118">Ziel Register</span><span class="sxs-lookup"><span data-stu-id="a48db-118">Destination register</span></span> |           |     |     | <span data-ttu-id="a48db-119">x</span><span class="sxs-lookup"><span data-stu-id="a48db-119">x</span></span>   | <span data-ttu-id="a48db-120">1\_4</span><span class="sxs-lookup"><span data-stu-id="a48db-120">1\_4</span></span>         |
| <span data-ttu-id="a48db-121">src</span><span class="sxs-lookup"><span data-stu-id="a48db-121">src</span></span>      | <span data-ttu-id="a48db-122">Quell Register</span><span class="sxs-lookup"><span data-stu-id="a48db-122">Source register</span></span>      |           |     | <span data-ttu-id="a48db-123">x</span><span class="sxs-lookup"><span data-stu-id="a48db-123">x</span></span>   |     | <span data-ttu-id="a48db-124">1 \_ 4 Phase 1</span><span class="sxs-lookup"><span data-stu-id="a48db-124">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="a48db-125">x</span><span class="sxs-lookup"><span data-stu-id="a48db-125">x</span></span>   | <span data-ttu-id="a48db-126">x</span><span class="sxs-lookup"><span data-stu-id="a48db-126">x</span></span>   | <span data-ttu-id="a48db-127">1 \_ 4-Phase</span><span class="sxs-lookup"><span data-stu-id="a48db-127">1\_4 phase</span></span>   |



 

<span data-ttu-id="a48db-128">Wenn Sie r (n) als Quell Register verwenden, müssen die ersten drei Komponenten (XYZ) in der vorherigen Phase des Shaders initialisiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="a48db-128">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="a48db-129">Weitere Informationen zu Registern finden Sie unter [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="a48db-129">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a48db-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a48db-130">Remarks</span></span>

<span data-ttu-id="a48db-131">Diese Anweisung gibt eine Stichprobe der Textur in der Textur Phase aus, die der Ziel Registernummer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a48db-131">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="a48db-132">Die Textur wird mithilfe von Texturkoordinaten Daten aus dem Quell Register entnommen.</span><span class="sxs-lookup"><span data-stu-id="a48db-132">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="a48db-133">Die Syntax für die Anweisungen texld und texcrd macht die Unterstützung für eine Projective Teilung mit einem Textur Register-Modifizierer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a48db-133">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="a48db-134">Für die Pixel-Shader-Version 1,4 \_ wird das Flag D3DTTFF projiziertes Textur Transform immer ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a48db-134">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="a48db-135">Regeln für die Verwendung von texld:</span><span class="sxs-lookup"><span data-stu-id="a48db-135">Rules for using texld:</span></span>

1.  <span data-ttu-id="a48db-136">Der gleiche. XYZ-oder. xyw-Modifizierer muss auf jeden Lesevorgang eines einzelnen t (n)-Registers in texcrd-oder texld-Anweisungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a48db-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="a48db-137">Wenn ". xyw" für t (n)-Registrierungs Lesevorgänge verwendet wird, kann dies mit anderen Lesevorgängen desselben t-Registers (n) mithilfe von. xyw DW gemischt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="a48db-137">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="a48db-138">Der- \_ Modifizierer für die DZ-Quelle ist nur für texld mit r (n)-Quell Register gültig (daher nur Phase 2).</span><span class="sxs-lookup"><span data-stu-id="a48db-138">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="a48db-139">Der- \_ Modifizierer für die DZ-Quelle darf nicht mehr als zwei Mal pro Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a48db-139">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="a48db-140">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="a48db-140">Pixel shader versions</span></span> | <span data-ttu-id="a48db-141">1\_1</span><span class="sxs-lookup"><span data-stu-id="a48db-141">1\_1</span></span> | <span data-ttu-id="a48db-142">1\_2</span><span class="sxs-lookup"><span data-stu-id="a48db-142">1\_2</span></span> | <span data-ttu-id="a48db-143">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a48db-143">1\_3</span></span> | <span data-ttu-id="a48db-144">1\_4</span><span class="sxs-lookup"><span data-stu-id="a48db-144">1\_4</span></span> | <span data-ttu-id="a48db-145">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a48db-145">2\_0</span></span> | <span data-ttu-id="a48db-146">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a48db-146">2\_x</span></span> | <span data-ttu-id="a48db-147">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a48db-147">2\_sw</span></span> | <span data-ttu-id="a48db-148">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a48db-148">3\_0</span></span> | <span data-ttu-id="a48db-149">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a48db-149">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a48db-150">texld</span><span class="sxs-lookup"><span data-stu-id="a48db-150">texld</span></span>                 |      |      |      | <span data-ttu-id="a48db-151">x</span><span class="sxs-lookup"><span data-stu-id="a48db-151">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="a48db-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a48db-152">Examples</span></span>

<span data-ttu-id="a48db-153">Die texld-Anweisung bietet eine gewisse Kontrolle darüber, welche Komponenten der Quell Textur Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a48db-153">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="a48db-154">Der vollständige Satz zulässiger Syntax für texld folgt und enthält alle gültigen Quell Registrierungs Modifizierern, Selektoren und Schreib Masken Kombinationen.</span><span class="sxs-lookup"><span data-stu-id="a48db-154">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a><span data-ttu-id="a48db-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a48db-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a48db-156">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="a48db-156">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




