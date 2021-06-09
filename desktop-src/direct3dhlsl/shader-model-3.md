---
title: Shadermodell 3 (HLSL-Referenz)
description: Vertex-Shader und Pixel-Shader werden erheblich von früheren Shaderversionen vereinfacht.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d87c791694e91de135052b4172e3bd5f55577d7
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827099"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="1ea43-103">Shadermodell 3 (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="1ea43-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="1ea43-104">Vertex-Shader und Pixel-Shader werden erheblich von früheren Shaderversionen vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1ea43-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="1ea43-105">Wenn Sie Shader in Hardware implementieren, verwenden Sie möglicherweise nicht im Vergleich zu 3 0 oder PS 3 0 mit anderen \_ \_ \_ Shaderversionen, und Sie verwenden keinen der Shadertypen mit der festen \_ Funktionspipeline.</span><span class="sxs-lookup"><span data-stu-id="1ea43-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="1ea43-106">Diese Änderungen ermöglichen es, Treiber und die Laufzeit zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="1ea43-107">Die einzige Ausnahme ist, dass Nur-Software-Shader im Vergleich zu \_ 3 \_ 0-Shadern mit jeder Pixel-Shaderversion verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1ea43-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="1ea43-108">Wenn Sie einen softwarebasierten Shader oder einen Shader 3 0 mit einer früheren Pixel-Shaderversion verwenden, kann der Vertex-Shader außerdem nur Ausgabesemantik verwenden, die mit flexiblen \_ \_ Vertexformatcodes (FVF) kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="1ea43-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="1ea43-109">Die für Vertex-Shader-Ausgaben verwendete Semantik muss für Pixel-Shadereingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="1ea43-110">Die Semantik wird verwendet, um die Vertex-Shader-Ausgaben den Pixel-Shadereingaben zu zuordnen, ähnlich wie die Vertexdeklaration den Vertex-Shader-Eingaberegistern und vorherigen Shadermodellen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="1ea43-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="1ea43-111">Weitere Informationen finden Sie unter Vergleichssemantik für Shader 3.0 und ps 3.0.</span><span class="sxs-lookup"><span data-stu-id="1ea43-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="1ea43-112">Zusätzliche Renderzustände im Umbruchmodus wurden hinzugefügt, um die Möglichkeit zusätzlicher Texturkoordinaten in diesem neuen Schema zu decken.</span><span class="sxs-lookup"><span data-stu-id="1ea43-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="1ea43-113">Attribute mit D3DDECLUSAGE TEXCOORD und verwendungsindex von 0 bis 15 werden im Wrap-Modus interpoliert, wenn der entsprechende \_ [**D3DRS \_ WRAP \***](/windows/desktop/direct3d9/d3drenderstatetype) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1ea43-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="1ea43-114">Vertex-Shadermodell 3-Features</span><span class="sxs-lookup"><span data-stu-id="1ea43-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="1ea43-115">Features des Pixels shader Model 3</span><span class="sxs-lookup"><span data-stu-id="1ea43-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="1ea43-116">Übereinstimmungssemantik für \_ 3 \_ 0- und PS \_ 3 \_ 0-Shader</span><span class="sxs-lookup"><span data-stu-id="1ea43-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="1ea43-117">Änderungen im Modus "Verschatten", "Tiefe" und "Schattierung"</span><span class="sxs-lookup"><span data-stu-id="1ea43-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="1ea43-118">Gleitkomma- und Ganzzahlkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="1ea43-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="1ea43-119">Angeben der vollständigen oder teilweisen Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="1ea43-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="1ea43-120">Softwarevertex- und Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="1ea43-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="1ea43-121">Vertex-Shadermodell 3-Features</span><span class="sxs-lookup"><span data-stu-id="1ea43-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="1ea43-122">Die Ausgaberegistertypen des Vertex-Shaders wurden in zwölf Register reduziert (siehe [Ausgaberegister](dx9-graphics-reference-asm-vs-registers-output.md)).</span><span class="sxs-lookup"><span data-stu-id="1ea43-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="1ea43-123">Jedes verwendete Register muss mithilfe der [dcl-Anweisung](dcl-usage---ps.md) und einer Semantik deklariert werden (z. B. dcl \_ color0 o0.xyzw).</span><span class="sxs-lookup"><span data-stu-id="1ea43-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="1ea43-124">Das 3 \_ 0-Vertex-Shadermodell (im Vergleich zu 3 0) erweitert die Features von vs. 2 0 mit einer leistungsfähigeren Registerindizierung, einer Reihe vereinfachter Ausgaberegister, der Möglichkeit, eine Textur in einem \_ \_ \_ Vertex-Shader zu beproben, und der Möglichkeit, die Rate zu steuern, mit der \_ Shadereingaben initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="1ea43-125">Indizieren beliebiger Register</span><span class="sxs-lookup"><span data-stu-id="1ea43-125">Index Any Register</span></span>

