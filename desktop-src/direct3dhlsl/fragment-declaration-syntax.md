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
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="4b539-103">Syntax der fragmentdeklaration (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="4b539-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="4b539-104">Jede Microsoft High Level Shader Language (HLSL)-Funktion kann mit dem Hinzufügen einer fragmentdeklaration in ein Shader-Fragment konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b539-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b539-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b539-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="4b539-106">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="4b539-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b539-107">fragmentschlüsselwort</span><span class="sxs-lookup"><span data-stu-id="4b539-107">fragmentKeyword</span></span>   | <span data-ttu-id="4b539-108">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="4b539-108">Required keyword.</span></span> <span data-ttu-id="4b539-109">Entweder Pixel Fragment oder vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="4b539-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="4b539-110">Fragmentname</span><span class="sxs-lookup"><span data-stu-id="4b539-110">FragmentName</span></span>      | <span data-ttu-id="4b539-111">Eine ASCII-Zeichenfolge, die den Namen des kompilierten Fragments angibt.</span><span class="sxs-lookup"><span data-stu-id="4b539-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="4b539-112">Kompilierungs \_ Fragment</span><span class="sxs-lookup"><span data-stu-id="4b539-112">compile\_fragment</span></span> | <span data-ttu-id="4b539-113">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="4b539-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="4b539-114">shaderprofile</span><span class="sxs-lookup"><span data-stu-id="4b539-114">shaderProfile</span></span>     | <span data-ttu-id="4b539-115">Das Shader-Modell, mit dem kompiliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b539-115">The shader model to compile against.</span></span> <span data-ttu-id="4b539-116">Ein beliebiges gültiges Vertex-Shader-Profil (siehe [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) oder Pixel-Shader-Profil (siehe [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="4b539-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="4b539-117">FunctionName ()</span><span class="sxs-lookup"><span data-stu-id="4b539-117">FunctionName()</span></span>    | <span data-ttu-id="4b539-118">Der Shader-Funktionsname, gefolgt von Klammern.</span><span class="sxs-lookup"><span data-stu-id="4b539-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="4b539-119">Parameter für freigegebene Fragmente werden durch Hinzufügen eines \_ Präfix "r" zu ihrer Semantik gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="4b539-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="4b539-120">In diesem Beispiel \_ erkennen die Semantik von r posworld und r \_ normalworld, dass diese beiden Parameter in anderen Fragmenten freigegebene Parameter sind.</span><span class="sxs-lookup"><span data-stu-id="4b539-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="4b539-121">Fragment Linker war eine Microsoft Direct3D 9-Technologie in D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="4b539-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="4b539-122">Der fragmentlinker war ein Tool (Flink.exe), eine D3DX 9-API und eine HLSL-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4b539-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="4b539-123">Der fragmentlinker wurde ab der DirectX SDK-Version vom August 2009 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4b539-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="4b539-124">Der fragmentlinker wird nie auf Microsoft Direct3D 10, Microsoft Direct3D 10,1 oder Microsoft Direct3D 11 angewendet.</span><span class="sxs-lookup"><span data-stu-id="4b539-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4b539-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b539-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b539-126">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4b539-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 