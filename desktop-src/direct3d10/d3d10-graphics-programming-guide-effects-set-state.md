---
description: Einige Effektkonstanten müssen nur initialisiert werden. Informationen zum Festlegen von Effektvariablen in Direct3D 10 finden Sie im grundlegenden Code.
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: Festlegen des Effektzustands (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df7133276b6392abca8d75eed16de896fb58f84
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404723"
---
# <a name="set-effect-state-direct3d-10"></a><span data-ttu-id="3b091-104">Festlegen des Effektzustands (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3b091-104">Set Effect State (Direct3D 10)</span></span>

<span data-ttu-id="3b091-105">Einige Effektkonstanten müssen nur initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b091-105">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="3b091-106">Nach der Initialisierung wird der Effektzustand für die gesamte Renderschleife auf das Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3b091-106">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="3b091-107">Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3b091-107">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="3b091-108">Der grundlegende Code zum Festlegen von Effektvariablen ist unten für jeden Variablentyp dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3b091-108">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="3b091-109">Ein Effekt kapselt den gesamten Renderzustand, der für einen Renderingdurchlauf erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3b091-109">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="3b091-110">Im Hinblick auf die API gibt es drei Arten von Zuständen, die in einem Effekt gekapselt sind.</span><span class="sxs-lookup"><span data-stu-id="3b091-110">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="3b091-111">Konstanter Zustand</span><span class="sxs-lookup"><span data-stu-id="3b091-111">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="3b091-112">Shaderstatus</span><span class="sxs-lookup"><span data-stu-id="3b091-112">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="3b091-113">Texturzustand</span><span class="sxs-lookup"><span data-stu-id="3b091-113">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="3b091-114">Konstanter Zustand</span><span class="sxs-lookup"><span data-stu-id="3b091-114">Constant State</span></span>

<span data-ttu-id="3b091-115">Deklarieren Sie zunächst Variablen in einem Effekt mit HLSL-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="3b091-115">First, declare variables in an effect using HLSL data types.</span></span>


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



<span data-ttu-id="3b091-116">Deklarieren Sie zweitens Variablen in der Anwendung, die von der Anwendung festgelegt werden können, und aktualisieren Sie dann die Auswirkungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="3b091-116">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


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



<span data-ttu-id="3b091-117">Verwenden Sie drittens die Updatemethoden, um den Wert der Variablen in der Anwendung in den Effect-Variablen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3b091-117">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="3b091-118">Zwei Möglichkeiten zum Abrufen des Zustands in einer Effektvariablen</span><span class="sxs-lookup"><span data-stu-id="3b091-118">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="3b091-119">Es gibt zwei Möglichkeiten, den in einer Effektvariablen enthaltenen Zustand abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b091-119">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="3b091-120">Gibt einen Effekt an, der in den Arbeitsspeicher geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="3b091-120">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="3b091-121">Eine Möglichkeit besteht darin, den Samplerzustand aus einer [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) abzurufen, die als Samplerschnittstelle castet wurde.</span><span class="sxs-lookup"><span data-stu-id="3b091-121">One way is to get the sampler state from an [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) that has been cast as a sampler interface.</span></span>


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



<span data-ttu-id="3b091-122">Die andere Möglichkeit besteht darin, den Samplerzustand aus einer [**ID3D10SamplerState-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate)abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b091-122">The other way is to get the sampler state from an [**ID3D10SamplerState Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span></span>


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



## <a name="shader-state"></a><span data-ttu-id="3b091-123">Shaderstatus</span><span class="sxs-lookup"><span data-stu-id="3b091-123">Shader State</span></span>

<span data-ttu-id="3b091-124">Der Shaderzustand wird in einer Effekttechnik innerhalb eines Durchlaufs deklariert und zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3b091-124">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


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



<span data-ttu-id="3b091-125">Dies funktioniert genauso wie bei der Verwendung eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="3b091-125">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="3b091-126">Es gibt drei Aufrufe, einen für jeden Shadertyp (Scheitelpunkt, Geometrie und Pixel).</span><span class="sxs-lookup"><span data-stu-id="3b091-126">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="3b091-127">Die erste , SetVertexShader, ruft [**ID3D10Device::VSSetShader auf.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader)</span><span class="sxs-lookup"><span data-stu-id="3b091-127">The first one, SetVertexShader, calls [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span></span> <span data-ttu-id="3b091-128">CompileShader ist eine Funktion mit speziellen Effekten, die das Shaderprofil (im Vergleich \_ zu 4 \_ 0) und den Namen der Vertexshaderfunktion (RenderVS) übernimmt.</span><span class="sxs-lookup"><span data-stu-id="3b091-128">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="3b091-129">Anders ausgedrückt: Jeder dieser SetXXXShader-Aufrufe kompiliert die zugeordnete Shaderfunktion und gibt einen Zeiger auf den kompilierten Shader zurück.</span><span class="sxs-lookup"><span data-stu-id="3b091-129">In other words, each of these SetXXXShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

## <a name="texture-state"></a><span data-ttu-id="3b091-130">Texturzustand</span><span class="sxs-lookup"><span data-stu-id="3b091-130">Texture State</span></span>

<span data-ttu-id="3b091-131">Der Texturzustand ist etwas komplexer als das Festlegen einer Variablen, da Texturdaten nicht einfach wie eine Variable gelesen werden, sondern aus einer Textur entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="3b091-131">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="3b091-132">Daher müssen Sie die Texturvariable definieren (genau wie eine normale Variable mit Ausnahme eines Texturtyps), und Sie müssen die Samplingbedingungen definieren.</span><span class="sxs-lookup"><span data-stu-id="3b091-132">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="3b091-133">Hier sehen Sie ein Beispiel für eine Texturvariablendeklaration und die entsprechende Samplingzustandsdeklaration.</span><span class="sxs-lookup"><span data-stu-id="3b091-133">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="3b091-134">Hier sehen Sie ein Beispiel für das Festlegen einer Textur aus einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3b091-134">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="3b091-135">In diesem Beispiel wird die Textur in den Gitternetzdaten gespeichert, die beim Erstellen des Effekts geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="3b091-135">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="3b091-136">Der erste Schritt besteht darin, einen Zeiger auf die Textur aus dem Effekt (aus dem Gitternetz) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b091-136">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="3b091-137">Im zweiten Schritt wird eine Ansicht für den Zugriff auf die Textur angegeben.</span><span class="sxs-lookup"><span data-stu-id="3b091-137">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="3b091-138">Die Ansicht definiert eine allgemeine Möglichkeit, auf die Daten aus der Texturressource zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="3b091-138">The view defines a general way to access the data from the texture resource.</span></span>


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



<span data-ttu-id="3b091-139">Weitere Informationen zum Anzeigen von Ressourcen finden Sie unter [Texturansichten (Direct3D 10).](d3d10-graphics-programming-guide-resources-access-views.md)</span><span class="sxs-lookup"><span data-stu-id="3b091-139">For more information about viewing resources, see [Texture Views (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b091-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b091-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b091-141">Rendern eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3b091-141">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



