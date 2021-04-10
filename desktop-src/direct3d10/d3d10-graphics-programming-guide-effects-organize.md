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
# <a name="organizing-state-in-an-effect-direct3d-10"></a>Organisieren des Zustands in einem Effekt (Direct3D 10)

Mit Direct3D 10 wird der Effekt Zustand für bestimmte Pipeline Stufen nach den folgenden Strukturen organisiert:



| Pipeline Status  | Struktur                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| Eingabe-Assembler | [**D3d10 \_ Eingabe \_ Element-Element \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| Rasterung   | [**D3d10 \_ Rasterizer- \_ Abteilung**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| Ausgabezusammenführung   | [**D3d10 \_ Blend \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) -Debug-und [ **d3d10- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

In den Shader-Phasen, in denen die Anzahl der Zustandsänderungen von einer Anwendung stärker gesteuert werden muss, wurde der Zustand in den konstanten Puffer Status, den samplerstatus und den Shader-Ressourcen Zustand aufgeteilt. Dadurch wird eine Anwendung ermöglicht, die sorgfältig entworfen wurde, um nur den geänderten Zustand zu aktualisieren. Dadurch wird die Leistung verbessert, da die Datenmenge reduziert wird, die an die GPU übermittelt werden muss.

Wie organisieren Sie also den Pipeline Status in einem Effekt?

Die Antwort ist, dass die Reihenfolge keine Rolle spielt. Globale Variablen müssen sich nicht im oberen Bereich befinden. Allerdings wird für alle Beispiele im SDK dieselbe Reihenfolge befolgt, da es eine bewährte Methode ist, die Daten auf die gleiche Weise zu organisieren. Dies ist eine kurze Beschreibung der Datenreihen Folge in den DirectX SDK-Beispielen.

-   [Globale Variablen](#global-variables)
-   [Shader](#shaders)
-   [Techniken und Durchgänge](#techniques-and-passes)

## <a name="global-variables"></a>Globale Variablen

Ebenso wie die Standard-C-Übung werden globale Variablen zuerst am Anfang der Datei deklariert. In den meisten Fällen handelt es sich hierbei um Variablen, die von einer Anwendung initialisiert und dann in einem Effekt verwendet werden. Manchmal werden Sie initialisiert und nie geändert, in anderen Fällen, in denen Sie jedes Frame aktualisiert werden. Ebenso wie Regeln des C-Funktions Bereichs sind Effekte, die außerhalb des Gültigkeits Bereichs von Effekten deklariert wurden, während des Effekts sichtbar. jede Variable, die innerhalb einer Effekt Funktion deklariert wird, ist nur innerhalb dieser Funktion sichtbar.

Im folgenden finden Sie ein Beispiel für die Variablen, die in BasicHLSL10. FX deklariert werden.


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



Die Syntax für Effekt Variablen wird in der [Variablen Syntax von Effect (Direct3D 10)](d3d10-effect-variable-syntax.md)ausführlicher beschrieben. Die Syntax für Effekt Textur-Samplern ist ausführlicher im [Samplingtyp (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md)ausführlich beschrieben.

## <a name="shaders"></a>Shader

Shader sind kleine ausführbare Programme. Sie können sich Shader als kapselnde shaderzustand vorstellen, da der HLSL-Code die shaderfunktionalität implementiert. Die Pipeline verwendet drei verschiedene Arten von Shadern.

-   Vertex-Shader: Arbeiten mit Vertex-Daten. Ein Scheitelpunkt in ergibt einen Scheitelpunkt aus.
-   Geometry-Shader: Arbeiten mit primitiven Daten. Ein primitiver in kann 0, 1 oder viele primitive ergeben.
-   Pixel-Shader: Arbeiten mit Pixeldaten. Ein Pixel in ergibt 1 Pixel, es sei denn, das Pixel ist aus einem Rendering herausgefiltert.

Shader sind lokale Funktionen und folgen Regeln für C-Stil Funktionen. Wenn ein Effekt kompiliert wird, wird jeder Shader kompiliert, und ein Zeiger auf jede Shader-Funktion wird intern gespeichert. Bei erfolgreicher Kompilierung wird eine ID3D10Effect-Schnittstelle zurückgegeben. An diesem Punkt liegt der kompilierte Effekt in einem zwischen Format vor.

Um weitere Informationen zu den kompilierten Shadern zu erhalten, müssen Sie die Shader-Reflektion verwenden. Dies entspricht im Wesentlichen dem Anfordern der Laufzeit, die Shader zu dekompilieren, und gibt Informationen über den Shader-Code zurück.


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



Die Syntax für Effekte-Shader ist in der [Funktions Syntax von "Effect" (Direct3D 10)](d3d10-effect-function-syntax.md)ausführlicher beschrieben.

## <a name="techniques-and-passes"></a>Techniken und Durchgänge

Eine Technik ist eine Sammlung von Renderingdurchläufen (es muss mindestens ein Durchlauf vorhanden sein). Jeder Effekt Durchlauf (ähnlich dem Bereich zu einem einzelnen Durchlauf in einer Renderschleife) definiert den Shader-Zustand und alle anderen Pipeline Zustände, die zum Rendern von Geometrie erforderlich sind.

Im folgenden finden Sie ein Beispiel für eine Technik (die einen Durchlauf umfasst) aus BasicHLSL10. fx.


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



Die Syntax für Effekte-Shader ist ausführlicher in der [Effekt Techniken-Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
