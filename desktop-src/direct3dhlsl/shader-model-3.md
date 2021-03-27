---
title: Shader-Modell 3 (HLSL-Referenz)
description: Vertex-Shader und Pixel-Shader werden aus früheren shaderversionen erheblich vereinfacht.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390500"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="65601-103">Shader-Modell 3 (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="65601-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="65601-104">Vertex-Shader und Pixel-Shader werden aus früheren shaderversionen erheblich vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="65601-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="65601-105">Wenn Sie Shader in Hardware implementieren, dürfen Sie vs \_ 3 \_ 0 oder PS \_ 3 \_ 0 nicht mit anderen shaderversionen verwenden, und Sie dürfen keinen shadertyp mit der Fixed-Funktions Pipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="65601-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="65601-106">Diese Änderungen ermöglichen es, Treiber und die Laufzeit zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="65601-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="65601-107">Die einzige Ausnahme besteht darin, dass nur-Software-oder \_ 3- \_ 0-Shader mit jeder Pixel-Shader-Version verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="65601-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="65601-108">Wenn Sie einen reinen Software-vs \_ 3 \_ 0-Shader mit einer früheren Pixel-Shader-Version verwenden, kann der Vertex-Shader außerdem nur Ausgabe Semantik verwenden, die mit flexiblen Scheitelpunkt Formaten (FVF) kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="65601-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="65601-109">Die für Vertex-Shader-Ausgaben verwendete Semantik muss für Pixel-shadereingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65601-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="65601-110">Die Semantik wird verwendet, um die Vertex-shaderausgaben den Pixel-shadereingaben zuzuordnen, ähnlich wie die Vertex-Deklaration den Vertex-Shader-Eingabe Registern und früheren shadermodellen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="65601-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="65601-111">Weitere Informationen finden Sie unter Match Semantik on vs 3,0 and PS 3,0 Shaders.</span><span class="sxs-lookup"><span data-stu-id="65601-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="65601-112">Zusätzliche Rendermodus-renderzustände wurden hinzugefügt, um die Möglichkeit zusätzlicher Texturkoordinaten in diesem neuen Schema abzudecken.</span><span class="sxs-lookup"><span data-stu-id="65601-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="65601-113">Attribute mit D3DDECLUSAGE \_ texcoord und der Verwendungs Index von 0 bis 15 werden im Umbruch Modus interpoliert, wenn der entsprechende [**D3DRS \_ Wrap \***](/windows/desktop/direct3d9/d3drenderstatetype) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="65601-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="65601-114">Vertex-Shader Model 3-Features</span><span class="sxs-lookup"><span data-stu-id="65601-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="65601-115">Pixel Shader Model 3-Features</span><span class="sxs-lookup"><span data-stu-id="65601-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="65601-116">Übereinstimmungs Semantik für vs \_ 3 \_ 0-und PS \_ 3 \_ 0-Shader</span><span class="sxs-lookup"><span data-stu-id="65601-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="65601-117">Änderungen bei Nebel, Tiefe und Schattierungs Modus</span><span class="sxs-lookup"><span data-stu-id="65601-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="65601-118">Gleit Komma-und Integer-Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="65601-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="65601-119">Angeben der vollständigen oder partiellen Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="65601-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="65601-120">Software Scheitelpunkt und Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="65601-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="65601-121">Vertex-Shader Model 3-Features</span><span class="sxs-lookup"><span data-stu-id="65601-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="65601-122">Die Vertex-Shader-Ausgabe Registrierungs Typen wurden in zwölf Register (siehe [Ausgabe Register](dx9-graphics-reference-asm-vs-registers-output.md)) reduziert.</span><span class="sxs-lookup"><span data-stu-id="65601-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="65601-123">Jedes verwendete Register muss mithilfe der [DCL](dcl-usage---ps.md) -Anweisung und einer Semantik (z. b. dcl \_ color0 o0. xyzw) deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="65601-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="65601-124">Das 3 \_ 0-Vertex-Shader-Modell (vs \_ 3 \_ 0) erweitert die Features von vs \_ 2 \_ 0 mit einer leistungsfähigeren Registrierungs Indizierung, einer Reihe von vereinfachten Ausgabe Registern, der Möglichkeit, eine Textur in einem Vertex-Shader zu modellieren, sowie der Möglichkeit, die Rate zu steuern, mit der shadereingaben initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="65601-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="65601-125">Index beliebiger Register</span><span class="sxs-lookup"><span data-stu-id="65601-125">Index Any Register</span></span>

