---
title: Syntax der Fragmentdeklaration (Direct3D 9 HLSL)
description: Jede HLSL-Funktion (High Level Shader Language) von Microsoft kann mit einer Fragmentdeklaration in ein Shaderfragment konvertiert werden.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825727"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Syntax der Fragmentdeklaration (Direct3D 9 HLSL)

Jede HLSL-Funktion (High Level Shader Language) von Microsoft kann mit einer Fragmentdeklaration in ein Shaderfragment konvertiert werden.

## <a name="syntax"></a>Syntax


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



Dabei gilt:



| Wert                  | Beschreibung                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | Erforderliches Schlüsselwort. Entweder pixelfragment oder vertexfragment.                                                                                                                                                                                             |
| FragmentName      | Eine ASCII-Textzeichenfolge, die den Kompilierten Fragmentnamen angibt.                                                                                                                                                                                       |
| Kompilieren des \_ Fragments | Erforderliches Schlüsselwort.                                                                                                                                                                                                                                     |
| shaderProfile     | Das Shadermodell, mit dem kompiliert werden soll. Ein beliebiges gültiges Vertexshaderprofil (siehe [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) oder ein Pixelshaderprofil (siehe [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)). |
| FunctionName()    | Der Name der Shaderfunktion, gefolgt von Klammern.                                                                                                                                                                                                    |



 

Freigegebene Fragmentparameter werden durch Hinzufügen eines Präfixes \_ "r" zu ihrer Semantik markiert.


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



In diesem Beispiel identifizieren die Semantik von r PosWorld und r NormalWorld, dass diese beiden Parameter gemeinsame Parameter \_ \_ für andere Fragmente sind.

> [!Note]  
> Fragmentlinker war eine Microsoft Direct3D 9-Technologie in D3DX 9. Der Fragmentlinker war ein Tool (Flink.exe), eine D3DX 9-API und eine HLSL-Erweiterung. Der Fragmentlinker wurde ab dem DirectX SDK-Release vom August 2009 gelöscht. Der Fragmentlinker wurde nie auf Microsoft Direct3D 10, Microsoft Direct3D 10.1 oder Microsoft Direct3D 11 angewendet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
