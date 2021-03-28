---
title: Organisieren des Zustands in einem Effekt (Direct3D 11)
description: Mit Direct3D 11 wird der Effekt Zustand für bestimmte Pipeline Stufen nach Strukturen organisiert.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993471"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a><span data-ttu-id="067bf-103">Organisieren des Zustands in einem Effekt (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="067bf-103">Organizing State in an Effect (Direct3D 11)</span></span>

<span data-ttu-id="067bf-104">Mit Direct3D 11 wird der Effekt Zustand für bestimmte Pipeline Stufen nach Strukturen organisiert.</span><span class="sxs-lookup"><span data-stu-id="067bf-104">With Direct3D 11, effect state for certain pipeline stages is organized by structures.</span></span> <span data-ttu-id="067bf-105">Im folgenden sind die Strukturen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="067bf-105">Here are the structures:</span></span>



| <span data-ttu-id="067bf-106">Pipeline Status</span><span class="sxs-lookup"><span data-stu-id="067bf-106">Pipeline State</span></span> | <span data-ttu-id="067bf-107">Struktur</span><span class="sxs-lookup"><span data-stu-id="067bf-107">Structure</span></span>                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="067bf-108">Rasterung</span><span class="sxs-lookup"><span data-stu-id="067bf-108">Rasterization</span></span>  | [<span data-ttu-id="067bf-109">**D3D11 \_ Rasterizer- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="067bf-109">**D3D11\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| <span data-ttu-id="067bf-110">Ausgabezusammenführung</span><span class="sxs-lookup"><span data-stu-id="067bf-110">Output Merger</span></span>  | <span data-ttu-id="067bf-111">[**D3D11 \_ Blend \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) -Debug-und [ **D3D11- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="067bf-111">[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) and [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span> |
| <span data-ttu-id="067bf-112">Shader</span><span class="sxs-lookup"><span data-stu-id="067bf-112">Shaders</span></span>        | <span data-ttu-id="067bf-113">Siehe unten</span><span class="sxs-lookup"><span data-stu-id="067bf-113">See below</span></span>                                                                                                          |



 

<span data-ttu-id="067bf-114">In den Shader-Phasen, in denen die Anzahl der Zustandsänderungen von einer Anwendung stärker gesteuert werden muss, wurde der Zustand in den konstanten Puffer Status, den samplerstatus, den Shader-Ressourcen Zustand und den Ansichts Zustand für ungeordnete Zugriffe (für Pixel-und Compute-Shader) aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="067bf-114">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, shader resource state, and unordered access view state (for pixel and compute shaders).</span></span> <span data-ttu-id="067bf-115">Dadurch wird eine Anwendung ermöglicht, die sorgfältig entworfen wurde, um nur den geänderten Zustand zu aktualisieren. Dadurch wird die Leistung verbessert, da die Datenmenge reduziert wird, die an die GPU übermittelt werden muss.</span><span class="sxs-lookup"><span data-stu-id="067bf-115">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="067bf-116">Wie organisieren Sie also den Pipeline Status in einem Effekt?</span><span class="sxs-lookup"><span data-stu-id="067bf-116">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="067bf-117">Die Antwort ist, dass die Reihenfolge keine Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="067bf-117">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="067bf-118">Globale Variablen müssen sich nicht im oberen Bereich befinden.</span><span class="sxs-lookup"><span data-stu-id="067bf-118">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="067bf-119">Allerdings wird für alle Beispiele im SDK dieselbe Reihenfolge befolgt, da es eine bewährte Methode ist, die Daten auf die gleiche Weise zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="067bf-119">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="067bf-120">Dies ist eine kurze Beschreibung der Datenreihen Folge in den DirectX SDK-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="067bf-120">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="067bf-121">Globale Variablen</span><span class="sxs-lookup"><span data-stu-id="067bf-121">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="067bf-122">Shader</span><span class="sxs-lookup"><span data-stu-id="067bf-122">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="067bf-123">Gruppen, Techniken und Durchgänge</span><span class="sxs-lookup"><span data-stu-id="067bf-123">Groups, Techniques, and Passes</span></span>](#groups-techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="067bf-124">Globale Variablen</span><span class="sxs-lookup"><span data-stu-id="067bf-124">Global Variables</span></span>

<span data-ttu-id="067bf-125">Ebenso wie die Standard-C-Übung werden globale Variablen zuerst am Anfang der Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="067bf-125">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="067bf-126">In den meisten Fällen handelt es sich hierbei um Variablen, die von einer Anwendung initialisiert und dann in einem Effekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="067bf-126">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="067bf-127">Manchmal werden Sie initialisiert und nie geändert, in anderen Fällen, in denen Sie jedes Frame aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="067bf-127">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="067bf-128">Ebenso wie Regeln des C-Funktions Bereichs sind Effekte, die außerhalb des Gültigkeits Bereichs von Effekten deklariert wurden, während des Effekts sichtbar. jede Variable, die innerhalb einer Effekt Funktion deklariert wird, ist nur innerhalb dieser Funktion sichtbar.</span><span class="sxs-lookup"><span data-stu-id="067bf-128">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="067bf-129">Im folgenden finden Sie ein Beispiel für die Variablen, die in BasicHLSL10. FX deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="067bf-129">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



<span data-ttu-id="067bf-130">Die Syntax für Effekt Variablen wird in der [Variablen Syntax von Effect (Direct3D 11)](d3d11-effect-variable-syntax.md)ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="067bf-130">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 11)](d3d11-effect-variable-syntax.md).</span></span> <span data-ttu-id="067bf-131">Die Syntax für Effekt Textur-Samplern ist ausführlicher im [Samplingtyp (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler)ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="067bf-131">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

## <a name="shaders"></a><span data-ttu-id="067bf-132">Shader</span><span class="sxs-lookup"><span data-stu-id="067bf-132">Shaders</span></span>

<span data-ttu-id="067bf-133">Shader sind kleine ausführbare Programme.</span><span class="sxs-lookup"><span data-stu-id="067bf-133">Shaders are small executable programs.</span></span> <span data-ttu-id="067bf-134">Sie können sich Shader als kapselnde shaderzustand vorstellen, da der HLSL-Code die shaderfunktionalität implementiert.</span><span class="sxs-lookup"><span data-stu-id="067bf-134">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="067bf-135">Die Grafik Pipeline bis zu fünf verschiedene Arten von Shadern.</span><span class="sxs-lookup"><span data-stu-id="067bf-135">The graphics pipeline up to five different kinds of shaders.</span></span>

-   <span data-ttu-id="067bf-136">Vertex-Shader: Arbeiten mit Vertex-Daten.</span><span class="sxs-lookup"><span data-stu-id="067bf-136">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="067bf-137">Ein Scheitelpunkt in ergibt einen Scheitelpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="067bf-137">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="067bf-138">Hull-Shader: Arbeiten mit Patchdaten.</span><span class="sxs-lookup"><span data-stu-id="067bf-138">Hull shaders - Operate on patch data.</span></span> <span data-ttu-id="067bf-139">Kontrollpunkt Phase: ein Aufruf ergibt einen Steuerungspunkt. Für jede Verzweigung und jede joinphase: ein Patch erzeugt eine gewisse Menge an Patch-konstantendaten.</span><span class="sxs-lookup"><span data-stu-id="067bf-139">Control Point Phase: one invocation yields one control point; For each Fork and Join Phases: one patch yields some amount of patch constant data.</span></span>
-   <span data-ttu-id="067bf-140">Domänen-Shader: Arbeiten mit primitiven Daten.</span><span class="sxs-lookup"><span data-stu-id="067bf-140">Domain shaders - Operate on primitive data.</span></span> <span data-ttu-id="067bf-141">Ein primitiver kann 0, 1 oder viele primitive ergeben.</span><span class="sxs-lookup"><span data-stu-id="067bf-141">One primitive may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="067bf-142">Geometry-Shader: Arbeiten mit primitiven Daten.</span><span class="sxs-lookup"><span data-stu-id="067bf-142">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="067bf-143">Ein primitiver in kann 0, 1 oder viele primitive ergeben.</span><span class="sxs-lookup"><span data-stu-id="067bf-143">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="067bf-144">Pixel-Shader: Arbeiten mit Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="067bf-144">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="067bf-145">Ein Pixel in ergibt 1 Pixel, es sei denn, das Pixel ist aus einem Rendering herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="067bf-145">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="067bf-146">Die COMPUTE-Shader-Pipeline verwendet einen Shader:</span><span class="sxs-lookup"><span data-stu-id="067bf-146">The compute shader pipeline uses one shader:</span></span>

-   <span data-ttu-id="067bf-147">Compute-Shader: Arbeiten auf jeder Art von Daten.</span><span class="sxs-lookup"><span data-stu-id="067bf-147">Compute shaders - Operate on any kind of data.</span></span> <span data-ttu-id="067bf-148">Die Ausgabe ist unabhängig von der Anzahl der Threads.</span><span class="sxs-lookup"><span data-stu-id="067bf-148">The output is independent of the number of threads.</span></span>

<span data-ttu-id="067bf-149">Shader sind lokale Funktionen und folgen Regeln für C-Stil Funktionen.</span><span class="sxs-lookup"><span data-stu-id="067bf-149">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="067bf-150">Wenn ein Effekt kompiliert wird, wird jeder Shader kompiliert, und ein Zeiger auf jede Shader-Funktion wird intern gespeichert.</span><span class="sxs-lookup"><span data-stu-id="067bf-150">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="067bf-151">Bei erfolgreicher Kompilierung wird eine ID3D11Effect-Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="067bf-151">An ID3D11Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="067bf-152">An diesem Punkt liegt der kompilierte Effekt in einem zwischen Format vor.</span><span class="sxs-lookup"><span data-stu-id="067bf-152">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="067bf-153">Um weitere Informationen zu den kompilierten Shadern zu erhalten, müssen Sie die Shader-Reflektion verwenden.</span><span class="sxs-lookup"><span data-stu-id="067bf-153">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="067bf-154">Dies entspricht im Wesentlichen dem Anfordern der Laufzeit, die Shader zu dekompilieren, und gibt Informationen über den Shader-Code zurück.</span><span class="sxs-lookup"><span data-stu-id="067bf-154">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



<span data-ttu-id="067bf-155">Die Syntax für Effekte-Shader ist in der [Funktions Syntax von "Effect" (Direct3D 11)](d3d11-effect-function-syntax.md)ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="067bf-155">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 11)](d3d11-effect-function-syntax.md).</span></span>

