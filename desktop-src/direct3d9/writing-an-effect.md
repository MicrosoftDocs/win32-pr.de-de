---
description: Das Schreiben eines Effekts erfordert, dass Sie die Syntax des Effekts verstehen und die erforderlichen Zustandsinformationen generieren. Sie können den Shader-Zustand, die Textur und den samplerstatus sowie den gesamten Pipeline Zustand hinzufügen, der für Ihre Anwendung erforderlich ist.
ms.assetid: 361dd260-526a-4484-8dc9-3857874e5023
title: Schreiben eines Effekts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0f456c5a2bce66f782b4da7d426de5c86bbb33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345389"
---
# <a name="writing-an-effect-direct3d-9"></a>Schreiben eines Effekts (Direct3D 9)

Das Schreiben eines Effekts erfordert, dass Sie die Syntax des Effekts verstehen und die erforderlichen Zustandsinformationen generieren. Sie können den Shader-Zustand, die Textur und den samplerstatus sowie den gesamten Pipeline Zustand hinzufügen, der für Ihre Anwendung erforderlich ist.

Die Effekt Syntax wird im [Effekt Format (Direct3D 9)](dx9-graphics-reference-effects-file-format.md)ausführlich beschrieben. Ein Effekt wird in der Regel in eine Effekt Datei (. fx) gekapselt, könnte aber auch als Text Zeichenfolge in einer Anwendung geschrieben werden.

## <a name="effect-example"></a>Beispiel für Effekte

Effekte enthalten drei Arten von Zuständen: shaderzustand, Textur-und samplerzustand und Pipeline Zustand. Im folgenden finden Sie ein Beispiel für einen Effekt aus dem [basichlsl](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx)-Beispiel:


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

texture g_MeshTexture;              // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
// Texture samplers
sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};
struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
  
    float4 vAnimatedPos = vPos;
    
    // Animation the vertex based on time and the vertex's object space position
    if( bAnimate )
        vAnimatedPos += float4(vNormal, 0) * (sin(g_fTime+5.5)+0.5)*5;
    
    // Transform the position from object space to homogeneous projection space
    Output.Position = mul(vAnimatedPos, g_mWorldViewProjection);
    
    // Transform the normal from object space to world space    
    vNormalWorldSpace = normalize(mul(vNormal, (float3x3)g_mWorld));
    
    // Compute simple directional lighting equation
    float3 vTotalLightDiffuse = float3(0,0,0);
    for(int i=0; i < nNumLights; i++ )
        vTotalLightDiffuse += g_LightDiffuse[i] * max(0,dot(vNormalWorldSpace, g_LightDir[i]));
        
    Output.Diffuse.rgb = g_MaterialDiffuseColor * vTotalLightDiffuse + 
                         g_MaterialAmbientColor * g_LightAmbient;   
    Output.Diffuse.a = 1.0f; 
    
    // Just copy the texture coordinate through
    if( bTexture ) 
        Output.TextureUV = vTexCoord0; 
    else
        Output.TextureUV = 0; 
    
    return Output;    
}
struct PS_OUTPUT
{
    float4 RGBColor : COLOR0;  // Pixel color    
};
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_1_1 RenderScenePS( true ); 
    }
}
```



Dieser Effekt enthält Folgendes:

-   Der Shader-Zustand, bei dem es sich um den Zustand handelt, der dem Vertex-Shader und dem Pixelshader zugeordnet ist. Dies wird durch die Funktionen Scheitelpunkt und PixelShader, alle benötigten globalen Variablen und Ihre Eingabe-und Ausgabedaten Strukturen definiert, die alle hier aufgelistet sind:

    ```
    struct VS_OUTPUT
    {  ...  };
    VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                             ...
    {  ...  }

    struct PS_OUTPUT
    {  ...  };
    PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                             uniform bool bTexture ) 
    {  ...  }
    ```

    

-   Textur-und samplerzustand, die die globalen Variablen für das Textur Objekt und das samplerobjekt sind:

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   Der andere Effekt Zustand. In diesem Beispiel wird kein anderer Wirkungs Zustand explizit verwendet. Wenn dies der Fall wäre, wäre es die Technik in der Übergabe, auf die es angewendet wurde:

    ```
    technique RenderSceneWithTexture1Light
    {
        pass P0
        {          
            // Any other effect state can be set here.

            VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
            PixelShader  = compile ps_1_1 RenderScenePS( true ); 
        }
    }
    
    ```

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a>Effekte enthalten mindestens eine Technik und einen Durchlauf

Effekt Rendering-Optionen werden durch das Hinzufügen von Techniken und Durchläufen gesteuert.

Effekte können mit zusätzlichen Durchläufen erstellt werden, um komplexere renderingeffekte zu vereinfachen. Eine Technik unterstützt eine beliebige Anzahl von Durchläufen:


```
technique T0
{
    pass P0
    { ... }

    pass P1
    { ... }

    ...

    pass Pn
    { ... }
}
```



Effekte können auch mit einer beliebigen Anzahl von Techniken erstellt werden.


```
technique T0
{
    pass P0
    { ... }
}

technique T1
{
    pass P0
    { ... }

    pass P1
    { ... }
}

...

technique Tn
{
    pass P0
    { ... }
}

technique TVertexShaderOnly
{
    pass P0
    {
        VertexShader =
        asm
        {
         // assembly-language shader code goes here
         ...
        };
    }
}
```



Den Techniken und Durchläufen können beliebige Namen zugewiesen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte](effects.md)
</dt> </dl>

 

 



