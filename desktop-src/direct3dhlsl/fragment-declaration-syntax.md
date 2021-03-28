---
title: Syntax der fragmentdeklaration (Direct3D 9 HLSL)
description: Jede Microsoft High Level Shader Language (HLSL)-Funktion kann mit dem Hinzufügen einer fragmentdeklaration in ein Shader-Fragment konvertiert werden.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98e609820e67cc3ede6c3e280f63513850fed364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039182"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Syntax der fragmentdeklaration (Direct3D 9 HLSL)

Jede Microsoft High Level Shader Language (HLSL)-Funktion kann mit dem Hinzufügen einer fragmentdeklaration in ein Shader-Fragment konvertiert werden.

## <a name="syntax"></a>Syntax


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



Dabei gilt:



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentschlüsselwort   | Erforderliches Schlüsselwort. Entweder Pixel Fragment oder vertexfragment.                                                                                                                                                                                             |
| Fragmentname      | Eine ASCII-Zeichenfolge, die den Namen des kompilierten Fragments angibt.                                                                                                                                                                                       |
| Kompilierungs \_ Fragment | Erforderliches Schlüsselwort.                                                                                                                                                                                                                                     |
| shaderprofile     | Das Shader-Modell, mit dem kompiliert werden soll. Ein beliebiges gültiges Vertex-Shader-Profil (siehe [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) oder Pixel-Shader-Profil (siehe [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)). |
| FunctionName ()    | Der Shader-Funktionsname, gefolgt von Klammern.                                                                                                                                                                                                    |



 

Parameter für freigegebene Fragmente werden durch Hinzufügen eines \_ Präfix "r" zu ihrer Semantik gekennzeichnet.


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



In diesem Beispiel \_ erkennen die Semantik von r posworld und r \_ normalworld, dass diese beiden Parameter in anderen Fragmenten freigegebene Parameter sind.

> [!Note]  
> Fragment Linker war eine Microsoft Direct3D 9-Technologie in D3DX 9. Der fragmentlinker war ein Tool (Flink.exe), eine D3DX 9-API und eine HLSL-Erweiterung. Der fragmentlinker wurde ab der DirectX SDK-Version vom August 2009 gelöscht. Der fragmentlinker wird nie auf Microsoft Direct3D 10, Microsoft Direct3D 10,1 oder Microsoft Direct3D 11 angewendet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 