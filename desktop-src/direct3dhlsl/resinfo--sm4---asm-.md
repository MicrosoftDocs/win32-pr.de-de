---
title: ResInfo (SM4-ASM)
description: Abfragen der Dimensionen einer bestimmten Eingabe Ressource.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389523"
---
# <a name="resinfo-sm4---asm"></a><span data-ttu-id="76a7e-103">ResInfo (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="76a7e-103">resinfo (sm4 - asm)</span></span>

<span data-ttu-id="76a7e-104">Abfragen der Dimensionen einer bestimmten Eingabe Ressource.</span><span class="sxs-lookup"><span data-stu-id="76a7e-104">Query the dimensions of a given input resource.</span></span>



| <span data-ttu-id="76a7e-105">ResInfo \[ \_ uint </span><span class="sxs-lookup"><span data-stu-id="76a7e-105">resinfo\[\_uint</span></span>\|<span data-ttu-id="76a7e-106">\_rcpfloat \] dest \[ . mask \] , srcmiplevel. Select \_ Component, srkresource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="76a7e-106">\_rcpFloat\] dest\[.mask\], srcMipLevel.select\_component, srcResource\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="76a7e-107">Element</span><span class="sxs-lookup"><span data-stu-id="76a7e-107">Item</span></span>                                                                                                               | <span data-ttu-id="76a7e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76a7e-108">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="76a7e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="76a7e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="76a7e-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="76a7e-110">\[in\] The address of the result of the operation.</span></span><br/>                             |
| <span data-ttu-id="76a7e-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcmiplevel*</span><span class="sxs-lookup"><span data-stu-id="76a7e-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span></span><br/> | <span data-ttu-id="76a7e-112">\[auf \] der MIP-Ebene.</span><span class="sxs-lookup"><span data-stu-id="76a7e-112">\[in\] The mip level.</span></span><br/>                                                          |
| <span data-ttu-id="76a7e-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="76a7e-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="76a7e-114">\[in \] einer t- \# oder u- \# Eingabe Textur, für die die Dimensionen abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="76a7e-114">\[in\] A t\# or u\# input texture for which the dimensions are being queried.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="76a7e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76a7e-115">Remarks</span></span>

<span data-ttu-id="76a7e-116">*srcmiplevel* wird als ganzzahliger Skalarwert ohne Vorzeichen gelesen, sodass eine einzelne Komponentenauswahl für das Quell Register erforderlich ist, wenn es sich nicht um einen skalaren unmittelbaren Wert handelt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-116">*srcMipLevel* is read as an unsigned integer scalar so a single component selector is required for the source register, if it is not a scalar immediate value.</span></span>

<span data-ttu-id="76a7e-117">*dest* empfängt \[ Breite, Höhe, Tiefe oder Array Größe, gesamter MIP-Count \] , von der Schreib Maske ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-117">*dest* receives \[width, height, depth or array size, total-mip-count\], selected by the write mask.</span></span>

