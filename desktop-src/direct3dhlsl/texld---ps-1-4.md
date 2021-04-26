---
title: texld – ps_1_4
description: Lädt das Zielregister mit Farbdaten (RGBA), die mit dem Inhalt des Quellregisters als Texturkoordinaten entnommen wurden. Die Textur mit Stichproben ist die Textur, die der Zielregisternummer zugeordnet ist.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996867"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="037b4-104">texld - ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="037b4-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="037b4-105">Lädt das Zielregister mit Farbdaten (RGBA), die mit dem Inhalt des Quellregisters als Texturkoordinaten entnommen wurden.</span><span class="sxs-lookup"><span data-stu-id="037b4-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="037b4-106">Die Textur mit Stichproben ist die Textur, die der Zielregisternummer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="037b4-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="037b4-107">texld dst, src</span><span class="sxs-lookup"><span data-stu-id="037b4-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="037b4-108">Register</span><span class="sxs-lookup"><span data-stu-id="037b4-108">Registers</span></span>



|          |                      | <span data-ttu-id="037b4-109">vn</span><span class="sxs-lookup"><span data-stu-id="037b4-109">vₙ</span></span>        | <span data-ttu-id="037b4-110">Cn</span><span class="sxs-lookup"><span data-stu-id="037b4-110">cₙ</span></span>  | <span data-ttu-id="037b4-111">Tn</span><span class="sxs-lookup"><span data-stu-id="037b4-111">tₙ</span></span>  | <span data-ttu-id="037b4-112">Rn</span><span class="sxs-lookup"><span data-stu-id="037b4-112">rₙ</span></span>  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="037b4-113">dst</span><span class="sxs-lookup"><span data-stu-id="037b4-113">dst</span></span>      | <span data-ttu-id="037b4-114">Zielregister</span><span class="sxs-lookup"><span data-stu-id="037b4-114">Destination register</span></span> |           |     |     | <span data-ttu-id="037b4-115">x</span><span class="sxs-lookup"><span data-stu-id="037b4-115">x</span></span>   | <span data-ttu-id="037b4-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="037b4-116">1\_4</span></span>         |
| <span data-ttu-id="037b4-117">src</span><span class="sxs-lookup"><span data-stu-id="037b4-117">src</span></span>      | <span data-ttu-id="037b4-118">Quellregister</span><span class="sxs-lookup"><span data-stu-id="037b4-118">Source register</span></span>      |           |     | <span data-ttu-id="037b4-119">x</span><span class="sxs-lookup"><span data-stu-id="037b4-119">x</span></span>   |     | <span data-ttu-id="037b4-120">1 \_ 4. Phase 1</span><span class="sxs-lookup"><span data-stu-id="037b4-120">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="037b4-121">x</span><span class="sxs-lookup"><span data-stu-id="037b4-121">x</span></span>   | <span data-ttu-id="037b4-122">x</span><span class="sxs-lookup"><span data-stu-id="037b4-122">x</span></span>   | <span data-ttu-id="037b4-123">1 \_ 4 Phase</span><span class="sxs-lookup"><span data-stu-id="037b4-123">1\_4 phase</span></span>   |



 

<span data-ttu-id="037b4-124">Wenn Sie r(n) als Quellregister verwenden, müssen die ersten drei Komponenten (XYZ) in der vorherigen Phase des Shaders initialisiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="037b4-124">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="037b4-125">Weitere Informationen zu Registern finden Sie unter [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register.](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)</span><span class="sxs-lookup"><span data-stu-id="037b4-125">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="037b4-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="037b4-126">Remarks</span></span>

<span data-ttu-id="037b4-127">Diese Anweisung erfasst die Textur in der Texturphase, die der Zielregisternummer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="037b4-127">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="037b4-128">Die Textur wird mithilfe von Texturkoordinatendaten aus dem Quellregister entnommen.</span><span class="sxs-lookup"><span data-stu-id="037b4-128">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="037b4-129">Die Syntax für die Texld- und Texcrd-Anweisungen macht Unterstützung für eine projektive Division mit einem Texturregistermodifizierer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="037b4-129">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="037b4-130">Für die Pixelshaderversion 1.4 wird das D3DTTFF \_ PROJECTED-Texturtransformationsflag immer ignoriert.</span><span class="sxs-lookup"><span data-stu-id="037b4-130">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="037b4-131">Regeln für die Verwendung von texld:</span><span class="sxs-lookup"><span data-stu-id="037b4-131">Rules for using texld:</span></span>

1.  <span data-ttu-id="037b4-132">Der gleiche .xyz- oder .xyw-Modifizierer muss auf jeden Lese- eines einzelnen t(n)-Registers in texcrd- oder texld-Anweisungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="037b4-132">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="037b4-133">Wenn .xyw für t(n)-Registerleseungen verwendet wird, kann dies mit anderen Lesezeichen desselben t(n)-Registers mit .xyw dw kombiniert \_ werden.</span><span class="sxs-lookup"><span data-stu-id="037b4-133">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="037b4-134">Der \_ dz-Quellmodifizierer ist nur für texld mit r(n) source register (also nur Phase 2) gültig.</span><span class="sxs-lookup"><span data-stu-id="037b4-134">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="037b4-135">Der \_ dz-Quellmodifizierer kann nicht mehr als zweimal pro Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="037b4-135">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="037b4-136">Pixelshaderversionen</span><span class="sxs-lookup"><span data-stu-id="037b4-136">Pixel shader versions</span></span> | <span data-ttu-id="037b4-137">1\_1</span><span class="sxs-lookup"><span data-stu-id="037b4-137">1\_1</span></span> | <span data-ttu-id="037b4-138">1\_2</span><span class="sxs-lookup"><span data-stu-id="037b4-138">1\_2</span></span> | <span data-ttu-id="037b4-139">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="037b4-139">1\_3</span></span> | <span data-ttu-id="037b4-140">1\_4</span><span class="sxs-lookup"><span data-stu-id="037b4-140">1\_4</span></span> | <span data-ttu-id="037b4-141">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="037b4-141">2\_0</span></span> | <span data-ttu-id="037b4-142">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="037b4-142">2\_x</span></span> | <span data-ttu-id="037b4-143">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="037b4-143">2\_sw</span></span> | <span data-ttu-id="037b4-144">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="037b4-144">3\_0</span></span> | <span data-ttu-id="037b4-145">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="037b4-145">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="037b4-146">texld</span><span class="sxs-lookup"><span data-stu-id="037b4-146">texld</span></span>                 |      |      |      | <span data-ttu-id="037b4-147">x</span><span class="sxs-lookup"><span data-stu-id="037b4-147">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="037b4-148">Beispiele</span><span class="sxs-lookup"><span data-stu-id="037b4-148">Examples</span></span>

<span data-ttu-id="037b4-149">Die texld-Anweisung bietet eine gewisse Kontrolle darüber, welche Komponenten der Quelltexturkoordinatendaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="037b4-149">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="037b4-150">Der vollständige Satz zulässiger Syntax für texld folgt und enthält alle gültigen Quellregistermodifizierer, Selektoren und Schreibmaskenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="037b4-150">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="037b4-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="037b4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="037b4-152">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="037b4-152">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