<span data-ttu-id="65601-126">Alle Register ( [Eingabe Register](dx9-graphics-reference-asm-vs-registers-input.md) und [Ausgabe Register](dx9-graphics-reference-asm-vs-registers-output.md)) können mithilfe des [Schleifen Leistungs Zählers](dx9-graphics-reference-asm-vs-registers-loop-counter.md) indiziert werden (in früheren Versionen konnten nur konstante Register indiziert werden.)</span><span class="sxs-lookup"><span data-stu-id="65601-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="65601-127">Vor der Indizierung müssen Sie die Eingabe-und Ausgabe Register deklarieren.</span><span class="sxs-lookup"><span data-stu-id="65601-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="65601-128">Allerdings können Sie keine Ausgabe Register indizieren, die mit einer Semantik der Positions-oder Punktgröße deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="65601-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="65601-129">Tatsächlich muss die Position und die Psize-Semantik in den o0-und O1-Registern deklariert werden, wenn die Indizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65601-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="65601-130">Sie können nur einen kontinuierlichen Bereich von Registern indizieren. Das heißt, Sie können nicht über Register hinweg indizieren, die nicht deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="65601-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="65601-131">Diese Einschränkung kann zwar unpraktisch sein, Sie ermöglicht jedoch eine Hardware Optimierung.</span><span class="sxs-lookup"><span data-stu-id="65601-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="65601-132">Wenn Sie versuchen, über nicht zusammenhängende Register zu indizieren, werden nicht definierte Ergebnisse erzeugt.</span><span class="sxs-lookup"><span data-stu-id="65601-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="65601-133">Die Shader-Überprüfung erzwingt diese Einschränkung nicht.</span><span class="sxs-lookup"><span data-stu-id="65601-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="65601-134">Vereinfachen von Ausgabe Registern</span><span class="sxs-lookup"><span data-stu-id="65601-134">Simplify Output Registers</span></span>

