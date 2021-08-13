---
title: Effect-Variablensyntax (Direct3D 11)
description: Eine Effect-Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25057f3cd2535a0b48072616c3dd59393f90a24fe044c1cdad8acea677a541ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538393"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Effect-Variablensyntax (Direct3D 11)

Eine Effect-Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.

## <a name="syntax"></a>Syntax

Grundlegende Syntax:

*DataType* *VariableName* \[ *: SemanticName* \]  <  *Annotations* =  >  \[ InitialValue \] ;

Die [vollständige Syntax finden Sie unter Variablensyntax (DirectX HLSL).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)



| Name         | Beschreibung                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Alle [grundlegenden](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)Typen, [Texturen,](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)ungeordnete Zugriffsansichten, Shader oder Zustandsblocktypen.                            |
| VariableName | Eine ASCII-Zeichenfolge, die den Namen der Effektvariablen eindeutig identifiziert.                                                                                                                   |
| SemanticName | Eine ASCII-Zeichenfolge, die zusätzliche Informationen darüber angibt, wie eine Variable verwendet werden soll. Eine Semantik ist eine ASCII-Zeichenfolge, die entweder ein vordefinierter Systemwert oder eine benutzerdefinierte Benutzerzeichenfolge sein kann. |
| Anmerkungen  | Mindestens ein Teil der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter [Anmerkungssyntax (Direct3D 11).](d3d11-effect-annotation-syntax.md)     |
| InitialValue | Der Standardwert der Variablen.                                                                                                                                                          |



 

Eine Effect-Variable, die außerhalb aller Funktionen deklariert wird, wird im Gültigkeitsbereich als global betrachtet. Variablen, die innerhalb einer Funktion deklariert werden, sind lokal für diese Funktion.

## <a name="example"></a>Beispiel

In diesem Beispiel werden numerische Variablen für globale Auswirkungen veranschaulicht.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



Dieses Beispiel veranschaulicht Effektvariablen, die lokal für eine Shaderfunktion sind.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



Dieses Beispiel veranschaulicht Funktionsparameter mit Semantik.


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



Dieses Beispiel veranschaulicht das Deklarieren einer globalen Texturvariablen.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Das Sampling einer Textur erfolgt mit einem Texturs sampler. Informationen zum Einrichten eines Samplers in einem Effekt finden Sie unter dem [Samplertyp](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

Dieses Beispiel veranschaulicht das Deklarieren von globalen variablen ungeordneten Zugriffsansichten.


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effect-Format](d3d11-effect-format.md)
</dt> </dl>

 

 