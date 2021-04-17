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
# <a name="effect-variable-syntax-direct3d-11"></a><span data-ttu-id="6e163-103">Syntax der Effekt Variablen (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6e163-103">Effect Variable Syntax (Direct3D 11)</span></span>

<span data-ttu-id="6e163-104">Eine Effekt Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="6e163-104">An effect variable is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e163-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e163-105">Syntax</span></span>

<span data-ttu-id="6e163-106">Grundlegende Syntax:</span><span class="sxs-lookup"><span data-stu-id="6e163-106">Basic syntax:</span></span>

<span data-ttu-id="6e163-107">*DataType* *VariableName* \[ *: semanticname* \]  <  *Annotations*  >  \[ = InitialValue \] ;</span><span class="sxs-lookup"><span data-stu-id="6e163-107">*DataType* *VariableName* \[ *: SemanticName* \] < *Annotations* > \[ = InitialValue \];</span></span>

<span data-ttu-id="6e163-108">Vollständige Syntax finden Sie unter [Variablen Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) .</span><span class="sxs-lookup"><span data-stu-id="6e163-108">See [Variable Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) for full syntax.</span></span>



| <span data-ttu-id="6e163-109">Name</span><span class="sxs-lookup"><span data-stu-id="6e163-109">Name</span></span>         | <span data-ttu-id="6e163-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e163-110">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e163-111">DataType</span><span class="sxs-lookup"><span data-stu-id="6e163-111">DataType</span></span>     | <span data-ttu-id="6e163-112">Alle [grundlegenden](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [Textur](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)-, ungeordneten Zugriffs Sichten, Shader-oder Zustands Blocktypen.</span><span class="sxs-lookup"><span data-stu-id="6e163-112">Any [basic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), unordered access view, shader or state block type.</span></span>                            |
| <span data-ttu-id="6e163-113">VariableName</span><span class="sxs-lookup"><span data-stu-id="6e163-113">VariableName</span></span> | <span data-ttu-id="6e163-114">Eine ASCII-Zeichenfolge, die den Namen der Effekt Variablen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6e163-114">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="6e163-115">Semanticname</span><span class="sxs-lookup"><span data-stu-id="6e163-115">SemanticName</span></span> | <span data-ttu-id="6e163-116">Eine ASCII-Zeichenfolge, die zusätzliche Informationen zur Verwendung einer Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="6e163-116">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="6e163-117">Eine Semantik ist eine ASCII-Zeichenfolge, bei der es sich entweder um eine vordefinierte System-oder benutzerdefinierte Zeichenfolge handeln kann.</span><span class="sxs-lookup"><span data-stu-id="6e163-117">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="6e163-118">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="6e163-118">Annotations</span></span>  | <span data-ttu-id="6e163-119">Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="6e163-119">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="6e163-120">Informationen zur Syntax finden Sie unter [Annotation-Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="6e163-120">For syntax, see [Annotation Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span></span>     |
| <span data-ttu-id="6e163-121">InitialValue</span><span class="sxs-lookup"><span data-stu-id="6e163-121">InitialValue</span></span> | <span data-ttu-id="6e163-122">Der Standardwert der Variablen.</span><span class="sxs-lookup"><span data-stu-id="6e163-122">The default value of the variable.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="6e163-123">Eine Effekt Variable, die außerhalb aller Funktionen deklariert ist, wird im Gültigkeitsbereich als Global betrachtet. innerhalb einer Funktion deklarierte Variablen sind für diese Funktion lokal.</span><span class="sxs-lookup"><span data-stu-id="6e163-123">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="6e163-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e163-124">Example</span></span>

<span data-ttu-id="6e163-125">In diesem Beispiel werden numerische Variablen des globalen Effekts veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6e163-125">This example illustrates global effect numeric variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="6e163-126">Dieses Beispiel veranschaulicht die Auswirkung von Variablen, die für eine Shader-Funktion lokal sind.</span><span class="sxs-lookup"><span data-stu-id="6e163-126">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="6e163-127">In diesem Beispiel werden Funktionsparameter mit Semantik veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6e163-127">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="6e163-128">In diesem Beispiel wird das Deklarieren einer globalen Textur Variablen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6e163-128">This example illustrates declaring a global texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="6e163-129">Die Stichprobenentnahme einer Textur erfolgt mit einem Textur Sampler.</span><span class="sxs-lookup"><span data-stu-id="6e163-129">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="6e163-130">Informationen zum Einrichten eines Samplers in einem Effekt finden Sie unter dem [samplertyp](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="6e163-130">To set up a sampler in an effect, see the [sampler type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

<span data-ttu-id="6e163-131">In diesem Beispiel wird das Deklarieren von Variablen der globalen ungeordneten Zugriffs Sicht veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="6e163-131">This example illustrates declaring global unordered access view variables.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6e163-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e163-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e163-133">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="6e163-133">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 