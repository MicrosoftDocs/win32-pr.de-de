---
title: Shadermodell 3 (HLSL-Referenz)
description: Vertex-Shader und Pixel-Shader werden gegenüber früheren Shaderversionen erheblich vereinfacht.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c277723628d5337e41e5fbf83baa9fda8af16adf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993867"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="c7389-103">Shadermodell 3 (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="c7389-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="c7389-104">Vertex-Shader und Pixel-Shader werden gegenüber früheren Shaderversionen erheblich vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c7389-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="c7389-105">Wenn Sie Shader in Hardware implementieren, dürfen Sie nicht vs \_ 3 \_ 0 oder ps \_ 3 \_ 0 mit anderen Shaderversionen verwenden, und Sie dürfen keinen shader-Typ mit der festen Funktionspipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7389-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="c7389-106">Diese Änderungen ermöglichen es, Treiber und die Runtime zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="c7389-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="c7389-107">Die einzige Ausnahme besteht darin, dass softwarebasierte Shader im Vergleich zu \_ \_ 3 0 Shadern mit einer beliebigen Pixelshaderversion verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c7389-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="c7389-108">Darüber hinaus kann der \_ \_ Vertex-Shader nur Ausgabesemantik verwenden, die mit FVF-Codes (Flexible Vertex Format) kompatibel ist, wenn Sie einen reinen Software- oder 3 0-Shader mit einer früheren Pixelshaderversion verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7389-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="c7389-109">Die Semantik, die für Vertex-Shaderausgaben verwendet wird, muss für Pixel-Shadereingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7389-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="c7389-110">Die Semantik wird verwendet, um die Vertex-Shaderausgaben den Pixel-Shadereingaben zuzuordnen, ähnlich wie die Vertexdeklaration den Vertex-Shader-Eingaberegistern und vorherigen Shadermodellen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="c7389-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="c7389-111">Weitere Informationen finden Sie unter Match Semantics on vs 3.0 and ps 3.0 Shaders (Übereinstimmungssemantik für Shader der 3.0- und ps 3.0-Shader).</span><span class="sxs-lookup"><span data-stu-id="c7389-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="c7389-112">Es wurden zusätzliche Renderzustände im Umbruchmodus hinzugefügt, um die Möglichkeit zusätzlicher Texturkoordinaten in diesem neuen Schema abzudecken.</span><span class="sxs-lookup"><span data-stu-id="c7389-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="c7389-113">Attribute mit D3DDECLUSAGE \_ TEXCOORD und Verwendungsindex von 0 bis 15 werden im Umbruchmodus interpoliert, wenn der entsprechende [**D3DRS \_ WRAP \***](/windows/desktop/direct3d9/d3drenderstatetype) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c7389-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="c7389-114">Features von Vertex-Shadermodell 3</span><span class="sxs-lookup"><span data-stu-id="c7389-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="c7389-115">Features des Pixelshadermodells 3</span><span class="sxs-lookup"><span data-stu-id="c7389-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="c7389-116">Match Semantics on vs \_ 3 \_ 0 and ps \_ 3 \_ 0 Shader</span><span class="sxs-lookup"><span data-stu-id="c7389-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="c7389-117">Änderungen am Modus "Verzweigungs-, Tiefen- und Schattierungsmodus"</span><span class="sxs-lookup"><span data-stu-id="c7389-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="c7389-118">Gleitkomma- und Ganzzahlkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="c7389-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="c7389-119">Angeben der vollständigen oder teilweisen Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="c7389-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="c7389-120">Softwarevertex- und Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="c7389-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="c7389-121">Vertex-Shadermodell 3-Features</span><span class="sxs-lookup"><span data-stu-id="c7389-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="c7389-122">Die Ausgaberegistertypen des Vertex-Shaders wurden in zwölf Register reduziert (siehe [Ausgaberegister](dx9-graphics-reference-asm-vs-registers-output.md)).</span><span class="sxs-lookup"><span data-stu-id="c7389-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="c7389-123">Jedes verwendete Register muss mithilfe der [dcl-Anweisung](dcl-usage---ps.md) und einer Semantik deklariert werden (z. B. dcl \_ color0 o0.xyzw).</span><span class="sxs-lookup"><span data-stu-id="c7389-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="c7389-124">Das 3 \_ 0-Vertex-Shadermodell (im Vergleich zu 3 0) erweitert die Features von vs. 2 0 mit einer leistungsfähigeren Registerindizierung, einer Reihe vereinfachter Ausgaberegister, der Möglichkeit, eine Textur in einem \_ \_ \_ Vertex-Shader zu beproben, und der Möglichkeit, die Rate zu steuern, mit der \_ Shadereingaben initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7389-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="c7389-125">Indizieren beliebiger Register</span><span class="sxs-lookup"><span data-stu-id="c7389-125">Index Any Register</span></span>

