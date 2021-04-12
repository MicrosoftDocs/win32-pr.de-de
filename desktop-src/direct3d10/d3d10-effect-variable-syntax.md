---
description: Eine Effekt Variable wird mit der folgenden Syntax deklariert.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Syntax der Effekt Variablen (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393101"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Syntax der Effekt Variablen (Direct3D 10)

Eine Effekt Variable wird mit der folgenden Syntax deklariert.

## <a name="syntax"></a>Syntax

*DataType* *VariableName* \[ : *semanticname* -Anmerkungen \]  <   >;



| Name         | BESCHREIBUNG                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Ein beliebiger [Grund](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) -oder [Textur](../direct3dhlsl/dx-graphics-hlsl-to-type.md) Datentyp.                                                                        |
| VariableName | Eine ASCII-Zeichenfolge, die den Namen der Effekt Variablen eindeutig identifiziert.                                                                                                                   |
| Semanticname | Eine ASCII-Zeichenfolge, die zusätzliche Informationen zur Verwendung einer Variablen angibt. Eine Semantik ist eine ASCII-Zeichenfolge, bei der es sich entweder um eine vordefinierte System-oder benutzerdefinierte Zeichenfolge handeln kann. |
| Anmerkungen  | Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter [Annotation-Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).     |



 

Eine Effekt Variable, die außerhalb aller Funktionen deklariert ist, wird im Gültigkeitsbereich als Global betrachtet. innerhalb einer Funktion deklarierte Variablen sind für diese Funktion lokal.

## <a name="example"></a>Beispiel

Im [BasicHLSL10-Beispiel](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) werden globale Variablen ohne Semantik für Material Farben, helle Eigenschaften und Transformations Matrizen verwendet.

In diesem Beispiel werden globale Effekt Variablen veranschaulicht.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



Dieses Beispiel veranschaulicht die Auswirkung von Variablen, die für eine Shader-Funktion lokal sind.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



In diesem Beispiel werden Funktionsparameter mit Semantik veranschaulicht.


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



In diesem Beispiel wird das Deklarieren einer Textur Variablen veranschaulicht.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Die Stichprobenentnahme einer Textur erfolgt mit einem Textur Sampler. Informationen zum Einrichten eines Samplers in einem Effekt finden Sie unter dem [samplertyp](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](d3d10-effect-format.md)
</dt> </dl>

 

 
