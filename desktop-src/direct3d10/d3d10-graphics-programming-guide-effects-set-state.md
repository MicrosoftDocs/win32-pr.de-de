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
# <a name="set-effect-state-direct3d-10"></a>Status des festgelegten Effekts (Direct3D 10)

Einige Effekt Konstanten müssen nur initialisiert werden. Nach der Initialisierung wird der Effekt Zustand auf das Gerät für die gesamte Renderschleife festgelegt. Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird. Der grundlegende Code für das Festlegen von Effekt Variablen wird unten für jeden der Variablen Typen angezeigt.

Ein Effekt kapselt den gesamten renderzustand, der zum Durchführen eines Renderings erforderlich ist. Im Hinblick auf die API gibt es drei Arten von Status, die in einem Effekt gekapselt sind.

-   [Konstanter Zustand](#constant-state)
-   [Shader-Status](#shader-state)
-   [Textur Zustand](#texture-state)

## <a name="constant-state"></a>Konstanter Zustand

Deklarieren Sie zunächst Variablen in einem Effekt mithilfe von HLSL-Datentypen.


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



Deklarieren Sie die Variablen in der Anwendung, die von der Anwendung festgelegt werden können, und aktualisieren Sie dann die Effekt Variablen.


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



Verwenden Sie Drittens die Update-Methoden, um den Wert der Variablen in der Anwendung in den Effekt Variablen festzulegen.


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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>Zwei Möglichkeiten, den Zustand in einer Effekt Variablen zu erhalten

Es gibt zwei Möglichkeiten, den Zustand zu erhalten, der in einer Effekt Variablen enthalten ist. Bei einem Effekt, der in den Arbeitsspeicher geladen wurde.

Eine Möglichkeit besteht darin, den samplerstatus von einer [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) zu erhalten, die als Sampler-Schnittstelle umgewandelt wurde.


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



Die andere Möglichkeit besteht darin, den samplerstatus aus einer [**ID3D10SamplerState-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate)zu erhalten.


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



## <a name="shader-state"></a>Shader-Status

Der Shader-Zustand wird in einem Durchlauf deklariert und in einem Effekt zugewiesen.


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



Dies funktioniert genauso wie bei Verwendung eines Effekts. Es gibt drei Aufrufe, eine für jeden Shader (Scheitelpunkt, Geometrie und Pixel). Der erste, setvertexshader, ruft [**ID3D10Device:: vssetshader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader)auf. Compileshader ist eine spezielle Effekt Funktion, die das Shader-Profil (vs \_ 4 \_ 0) und den Namen der Vertex-Shader-Funktion (rendervs) annimmt. Mit anderen Worten: jeder dieser setxxxshader-Aufrufe kompiliert die zugehörige shaderfunktion und gibt einen Zeiger auf den kompilierten Shader zurück.

## <a name="texture-state"></a>Textur Zustand

Der Textur Zustand ist ein wenig komplexer als das Festlegen einer Variablen, da Textur Daten nicht einfach wie eine Variable gelesen werden, sondern aus einer Textur entnommen werden. Daher müssen Sie die Textur Variable definieren (genau wie eine normale Variable, mit der Ausnahme, dass ein Textur-Typ verwendet wird), und Sie müssen die Samplings definieren. Im folgenden finden Sie ein Beispiel für eine Textur Variablen Deklaration und die entsprechende Samplings-Zustands Deklaration.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Im folgenden finden Sie ein Beispiel für das Festlegen einer Textur aus einer Anwendung. In diesem Beispiel wird die Textur in den Mesh-Daten gespeichert, die beim Erstellen des Effekts geladen wurden.

Der erste Schritt besteht darin, einen Zeiger auf die Textur aus dem Effekt (aus dem Mesh) zu erhalten.


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



Der zweite Schritt besteht darin, eine Sicht für den Zugriff auf die Textur anzugeben. Die Sicht definiert eine allgemeine Methode für den Zugriff auf die Daten aus der Textur Ressource.


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



Weitere Informationen zum Anzeigen von Ressourcen finden Sie unter [Textur Ansichten (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