## <a name="groups-techniques-and-passes"></a><span data-ttu-id="067bf-156">Gruppen, Techniken und Durchgänge</span><span class="sxs-lookup"><span data-stu-id="067bf-156">Groups, Techniques, and Passes</span></span>

<span data-ttu-id="067bf-157">Bei einer Gruppe handelt es sich um eine Sammlung von Techniken.</span><span class="sxs-lookup"><span data-stu-id="067bf-157">A group is a collection of techniques.</span></span> <span data-ttu-id="067bf-158">Eine Technik ist eine Sammlung von Renderingdurchläufen (es muss mindestens ein Durchlauf vorhanden sein).</span><span class="sxs-lookup"><span data-stu-id="067bf-158">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="067bf-159">Jeder Effekt Durchlauf (ähnlich dem Bereich zu einem einzelnen Durchlauf in einer Renderschleife) definiert den Shader-Zustand und alle anderen Pipeline Zustände, die zum Rendern von Geometrie erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="067bf-159">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="067bf-160">Gruppen sind optional.</span><span class="sxs-lookup"><span data-stu-id="067bf-160">Groups are optional.</span></span> <span data-ttu-id="067bf-161">Es gibt eine einzelne, unbenannte Gruppe, die alle globalen Techniken umfasst.</span><span class="sxs-lookup"><span data-stu-id="067bf-161">There is a single, unnamed group which encompasses all global techniques.</span></span> <span data-ttu-id="067bf-162">Alle anderen Gruppen müssen benannt werden.</span><span class="sxs-lookup"><span data-stu-id="067bf-162">All other groups must be named.</span></span>

<span data-ttu-id="067bf-163">Im folgenden finden Sie ein Beispiel für eine Technik (die einen Durchlauf umfasst) aus BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="067bf-163">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



<span data-ttu-id="067bf-164">Die Syntax für Effekte-Shader ist ausführlicher in der [Effekt Techniken-Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="067bf-164">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="067bf-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="067bf-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="067bf-166">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="067bf-166">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 