<span data-ttu-id="c7389-126">Alle Register ( [Eingaberegister](dx9-graphics-reference-asm-vs-registers-input.md) und [Ausgaberegister](dx9-graphics-reference-asm-vs-registers-output.md)) können mithilfe des Schleifenzählerregisters indiziert werden [(nur](dx9-graphics-reference-asm-vs-registers-loop-counter.md) konstante Register konnten in früheren Versionen indiziert werden).</span><span class="sxs-lookup"><span data-stu-id="c7389-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="c7389-127">Sie müssen Eingabe- und Ausgaberegister deklarieren, bevor Sie sie indizieren.</span><span class="sxs-lookup"><span data-stu-id="c7389-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="c7389-128">Sie dürfen jedoch kein Ausgaberegister indizieren, das mit einer Semantik der Position oder Punktgröße deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="c7389-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="c7389-129">Wenn die Indizierung verwendet wird, müssen die Position und die Psize-Semantik in den Registern o0 bzw. o1 deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="c7389-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="c7389-130">Sie dürfen nur einen kontinuierlichen Bereich von Registern indizieren. Das heißt, Sie können nicht über Register hinweg indizieren, die nicht deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="c7389-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="c7389-131">Diese Einschränkung kann zwar unwesentlich sein, ermöglicht aber die Hardwareoptimierung.</span><span class="sxs-lookup"><span data-stu-id="c7389-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="c7389-132">Der Versuch, nicht zusammenhängende Register zu indizieren, führt zu nicht definierten Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="c7389-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="c7389-133">Die Shaderüberprüfung erzwingt diese Einschränkung nicht.</span><span class="sxs-lookup"><span data-stu-id="c7389-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="c7389-134">Vereinfachen von Ausgaberegistern</span><span class="sxs-lookup"><span data-stu-id="c7389-134">Simplify Output Registers</span></span>

