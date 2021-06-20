---
title: Festlegen des Effektzustands (Direct3D 11)
description: Einige Effektkonstanten müssen nur initialisiert werden. Informationen zum Festlegen von Effektvariablen in Direct3D 12 finden Sie im grundlegenden Code.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c64f9e642e867e9398722d4590a4c2ce9193b4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407663"
---
# <a name="set-effect-state-direct3d-11"></a>Festlegen des Effektzustands (Direct3D 11)

Einige Effektkonstanten müssen nur initialisiert werden. Nach der Initialisierung wird der Effektzustand für die gesamte Renderschleife auf das Gerät festgelegt. Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird. Der grundlegende Code zum Festlegen von Effektvariablen ist unten für jeden Variablentyp dargestellt.

Ein Effekt kapselt den gesamten Renderzustand, der für einen Renderingdurchlauf erforderlich ist. Im Hinblick auf die API gibt es drei Arten von Zuständen, die in einem Effekt gekapselt sind.

-   [Konstanter Zustand](#constant-state)
-   [Shaderstatus](#shader-state)
-   [Texturzustand](#texture-state)

## <a name="constant-state"></a>Konstanter Zustand

Deklarieren Sie zunächst Variablen in einem Effekt mit HLSL-Datentypen.


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



Deklarieren Sie zweitens Variablen in der Anwendung, die von der Anwendung festgelegt werden können, und aktualisieren Sie dann die Auswirkungsvariablen.


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



Verwenden Sie drittens die Updatemethoden, um den Wert der Variablen in der Anwendung in den Effect-Variablen festzulegen.


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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>Zwei Möglichkeiten zum Abrufen des Zustands in einer Effektvariablen

Es gibt zwei Möglichkeiten, den in einer Effektvariablen enthaltenen Zustand abzurufen. Bei einem Effekt, der in den Arbeitsspeicher geladen wurde.

Eine Möglichkeit besteht darin, den Samplerzustand aus einer [**ID3DX11EffectVariable**](id3dx11effectvariable.md) abzurufen, die als Samplerschnittstelle castet wurde.


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



Die andere Möglichkeit besteht darin, den Samplerzustand aus einem [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)abzurufen.


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



## <a name="shader-state"></a>Shaderstatus

Der Shaderzustand wird in einer Effekttechnik innerhalb eines Durchlaufs deklariert und zugewiesen.


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



Dies funktioniert genauso wie bei verwendung eines Effekts. Es gibt drei Aufrufe, einen für jeden Shadertyp (Scheitelpunkt, Geometrie und Pixel). Die erste , SetVertexShader, ruft [**ID3D11DeviceContext::VSSetShader auf.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader) CompileShader ist eine Funktion mit speziellen Effekten, die das Shaderprofil (im Vergleich \_ zu 4 \_ 0) und den Namen der Vertexshaderfunktion (RenderVS) übernimmt. Anders ausgedrückt: Jeder dieser CompileShader-Aufrufe kompiliert die zugeordnete Shaderfunktion und gibt einen Zeiger auf den kompilierten Shader zurück.

Beachten Sie, dass nicht der gesamte Shaderzustand festgelegt werden muss. Dieser Durchlauf enthält keine SetHullShader- oder SetDomainShader-Aufrufe, was bedeutet, dass die derzeit gebundene Hülle und die Domänenshader unverändert bleiben.

## <a name="texture-state"></a>Texturzustand

Der Texturzustand ist etwas komplexer als das Festlegen einer Variablen, da Texturdaten nicht einfach wie eine Variable gelesen werden, sondern aus einer Textur entnommen werden. Daher müssen Sie die Texturvariable definieren (genau wie eine normale Variable mit Ausnahme eines Texturtyps), und Sie müssen die Samplingbedingungen definieren. Hier sehen Sie ein Beispiel für eine Texturvariablendeklaration und die entsprechende Samplingzustandsdeklaration.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Hier sehen Sie ein Beispiel für das Festlegen einer Textur aus einer Anwendung. In diesem Beispiel wird die Textur in den Gitternetzdaten gespeichert, die beim Erstellen des Effekts geladen wurden.

Der erste Schritt besteht darin, einen Zeiger auf die Textur aus dem Effekt (aus dem Gitternetz) zu erhalten.


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



Im zweiten Schritt wird eine Ansicht für den Zugriff auf die Textur angegeben. Die Ansicht definiert eine allgemeine Möglichkeit, auf die Daten aus der Texturressource zuzugreifen.


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



Aus Sicht der Anwendung werden unsortierte Zugriffsansichten ähnlich wie Shaderressourcenansichten behandelt. In den Effekten Pixel-Shader und Compute-Shaderfunktionen werden ungeordnete Zugriffsansichtsdaten jedoch direkt aus gelesen bzw. in diese geschrieben. Sie können keine Stichproben aus einer ungeordneten Zugriffsansicht erstellen.

Weitere Informationen zum Anzeigen von Ressourcen finden Sie unter [Ressourcen](overviews-direct3d-11-resources.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




