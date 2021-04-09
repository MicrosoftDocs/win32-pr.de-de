---
description: Einige Effekt Konstanten müssen nur initialisiert werden.
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: Status des festgelegten Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f14d4cdfb23c56f9534d1b4029482ce4e494b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958273"
---
# <a name="set-effect-state-direct3d-10"></a><span data-ttu-id="078c7-103">Status des festgelegten Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="078c7-103">Set Effect State (Direct3D 10)</span></span>

<span data-ttu-id="078c7-104">Einige Effekt Konstanten müssen nur initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="078c7-104">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="078c7-105">Nach der Initialisierung wird der Effekt Zustand auf das Gerät für die gesamte Renderschleife festgelegt.</span><span class="sxs-lookup"><span data-stu-id="078c7-105">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="078c7-106">Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="078c7-106">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="078c7-107">Der grundlegende Code für das Festlegen von Effekt Variablen wird unten für jeden der Variablen Typen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="078c7-107">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="078c7-108">Ein Effekt kapselt den gesamten renderzustand, der zum Durchführen eines Renderings erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="078c7-108">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="078c7-109">Im Hinblick auf die API gibt es drei Arten von Status, die in einem Effekt gekapselt sind.</span><span class="sxs-lookup"><span data-stu-id="078c7-109">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="078c7-110">Konstanter Zustand</span><span class="sxs-lookup"><span data-stu-id="078c7-110">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="078c7-111">Shader-Status</span><span class="sxs-lookup"><span data-stu-id="078c7-111">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="078c7-112">Textur Zustand</span><span class="sxs-lookup"><span data-stu-id="078c7-112">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="078c7-113">Konstanter Zustand</span><span class="sxs-lookup"><span data-stu-id="078c7-113">Constant State</span></span>

<span data-ttu-id="078c7-114">Deklarieren Sie zunächst Variablen in einem Effekt mithilfe von HLSL-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="078c7-114">First, declare variables in an effect using HLSL data types.</span></span>


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



<span data-ttu-id="078c7-115">Deklarieren Sie die Variablen in der Anwendung, die von der Anwendung festgelegt werden können, und aktualisieren Sie dann die Effekt Variablen.</span><span class="sxs-lookup"><span data-stu-id="078c7-115">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


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

    
OnD3D10CreateDevice()
{
  ...
    g_pLightDir = g_pEffect10->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect10->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect10->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect10->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect10->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect10->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect10->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect10->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="078c7-116">Verwenden Sie Drittens die Update-Methoden, um den Wert der Variablen in der Anwendung in den Effekt Variablen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="078c7-116">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D10FrameRender()
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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="078c7-117">Zwei Möglichkeiten, den Zustand in einer Effekt Variablen zu erhalten</span><span class="sxs-lookup"><span data-stu-id="078c7-117">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="078c7-118">Es gibt zwei Möglichkeiten, den Zustand zu erhalten, der in einer Effekt Variablen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="078c7-118">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="078c7-119">Bei einem Effekt, der in den Arbeitsspeicher geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="078c7-119">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="078c7-120">Eine Möglichkeit besteht darin, den samplerstatus von einer [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) zu erhalten, die als Sampler-Schnittstelle umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="078c7-120">One way is to get the sampler state from an [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) that has been cast as a sampler interface.</span></span>


```
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
        hr = (l_pD3D10EffectVariable->AsSampler())->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="078c7-121">Die andere Möglichkeit besteht darin, den samplerstatus aus einer [**ID3D10SamplerState-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="078c7-121">The other way is to get the sampler state from an [**ID3D10SamplerState Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span></span>


```
ID3D10SamplerState* l_ppSamplerState = NULL;
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
    {
        hr = (l_pD3D10EffectVariable->AsSampler())->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="078c7-122">Shader-Status</span><span class="sxs-lookup"><span data-stu-id="078c7-122">Shader State</span></span>

<span data-ttu-id="078c7-123">Der Shader-Zustand wird in einem Durchlauf deklariert und in einem Effekt zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="078c7-123">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


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



<span data-ttu-id="078c7-124">Dies funktioniert genauso wie bei Verwendung eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="078c7-124">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="078c7-125">Es gibt drei Aufrufe, eine für jeden Shader (Scheitelpunkt, Geometrie und Pixel).</span><span class="sxs-lookup"><span data-stu-id="078c7-125">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="078c7-126">Der erste, setvertexshader, ruft [**ID3D10Device:: vssetshader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader)auf.</span><span class="sxs-lookup"><span data-stu-id="078c7-126">The first one, SetVertexShader, calls [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span></span> <span data-ttu-id="078c7-127">Compileshader ist eine spezielle Effekt Funktion, die das Shader-Profil (vs \_ 4 \_ 0) und den Namen der Vertex-Shader-Funktion (rendervs) annimmt.</span><span class="sxs-lookup"><span data-stu-id="078c7-127">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="078c7-128">Mit anderen Worten: jeder dieser setxxxshader-Aufrufe kompiliert die zugehörige shaderfunktion und gibt einen Zeiger auf den kompilierten Shader zurück.</span><span class="sxs-lookup"><span data-stu-id="078c7-128">In other words, each of these SetXXXShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

## <a name="texture-state"></a><span data-ttu-id="078c7-129">Textur Zustand</span><span class="sxs-lookup"><span data-stu-id="078c7-129">Texture State</span></span>

<span data-ttu-id="078c7-130">Der Textur Zustand ist ein wenig komplexer als das Festlegen einer Variablen, da Textur Daten nicht einfach wie eine Variable gelesen werden, sondern aus einer Textur entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="078c7-130">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="078c7-131">Daher müssen Sie die Textur Variable definieren (genau wie eine normale Variable, mit der Ausnahme, dass ein Textur-Typ verwendet wird), und Sie müssen die Samplings definieren.</span><span class="sxs-lookup"><span data-stu-id="078c7-131">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="078c7-132">Im folgenden finden Sie ein Beispiel für eine Textur Variablen Deklaration und die entsprechende Samplings-Zustands Deklaration.</span><span class="sxs-lookup"><span data-stu-id="078c7-132">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="078c7-133">Im folgenden finden Sie ein Beispiel für das Festlegen einer Textur aus einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="078c7-133">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="078c7-134">In diesem Beispiel wird die Textur in den Mesh-Daten gespeichert, die beim Erstellen des Effekts geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="078c7-134">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="078c7-135">Der erste Schritt besteht darin, einen Zeiger auf die Textur aus dem Effekt (aus dem Mesh) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="078c7-135">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="078c7-136">Der zweite Schritt besteht darin, eine Sicht für den Zugriff auf die Textur anzugeben.</span><span class="sxs-lookup"><span data-stu-id="078c7-136">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="078c7-137">Die Sicht definiert eine allgemeine Methode für den Zugriff auf die Daten aus der Textur Ressource.</span><span class="sxs-lookup"><span data-stu-id="078c7-137">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D10FrameRender()
{
  ID3D10ShaderResourceView* pDiffuseRV = NULL;

   ...
   pDiffuseRV = g_Mesh10.GetMaterial(pSubset->MaterialID)->pDiffuseRV10;
   g_ptxDiffuse->SetResource( pDiffuseRV );
   ...
}   
```



<span data-ttu-id="078c7-138">Weitere Informationen zum Anzeigen von Ressourcen finden Sie unter [Textur Ansichten (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="078c7-138">For more information about viewing resources, see [Texture Views (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="078c7-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="078c7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="078c7-140">Rendern eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="078c7-140">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



