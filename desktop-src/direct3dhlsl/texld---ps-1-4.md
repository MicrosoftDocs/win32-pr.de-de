---
title: texld – ps_1_4
description: Lädt das Zielregister mit Farbdaten (RGBA), die mithilfe des Inhalts des Quellregisters als Texturkoordinaten entnommen wurden. Die entnommene Textur ist die Textur, die der Zielregisternummer zugeordnet ist.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d956d9176a6356dc3837ee4f4d13b5bb700dda98
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118825"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="b73a9-104">texld – ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b73a9-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="b73a9-105">Lädt das Zielregister mit Farbdaten (RGBA), die mithilfe des Inhalts des Quellregisters als Texturkoordinaten entnommen wurden.</span><span class="sxs-lookup"><span data-stu-id="b73a9-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="b73a9-106">Die entnommene Textur ist die Textur, die der Zielregisternummer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b73a9-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="b73a9-107">texld dst, src</span><span class="sxs-lookup"><span data-stu-id="b73a9-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="b73a9-108">Register</span><span class="sxs-lookup"><span data-stu-id="b73a9-108">Registers</span></span>



| <span data-ttu-id="b73a9-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b73a9-109">Value</span></span>         | <span data-ttu-id="b73a9-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b73a9-110">Description</span></span>                     | <span data-ttu-id="b73a9-111">vn</span><span class="sxs-lookup"><span data-stu-id="b73a9-111">vₙ</span></span>        | <span data-ttu-id="b73a9-112">Cn</span><span class="sxs-lookup"><span data-stu-id="b73a9-112">cₙ</span></span>  | <span data-ttu-id="b73a9-113">Tn</span><span class="sxs-lookup"><span data-stu-id="b73a9-113">tₙ</span></span>  | <span data-ttu-id="b73a9-114">Rn</span><span class="sxs-lookup"><span data-stu-id="b73a9-114">rₙ</span></span>  | <span data-ttu-id="b73a9-115">Pixel-Shaderversion</span><span class="sxs-lookup"><span data-stu-id="b73a9-115">Pixel shader version</span></span>              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="b73a9-116">dst</span><span class="sxs-lookup"><span data-stu-id="b73a9-116">dst</span></span>      | <span data-ttu-id="b73a9-117">Zielregister</span><span class="sxs-lookup"><span data-stu-id="b73a9-117">Destination register</span></span> |           |     |     | <span data-ttu-id="b73a9-118">x</span><span class="sxs-lookup"><span data-stu-id="b73a9-118">x</span></span>   | <span data-ttu-id="b73a9-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="b73a9-119">1\_4</span></span>         |
| <span data-ttu-id="b73a9-120">src</span><span class="sxs-lookup"><span data-stu-id="b73a9-120">src</span></span>      | <span data-ttu-id="b73a9-121">Quellregister</span><span class="sxs-lookup"><span data-stu-id="b73a9-121">Source register</span></span>      |           |     | <span data-ttu-id="b73a9-122">x</span><span class="sxs-lookup"><span data-stu-id="b73a9-122">x</span></span>   |     | <span data-ttu-id="b73a9-123">1 \_ 4 Phase 1</span><span class="sxs-lookup"><span data-stu-id="b73a9-123">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="b73a9-124">x</span><span class="sxs-lookup"><span data-stu-id="b73a9-124">x</span></span>   | <span data-ttu-id="b73a9-125">x</span><span class="sxs-lookup"><span data-stu-id="b73a9-125">x</span></span>   | <span data-ttu-id="b73a9-126">1 \_ 4 Phase</span><span class="sxs-lookup"><span data-stu-id="b73a9-126">1\_4 phase</span></span>   |



 

<span data-ttu-id="b73a9-127">Bei Verwendung von r(n) als Quellregister müssen die ersten drei Komponenten (XYZ) in der vorherigen Phase des Shaders initialisiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="b73a9-127">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="b73a9-128">Weitere Informationen zu Registern finden Sie unter [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register.](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)</span><span class="sxs-lookup"><span data-stu-id="b73a9-128">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b73a9-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b73a9-129">Remarks</span></span>

<span data-ttu-id="b73a9-130">Diese Anweisung untersucht die Textur in der Texturphase, die der Zielregisternummer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b73a9-130">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="b73a9-131">Die Textur wird mithilfe von Texturkoordinatendaten aus dem Quellregister entnommen.</span><span class="sxs-lookup"><span data-stu-id="b73a9-131">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="b73a9-132">Die Syntax für die Anweisungen texld und texcrd macht Unterstützung für eine projektive Division mit einem Texturregistermodifizierer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b73a9-132">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="b73a9-133">Für Die Pixel-Shaderversion 1.4 wird das D3DTTFF \_ PROJECTED-Texturtransformationsflag immer ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b73a9-133">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="b73a9-134">Regeln für die Verwendung von texld:</span><span class="sxs-lookup"><span data-stu-id="b73a9-134">Rules for using texld:</span></span>

1.  <span data-ttu-id="b73a9-135">Der gleiche MODIFI-Modifizierer ".xyz" oder ".xyw" muss sowohl in texcrd- als auch in texld-Anweisungen auf jeden Leses eines einzelnen t(n)-Registers angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b73a9-135">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="b73a9-136">Wenn .xyw für t(n)-Registerlesedaten verwendet wird, kann dies mit anderen Lesezeichen desselben t(n)-Registers mithilfe von .xyw dw gemischt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="b73a9-136">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="b73a9-137">Der \_ Quellcodemodifizierer ist nur für texld mit dem Quellregister r(n) gültig (daher nur Phase 2).</span><span class="sxs-lookup"><span data-stu-id="b73a9-137">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="b73a9-138">Der \_ Quellmodifizierer kann nicht mehr als zweimal pro Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b73a9-138">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="b73a9-139">Pixel-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="b73a9-139">Pixel shader versions</span></span> | <span data-ttu-id="b73a9-140">1\_1</span><span class="sxs-lookup"><span data-stu-id="b73a9-140">1\_1</span></span> | <span data-ttu-id="b73a9-141">1\_2</span><span class="sxs-lookup"><span data-stu-id="b73a9-141">1\_2</span></span> | <span data-ttu-id="b73a9-142">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b73a9-142">1\_3</span></span> | <span data-ttu-id="b73a9-143">1\_4</span><span class="sxs-lookup"><span data-stu-id="b73a9-143">1\_4</span></span> | <span data-ttu-id="b73a9-144">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b73a9-144">2\_0</span></span> | <span data-ttu-id="b73a9-145">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b73a9-145">2\_x</span></span> | <span data-ttu-id="b73a9-146">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b73a9-146">2\_sw</span></span> | <span data-ttu-id="b73a9-147">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b73a9-147">3\_0</span></span> | <span data-ttu-id="b73a9-148">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b73a9-148">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b73a9-149">texld</span><span class="sxs-lookup"><span data-stu-id="b73a9-149">texld</span></span>                 |      |      |      | <span data-ttu-id="b73a9-150">x</span><span class="sxs-lookup"><span data-stu-id="b73a9-150">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="b73a9-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b73a9-151">Examples</span></span>

<span data-ttu-id="b73a9-152">Die texld-Anweisung bietet eine gewisse Kontrolle darüber, welche Komponenten der Quelltexturkoordinatendaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b73a9-152">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="b73a9-153">Der vollständige Satz zulässiger Syntax für texld folgt und enthält alle gültigen Quellregistermodifizierer, Selektoren und Schreibmaskenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="b73a9-153">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b73a9-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b73a9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b73a9-155">Anweisungen für Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="b73a9-155">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




