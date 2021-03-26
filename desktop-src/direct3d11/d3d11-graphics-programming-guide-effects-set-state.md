---
title: Status des festgelegten Effekts (Direct3D 11)
description: Einige Effekt Konstanten müssen nur initialisiert werden.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df65e164c2df01f78ae9ea9ab83a547b977335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515530"
---
# <a name="set-effect-state-direct3d-11"></a><span data-ttu-id="7d0ef-103">Status des festgelegten Effekts (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="7d0ef-103">Set Effect State (Direct3D 11)</span></span>

<span data-ttu-id="7d0ef-104">Einige Effekt Konstanten müssen nur initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-104">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="7d0ef-105">Nach der Initialisierung wird der Effekt Zustand auf das Gerät für die gesamte Renderschleife festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-105">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="7d0ef-106">Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-106">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="7d0ef-107">Der grundlegende Code für das Festlegen von Effekt Variablen wird unten für jeden der Variablen Typen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-107">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="7d0ef-108">Ein Effekt kapselt den gesamten renderzustand, der zum Durchführen eines Renderings erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-108">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="7d0ef-109">Im Hinblick auf die API gibt es drei Arten von Status, die in einem Effekt gekapselt sind.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-109">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="7d0ef-110">Konstanter Zustand</span><span class="sxs-lookup"><span data-stu-id="7d0ef-110">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="7d0ef-111">Shader-Status</span><span class="sxs-lookup"><span data-stu-id="7d0ef-111">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="7d0ef-112">Textur Zustand</span><span class="sxs-lookup"><span data-stu-id="7d0ef-112">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="7d0ef-113">Konstanter Zustand</span><span class="sxs-lookup"><span data-stu-id="7d0ef-113">Constant State</span></span>

<span data-ttu-id="7d0ef-114">Deklarieren Sie zunächst Variablen in einem Effekt mithilfe von HLSL-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-114">First, declare variables in an effect using HLSL data types.</span></span>


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



<span data-ttu-id="7d0ef-115">Deklarieren Sie die Variablen in der Anwendung, die von der Anwendung festgelegt werden können, und aktualisieren Sie dann die Effekt Variablen.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-115">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D11CreateDevice()
{
  ...
    g_pLightDir = g_pEffect11->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect11->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect11->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect11->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect11->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect11->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect11->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect11->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="7d0ef-116">Verwenden Sie Drittens die Update-Methoden, um den Wert der Variablen in der Anwendung in den Effekt Variablen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-116">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D11FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="7d0ef-117">Zwei Möglichkeiten, den Zustand in einer Effekt Variablen zu erhalten</span><span class="sxs-lookup"><span data-stu-id="7d0ef-117">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="7d0ef-118">Es gibt zwei Möglichkeiten, den Zustand zu erhalten, der in einer Effekt Variablen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-118">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="7d0ef-119">Bei einem Effekt, der in den Arbeitsspeicher geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-119">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="7d0ef-120">Eine Möglichkeit besteht darin, den samplerstatus von einem [**ID3DX11EffectVariable**](id3dx11effectvariable.md) zu erhalten, der als Sampler-Schnittstelle umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-120">One way is to get the sampler state from an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) that has been cast as a sampler interface.</span></span>


