---
description: 'Mit Direct3D 10 wird der Effektzustand für bestimmte Pipelinephasen nach den folgenden Strukturen organisiert:'
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organisieren des Zustands in einem Effekt (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0fdd4389ce4db34a64e4bc5e39f21998c90481d4a43a06244be2b231cca999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753750"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a>Organisieren des Zustands in einem Effekt (Direct3D 10)

Mit Direct3D 10 wird der Effektzustand für bestimmte Pipelinephasen nach den folgenden Strukturen organisiert:



| Pipelinestatus  | Struktur                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| Eingabe-Assembler | [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| Rasterung   | [**D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| Ausgabezusammenführung   | [**D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) und [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

Für die Shaderstufen, in denen die Anzahl der Zustandsänderungen von einer Anwendung gesteuert werden muss, wurde der Zustand in einen konstanten Pufferzustand, einen sampler-Zustand und einen Shaderressourcenzustand unterteilt. Dadurch kann eine Anwendung, die sorgfältig darauf ausgelegt ist, nur den zustandsverändernden Zustand zu aktualisieren, wodurch die Leistung verbessert wird, indem die Datenmenge reduziert wird, die an die GPU übergeben werden muss.

Wie organisieren Sie den Pipelinezustand also in einem Effekt?

Die Antwort ist, dass die Reihenfolge keine Rolle spielt. Globale Variablen müssen sich nicht oben befinden. Alle Beispiele im SDK folgen jedoch derselben Reihenfolge, da es eine bewährte Methode ist, die Daten auf die gleiche Weise zu organisieren. Dies ist also eine kurze Beschreibung der Datenreihenfolge in den DirectX SDK-Beispielen.

-   [Globale Variablen](#global-variables)
-   [Shader](#shaders)
-   [Techniken und Durchläufe](#techniques-and-passes)

## <a name="global-variables"></a>Globale Variablen

Wie bei C standard werden globale Variablen zuerst am Anfang der Datei deklariert. In den meisten Fällen handelt es sich hierbei um Variablen, die von einer Anwendung initialisiert und dann in einem Effekt verwendet werden. Manchmal werden sie initialisiert und nie geändert, andernfalls werden sie bei jedem Frame aktualisiert. Genau wie C-Funktionsbereichsregeln sind Effektvariablen, die außerhalb des Gültigkeitsbereichs von Effektfunktionen deklariert sind, während des gesamten Effekts sichtbar. Jede Variable, die innerhalb einer Effect-Funktion deklariert ist, ist nur innerhalb dieser Funktion sichtbar.

Hier sehen Sie ein Beispiel für die In BasicHLSL10.fx deklarierten Variablen.


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



Die Syntax für Effektvariablen wird unter [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md)ausführlicher beschrieben. Die Syntax für Effekttextur-Sampler wird unter [Samplertyp (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md)ausführlicher beschrieben.

## <a name="shaders"></a>Shader

Shader sind kleine ausführbare Programme. Sie können sich Shader als das Kapseln des Shaderzustands vorstellen, da der HLSL-Code die Shaderfunktionalität implementiert. Die Pipeline verwendet drei verschiedene Arten von Shadern.

-   Vertex-Shader: Arbeiten mit Scheitelpunktdaten. Ein Scheitelpunkt in ergibt einen Scheitelpunkt.
-   Geometrie-Shader: Arbeiten mit primitiven Daten. Ein Primitiver in kann 0, 1 oder viele Primitive ergeben.
-   Pixel-Shader: Arbeiten mit Pixeldaten. Ein Pixel in ergibt 1 Pixel (es sei denn, das Pixel wird aus einem Renderr herausgekäuelt).

Shader sind lokale Funktionen und folgen den Funktionsregeln im C-Stil. Wenn ein Effekt kompiliert wird, wird jeder Shader kompiliert, und ein Zeiger auf jede Shaderfunktion wird intern gespeichert. Eine ID3D10Effect-Schnittstelle wird zurückgegeben, wenn die Kompilierung erfolgreich ist. An diesem Punkt befindet sich der kompilierte Effekt in einem Zwischenformat.

Um weitere Informationen zu den kompilierten Shadern zu erhalten, müssen Sie Shaderreflektion verwenden. Dies ist im Wesentlichen so, als ob die Runtime aufgefordert wird, die Shader zu dekompilieren und Informationen zum Shadercode an Sie zurückzugeben.


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



Die Syntax für Effekt-Shader wird unter [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md)ausführlicher beschrieben.

## <a name="techniques-and-passes"></a>Techniken und Durchläufe

Eine Technik ist eine Auflistung von Renderingdurchläufen (es muss mindestens ein Durchlauf vorhanden sein). Jeder Effektdurchlauf (der im Gültigkeitsbereich einem einzelnen Durchlauf in einer Renderschleife ähnelt) definiert den Shaderzustand und jeden anderen Pipelinezustand, der zum Rendern der Geometrie erforderlich ist.

Hier sehen Sie ein Beispiel für eine Technik (die einen Durchlauf enthält) von BasicHLSL10.fx.


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



Die Syntax für Effekt-Shader wird ausführlicher unter [Effect Technique Syntax (Direct3D 10) (Effekttechniksyntax (Direct3D 10))](d3d10-effect-technique-syntax.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