<span data-ttu-id="c7389-135">Alle verschiedenen Arten von Ausgaberegistern wurden in zwölf Ausgaberegister reduziert: 1 für Position, 2 für Farbe, 8 für Textur und 1 für Diess oder Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="c7389-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="c7389-136">Diese Register interpolieren alle Daten, die sie für den Pixel-Shader enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7389-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="c7389-137">Ausgaberegisterdeklarationen sind erforderlich, und jedem Register wird Semantik zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c7389-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="c7389-138">Die Register können wie folgt aufgeschlüsselt werden:</span><span class="sxs-lookup"><span data-stu-id="c7389-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="c7389-139">Mindestens ein Register muss als Positionsregister mit vier Komponenten deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="c7389-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="c7389-140">Dies ist das einzige Vertex-Shaderregister, das erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c7389-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="c7389-141">Die ersten zehn Register, die von einem Shader genutzt werden, können maximal vier Komponenten (xyzw) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7389-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="c7389-142">Das letzte (oder zwölfte) Register darf nur einen Skalar (z. B. punktgröße) enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7389-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="c7389-143">Eine Liste der Register finden Sie unter [Register – vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="c7389-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="c7389-144">Texturbeispiel in einem Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="c7389-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="c7389-145">Vertex-Shader 3 \_ 0 unterstützt die Textursuche im Vertex-Shader mithilfe von [Texldl im Vergleich zu](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="c7389-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="c7389-146">Features des Pixelshadermodells 3</span><span class="sxs-lookup"><span data-stu-id="c7389-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="c7389-147">Die Farb- und Texturregister des Pixelshader wurden in zehn Eingaberegister reduziert (siehe [Eingaberegistertypen](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="c7389-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="c7389-148">Das Gesichtsregister ist ein Gleitkomma-Skalarregister.</span><span class="sxs-lookup"><span data-stu-id="c7389-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="c7389-149">Nur das Vorzeichen dieses Registers ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c7389-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="c7389-150">Wenn das Vorzeichen negativ ist, ist der Grundtyp ein Rückwand.</span><span class="sxs-lookup"><span data-stu-id="c7389-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="c7389-151">Dies kann z. B. in einem Pixel-Shader verwendet werden, um eine zweiseitige Beleuchtung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="c7389-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="c7389-152">Das Positionsregister verweist auf die aktuellen Pixel (x,y).</span><span class="sxs-lookup"><span data-stu-id="c7389-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="c7389-153">Die Shaderkonstantenregister können wie hier dargestellt festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c7389-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="c7389-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="c7389-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="c7389-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="c7389-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="c7389-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="c7389-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="c7389-157">Match Semantics on vs \_ 3 \_ 0 and ps \_ 3 \_ 0 Shader</span><span class="sxs-lookup"><span data-stu-id="c7389-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="c7389-158">Es gibt einige Einschränkungen für die semantische Verwendung mit gegenüber \_ \_ 3 0 und ps \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c7389-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="c7389-159">Im Allgemeinen müssen Sie vorsichtig sein, wenn Sie eine Semantik für eine Shadereingabe verwenden, die einer in einer Shaderausgabe verwendeten Semantik entspricht.</span><span class="sxs-lookup"><span data-stu-id="c7389-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="c7389-160">Dieser Pixelshader packt beispielsweise mehrere Namen in ein Register:</span><span class="sxs-lookup"><span data-stu-id="c7389-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="c7389-161">Jedes Register hat eine andere Semantik.</span><span class="sxs-lookup"><span data-stu-id="c7389-161">Each register has a different semantic.</span></span> <span data-ttu-id="c7389-162">Beachten Sie, dass Sie auch v0.x und v0.yz mit unterschiedlicher (mehrfacher) Semantik benennen können, da die Schreibmaske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7389-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="c7389-163">Angesichts des Pixels shaders kann der folgende und \_ der folgende \_ 3 0-Shader nicht mit ihm gekoppelt werden:</span><span class="sxs-lookup"><span data-stu-id="c7389-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="c7389-164">Diese beiden Shader stehen in Konflikt mit der Verwendung der [**Semantik D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) und **D3DDECLUSAGE \_ TEXCOORD1.**</span><span class="sxs-lookup"><span data-stu-id="c7389-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="c7389-165">Schreiben Sie den Vertex-Shader wie diesen um, um die semantische Kollision zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="c7389-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="c7389-166">Ebenso kann ein semantischer Name, der in verschiedenen Eingaberegistern im Pixel-Shader deklariert ist (v0 und v1 im Pixel-Shader), nicht in einem einzelnen Ausgaberegister in diesem Vertex-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7389-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="c7389-167">Dieser Vertex-Shader kann beispielsweise nicht mit dem Pixel-Shader gekoppelt werden, da D3DDECLUSAGE TEXCOORD1 sowohl für Pixel-Shadereingaberegister (v0, v1) als auch für das \_ Vertex-Shader-Ausgaberegister o3 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7389-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="c7389-168">Andererseits kann dieser Vertex-Shader nicht mit dem Pixel-Shader gekoppelt werden, da die Ausgabemaske für einen Parameter mit einer bestimmten Semantik nicht die vom Pixel-Shader angeforderten Daten enthält:</span><span class="sxs-lookup"><span data-stu-id="c7389-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="c7389-169">Dieser Vertex-Shader stellt keine Ausgabe mit einem der vom Pixel-Shader angeforderten semantischen Namen zur Verfügung, sodass die Shaderkopplung ungültig ist:</span><span class="sxs-lookup"><span data-stu-id="c7389-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


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



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="c7389-170">Änderungen im Modus "Verschatten", "Tiefe" und "Schattierung"</span><span class="sxs-lookup"><span data-stu-id="c7389-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="c7389-171">Wenn D3DRS SHADEMODE während der Clipping- und Dreiecksrasterung für flache Schattierung festgelegt ist, werden Attribute mit \_ D3DDECLUSAGE COLOR als flach schattiert \_ interpoliert.</span><span class="sxs-lookup"><span data-stu-id="c7389-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="c7389-172">Wenn Komponenten eines Registers mit einer Farbsemantik deklariert werden, andere Komponenten desselben Registers jedoch eine andere Semantik erhalten, ist die flache Schattierungsinterpolation (linear im Vergleich zu flach) für die Komponenten in diesem Register ohne Farbsemantik nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c7389-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="c7389-173">Wenn ein Rendern von 3 0 und ps 3 0 gewünscht ist, müssen \_ \_ \_ \_ Shader 3 0 und 3 0 -Shader Eine-0-Shader implementieren.</span><span class="sxs-lookup"><span data-stu-id="c7389-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="c7389-174">Außerhalb der Shader werden keine Berechnungsberechnungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7389-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="c7389-175">Im Vergleich zu 3 0 gibt es kein Register für 3 \_ \_ 0, und es wurden zusätzliche Semantiken wie D3DDECLUSAGE \_ PIXELS (für berechnete Blendfaktor pro Scheitelpunkt) und D3DDECLUSAGE \_ DEPTH (für die Übergabe eines Tiefenwerts an den Pixel-Shader zum Berechnen des Mischungsfaktors für Denkelemente) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c7389-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="c7389-176">Der Texturphasenzustand D3DTSS \_ TEXCOORDINDEX wird bei Verwendung des Pixelshaders 3.0 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c7389-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="c7389-177">Die folgenden Werte wurden hinzugefügt, um diese Änderungen zu berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="c7389-177">The following values have been added to accommodate these changes:</span></span>


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



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="c7389-178">Gleitkomma- und Ganzzahlkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="c7389-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="c7389-179">Gleitkommamathematik erfolgt mit unterschiedlicher Genauigkeit und unterschiedlichen Bereichen (16-Bit, 24-Bit und 32-Bit) in verschiedenen Teilen der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7389-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="c7389-180">Ein Wert, der größer als der dynamische Bereich der Pipeline ist, die in diese Pipeline eintritt (z. B. wird eine 32-Bit-Floattexturzuordnung in eine 24-Bit-Floatpipeline in ps \_ 2 \_ 0 entnommen), erzeugt ein nicht definiertes Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="c7389-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="c7389-181">Für vorhersagbares Verhalten sollten Sie einen solchen Wert an den maximalen dynamischen Bereich anbinden.</span><span class="sxs-lookup"><span data-stu-id="c7389-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="c7389-182">Die Konvertierung von einem Gleitkommawert in eine ganze Zahl erfolgt an mehreren Stellen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="c7389-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="c7389-183">Beim Auftreten einer [MOVA-Anweisung](mova---vs.md) im Vergleich zu einer -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="c7389-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="c7389-184">Während der Texturadressierung.</span><span class="sxs-lookup"><span data-stu-id="c7389-184">During texture addressing.</span></span>
-   <span data-ttu-id="c7389-185">Beim Schreiben in ein Nicht-Gleitkommarenderziel.</span><span class="sxs-lookup"><span data-stu-id="c7389-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="c7389-186">Angeben der vollständigen oder teilweisen Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="c7389-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="c7389-187">Sowohl ps \_ 3 \_ 0 als auch ps \_ 2 \_ x bieten Unterstützung für zwei Genauigkeitsebenen:</span><span class="sxs-lookup"><span data-stu-id="c7389-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



