---
title: Syntax der Effekt Variablen (Direct3D 11)
description: Eine Effekt Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473181"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Syntax der Effekt Variablen (Direct3D 11)

Eine Effekt Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.

## <a name="syntax"></a>Syntax

Grundlegende Syntax:

*DataType* *VariableName* \[ *: semanticname* \]  <  *Annotations*  >  \[ = InitialValue \] ;

Vollständige Syntax finden Sie unter [Variablen Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) .



| Name         | BESCHREIBUNG                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Alle [grundlegenden](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [Textur](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)-, ungeordneten Zugriffs Sichten, Shader-oder Zustands Blocktypen.                            |
| VariableName | Eine ASCII-Zeichenfolge, die den Namen der Effekt Variablen eindeutig identifiziert.                                                                                                                   |
| Semanticname | Eine ASCII-Zeichenfolge, die zusätzliche Informationen zur Verwendung einer Variablen angibt. Eine Semantik ist eine ASCII-Zeichenfolge, bei der es sich entweder um eine vordefinierte System-oder benutzerdefinierte Zeichenfolge handeln kann. |
| Anmerkungen  | Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter [Annotation-Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).     |
| InitialValue | Der Standardwert der Variablen.                                                                                                                                                          |



 

Eine Effekt Variable, die außerhalb aller Funktionen deklariert ist, wird im Gültigkeitsbereich als Global betrachtet. innerhalb einer Funktion deklarierte Variablen sind für diese Funktion lokal.

## <a name="example"></a>Beispiel

In diesem Beispiel werden numerische Variablen des globalen Effekts veranschaulicht.


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



In diesem Beispiel wird das Deklarieren einer globalen Textur Variablen veranschaulicht.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Die Stichprobenentnahme einer Textur erfolgt mit einem Textur Sampler. Informationen zum Einrichten eines Samplers in einem Effekt finden Sie unter dem [samplertyp](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

In diesem Beispiel wird das Deklarieren von Variablen der globalen ungeordneten Zugriffs Sicht veranschaulicht


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

[Effekt Format](d3d11-effect-format.md)
</dt> </dl>

 

 