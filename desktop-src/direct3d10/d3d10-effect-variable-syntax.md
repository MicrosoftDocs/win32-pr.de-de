---
description: Eine Effect-Variable wird mit der folgenden Syntax deklariert.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Effect-Variablensyntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2422ba2cebf18c72a14d621ef13a98700aefd2858169c6e96566b455ec21d2ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497710"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Effect-Variablensyntax (Direct3D 10)

Eine Effect-Variable wird mit der folgenden Syntax deklariert.

## <a name="syntax"></a>Syntax

*DataType* *VariableName* \[ : *SemanticName* \]  <  *Annotations* >;



| Name         | Beschreibung                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Ein [beliebiger Basis-](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) oder [Texturtyp.](../direct3dhlsl/dx-graphics-hlsl-to-type.md)                                                                        |
| VariableName | Eine ASCII-Zeichenfolge, die den Namen der Effektvariablen eindeutig identifiziert.                                                                                                                   |
| SemanticName | Eine ASCII-Zeichenfolge, die zusätzliche Informationen zur Verwendung einer Variablen andementiert. Eine Semantik ist eine ASCII-Zeichenfolge, die entweder ein vordefinierter Systemwert oder eine benutzerdefinierte Zeichenfolge sein kann. |
| Anmerkungen  | Eine oder mehrere vom Benutzer bereitgestellte Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter [Anmerkungssyntax (Direct3D 10).](d3d10-effect-annotation-syntax.md)     |



 

Eine Effektvariable, die außerhalb aller Funktionen deklariert wird, wird im Gültigkeitsbereich als global betrachtet. Variablen, die innerhalb einer Funktion deklariert werden, sind lokal für diese Funktion.

## <a name="example"></a>Beispiel

Im [BasicHLSL10-Beispiel](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) werden globale Variablen ohne Semantik für Materialfarben, helle Eigenschaften und Transformationsmatrizen verwendet.

In diesem Beispiel werden globale Effektvariablen veranschaulicht.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



In diesem Beispiel werden Effektvariablen veranschaulicht, die für eine Shaderfunktion lokal sind.


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



In diesem Beispiel wird das Deklarieren einer Texturvariablen veranschaulicht.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Das Sampling einer Textur erfolgt mit einem Textursampling. Informationen zum Einrichten eines Samplers in einem Effekt finden Sie im [Samplertyp](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektformat](d3d10-effect-format.md)
</dt> </dl>

 

 
