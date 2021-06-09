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
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="1acf2-103">Syntax der Fragmentdeklaration (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="1acf2-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="1acf2-104">Jede HLSL-Funktion (High Level Shader Language) von Microsoft kann mit einer Fragmentdeklaration in ein Shaderfragment konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="1acf2-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="1acf2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1acf2-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="1acf2-106">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="1acf2-106">where:</span></span>



| <span data-ttu-id="1acf2-107">Wert</span><span class="sxs-lookup"><span data-stu-id="1acf2-107">Value</span></span>                  | <span data-ttu-id="1acf2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1acf2-108">Description</span></span>                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acf2-109">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="1acf2-109">fragmentKeyword</span></span>   | <span data-ttu-id="1acf2-110">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="1acf2-110">Required keyword.</span></span> <span data-ttu-id="1acf2-111">Entweder pixelfragment oder vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="1acf2-111">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="1acf2-112">FragmentName</span><span class="sxs-lookup"><span data-stu-id="1acf2-112">FragmentName</span></span>      | <span data-ttu-id="1acf2-113">Eine ASCII-Textzeichenfolge, die den Kompilierten Fragmentnamen angibt.</span><span class="sxs-lookup"><span data-stu-id="1acf2-113">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="1acf2-114">Kompilieren des \_ Fragments</span><span class="sxs-lookup"><span data-stu-id="1acf2-114">compile\_fragment</span></span> | <span data-ttu-id="1acf2-115">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="1acf2-115">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="1acf2-116">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="1acf2-116">shaderProfile</span></span>     | <span data-ttu-id="1acf2-117">Das Shadermodell, mit dem kompiliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1acf2-117">The shader model to compile against.</span></span> <span data-ttu-id="1acf2-118">Ein beliebiges gültiges Vertexshaderprofil (siehe [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) oder ein Pixelshaderprofil (siehe [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="1acf2-118">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="1acf2-119">FunctionName()</span><span class="sxs-lookup"><span data-stu-id="1acf2-119">FunctionName()</span></span>    | <span data-ttu-id="1acf2-120">Der Name der Shaderfunktion, gefolgt von Klammern.</span><span class="sxs-lookup"><span data-stu-id="1acf2-120">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="1acf2-121">Freigegebene Fragmentparameter werden durch Hinzufügen eines Präfixes \_ "r" zu ihrer Semantik markiert.</span><span class="sxs-lookup"><span data-stu-id="1acf2-121">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="1acf2-122">In diesem Beispiel identifizieren die Semantik von r PosWorld und r NormalWorld, dass diese beiden Parameter gemeinsame Parameter \_ \_ für andere Fragmente sind.</span><span class="sxs-lookup"><span data-stu-id="1acf2-122">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="1acf2-123">Fragmentlinker war eine Microsoft Direct3D 9-Technologie in D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="1acf2-123">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="1acf2-124">Der Fragmentlinker war ein Tool (Flink.exe), eine D3DX 9-API und eine HLSL-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="1acf2-124">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="1acf2-125">Der Fragmentlinker wurde ab dem DirectX SDK-Release vom August 2009 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1acf2-125">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="1acf2-126">Der Fragmentlinker wurde nie auf Microsoft Direct3D 10, Microsoft Direct3D 10.1 oder Microsoft Direct3D 11 angewendet.</span><span class="sxs-lookup"><span data-stu-id="1acf2-126">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1acf2-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1acf2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1acf2-128">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1acf2-128">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
