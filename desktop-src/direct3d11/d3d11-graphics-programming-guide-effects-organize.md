---
title: Organisieren des Zustands in einem Effekt (Direct3D 11)
description: Bei Direct3D 11 ist der Effektzustand für bestimmte Pipelinestufen nach Strukturen organisiert.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d36bf99887e96dc5854778edb24f0ceacbc0cdf5a7994532bc2ebd94137fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126094"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a>Organisieren des Zustands in einem Effekt (Direct3D 11)

Bei Direct3D 11 ist der Effektzustand für bestimmte Pipelinestufen nach Strukturen organisiert. Dies sind die Strukturen:



| Pipelinezustand | Struktur                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| Rasterung  | [**D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| Ausgabezusammenführung  | [**D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) und [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) |
| Shader        | Siehe unten                                                                                                          |



 

Für die Shaderstufen, in denen die Anzahl der Zustandsänderungen von einer Anwendung stärker gesteuert werden muss, wurde der Zustand in konstanten Pufferzustand, Samplerzustand, Shaderressourcenstatus und ungeordneten Zugriffsansichtszustand (für Pixel- und Compute-Shader) unterteilt. Dies ermöglicht einer Anwendung, die sorgfältig darauf ausgelegt ist, nur den Zustand zu aktualisieren, der sich ändert. Dies verbessert die Leistung, indem die Menge der Daten reduziert wird, die an die GPU übergeben werden müssen.

Wie organisieren Sie also den Pipelinezustand in einem Effekt?

Die Antwort ist, dass die Reihenfolge keine Rolle spielt. Globale Variablen müssen sich nicht oben befinden. Alle Beispiele im SDK folgen jedoch der gleichen Reihenfolge, da es eine bewährte Methode ist, die Daten auf die gleiche Weise zu organisieren. Dies ist also eine kurze Beschreibung der Daten reihenfolge in den DirectX SDK-Beispielen.

-   [Globale Variablen](#global-variables)
-   [Shader](#shaders)
-   [Gruppen, Techniken und Durchläufe](#groups-techniques-and-passes)

## <a name="global-variables"></a>Globale Variablen

Wie bei der C-Standardübung werden globale Variablen zuerst am Anfang der Datei deklariert. Am häufigsten handelt es sich dabei um Variablen, die von einer Anwendung initialisiert und dann in einem Effekt verwendet werden. Manchmal werden sie initialisiert und nie geändert, mal werden sie für jeden Frame aktualisiert. Genau wie C-Funktionsbereichsregeln sind Effektvariablen, die außerhalb des Gültigkeitsbereichs von Effektfunktionen deklariert sind, während des gesamten Effekts sichtbar. Jede Variable, die innerhalb einer Effect-Funktion deklariert ist, ist nur innerhalb dieser Funktion sichtbar.

Im Folgenden finden Sie ein Beispiel für die Variablen, die in BasicHLSL10.fx deklariert sind.


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



Die Syntax für Effektvariablen ist unter [Effect Variable Syntax (Direct3D 11) ausführlicher.](d3d11-effect-variable-syntax.md) Die Syntax für Effekttextur-Sampler ist unter [Samplertyp (DirectX HLSL) ausführlicher.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler)

## <a name="shaders"></a>Shader

Shader sind kleine ausführbare Programme. Sie können sich Shader als Kapseln des Shaderzustands kapseln, da der HLSL-Code die Shaderfunktionalität implementiert. Die Grafikpipeline bis zu fünf verschiedene Arten von Shadern.

-   Vertex-Shader: Arbeiten Sie mit Scheitelpunktdaten. Ein Scheitelpunkt in ergibt einen Scheitelpunkt.
-   Hüllen-Shader: Arbeiten Sie mit Patchdaten. Kontrollpunktphase: Ein Aufruf ergibt einen Kontrollpunkt. Für jede Fork- und Join-Phase: Ein Patch ergibt eine gewisse Menge an konstanten Patchdaten.
-   Domänen-Shader: Arbeiten Sie mit primitiven Daten. Ein Primitiv kann 0, 1 oder viele Primitive ergeben.
-   Geometrie-Shader: Arbeiten Sie mit primitiven Daten. Ein Primitiv in kann 0, 1 oder viele Primitive ergeben.
-   Pixel-Shader: Arbeiten sie mit Pixeldaten. Ein Pixel in ergibt 1 Pixel aus (es sei denn, das Pixel wird aus einem Render heraus gecullt).

Die Compute-Shaderpipeline verwendet einen Shader:

-   Compute-Shader: Arbeiten Sie mit jeder Art von Daten. Die Ausgabe ist unabhängig von der Anzahl der Threads.

Shader sind lokale Funktionen und befolgen Funktionsregeln im C-Stil. Wenn ein Effekt kompiliert wird, wird jeder Shader kompiliert, und ein Zeiger auf jede Shaderfunktion wird intern gespeichert. Eine ID3D11Effect-Schnittstelle wird zurückgegeben, wenn die Kompilierung erfolgreich ist. An diesem Punkt liegt der kompilierte Effekt in einem Zwischenformat vor.

Um weitere Informationen zu den kompilierten Shadern zu erhalten, müssen Sie shader-Reflektion verwenden. Dies ist im Wesentlichen so, als ob die Runtime aufgefordert wird, die Shader zu dekompilieren und Informationen zum Shadercode an Sie zurücksenden.


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



Die Syntax für Effekt-Shader ist unter [Effect Function Syntax (Direct3D 11) ausführlicher.](d3d11-effect-function-syntax.md)

## <a name="groups-techniques-and-passes"></a>Gruppen, Techniken und Durchläufe

Eine Gruppe ist eine Sammlung von Techniken. Eine Technik ist eine Auflistung von Renderingüberläufen (es muss mindestens ein Durchgang sein). Jeder Effektüberlauf (der im Gültigkeitsbereich einem einzelnen Durchlauf in einer Renderschleife ähnelt) definiert den Shaderzustand und alle anderen Pipelinestatus, die zum Rendern der Geometrie erforderlich sind.

Gruppen sind optional. Es gibt eine einzelne unbenannte Gruppe, die alle globalen Techniken umfasst. Alle anderen Gruppen müssen benannt werden.

Hier ist ein Beispiel für eine Technik (die einen Durchgang enthält) aus BasicHLSL10.fx.


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



Die Syntax für Effekt-Shader ist unter [Effect Technique Syntax (Direct3D 11) ausführlicher.](d3d11-effect-technique-syntax.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 