<span data-ttu-id="65601-135">Alle verschiedenen Typen von Ausgabe Registern wurden in zwölf Ausgabe Register reduziert: 1 für Position, 2 für Farbe, 8 für Textur und 1 für Nebel oder Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="65601-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="65601-136">Diese Register interpolieren alle Daten, die Sie für den Pixelshader enthalten.</span><span class="sxs-lookup"><span data-stu-id="65601-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="65601-137">Ausgabe Register Deklarationen sind erforderlich, und die Semantik wird jedem Register zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="65601-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="65601-138">Die Register können wie folgt aufgegliedert werden:</span><span class="sxs-lookup"><span data-stu-id="65601-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="65601-139">Mindestens ein Register muss als ein vier-Komponenten-Positions Register deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="65601-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="65601-140">Dies ist das einzige erforderliche Vertex-Shader-Register.</span><span class="sxs-lookup"><span data-stu-id="65601-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="65601-141">Die ersten zehn von einem Shader genutzten Register können maximal vier Komponenten (xyzw) verwenden.</span><span class="sxs-lookup"><span data-stu-id="65601-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="65601-142">Das letzte (oder zwölfte) Register darf nur ein Skalar (z. b. die Punktgröße) enthalten.</span><span class="sxs-lookup"><span data-stu-id="65601-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="65601-143">Eine Auflistung der Register finden Sie unter [Registern-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="65601-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="65601-144">Textur Beispiel in einem Scheitelpunkt-Shader</span><span class="sxs-lookup"><span data-stu-id="65601-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="65601-145">Vertex Shader 3 \_ 0 unterstützt Textur Suche im Vertex-Shader mithilfe von [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="65601-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="65601-146">Pixel Shader Model 3-Features</span><span class="sxs-lookup"><span data-stu-id="65601-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="65601-147">Die Pixel-Shader-Farbe und Textur Register wurden in zehn Eingabe Register reduziert (siehe [Eingabe Register Typen](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="65601-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="65601-148">Das Gesichts Register ist ein Gleit Komma-skalarregister.</span><span class="sxs-lookup"><span data-stu-id="65601-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="65601-149">Nur das Vorzeichen dieses Registers ist gültig.</span><span class="sxs-lookup"><span data-stu-id="65601-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="65601-150">Wenn das Vorzeichen negativ ist, ist der primitive ein Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="65601-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="65601-151">Dies kann beispielsweise in einem Pixelshader verwendet werden, um eine zweiseitige Beleuchtung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="65601-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="65601-152">Das Positions Register verweist auf die aktuellen (x, y) Pixel.</span><span class="sxs-lookup"><span data-stu-id="65601-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="65601-153">Die Shader-Konstanten Register können mithilfe von festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="65601-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="65601-154">**Setpixelshaderconstantb**</span><span class="sxs-lookup"><span data-stu-id="65601-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="65601-155">**Setpixelshaderconstanti**</span><span class="sxs-lookup"><span data-stu-id="65601-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="65601-156">**Setpixelshaderconstantf**</span><span class="sxs-lookup"><span data-stu-id="65601-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="65601-157">Übereinstimmungs Semantik für vs \_ 3 \_ 0-und PS \_ 3 \_ 0-Shader</span><span class="sxs-lookup"><span data-stu-id="65601-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="65601-158">Es gibt einige Einschränkungen bei der semantischen Verwendung mit vs \_ 3 \_ 0 und PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="65601-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="65601-159">Im Allgemeinen müssen Sie sorgfältig vorgehen, wenn Sie eine Semantik für eine Shadereingabe verwenden, die einer für eine shaderausgabe verwendeten Semantik entspricht.</span><span class="sxs-lookup"><span data-stu-id="65601-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="65601-160">Beispielsweise packt dieser Pixel-Shader mehrere Namen in ein Register:</span><span class="sxs-lookup"><span data-stu-id="65601-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="65601-161">Jedes Register weist eine andere Semantik auf.</span><span class="sxs-lookup"><span data-stu-id="65601-161">Each register has a different semantic.</span></span> <span data-ttu-id="65601-162">Beachten Sie, dass Sie auch "v0. x" und "v0. YZ" mit einer anderen (mehrfachen) Semantik benennen können, weil die Schreib Maske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65601-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="65601-163">Wenn der Pixelshader angegeben ist, kann der folgende vs \_ 3 \_ 0-Shader nicht mit ihm gekoppelt werden:</span><span class="sxs-lookup"><span data-stu-id="65601-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="65601-164">Diese beiden Shader stehen in Konflikt mit der Verwendung der Semantik [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) und **D3DDECLUSAGE \_ TEXCOORD1** .</span><span class="sxs-lookup"><span data-stu-id="65601-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="65601-165">Schreiben Sie den Vertex-Shader wie folgt um, um die semantische Kollision zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="65601-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="65601-166">Ebenso kann ein semantischer Name, der für verschiedene Eingabe Register im Pixelshader (V0 und v1 im Pixelshader) deklariert ist, nicht in einem einzelnen Ausgabe Register in diesem Vertex-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65601-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="65601-167">Dieser Vertex-Shader kann z. b. nicht mit dem Pixelshader gekoppelt werden, da D3DDECLUSAGE \_ TEXCOORD1 sowohl für Pixel-Shader-Eingabe Register (v0, v1) als auch für das Vertex-Shader-Ausgabe Register (O3) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65601-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="65601-168">Der Vertex-Shader kann dagegen nicht mit dem Pixelshader kombiniert werden, da die Ausgabe Maske für einen Parameter mit einer gegebenen Semantik nicht die vom Pixelshader angeforderten Daten bereitstellt:</span><span class="sxs-lookup"><span data-stu-id="65601-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="65601-169">Dieser Vertex-Shader stellt keine Ausgabe mit einem der vom Pixelshader angeforderten semantischen Namen bereit, sodass die Shader-Kopplung ungültig ist:</span><span class="sxs-lookup"><span data-stu-id="65601-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


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



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="65601-170">Änderungen bei Nebel, Tiefe und Schattierungs Modus</span><span class="sxs-lookup"><span data-stu-id="65601-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="65601-171">Wenn D3DRS \_ SHADEMODE für die flache Schattierung während Clipping und Dreieck-rasterisierung festgelegt ist, werden Attribute mit D3DDECLUSAGE- \_ Farbe als flach schattiert interpoliert.</span><span class="sxs-lookup"><span data-stu-id="65601-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="65601-172">Wenn alle Komponenten eines Registers mit einer Farb Semantik deklariert sind, aber andere Komponenten desselben Registers unterschiedliche Semantik aufweisen, ist die flache Schattierungs Interpolation (Linear und Flat) für die Komponenten in, die ohne Farb Semantik registriert werden, nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="65601-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="65601-173">Wenn ein Nebel Rendering gewünscht ist, \_ müssen vs 3 \_ 0-und PS \_ 3 \_ 0-Shader Nebel implementieren.</span><span class="sxs-lookup"><span data-stu-id="65601-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="65601-174">Außerhalb der Shader werden keine Nebel Berechnungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="65601-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="65601-175">In vs 3 0 gibt es kein Nebel Register \_ \_ , und zusätzliche Semantik D3DDECLUSAGE \_ Nebel (für die Berechnung pro Scheitelpunkt pro Scheitelpunkt) und die D3DDECLUSAGE- \_ Tiefe (für die Übergabe eines tiefen Werts an den Pixelshader zur Berechnung des Nebel Blend-Faktors) wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="65601-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="65601-176">Textur Phasen Status D3DTSS \_ texcoordindex wird bei Verwendung von Pixel Shader 3,0 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="65601-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="65601-177">Die folgenden Werte wurden hinzugefügt, um diese Änderungen zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="65601-177">The following values have been added to accommodate these changes:</span></span>


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



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="65601-178">Gleit Komma-und Integer-Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="65601-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="65601-179">Gleit Komma Berechnungen werden in verschiedenen Teilen der Pipeline mit unterschiedlichen Genauigkeit und Bereichen (16-Bit, 24-Bit und 32-Bit) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65601-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="65601-180">Ein Wert, der größer ist als der dynamische Bereich der Pipeline, der in diese Pipeline Eintritt (z. b. eine 32-Bit-Float-Textur Zuordnung wird in PS 2 0 in eine 24-Bit-Float-Pipeline entnommen), wird \_ \_ ein nicht definiertes Ergebnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="65601-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="65601-181">Für ein vorhersagbares Verhalten sollten Sie einen solchen Wert an den dynamischen Bereichs Wert binden.</span><span class="sxs-lookup"><span data-stu-id="65601-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="65601-182">Die Konvertierung von einem Gleit Komma Wert in eine Ganzzahl erfolgt an verschiedenen Stellen, z. b.:</span><span class="sxs-lookup"><span data-stu-id="65601-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="65601-183">Wenn eine " [MUVA-vs"-](mova---vs.md) Anweisung auftritt.</span><span class="sxs-lookup"><span data-stu-id="65601-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="65601-184">Während der Textur Adressierung.</span><span class="sxs-lookup"><span data-stu-id="65601-184">During texture addressing.</span></span>
-   <span data-ttu-id="65601-185">Beim Schreiben in ein nicht Gleit Komma-Renderziel.</span><span class="sxs-lookup"><span data-stu-id="65601-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="65601-186">Angeben der vollständigen oder partiellen Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="65601-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="65601-187">Sowohl PS \_ 3 \_ 0 als auch PS \_ 2 \_ x bieten Unterstützung für zwei Genauigkeits Stufen:</span><span class="sxs-lookup"><span data-stu-id="65601-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="65601-188">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="65601-188">ps\_3\_0</span></span> | <span data-ttu-id="65601-189">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="65601-189">ps\_2\_0</span></span> | <span data-ttu-id="65601-190">Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="65601-190">Precision</span></span>         | <span data-ttu-id="65601-191">Wert</span><span class="sxs-lookup"><span data-stu-id="65601-191">Value</span></span>                |
| <span data-ttu-id="65601-192">x</span><span class="sxs-lookup"><span data-stu-id="65601-192">x</span></span>        |          | <span data-ttu-id="65601-193">Vollständig</span><span class="sxs-lookup"><span data-stu-id="65601-193">Full</span></span>              | <span data-ttu-id="65601-194">FP32 oder höher</span><span class="sxs-lookup"><span data-stu-id="65601-194">fp32 or higher</span></span>       |
| <span data-ttu-id="65601-195">x</span><span class="sxs-lookup"><span data-stu-id="65601-195">x</span></span>        |          | <span data-ttu-id="65601-196">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="65601-196">Partial precision</span></span> | <span data-ttu-id="65601-197">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="65601-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="65601-198">x</span><span class="sxs-lookup"><span data-stu-id="65601-198">x</span></span>        | <span data-ttu-id="65601-199">x</span><span class="sxs-lookup"><span data-stu-id="65601-199">x</span></span>        | <span data-ttu-id="65601-200">Vollständig</span><span class="sxs-lookup"><span data-stu-id="65601-200">Full</span></span>              | <span data-ttu-id="65601-201">fp24 = s16e7 oder höher</span><span class="sxs-lookup"><span data-stu-id="65601-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="65601-202">x</span><span class="sxs-lookup"><span data-stu-id="65601-202">x</span></span>        | <span data-ttu-id="65601-203">x</span><span class="sxs-lookup"><span data-stu-id="65601-203">x</span></span>        | <span data-ttu-id="65601-204">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="65601-204">Partial precision</span></span> | <span data-ttu-id="65601-205">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="65601-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="65601-206">PS \_ 3 \_ 0 unterstützt mehr Genauigkeit als PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="65601-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="65601-207">Standardmäßig erfolgen alle Vorgänge auf der Ebene mit vollständiger Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="65601-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="65601-208">Die partielle Genauigkeit (Weitere Informationen finden Sie unter " [Pixel-Shader-registrierungsmodifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md)") wird durch Hinzufügen des \_ PP-Modifizierers zum Shader-Code angefordert</span><span class="sxs-lookup"><span data-stu-id="65601-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="65601-209">Implementierungen können den-Modifizierer jederzeit ignorieren und die betroffenen Vorgänge mit vollständiger Genauigkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="65601-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="65601-210">Der \_ PP-Modifizierer kann in zwei Kontexten vorkommen:</span><span class="sxs-lookup"><span data-stu-id="65601-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="65601-211">In einer Texturkoordinaten Deklaration, um Texturkoordinaten mit partieller Genauigkeit an den Pixelshader zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="65601-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="65601-212">Dieser Wert kann verwendet werden, wenn die Textur Daten an den Pixelshader weiterleitet, was bei einigen Implementierungen mit einer partiellen Genauigkeit schneller ist als mit der vollständigen Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="65601-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="65601-213">Bei einer beliebigen Anweisung, um die Verwendung der partiellen Genauigkeit, einschließlich der Anweisungen zum Laden von Text, anzufordern.</span><span class="sxs-lookup"><span data-stu-id="65601-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="65601-214">Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein Ergebnis mit teilweiser Genauigkeit speichern darf.</span><span class="sxs-lookup"><span data-stu-id="65601-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="65601-215">Wenn kein expliziter Modifizierer vorhanden ist, muss die Anweisung mit vollständiger Genauigkeit (unabhängig von der Genauigkeit der Eingabe Operanden) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="65601-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="65601-216">Eine Anwendung kann sich bewusst entscheiden, dass die Genauigkeit der Leistung beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="65601-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="65601-217">Es gibt verschiedene Arten von shadereingabedaten, die natürliche Kandidaten für die Verarbeitung mit teilweiser Genauigkeit sind:</span><span class="sxs-lookup"><span data-stu-id="65601-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="65601-218">Farbiteratoren werden durch Werte mit partieller Genauigkeit gut dargestellt.</span><span class="sxs-lookup"><span data-stu-id="65601-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="65601-219">Textur Werte aus den meisten Formaten können durch partielle Genauigkeits Werte genau dargestellt werden (Werte, die von 32-Bit entnommen werden, und es handelt sich um eine offensichtliche Ausnahme).</span><span class="sxs-lookup"><span data-stu-id="65601-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="65601-220">Konstanten können entsprechend dem Shader durch eine Darstellung mit partieller Genauigkeit dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="65601-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="65601-221">In all diesen Fällen kann der Entwickler eine partielle Genauigkeit angeben, um die Daten zu verarbeiten. dabei ist zu erkennen, dass keine Genauigkeit der Eingabedaten verloren geht.</span><span class="sxs-lookup"><span data-stu-id="65601-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="65601-222">In einigen Fällen erfordert ein Shader möglicherweise, dass die internen Schritte einer Berechnung mit vollständiger Genauigkeit durchgeführt werden, auch wenn Eingabe-und endgültige Ausgabewerte nicht mehr als partielle Genauigkeit aufweisen.</span><span class="sxs-lookup"><span data-stu-id="65601-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="65601-223">Software Scheitelpunkt und Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="65601-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="65601-224">Für Software Implementierungen (Laufzeit und Verweis für Vertex-Shader und Referenz für Pixel-Shader) der Versionen 2 \_ 0-Shader und höher wird die Validierung gelockert.</span><span class="sxs-lookup"><span data-stu-id="65601-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="65601-225">Dies ist nützlich für das Debuggen und das Prototypen.</span><span class="sxs-lookup"><span data-stu-id="65601-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="65601-226">Die Anwendung zeigt der Laufzeit/dem Assembler an, dass ein Teil der Validierung mit dem \_ SW-Flag im Assembler (z. b. vs \_ 2 \_ SW) gelockert werden muss.</span><span class="sxs-lookup"><span data-stu-id="65601-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="65601-227">Ein Software-Shader funktioniert nicht mit Hardware.</span><span class="sxs-lookup"><span data-stu-id="65601-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="65601-228">vs \_ 2 \_ SW ist eine Lockerung der maximalen Anzahl von vs \_ 2 \_ x. gleichermaßen ist PS \_ 2 \_ SW eine Lockerung der maximalen Anzahl von PS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="65601-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="65601-229">Insbesondere werden die folgenden Überprüfungen gelockert:</span><span class="sxs-lookup"><span data-stu-id="65601-229">Specifically, the following validations are relaxed:</span></span>



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65601-230">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="65601-230">Shader Model</span></span>                               | <span data-ttu-id="65601-231">Resource</span><span class="sxs-lookup"><span data-stu-id="65601-231">Resource</span></span>                             | <span data-ttu-id="65601-232">Begrenzung</span><span class="sxs-lookup"><span data-stu-id="65601-232">Limit</span></span>                                                                                                                             |
| <span data-ttu-id="65601-233">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="65601-234">Anweisungs Anzahl</span><span class="sxs-lookup"><span data-stu-id="65601-234">Instruction Counts</span></span>                   | <span data-ttu-id="65601-235">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="65601-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="65601-236">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="65601-237">Float-Konstante Register</span><span class="sxs-lookup"><span data-stu-id="65601-237">Float Constant Registers</span></span>             | <span data-ttu-id="65601-238">8192</span><span class="sxs-lookup"><span data-stu-id="65601-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="65601-239">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="65601-240">Ganzzahlige Konstante Register</span><span class="sxs-lookup"><span data-stu-id="65601-240">Integer Constant Registers</span></span>           | <span data-ttu-id="65601-241">2048</span><span class="sxs-lookup"><span data-stu-id="65601-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="65601-242">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="65601-243">Boolesche Konstante Register</span><span class="sxs-lookup"><span data-stu-id="65601-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="65601-244">2048</span><span class="sxs-lookup"><span data-stu-id="65601-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="65601-245">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="65601-246">Abhängige Lese Tiefe</span><span class="sxs-lookup"><span data-stu-id="65601-246">Dependent-read depth</span></span>                 | <span data-ttu-id="65601-247">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="65601-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="65601-248">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="65601-249">Anweisungen und Bezeichnungen der Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="65601-249">flow control instructions and labels</span></span> | <span data-ttu-id="65601-250">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="65601-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="65601-251">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="65601-252">Schleifenstart/-Schritt/-Anzahl</span><span class="sxs-lookup"><span data-stu-id="65601-252">Loop start/step/counts</span></span>               | <span data-ttu-id="65601-253">Die Iterations-und Iterations Schrittgröße für rep-und Loop-Anweisungen sind 32-Bit-Ganzzahlen mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="65601-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="65601-254">"Count" kann bis Max \_ . int/64 betragen.</span><span class="sxs-lookup"><span data-stu-id="65601-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="65601-255">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="65601-256">Port Limits</span><span class="sxs-lookup"><span data-stu-id="65601-256">Port limits</span></span>                          | <span data-ttu-id="65601-257">Die Port Limits für alle Register Dateien werden gelockert.</span><span class="sxs-lookup"><span data-stu-id="65601-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="65601-258">vs \_ 3- \_ SW</span><span class="sxs-lookup"><span data-stu-id="65601-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="65601-259">Anzahl von Interpolatoren</span><span class="sxs-lookup"><span data-stu-id="65601-259">Number of interpolators</span></span>              | <span data-ttu-id="65601-260">16 Ausgabe Register in vs \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="65601-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="65601-261">PS \_ 3 ( \_ SW)</span><span class="sxs-lookup"><span data-stu-id="65601-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="65601-262">Anzahl von Interpolatoren</span><span class="sxs-lookup"><span data-stu-id="65601-262">Number of interpolators</span></span>              | <span data-ttu-id="65601-263">14 (16-2) Eingabe Register für PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="65601-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="65601-264">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65601-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65601-265">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65601-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 