<span data-ttu-id="76a7e-118">Die zurückgegebenen Werte für Breite, Höhe und Tiefe gelten für die durch den *srcmiplevel* -Parameter ausgewählte MIP-Ebene und sind unabhängig von der texgrößengröße in der Anzahl von texeln.</span><span class="sxs-lookup"><span data-stu-id="76a7e-118">The returned width, height and depth values are for the mip-level selected by the *srcMipLevel* parameter, and are in number of texels, independent of texel data size.</span></span> <span data-ttu-id="76a7e-119">Bei Multisampling-Ressourcen (texture2D \[ array \] MS \# ) werden Breite und Höhe auch in Texels und nicht in Beispielen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76a7e-119">For multisample resources (texture2D\[Array\]MS\#), width and height are also returned in texels, not samples.</span></span>

<span data-ttu-id="76a7e-120">Der *srcmiplevel* -Parameter hat keine Auswirkungen auf die Gesamtanzahl der in *dest. w* zurückgegebenen MIP-Anzahl.</span><span class="sxs-lookup"><span data-stu-id="76a7e-120">The total mip count returned in *dest.w* is unaffected by the *srcMipLevel* parameter.</span></span>

<span data-ttu-id="76a7e-121">Bei UAVs (u \# ) ist die Anzahl der MIP-Ebenen immer 1.</span><span class="sxs-lookup"><span data-stu-id="76a7e-121">For UAVs (u\#), the number of mip levels is always 1.</span></span>

<span data-ttu-id="76a7e-122">Alle Aspekte dieser Anweisung basieren auf den Merkmalen der Ressourcen Sicht, die an t \# /u gebunden \# ist, nicht an der zugrunde liegenden Basis Ressource.</span><span class="sxs-lookup"><span data-stu-id="76a7e-122">All aspects of this instruction are based on the characteristics of the resource view bound at the t\#/u\#, not the underlying base resource.</span></span>

<span data-ttu-id="76a7e-123">Zurückgegebene Werte sind alle Gleit Komma Werte, es sei denn \_ , der uint-Modifizierer wird verwendet. in diesem Fall sind die zurückgegebenen Werte alle Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="76a7e-123">Returned values are all floating point, unless the \_uint modifier is used, in which case the returned values are all integers.</span></span> <span data-ttu-id="76a7e-124">Wenn der \_ rcpfloat-Modifizierer verwendet wird, sind alle zurückgegebenen Werte Gleit Komma Werte, und die Breite, Höhe und Tiefe werden als Gegenstücke (1.0 f/Width, 1.0 f/Height, 1.0 f/Tiefe) zurückgegeben, einschließlich inf, wenn "width/height/Tiefe" den Wert "0" für das außerhalb des gültigen *srcmiplevel*</span><span class="sxs-lookup"><span data-stu-id="76a7e-124">If the \_rcpFloat modifier is used, all returned values are floating point, and the width, height and depth are returned as reciprocals (1.0f/width, 1.0f/height, 1.0f/depth), including INF if width/height/depth are 0 from out-of-range *srcMipLevel* behavior.</span></span> <span data-ttu-id="76a7e-125">Der \_ rcpfloat-Modifizierer gilt nur für Werte vom Typ "width", "Height" und "Tiefe" und gilt nicht für Werte, die auf "0" festgelegt sind und daher nicht zurückgegeben werden, und gilt nicht für die Rückgabe von Array Größen.</span><span class="sxs-lookup"><span data-stu-id="76a7e-125">The \_rcpFloat modifier only applies to width, height, and depth returned values and does not apply to values that are set to 0 and thus not returned, and also does not apply to array size returns.</span></span>

<span data-ttu-id="76a7e-126">Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="76a7e-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="76a7e-127">Wenn *srkresource* ein Texture1D ist, wird Width in *dest. x* zurückgegeben, und *dest. YZ* wird auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-127">If *srcResource* is a Texture1D, then width is returned in *dest.x*, and *dest.yz* are set to 0.</span></span>

<span data-ttu-id="76a7e-128">Wenn *srkresource* ein Texture1DArray ist, wird "width" in " *dest. x*" zurückgegeben, die Array Größe wird in " *dest. y*" zurückgegeben, und " *dest. z* " wird auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-128">If *srcResource* is a Texture1DArray, then width is returned in *dest.x*, the array size is returned in *dest.y*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="76a7e-129">Wenn *srkresource* ein Texture2D-Wert ist, werden Width und height in " *dest. XY*" zurückgegeben, und " *dest. z* " wird auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-129">If *srcResource* is a Texture2D, then width and height are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="76a7e-130">Wenn *srkresource* ein Texture2DArray ist, werden Width und height in " *dest. XY*" zurückgegeben, und die Array Größe wird in " *dest. z*" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76a7e-130">If *srcResource* is a Texture2DArray, then width and height are returned in *dest.xy*, and the array size is returned in *dest.z*.</span></span>

<span data-ttu-id="76a7e-131">Wenn *srkresource* ein Texture3D-Wert ist, werden Width, Height und Tiefe in *dest.XYZ* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76a7e-131">If *srcResource* is a Texture3D, then width, height and depth are returned in *dest.xyz*.</span></span>

<span data-ttu-id="76a7e-132">Wenn *srkresource* ein texturecube-Element ist, werden die Breite und Höhe der einzelnen Dimensions Abmessungen in " *dest. XY*" zurückgegeben, und " *dest. z* " wird auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-132">If *srcResource* is a TextureCube, then the width and height of the individual cube face dimensions are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="76a7e-133">Wenn *srkresource* ein texturecubearray ist, werden die Dimensionen Breite und Höhe in den Dimensionen " *dest. XY*" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76a7e-133">If *srcResource* is a TextureCubeArray, then the width and height the individual cube face dimensions are returned in *dest.xy*.</span></span> <span data-ttu-id="76a7e-134">" *dest. z* " ist auf einen nicht definierten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-134">*dest.z* is set to an undefined value.</span></span>

<span data-ttu-id="76a7e-135">Wenn für *srkresource* die MIP-Klammer pro Ressource angegeben wurde, gibt ResInfo unabhängig von der Klammer immer die Gesamtzahl von Mipmaps in der Ansicht für die MIP-Anzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="76a7e-135">If the a per-resource mip clamp has been specified on *srcResource*, resinfo always returns the total number of mipmaps in the view for the mip count, regardless of the clamp.</span></span> <span data-ttu-id="76a7e-136">Wenn jedoch die Dimensionen einer bestimmten miplevel von ResInfo angefordert werden und die miplevel-Methode ausgeschaltet wurde (z. b. eine Klammer von 2,2 bedeutet, dass MIPS 0 und 1 geklemmt wurden), sind die zurückgegebenen Dimensionen nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="76a7e-136">However, if the dimensions of a given miplevel are requested by resinfo and the miplevel has been clamped off (e.g. a clamp of 2.2 means that mips 0 and 1 have been clamped off), the dimensions returned are undefined.</span></span> <span data-ttu-id="76a7e-137">Einige Implementierungen geben das Verhalten von außerhalb des gültigen Bereichs für ResInfo zurück, wenn sich die miplevel außerhalb des gültigen Bereichs befindet.</span><span class="sxs-lookup"><span data-stu-id="76a7e-137">Some implementations will return the out of bounds behavior specified for resinfo when the miplevel is out of range.</span></span> <span data-ttu-id="76a7e-138">Andere Implementierungen geben die Dimensionen des MIP so zurück, als würden Sie nicht geklammert werden.</span><span class="sxs-lookup"><span data-stu-id="76a7e-138">Other implementations will return the dimensions of the mip as if it had not been clamped.</span></span>

### <a name="restrictions"></a><span data-ttu-id="76a7e-139">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="76a7e-139">Restrictions</span></span>

-   <span data-ttu-id="76a7e-140">*srkresource* muss ein t- \# oder u-Register sein, \# das kein Puffer ist, sondern eine Textur ist \* .</span><span class="sxs-lookup"><span data-stu-id="76a7e-140">*srcResource* must be a t\# or u\# register that is not a Buffer, but is a Texture\*.</span></span>
-   <span data-ttu-id="76a7e-141">Die relative Adressierung von *srkresource* ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="76a7e-141">Relative addressing of *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="76a7e-142">*srcmiplevel* muss eine einzelne Komponentenauswahl verwenden, wenn es sich nicht um eine sofortige skalare handelt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-142">*srcMipLevel* must use a single component selector if it is not a scalar immediate.</span></span>
-   <span data-ttu-id="76a7e-143">Durch das Abrufen von t \# oder u \# , das nichts daran gebunden ist, wird 0 für Breite, Höhe, Tiefe oder arraySize und "Total-MIP-count" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76a7e-143">Fetching from t\# or u\# that has nothing bound to it returns 0 for width, height, depth or arraysize, and total-mip-count.</span></span> <span data-ttu-id="76a7e-144">Der \_ rcpfloat-Modifizierer wird in diesem Fall immer noch berücksichtigt und gibt daher inf für die anwendbaren zurückgegebenen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="76a7e-144">The \_rcpFloat modifier is still honored in this case, thus returning INF for the applicable returned values.</span></span>
-   <span data-ttu-id="76a7e-145">Wenn *srcmiplevel* außerhalb des Bereichs der verfügbaren Anzahl von miplevels in der Ressource liegt, ist das Verhalten der Größen Rückgabe (*dest.XYZ*) identisch mit der einer ungebundenen t- \# oder u- \# Ressource.</span><span class="sxs-lookup"><span data-stu-id="76a7e-145">If *srcMipLevel* is out of the range of the available number of miplevels in the resource, the behavior for the size return (*dest.xyz*) is identical to that of an unbound t\# or u\# resource.</span></span> <span data-ttu-id="76a7e-146">Die gesamte MIP-Anzahl wird in diesem Fall weiterhin in " *dest. w* " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76a7e-146">The total mip count is still returned in *dest.w* for this case.</span></span>

<span data-ttu-id="76a7e-147">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="76a7e-147">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="76a7e-148">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="76a7e-148">Vertex Shader</span></span> | <span data-ttu-id="76a7e-149">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="76a7e-149">Geometry Shader</span></span> | <span data-ttu-id="76a7e-150">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="76a7e-150">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="76a7e-151">x</span><span class="sxs-lookup"><span data-stu-id="76a7e-151">x</span></span>             | <span data-ttu-id="76a7e-152">x</span><span class="sxs-lookup"><span data-stu-id="76a7e-152">x</span></span>               | <span data-ttu-id="76a7e-153">x</span><span class="sxs-lookup"><span data-stu-id="76a7e-153">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="76a7e-154">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="76a7e-154">Minimum Shader Model</span></span>

<span data-ttu-id="76a7e-155">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76a7e-155">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="76a7e-156">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="76a7e-156">Shader Model</span></span>                                              | <span data-ttu-id="76a7e-157">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="76a7e-157">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="76a7e-158">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="76a7e-158">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="76a7e-159">ja</span><span class="sxs-lookup"><span data-stu-id="76a7e-159">yes</span></span>       |
| [<span data-ttu-id="76a7e-160">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="76a7e-160">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="76a7e-161">ja</span><span class="sxs-lookup"><span data-stu-id="76a7e-161">yes</span></span>       |
| [<span data-ttu-id="76a7e-162">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="76a7e-162">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="76a7e-163">ja</span><span class="sxs-lookup"><span data-stu-id="76a7e-163">yes</span></span>       |
| [<span data-ttu-id="76a7e-164">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a7e-164">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="76a7e-165">nein</span><span class="sxs-lookup"><span data-stu-id="76a7e-165">no</span></span>        |
| [<span data-ttu-id="76a7e-166">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a7e-166">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="76a7e-167">nein</span><span class="sxs-lookup"><span data-stu-id="76a7e-167">no</span></span>        |
| [<span data-ttu-id="76a7e-168">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a7e-168">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="76a7e-169">nein</span><span class="sxs-lookup"><span data-stu-id="76a7e-169">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="76a7e-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76a7e-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76a7e-171">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a7e-171">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