```
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid() )
        hr = (l_pD3D11EffectVariable->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="7d0ef-121">Die andere Möglichkeit besteht darin, den samplerstatus von einem [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-121">The other way is to get the sampler state from an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span></span>


```
ID3D11SamplerState* l_ppSamplerState = NULL;
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid )
    {
        hr = l_pD3D11EffectVariable->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="7d0ef-122">Shader-Status</span><span class="sxs-lookup"><span data-stu-id="7d0ef-122">Shader State</span></span>

<span data-ttu-id="7d0ef-123">Der Shader-Zustand wird in einem Durchlauf deklariert und in einem Effekt zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-123">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
VertexShader vsRenderScene = CompileShader( vs_4_0, RenderSceneVS( 1, true, true );  
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( vsRenderScene );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="7d0ef-124">Dies funktioniert genauso wie bei Verwendung eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-124">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="7d0ef-125">Es gibt drei Aufrufe, eine für jeden Shader (Scheitelpunkt, Geometrie und Pixel).</span><span class="sxs-lookup"><span data-stu-id="7d0ef-125">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="7d0ef-126">Der erste, setvertexshader, ruft [**Verknüpfung id3d11devicecontext aus:: vssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader)auf.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-126">The first one, SetVertexShader, calls [**ID3D11DeviceContext::VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span></span> <span data-ttu-id="7d0ef-127">Compileshader ist eine spezielle Effekt Funktion, die das Shader-Profil (vs \_ 4 \_ 0) und den Namen der Vertex-Shader-Funktion (rendervs) annimmt.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-127">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="7d0ef-128">Mit anderen Worten: jeder dieser compileshader-Aufrufe kompiliert die zugehörige shaderfunktion und gibt einen Zeiger auf den kompilierten Shader zurück.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-128">In other words, each of these CompileShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

<span data-ttu-id="7d0ef-129">Beachten Sie, dass nicht der gesamte shaderzustand festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-129">Note that not all shader state must be set.</span></span> <span data-ttu-id="7d0ef-130">Dieser Durchlauf umfasst keine sethullshader-oder setdomainshader-Aufrufe, was bedeutet, dass die derzeit gebundene Hülle und die Domänen-Shader unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-130">This pass does not include any SetHullShader or SetDomainShader calls, meaning that the currently bound hull and domain shaders will be unchanged.</span></span>

## <a name="texture-state"></a><span data-ttu-id="7d0ef-131">Textur Zustand</span><span class="sxs-lookup"><span data-stu-id="7d0ef-131">Texture State</span></span>

<span data-ttu-id="7d0ef-132">Der Textur Zustand ist ein wenig komplexer als das Festlegen einer Variablen, da Textur Daten nicht einfach wie eine Variable gelesen werden, sondern aus einer Textur entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-132">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="7d0ef-133">Daher müssen Sie die Textur Variable definieren (genau wie eine normale Variable, mit der Ausnahme, dass ein Textur-Typ verwendet wird), und Sie müssen die Samplings definieren.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-133">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="7d0ef-134">Im folgenden finden Sie ein Beispiel für eine Textur Variablen Deklaration und die entsprechende Samplings-Zustands Deklaration.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-134">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="7d0ef-135">Im folgenden finden Sie ein Beispiel für das Festlegen einer Textur aus einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-135">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="7d0ef-136">In diesem Beispiel wird die Textur in den Mesh-Daten gespeichert, die beim Erstellen des Effekts geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-136">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="7d0ef-137">Der erste Schritt besteht darin, einen Zeiger auf die Textur aus dem Effekt (aus dem Mesh) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-137">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="7d0ef-138">Der zweite Schritt besteht darin, eine Sicht für den Zugriff auf die Textur anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-138">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="7d0ef-139">Die Sicht definiert eine allgemeine Methode für den Zugriff auf die Daten aus der Textur Ressource.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-139">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D11FrameRender()
{
  ID3D11ShaderResourceView* pDiffuseRV = NULL;

  ...
  pDiffuseRV = g_Mesh11.GetMaterial(pSubset->MaterialID)->pDiffuseRV11;
  g_ptxDiffuse->SetResource( pDiffuseRV );
  ...
}   
```



<span data-ttu-id="7d0ef-140">Aus Sicht der Anwendung werden ungeordnete Zugriffs Sichten ähnlich wie Shader-Ressourcen Ansichten behandelt.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-140">From the application perspective, unordered access views are handled similarly to shader resource views.</span></span> <span data-ttu-id="7d0ef-141">Allerdings werden bei der Auswirkung von Pixelshader-und Compute-Shaderfunktionen nicht geordnete zugriffsansichts Daten direkt aus/geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-141">However, in the effect pixel shader and compute shader functions, unordered access view data is read from/written to directly.</span></span> <span data-ttu-id="7d0ef-142">Eine Stichprobe kann nicht aus einer unsortierter Zugriffs Ansicht entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="7d0ef-142">You cannot sample from an unordered access view.</span></span>

<span data-ttu-id="7d0ef-143">Weitere Informationen zum Anzeigen von Ressourcen finden Sie unter [Ressourcen](overviews-direct3d-11-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7d0ef-143">For more information about viewing resources, see [Resources](overviews-direct3d-11-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d0ef-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d0ef-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d0ef-145">Rendern eines Effekts (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="7d0ef-145">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




