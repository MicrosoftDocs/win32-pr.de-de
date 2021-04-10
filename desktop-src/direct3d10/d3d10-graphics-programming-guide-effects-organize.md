---
description: 'Mit Direct3D 10 wird der Effekt Zustand für bestimmte Pipeline Stufen nach den folgenden Strukturen organisiert:'
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organisieren des Zustands in einem Effekt (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126320"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a><span data-ttu-id="3638f-103">Organisieren des Zustands in einem Effekt (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3638f-103">Organizing State in an Effect (Direct3D 10)</span></span>

<span data-ttu-id="3638f-104">Mit Direct3D 10 wird der Effekt Zustand für bestimmte Pipeline Stufen nach den folgenden Strukturen organisiert:</span><span class="sxs-lookup"><span data-stu-id="3638f-104">With Direct3D 10, effect state for certain pipeline stages is organized by the following structures:</span></span>



| <span data-ttu-id="3638f-105">Pipeline Status</span><span class="sxs-lookup"><span data-stu-id="3638f-105">Pipeline State</span></span>  | <span data-ttu-id="3638f-106">Struktur</span><span class="sxs-lookup"><span data-stu-id="3638f-106">Structure</span></span>                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3638f-107">Eingabe-Assembler</span><span class="sxs-lookup"><span data-stu-id="3638f-107">Input Assembler</span></span> | [<span data-ttu-id="3638f-108">**D3d10 \_ Eingabe \_ Element-Element \_**</span><span class="sxs-lookup"><span data-stu-id="3638f-108">**D3D10\_INPUT\_ELEMENT\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| <span data-ttu-id="3638f-109">Rasterung</span><span class="sxs-lookup"><span data-stu-id="3638f-109">Rasterization</span></span>   | [<span data-ttu-id="3638f-110">**D3d10 \_ Rasterizer- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="3638f-110">**D3D10\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| <span data-ttu-id="3638f-111">Ausgabezusammenführung</span><span class="sxs-lookup"><span data-stu-id="3638f-111">Output Merger</span></span>   | <span data-ttu-id="3638f-112">[**D3d10 \_ Blend \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) -Debug-und [ **d3d10- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="3638f-112">[**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) and [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |



 

<span data-ttu-id="3638f-113">In den Shader-Phasen, in denen die Anzahl der Zustandsänderungen von einer Anwendung stärker gesteuert werden muss, wurde der Zustand in den konstanten Puffer Status, den samplerstatus und den Shader-Ressourcen Zustand aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="3638f-113">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, and shader resource state.</span></span> <span data-ttu-id="3638f-114">Dadurch wird eine Anwendung ermöglicht, die sorgfältig entworfen wurde, um nur den geänderten Zustand zu aktualisieren. Dadurch wird die Leistung verbessert, da die Datenmenge reduziert wird, die an die GPU übermittelt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3638f-114">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="3638f-115">Wie organisieren Sie also den Pipeline Status in einem Effekt?</span><span class="sxs-lookup"><span data-stu-id="3638f-115">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="3638f-116">Die Antwort ist, dass die Reihenfolge keine Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="3638f-116">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="3638f-117">Globale Variablen müssen sich nicht im oberen Bereich befinden.</span><span class="sxs-lookup"><span data-stu-id="3638f-117">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="3638f-118">Allerdings wird für alle Beispiele im SDK dieselbe Reihenfolge befolgt, da es eine bewährte Methode ist, die Daten auf die gleiche Weise zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="3638f-118">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="3638f-119">Dies ist eine kurze Beschreibung der Datenreihen Folge in den DirectX SDK-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="3638f-119">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="3638f-120">Globale Variablen</span><span class="sxs-lookup"><span data-stu-id="3638f-120">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="3638f-121">Shader</span><span class="sxs-lookup"><span data-stu-id="3638f-121">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="3638f-122">Techniken und Durchgänge</span><span class="sxs-lookup"><span data-stu-id="3638f-122">Techniques and Passes</span></span>](#techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="3638f-123">Globale Variablen</span><span class="sxs-lookup"><span data-stu-id="3638f-123">Global Variables</span></span>

<span data-ttu-id="3638f-124">Ebenso wie die Standard-C-Übung werden globale Variablen zuerst am Anfang der Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="3638f-124">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="3638f-125">In den meisten Fällen handelt es sich hierbei um Variablen, die von einer Anwendung initialisiert und dann in einem Effekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3638f-125">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="3638f-126">Manchmal werden Sie initialisiert und nie geändert, in anderen Fällen, in denen Sie jedes Frame aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3638f-126">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="3638f-127">Ebenso wie Regeln des C-Funktions Bereichs sind Effekte, die außerhalb des Gültigkeits Bereichs von Effekten deklariert wurden, während des Effekts sichtbar. jede Variable, die innerhalb einer Effekt Funktion deklariert wird, ist nur innerhalb dieser Funktion sichtbar.</span><span class="sxs-lookup"><span data-stu-id="3638f-127">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="3638f-128">Im folgenden finden Sie ein Beispiel für die Variablen, die in BasicHLSL10. FX deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="3638f-128">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="3638f-129">Die Syntax für Effekt Variablen wird in der [Variablen Syntax von Effect (Direct3D 10)](d3d10-effect-variable-syntax.md)ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3638f-129">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md).</span></span> <span data-ttu-id="3638f-130">Die Syntax für Effekt Textur-Samplern ist ausführlicher im [Samplingtyp (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md)ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3638f-130">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="shaders"></a><span data-ttu-id="3638f-131">Shader</span><span class="sxs-lookup"><span data-stu-id="3638f-131">Shaders</span></span>

<span data-ttu-id="3638f-132">Shader sind kleine ausführbare Programme.</span><span class="sxs-lookup"><span data-stu-id="3638f-132">Shaders are small executable programs.</span></span> <span data-ttu-id="3638f-133">Sie können sich Shader als kapselnde shaderzustand vorstellen, da der HLSL-Code die shaderfunktionalität implementiert.</span><span class="sxs-lookup"><span data-stu-id="3638f-133">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="3638f-134">Die Pipeline verwendet drei verschiedene Arten von Shadern.</span><span class="sxs-lookup"><span data-stu-id="3638f-134">The pipeline uses three different kinds of shaders.</span></span>

-   <span data-ttu-id="3638f-135">Vertex-Shader: Arbeiten mit Vertex-Daten.</span><span class="sxs-lookup"><span data-stu-id="3638f-135">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="3638f-136">Ein Scheitelpunkt in ergibt einen Scheitelpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="3638f-136">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="3638f-137">Geometry-Shader: Arbeiten mit primitiven Daten.</span><span class="sxs-lookup"><span data-stu-id="3638f-137">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="3638f-138">Ein primitiver in kann 0, 1 oder viele primitive ergeben.</span><span class="sxs-lookup"><span data-stu-id="3638f-138">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="3638f-139">Pixel-Shader: Arbeiten mit Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="3638f-139">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="3638f-140">Ein Pixel in ergibt 1 Pixel, es sei denn, das Pixel ist aus einem Rendering herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="3638f-140">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="3638f-141">Shader sind lokale Funktionen und folgen Regeln für C-Stil Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3638f-141">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="3638f-142">Wenn ein Effekt kompiliert wird, wird jeder Shader kompiliert, und ein Zeiger auf jede Shader-Funktion wird intern gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3638f-142">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="3638f-143">Bei erfolgreicher Kompilierung wird eine ID3D10Effect-Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3638f-143">An ID3D10Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="3638f-144">An diesem Punkt liegt der kompilierte Effekt in einem zwischen Format vor.</span><span class="sxs-lookup"><span data-stu-id="3638f-144">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="3638f-145">Um weitere Informationen zu den kompilierten Shadern zu erhalten, müssen Sie die Shader-Reflektion verwenden.</span><span class="sxs-lookup"><span data-stu-id="3638f-145">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="3638f-146">Dies entspricht im Wesentlichen dem Anfordern der Laufzeit, die Shader zu dekompilieren, und gibt Informationen über den Shader-Code zurück.</span><span class="sxs-lookup"><span data-stu-id="3638f-146">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="3638f-147">Die Syntax für Effekte-Shader ist in der [Funktions Syntax von "Effect" (Direct3D 10)](d3d10-effect-function-syntax.md)ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3638f-147">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md).</span></span>

## <a name="techniques-and-passes"></a><span data-ttu-id="3638f-148">Techniken und Durchgänge</span><span class="sxs-lookup"><span data-stu-id="3638f-148">Techniques and Passes</span></span>

<span data-ttu-id="3638f-149">Eine Technik ist eine Sammlung von Renderingdurchläufen (es muss mindestens ein Durchlauf vorhanden sein).</span><span class="sxs-lookup"><span data-stu-id="3638f-149">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="3638f-150">Jeder Effekt Durchlauf (ähnlich dem Bereich zu einem einzelnen Durchlauf in einer Renderschleife) definiert den Shader-Zustand und alle anderen Pipeline Zustände, die zum Rendern von Geometrie erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3638f-150">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="3638f-151">Im folgenden finden Sie ein Beispiel für eine Technik (die einen Durchlauf umfasst) aus BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="3638f-151">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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
```



<span data-ttu-id="3638f-152">Die Syntax für Effekte-Shader ist ausführlicher in der [Effekt Techniken-Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="3638f-152">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3638f-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3638f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3638f-154">Effekte (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3638f-154">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