<span data-ttu-id="1ea43-126">Alle Register ( [Eingaberegister](dx9-graphics-reference-asm-vs-registers-input.md) und [Ausgaberegister](dx9-graphics-reference-asm-vs-registers-output.md)) können mithilfe des Schleifenzählerregisters indiziert werden [(nur](dx9-graphics-reference-asm-vs-registers-loop-counter.md) konstante Register konnten in früheren Versionen indiziert werden).</span><span class="sxs-lookup"><span data-stu-id="1ea43-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="1ea43-127">Sie müssen Eingabe- und Ausgaberegister deklarieren, bevor Sie sie indizieren.</span><span class="sxs-lookup"><span data-stu-id="1ea43-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="1ea43-128">Sie dürfen jedoch kein Ausgaberegister indizieren, das mit einer Semantik der Position oder Punktgröße deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ea43-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="1ea43-129">Wenn die Indizierung verwendet wird, müssen die Position und die Psize-Semantik in den Registern o0 bzw. o1 deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="1ea43-130">Sie dürfen nur einen kontinuierlichen Bereich von Registern indizieren. Das heißt, Sie können nicht über Register hinweg indizieren, die nicht deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="1ea43-131">Diese Einschränkung kann zwar unwesentlich sein, ermöglicht aber die Hardwareoptimierung.</span><span class="sxs-lookup"><span data-stu-id="1ea43-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="1ea43-132">Der Versuch, nicht zusammenhängende Register zu indizieren, führt zu nicht definierten Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="1ea43-133">Die Shaderüberprüfung erzwingt diese Einschränkung nicht.</span><span class="sxs-lookup"><span data-stu-id="1ea43-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="1ea43-134">Vereinfachen von Ausgaberegistern</span><span class="sxs-lookup"><span data-stu-id="1ea43-134">Simplify Output Registers</span></span>

