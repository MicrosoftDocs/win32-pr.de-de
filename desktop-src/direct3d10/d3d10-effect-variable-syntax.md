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
# <a name="effect-variable-syntax-direct3d-10"></a><span data-ttu-id="2852f-103">Syntax der Effekt Variablen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="2852f-103">Effect Variable Syntax (Direct3D 10)</span></span>

<span data-ttu-id="2852f-104">Eine Effekt Variable wird mit der folgenden Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="2852f-104">An effect variable is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="2852f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2852f-105">Syntax</span></span>

<span data-ttu-id="2852f-106">*DataType* *VariableName* \[ : *semanticname* -Anmerkungen \]  <   >;</span><span class="sxs-lookup"><span data-stu-id="2852f-106">*DataType* *VariableName* \[ : *SemanticName* \] < *Annotations* >;</span></span>



| <span data-ttu-id="2852f-107">Name</span><span class="sxs-lookup"><span data-stu-id="2852f-107">Name</span></span>         | <span data-ttu-id="2852f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2852f-108">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2852f-109">DataType</span><span class="sxs-lookup"><span data-stu-id="2852f-109">DataType</span></span>     | <span data-ttu-id="2852f-110">Ein beliebiger [Grund](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) -oder [Textur](../direct3dhlsl/dx-graphics-hlsl-to-type.md) Datentyp.</span><span class="sxs-lookup"><span data-stu-id="2852f-110">Any [basic](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) or [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) type.</span></span>                                                                        |
| <span data-ttu-id="2852f-111">VariableName</span><span class="sxs-lookup"><span data-stu-id="2852f-111">VariableName</span></span> | <span data-ttu-id="2852f-112">Eine ASCII-Zeichenfolge, die den Namen der Effekt Variablen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2852f-112">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="2852f-113">Semanticname</span><span class="sxs-lookup"><span data-stu-id="2852f-113">SemanticName</span></span> | <span data-ttu-id="2852f-114">Eine ASCII-Zeichenfolge, die zusätzliche Informationen zur Verwendung einer Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="2852f-114">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="2852f-115">Eine Semantik ist eine ASCII-Zeichenfolge, bei der es sich entweder um eine vordefinierte System-oder benutzerdefinierte Zeichenfolge handeln kann.</span><span class="sxs-lookup"><span data-stu-id="2852f-115">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="2852f-116">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="2852f-116">Annotations</span></span>  | <span data-ttu-id="2852f-117">Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="2852f-117">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="2852f-118">Informationen zur Syntax finden Sie unter [Annotation-Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="2852f-118">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>     |



 

<span data-ttu-id="2852f-119">Eine Effekt Variable, die außerhalb aller Funktionen deklariert ist, wird im Gültigkeitsbereich als Global betrachtet. innerhalb einer Funktion deklarierte Variablen sind für diese Funktion lokal.</span><span class="sxs-lookup"><span data-stu-id="2852f-119">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="2852f-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2852f-120">Example</span></span>

<span data-ttu-id="2852f-121">Im [BasicHLSL10-Beispiel](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) werden globale Variablen ohne Semantik für Material Farben, helle Eigenschaften und Transformations Matrizen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2852f-121">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses global variables without semantics for material colors, light properties and transformation matrices.</span></span>

<span data-ttu-id="2852f-122">In diesem Beispiel werden globale Effekt Variablen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2852f-122">This example illustrates global effect variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="2852f-123">Dieses Beispiel veranschaulicht die Auswirkung von Variablen, die für eine Shader-Funktion lokal sind.</span><span class="sxs-lookup"><span data-stu-id="2852f-123">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="2852f-124">In diesem Beispiel werden Funktionsparameter mit Semantik veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2852f-124">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="2852f-125">In diesem Beispiel wird das Deklarieren einer Textur Variablen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2852f-125">This example illustrates declaring a texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="2852f-126">Die Stichprobenentnahme einer Textur erfolgt mit einem Textur Sampler.</span><span class="sxs-lookup"><span data-stu-id="2852f-126">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="2852f-127">Informationen zum Einrichten eines Samplers in einem Effekt finden Sie unter dem [samplertyp](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2852f-127">To set up a sampler in an effect, see the [sampler type](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2852f-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2852f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2852f-129">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="2852f-129">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