| <span data-ttu-id="c7389-188">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7389-188">ps\_3\_0</span></span> | <span data-ttu-id="c7389-189">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7389-189">ps\_2\_0</span></span> | <span data-ttu-id="c7389-190">Precision</span><span class="sxs-lookup"><span data-stu-id="c7389-190">Precision</span></span>         | <span data-ttu-id="c7389-191">Wert</span><span class="sxs-lookup"><span data-stu-id="c7389-191">Value</span></span>                |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="c7389-192">x</span><span class="sxs-lookup"><span data-stu-id="c7389-192">x</span></span>        |          | <span data-ttu-id="c7389-193">Vollständig</span><span class="sxs-lookup"><span data-stu-id="c7389-193">Full</span></span>              | <span data-ttu-id="c7389-194">fp32 oder höher</span><span class="sxs-lookup"><span data-stu-id="c7389-194">fp32 or higher</span></span>       |
| <span data-ttu-id="c7389-195">x</span><span class="sxs-lookup"><span data-stu-id="c7389-195">x</span></span>        |          | <span data-ttu-id="c7389-196">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="c7389-196">Partial precision</span></span> | <span data-ttu-id="c7389-197">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="c7389-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="c7389-198">x</span><span class="sxs-lookup"><span data-stu-id="c7389-198">x</span></span>        | <span data-ttu-id="c7389-199">x</span><span class="sxs-lookup"><span data-stu-id="c7389-199">x</span></span>        | <span data-ttu-id="c7389-200">Vollständig</span><span class="sxs-lookup"><span data-stu-id="c7389-200">Full</span></span>              | <span data-ttu-id="c7389-201">fp24=s16e7 oder höher</span><span class="sxs-lookup"><span data-stu-id="c7389-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="c7389-202">x</span><span class="sxs-lookup"><span data-stu-id="c7389-202">x</span></span>        | <span data-ttu-id="c7389-203">x</span><span class="sxs-lookup"><span data-stu-id="c7389-203">x</span></span>        | <span data-ttu-id="c7389-204">Partielle Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="c7389-204">Partial precision</span></span> | <span data-ttu-id="c7389-205">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="c7389-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="c7389-206">ps \_ 3 \_ 0 unterstützt mehr Genauigkeit als ps \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c7389-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="c7389-207">Standardmäßig erfolgen alle Vorgänge auf der Ebene der vollständigen Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="c7389-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="c7389-208">Die partielle Genauigkeit (siehe Modifizierer für das [Pixel-Shaderregister)](dx9-graphics-reference-asm-ps-registers-modifiers.md)wird angefordert, indem der pp-Modifizierer zum Shadercode hinzugefügt wird (vorausgesetzt, die zugrunde liegende Implementierung \_ unterstützt ihn).</span><span class="sxs-lookup"><span data-stu-id="c7389-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="c7389-209">Implementierungen können den Modifizierer immer ignorieren und die betroffenen Vorgänge mit voller Genauigkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7389-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="c7389-210">Der \_ pp-Modifizierer kann in zwei Kontexten auftreten:</span><span class="sxs-lookup"><span data-stu-id="c7389-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="c7389-211">In einer Texturkoordinatendeklaration, um Texturkoordinaten mit teilweiser Genauigkeit an den Pixel-Shader zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c7389-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="c7389-212">Dies kann verwendet werden, wenn Texturkoordinaten Farbdaten an den Pixel-Shader weiterleiten, die in einigen Implementierungen möglicherweise schneller mit partieller Genauigkeit als mit vollständiger Genauigkeit sind.</span><span class="sxs-lookup"><span data-stu-id="c7389-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="c7389-213">Für jede Anweisung zum Anfordern der Verwendung von partieller Genauigkeit, einschließlich Anweisungen zum Laden von Texturen.</span><span class="sxs-lookup"><span data-stu-id="c7389-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="c7389-214">Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein Ergebnis mit teilweiser Genauigkeit speichern darf.</span><span class="sxs-lookup"><span data-stu-id="c7389-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="c7389-215">Ohne expliziten Modifizierer muss die Anweisung mit voller Genauigkeit ausgeführt werden (unabhängig von der Genauigkeit der Eingabeopernden).</span><span class="sxs-lookup"><span data-stu-id="c7389-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="c7389-216">Eine Anwendung entscheidet sich möglicherweise absichtlich dafür, genauigkeits- und leistungssenklich abzuhandeln.</span><span class="sxs-lookup"><span data-stu-id="c7389-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="c7389-217">Es gibt mehrere Arten von Shadereingabedaten, die natürliche Kandidaten für die Verarbeitung mit teilweiser Genauigkeit sind:</span><span class="sxs-lookup"><span data-stu-id="c7389-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="c7389-218">Farb iteratoren werden durch Teilweisegenauigkeitswerte gut dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c7389-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="c7389-219">Texturwerte aus den meisten Formaten können genau durch Teilweisegenauigkeitswerte dargestellt werden (Werte, die aus 32-Bit-Gleitkommaformattexturen entnommen wurden, sind eine offensichtliche Ausnahme).</span><span class="sxs-lookup"><span data-stu-id="c7389-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="c7389-220">Konstanten können entsprechend dem Shader durch eine teilweise Genauigkeitsdarstellung dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c7389-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="c7389-221">In all diesen Fällen kann der Entwickler die partielle Genauigkeit angeben, um die Daten zu verarbeiten, da er weiß, dass keine Genauigkeit der Eingabedaten verloren geht.</span><span class="sxs-lookup"><span data-stu-id="c7389-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="c7389-222">In einigen Fällen kann ein Shader erfordern, dass die internen Schritte einer Berechnung mit vollständiger Genauigkeit ausgeführt werden, auch wenn eingabe- und endgültige Ausgabewerte nicht mehr als partielle Genauigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="c7389-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="c7389-223">Softwarevertex- und Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="c7389-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="c7389-224">Softwareimplementierungen (Laufzeit und Referenz für Vertex-Shader und Referenz für Pixel-Shader) von Shadern der Version 2 \_ 0 und höher haben eine gewisse Überprüfung gelockert.</span><span class="sxs-lookup"><span data-stu-id="c7389-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="c7389-225">Dies ist für Debug- und Prototypzwecke nützlich.</span><span class="sxs-lookup"><span data-stu-id="c7389-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="c7389-226">Die Anwendung gibt der Runtime/dem Assembler an, dass sie einen Teil der Validierung mithilfe des Flags sw im Assembler gelockert haben muss \_ (z. B. im Vergleich zu \_ 2 \_ SW).</span><span class="sxs-lookup"><span data-stu-id="c7389-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="c7389-227">Ein Software-Shader funktioniert nicht mit Hardware.</span><span class="sxs-lookup"><span data-stu-id="c7389-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="c7389-228">Vs \_ 2 \_ sw ist ein Ausgleich für die maximalen Obergrenzen von vs \_ 2 \_ x; ebenso ist ps \_ 2 sw ein \_ Mäßigung für die maximalen Obergrenzen von ps \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="c7389-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="c7389-229">Insbesondere werden die folgenden Überprüfungen gelockert:</span><span class="sxs-lookup"><span data-stu-id="c7389-229">Specifically, the following validations are relaxed:</span></span>



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7389-230">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c7389-230">Shader Model</span></span>                               | <span data-ttu-id="c7389-231">Resource</span><span class="sxs-lookup"><span data-stu-id="c7389-231">Resource</span></span>                             | <span data-ttu-id="c7389-232">Begrenzung</span><span class="sxs-lookup"><span data-stu-id="c7389-232">Limit</span></span>                                                                                                                             |
| <span data-ttu-id="c7389-233">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="c7389-234">Anweisungsanzahl</span><span class="sxs-lookup"><span data-stu-id="c7389-234">Instruction Counts</span></span>                   | <span data-ttu-id="c7389-235">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="c7389-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="c7389-236">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="c7389-237">Gleitkommakonstantenregister</span><span class="sxs-lookup"><span data-stu-id="c7389-237">Float Constant Registers</span></span>             | <span data-ttu-id="c7389-238">8192</span><span class="sxs-lookup"><span data-stu-id="c7389-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="c7389-239">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="c7389-240">Integer Constant Registers</span><span class="sxs-lookup"><span data-stu-id="c7389-240">Integer Constant Registers</span></span>           | <span data-ttu-id="c7389-241">2048</span><span class="sxs-lookup"><span data-stu-id="c7389-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="c7389-242">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="c7389-243">Boolesche Konstantenregister</span><span class="sxs-lookup"><span data-stu-id="c7389-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="c7389-244">2048</span><span class="sxs-lookup"><span data-stu-id="c7389-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="c7389-245">ps \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="c7389-246">Abhängige Lesetiefe</span><span class="sxs-lookup"><span data-stu-id="c7389-246">Dependent-read depth</span></span>                 | <span data-ttu-id="c7389-247">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="c7389-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="c7389-248">vs \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="c7389-249">Anweisungen und Bezeichnungen für die Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="c7389-249">flow control instructions and labels</span></span> | <span data-ttu-id="c7389-250">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="c7389-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="c7389-251">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="c7389-252">Start/Schritt/Anzahl der Schleifen</span><span class="sxs-lookup"><span data-stu-id="c7389-252">Loop start/step/counts</span></span>               | <span data-ttu-id="c7389-253">Iterationsstart und Iterationsschrittgröße für Rep- und Schleifenanweisungen sind 32-Bit-Ganzzahlen mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c7389-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="c7389-254">Die Anzahl kann bis zu MAX \_ INT/64 sein.</span><span class="sxs-lookup"><span data-stu-id="c7389-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="c7389-255">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="c7389-256">Portgrenzwerte</span><span class="sxs-lookup"><span data-stu-id="c7389-256">Port limits</span></span>                          | <span data-ttu-id="c7389-257">Portgrenzwerte für alle Registerdateien werden gelockert.</span><span class="sxs-lookup"><span data-stu-id="c7389-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="c7389-258">vs \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="c7389-259">Anzahl von Interpolatoren</span><span class="sxs-lookup"><span data-stu-id="c7389-259">Number of interpolators</span></span>              | <span data-ttu-id="c7389-260">16 Ausgaberegister in im Vergleich \_ zu 3 \_ Sw.</span><span class="sxs-lookup"><span data-stu-id="c7389-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="c7389-261">ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7389-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="c7389-262">Anzahl von Interpolatoren</span><span class="sxs-lookup"><span data-stu-id="c7389-262">Number of interpolators</span></span>              | <span data-ttu-id="c7389-263">14(16-2) Eingaberegister für ps \_ 3 \_ sw.</span><span class="sxs-lookup"><span data-stu-id="c7389-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="c7389-264">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7389-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7389-265">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7389-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