<span data-ttu-id="1ea43-135">Alle verschiedenen Arten von Ausgaberegistern wurden in zwölf Ausgaberegister reduziert: 1 für Position, 2 für Farbe, 8 für Textur und 1 für Diess oder Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="1ea43-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="1ea43-136">Diese Register interpolieren alle Daten, die sie für den Pixel-Shader enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ea43-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="1ea43-137">Ausgaberegisterdeklarationen sind erforderlich, und jedem Register wird Semantik zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="1ea43-138">Die Register können wie folgt aufgeschlüsselt werden:</span><span class="sxs-lookup"><span data-stu-id="1ea43-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="1ea43-139">Mindestens ein Register muss als Positionsregister mit vier Komponenten deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="1ea43-140">Dies ist das einzige Vertex-Shaderregister, das erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1ea43-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="1ea43-141">Die ersten zehn Register, die von einem Shader verwendet werden, können maximal vier Komponenten (xyzw) verwenden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="1ea43-142">Das letzte (oder zwölfte) Register darf nur einen Skalar (z. B. Punktgröße) enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ea43-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="1ea43-143">Eine Liste der Register finden Sie unter [Register – im Vergleich zu \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="1ea43-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="1ea43-144">Texturbeispiel in einem Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="1ea43-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="1ea43-145">Vertex-Shader 3 \_ 0 unterstützt Die Textursuche im Vertex-Shader mit [texldl im Vergleich zu](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="1ea43-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="1ea43-146">Features des Pixels shader Model 3</span><span class="sxs-lookup"><span data-stu-id="1ea43-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="1ea43-147">Die Pixel-Shaderfarbe und texturregister wurden in zehn Eingaberegister reduziert (siehe [Eingaberegistertypen](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="1ea43-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="1ea43-148">Das Gesichtsregister ist ein Gleitkommaskalarregister.</span><span class="sxs-lookup"><span data-stu-id="1ea43-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="1ea43-149">Nur das Vorzeichen dieses Registers ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1ea43-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="1ea43-150">Wenn das Vorzeichen negativ ist, handelt es sich bei dem Primitiv um ein Gesicht im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="1ea43-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="1ea43-151">Dies kann beispielsweise in einem Pixel-Shader verwendet werden, um eine zweiseitige Beleuchtung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="1ea43-152">Das Positionsregister verweist auf die aktuellen Pixel (x,y).</span><span class="sxs-lookup"><span data-stu-id="1ea43-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="1ea43-153">Die Shader-Konstantenregister können mithilfe von festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1ea43-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="1ea43-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="1ea43-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="1ea43-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="1ea43-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="1ea43-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="1ea43-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="1ea43-157">Übereinstimmungssemantik für \_ 3 \_ 0- und PS \_ 3 \_ 0-Shader</span><span class="sxs-lookup"><span data-stu-id="1ea43-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="1ea43-158">Es gibt einige Einschränkungen bei der semantischen Verwendung im Vergleich \_ zu 3 \_ 0 und ps \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="1ea43-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="1ea43-159">Im Allgemeinen müssen Sie vorsichtig sein, wenn Sie eine Semantik für eine Shadereingabe verwenden, die einer Semantik entspricht, die für eine Shaderausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ea43-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="1ea43-160">Beispielsweise packt dieser Pixel-Shader mehrere Namen in ein Register:</span><span class="sxs-lookup"><span data-stu-id="1ea43-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="1ea43-161">Jedes Register hat eine andere Semantik.</span><span class="sxs-lookup"><span data-stu-id="1ea43-161">Each register has a different semantic.</span></span> <span data-ttu-id="1ea43-162">Beachten Sie, dass Sie auch v0.x und v0.yz mit unterschiedlicher (mehrfacher) Semantik benennen können, da die Schreibmaske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ea43-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="1ea43-163">Angesichts des Pixels shaders kann der folgende und \_ der folgende \_ 3 0-Shader nicht mit ihm gekoppelt werden:</span><span class="sxs-lookup"><span data-stu-id="1ea43-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="1ea43-164">Diese beiden Shader stehen in Konflikt mit der Verwendung der [**Semantik D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) und **D3DDECLUSAGE \_ TEXCOORD1.**</span><span class="sxs-lookup"><span data-stu-id="1ea43-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="1ea43-165">Schreiben Sie den Vertex-Shader wie diesen um, um die semantische Kollision zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="1ea43-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="1ea43-166">Ebenso kann ein semantischer Name, der in verschiedenen Eingaberegistern im Pixel-Shader deklariert ist (v0 und v1 im Pixel-Shader), nicht in einem einzelnen Ausgaberegister in diesem Vertex-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="1ea43-167">Dieser Vertex-Shader kann beispielsweise nicht mit dem Pixel-Shader gekoppelt werden, da D3DDECLUSAGE TEXCOORD1 sowohl für Pixel-Shadereingaberegister (v0, v1) als auch für das \_ Vertex-Shader-Ausgaberegister o3 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ea43-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="1ea43-168">Andererseits kann dieser Vertex-Shader nicht mit dem Pixel-Shader gekoppelt werden, da die Ausgabemaske für einen Parameter mit einer bestimmten Semantik nicht die vom Pixel-Shader angeforderten Daten enthält:</span><span class="sxs-lookup"><span data-stu-id="1ea43-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="1ea43-169">Dieser Vertex-Shader stellt keine Ausgabe mit einem der vom Pixel-Shader angeforderten semantischen Namen zur Verfügung, sodass die Shaderkopplung ungültig ist:</span><span class="sxs-lookup"><span data-stu-id="1ea43-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="1ea43-170">Änderungen im Modus "Verschatten", "Tiefe" und "Schattierung"</span><span class="sxs-lookup"><span data-stu-id="1ea43-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="1ea43-171">Wenn D3DRS SHADEMODE während der Clipping- und Dreiecksrasterung für flache Schattierung festgelegt ist, werden Attribute mit \_ D3DDECLUSAGE COLOR als flach schattiert \_ interpoliert.</span><span class="sxs-lookup"><span data-stu-id="1ea43-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="1ea43-172">Wenn Komponenten eines Registers mit einer Farbsemantik deklariert werden, andere Komponenten desselben Registers jedoch eine andere Semantik erhalten, ist die flache Schattierungsinterpolation (linear im Vergleich zu flach) für die Komponenten in diesem Register ohne Farbsemantik nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1ea43-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="1ea43-173">Wenn ein Rendern von 3 0 und ps 3 0 gewünscht ist, müssen \_ \_ \_ \_ Shader 3 0 und 3 0 -Shader Eine-0-Shader implementieren.</span><span class="sxs-lookup"><span data-stu-id="1ea43-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="1ea43-174">Außerhalb der Shader werden keine Berechnungsberechnungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ea43-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="1ea43-175">Es gibt kein Register in vs. 3 0, und es wurden zusätzliche Semantiken D3DDECLUSAGE CT (für den pro Scheitelpunkt berechneten Blendfaktor) und \_ \_ \_ D3DDECLUSAGE DEPTH (für die Übergabe eines Tiefenwerts an den Pixel-Shader zum Berechnen des Blendfaktors \_ des Blendings) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1ea43-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="1ea43-176">Der Texturphasenzustand D3DTSS TEXCOORDINDEX wird ignoriert, wenn \_ der Pixel-Shader 3.0 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ea43-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="1ea43-177">Die folgenden Werte wurden hinzugefügt, um diese Änderungen zu reagieren:</span><span class="sxs-lookup"><span data-stu-id="1ea43-177">The following values have been added to accommodate these changes:</span></span>


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="1ea43-178">Gleitkomma- und Ganzzahlkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="1ea43-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="1ea43-179">Gleitkomma-Berechnungen werden mit unterschiedlicher Genauigkeit und unterschiedlichen Bereichen (16-Bit, 24-Bit und 32-Bit) in unterschiedlichen Teilen der Pipeline erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1ea43-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="1ea43-180">Ein Wert, der größer ist als der dynamische Bereich der Pipeline, die in diese Pipeline eintritt (z. B. wird eine 32-Bit-Gleitkommatexturzuordnung in eine 24-Bit-Float-Pipeline in PS \_ 2 0 entnommen), erzeugt ein nicht definiertes \_ Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="1ea43-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="1ea43-181">Für ein vorhersagbares Verhalten sollten Sie einen solchen Wert an das Maximum des dynamischen Bereichs klammern.</span><span class="sxs-lookup"><span data-stu-id="1ea43-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="1ea43-182">Die Konvertierung von einem Gleitkommawert in eine ganze Zahl erfolgt an mehreren Stellen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="1ea43-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="1ea43-183">Beim Auftreten einer [mova- vs-Anweisung.](mova---vs.md)</span><span class="sxs-lookup"><span data-stu-id="1ea43-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="1ea43-184">Während der Textur adressierung.</span><span class="sxs-lookup"><span data-stu-id="1ea43-184">During texture addressing.</span></span>
-   <span data-ttu-id="1ea43-185">Beim Schreiben in ein Renderziel ohne Gleitkomma.</span><span class="sxs-lookup"><span data-stu-id="1ea43-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="1ea43-186">Angeben der vollständigen oder teilweisen Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="1ea43-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="1ea43-187">Sowohl ps \_ 3 \_ 0 als auch ps \_ 2 \_ x bieten Unterstützung für zwei Genauigkeitsstufen:</span><span class="sxs-lookup"><span data-stu-id="1ea43-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



| <span data-ttu-id="1ea43-188">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ea43-188">ps\_3\_0</span></span> | <span data-ttu-id="1ea43-189">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ea43-189">ps\_2\_0</span></span> | <span data-ttu-id="1ea43-190">Precision</span><span class="sxs-lookup"><span data-stu-id="1ea43-190">Precision</span></span>         | <span data-ttu-id="1ea43-191">Wert</span><span class="sxs-lookup"><span data-stu-id="1ea43-191">Value</span></span>                |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="1ea43-192">x</span><span class="sxs-lookup"><span data-stu-id="1ea43-192">x</span></span>        |          | <span data-ttu-id="1ea43-193">Vollständig</span><span class="sxs-lookup"><span data-stu-id="1ea43-193">Full</span></span>              | <span data-ttu-id="1ea43-194">fp32 oder höher</span><span class="sxs-lookup"><span data-stu-id="1ea43-194">fp32 or higher</span></span>       |
| <span data-ttu-id="1ea43-195">x</span><span class="sxs-lookup"><span data-stu-id="1ea43-195">x</span></span>        |          | <span data-ttu-id="1ea43-196">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="1ea43-196">Partial precision</span></span> | <span data-ttu-id="1ea43-197">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="1ea43-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="1ea43-198">x</span><span class="sxs-lookup"><span data-stu-id="1ea43-198">x</span></span>        | <span data-ttu-id="1ea43-199">x</span><span class="sxs-lookup"><span data-stu-id="1ea43-199">x</span></span>        | <span data-ttu-id="1ea43-200">Vollständig</span><span class="sxs-lookup"><span data-stu-id="1ea43-200">Full</span></span>              | <span data-ttu-id="1ea43-201">fp24=s16e7 oder höher</span><span class="sxs-lookup"><span data-stu-id="1ea43-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="1ea43-202">x</span><span class="sxs-lookup"><span data-stu-id="1ea43-202">x</span></span>        | <span data-ttu-id="1ea43-203">x</span><span class="sxs-lookup"><span data-stu-id="1ea43-203">x</span></span>        | <span data-ttu-id="1ea43-204">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="1ea43-204">Partial precision</span></span> | <span data-ttu-id="1ea43-205">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="1ea43-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="1ea43-206">ps \_ 3 \_ 0 unterstützt eine größere Genauigkeit als ps \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="1ea43-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="1ea43-207">Standardmäßig werden alle Vorgänge auf der Ebene der vollständigen Genauigkeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ea43-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="1ea43-208">Teilgenauigkeit (siehe [Pixelshader-Registermodifizierer)](dx9-graphics-reference-asm-ps-registers-modifiers.md)wird angefordert, indem der \_ pp-Modifizierer dem Shadercode hinzugefügt wird (sofern die zugrunde liegende Implementierung dies unterstützt).</span><span class="sxs-lookup"><span data-stu-id="1ea43-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="1ea43-209">Implementierungen können den Modifizierer immer ignorieren und die betroffenen Vorgänge mit voller Genauigkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="1ea43-210">Der \_ pp-Modifizierer kann in zwei Kontexten auftreten:</span><span class="sxs-lookup"><span data-stu-id="1ea43-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="1ea43-211">In einer Texturkoordinatendeklaration, um Texturkoordinaten mit teilweiser Genauigkeit an den Pixelshader zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="1ea43-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="1ea43-212">Dies kann verwendet werden, wenn Texturkoordinaten Farbdaten an den Pixelshader weiterleiten, was in einigen Implementierungen mit teilweiser Genauigkeit schneller als mit vollständiger Genauigkeit sein kann.</span><span class="sxs-lookup"><span data-stu-id="1ea43-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="1ea43-213">Für jede Anweisung, die Verwendung von teilgenauer Genauigkeit anzufordern, einschließlich Anweisungen zum Laden von Texturen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="1ea43-214">Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein Ergebnis mit teilweiser Genauigkeit speichern darf.</span><span class="sxs-lookup"><span data-stu-id="1ea43-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="1ea43-215">Wenn kein expliziter Modifizierer vorhanden ist, muss die Anweisung mit voller Genauigkeit ausgeführt werden (unabhängig von der Genauigkeit der Eingabeopernden).</span><span class="sxs-lookup"><span data-stu-id="1ea43-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="1ea43-216">Eine Anwendung entscheidet sich möglicherweise absichtlich dafür, die Genauigkeit auf die Leistung abzuhandeln.</span><span class="sxs-lookup"><span data-stu-id="1ea43-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="1ea43-217">Es gibt verschiedene Arten von Shadereingabedaten, die natürliche Kandidaten für die Verarbeitung teilweiser Genauigkeit sind:</span><span class="sxs-lookup"><span data-stu-id="1ea43-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="1ea43-218">Farb iteratoren werden durch Werte mit teilweiser Genauigkeit gut dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1ea43-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="1ea43-219">Texturwerte aus den meisten Formaten können genau durch Werte mit teilweiser Genauigkeit dargestellt werden (Werte aus 32-Bit-Gleitkommaformattexturen sind eine offensichtliche Ausnahme).</span><span class="sxs-lookup"><span data-stu-id="1ea43-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="1ea43-220">Konstanten können entsprechend dem Shader durch eine Darstellung mit teilweiser Genauigkeit dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1ea43-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="1ea43-221">In all diesen Fällen kann der Entwickler eine Teilgenauigkeit angeben, um die Daten zu verarbeiten, da er weiß, dass keine Genauigkeit der Eingabedaten verloren geht.</span><span class="sxs-lookup"><span data-stu-id="1ea43-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="1ea43-222">In einigen Fällen erfordert ein Shader möglicherweise, dass die internen Schritte einer Berechnung mit voller Genauigkeit ausgeführt werden, auch wenn eingabe- und endgültige Ausgabewerte nicht mehr als eine partielle Genauigkeit aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="1ea43-223">Softwarevertex- und Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="1ea43-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="1ea43-224">Softwareimplementierungen (Laufzeit und Referenz für Vertex-Shader und Referenz für Pixel-Shader) von Shadern der Version 2 \_ 0 und höher haben eine gewisse Überprüfung gelockert.</span><span class="sxs-lookup"><span data-stu-id="1ea43-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="1ea43-225">Dies ist für Debug- und Prototypzwecke nützlich.</span><span class="sxs-lookup"><span data-stu-id="1ea43-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="1ea43-226">Die Anwendung gibt der Runtime/dem Assembler an, dass sie einen Teil der Validierung mithilfe des Flags sw im Assembler gelockert haben muss \_ (z. B. im Vergleich zu \_ 2 \_ SW).</span><span class="sxs-lookup"><span data-stu-id="1ea43-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="1ea43-227">Ein Software-Shader funktioniert nicht mit Hardware.</span><span class="sxs-lookup"><span data-stu-id="1ea43-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="1ea43-228">Vs \_ 2 \_ sw ist ein Ausgleich für die maximalen Obergrenzen von vs \_ 2 \_ x; ebenso ist ps \_ 2 sw ein \_ Abstrich auf die maximalen Obergrenzen von ps \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="1ea43-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="1ea43-229">Insbesondere werden die folgenden Überprüfungen gelockert:</span><span class="sxs-lookup"><span data-stu-id="1ea43-229">Specifically, the following validations are relaxed:</span></span>



| <span data-ttu-id="1ea43-230">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1ea43-230">Shader model</span></span>                                           |  <span data-ttu-id="1ea43-231">Resource</span><span class="sxs-lookup"><span data-stu-id="1ea43-231">Resource</span></span>                                    |  <span data-ttu-id="1ea43-232">Begrenzung</span><span class="sxs-lookup"><span data-stu-id="1ea43-232">Limit</span></span>                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea43-233">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="1ea43-234">Anweisungsanzahl</span><span class="sxs-lookup"><span data-stu-id="1ea43-234">Instruction Counts</span></span>                   | <span data-ttu-id="1ea43-235">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="1ea43-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="1ea43-236">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="1ea43-237">Float-Konstantenregister</span><span class="sxs-lookup"><span data-stu-id="1ea43-237">Float Constant Registers</span></span>             | <span data-ttu-id="1ea43-238">8192</span><span class="sxs-lookup"><span data-stu-id="1ea43-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="1ea43-239">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="1ea43-240">Integer Constant Registers</span><span class="sxs-lookup"><span data-stu-id="1ea43-240">Integer Constant Registers</span></span>           | <span data-ttu-id="1ea43-241">2048</span><span class="sxs-lookup"><span data-stu-id="1ea43-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="1ea43-242">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="1ea43-243">Boolesche Konstantenregister</span><span class="sxs-lookup"><span data-stu-id="1ea43-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="1ea43-244">2048</span><span class="sxs-lookup"><span data-stu-id="1ea43-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="1ea43-245">ps \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="1ea43-246">Abhängige Lesetiefe</span><span class="sxs-lookup"><span data-stu-id="1ea43-246">Dependent-read depth</span></span>                 | <span data-ttu-id="1ea43-247">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="1ea43-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="1ea43-248">vs \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="1ea43-249">Anweisungen und Bezeichnungen für die Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="1ea43-249">flow control instructions and labels</span></span> | <span data-ttu-id="1ea43-250">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="1ea43-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="1ea43-251">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="1ea43-252">Start/Schritt/Anzahl der Schleifen</span><span class="sxs-lookup"><span data-stu-id="1ea43-252">Loop start/step/counts</span></span>               | <span data-ttu-id="1ea43-253">Die Größe von Iterationsstart- und Iterationsschritten für Rep- und Schleifenanweisungen sind 32-Bit-Ganzzahlen mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="1ea43-254">Die Anzahl kann bis zu \_ MAX. INT/64 sein.</span><span class="sxs-lookup"><span data-stu-id="1ea43-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="1ea43-255">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="1ea43-256">Portlimits</span><span class="sxs-lookup"><span data-stu-id="1ea43-256">Port limits</span></span>                          | <span data-ttu-id="1ea43-257">Portlimits für alle Registerdateien werden gelockert.</span><span class="sxs-lookup"><span data-stu-id="1ea43-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="1ea43-258">vs \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="1ea43-259">Anzahl der Interpolatoren</span><span class="sxs-lookup"><span data-stu-id="1ea43-259">Number of interpolators</span></span>              | <span data-ttu-id="1ea43-260">16 Ausgaberegister in vs \_ 3 \_ sw.</span><span class="sxs-lookup"><span data-stu-id="1ea43-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="1ea43-261">ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ea43-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="1ea43-262">Anzahl der Interpolatoren</span><span class="sxs-lookup"><span data-stu-id="1ea43-262">Number of interpolators</span></span>              | <span data-ttu-id="1ea43-263">14(16-2) Eingaberegister für ps \_ 3 \_ sw.</span><span class="sxs-lookup"><span data-stu-id="1ea43-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="1ea43-264">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ea43-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea43-265">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ea43-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
