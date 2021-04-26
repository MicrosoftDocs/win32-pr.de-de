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
ms.openlocfilehash: 9c9090caec35bfc5e46d7024bf6de44d865d4ad6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998307"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="4da7c-103">Syntax der Fragmentdeklaration (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="4da7c-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="4da7c-104">Jede HLSL-Funktion (High Level Shader Language) von Microsoft kann mit einer Fragmentdeklaration in ein Shaderfragment konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="4da7c-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4da7c-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="4da7c-106">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="4da7c-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da7c-107">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="4da7c-107">fragmentKeyword</span></span>   | <span data-ttu-id="4da7c-108">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="4da7c-108">Required keyword.</span></span> <span data-ttu-id="4da7c-109">Entweder pixelfragment oder vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="4da7c-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="4da7c-110">FragmentName</span><span class="sxs-lookup"><span data-stu-id="4da7c-110">FragmentName</span></span>      | <span data-ttu-id="4da7c-111">Eine ASCII-Textzeichenfolge, die den Kompilierten Fragmentnamen angibt.</span><span class="sxs-lookup"><span data-stu-id="4da7c-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="4da7c-112">Kompilieren des \_ Fragments</span><span class="sxs-lookup"><span data-stu-id="4da7c-112">compile\_fragment</span></span> | <span data-ttu-id="4da7c-113">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="4da7c-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="4da7c-114">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="4da7c-114">shaderProfile</span></span>     | <span data-ttu-id="4da7c-115">Das Shadermodell, mit dem kompiliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4da7c-115">The shader model to compile against.</span></span> <span data-ttu-id="4da7c-116">Ein beliebiges gültiges Vertexshaderprofil (siehe [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) oder ein Pixelshaderprofil (siehe [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="4da7c-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="4da7c-117">FunctionName()</span><span class="sxs-lookup"><span data-stu-id="4da7c-117">FunctionName()</span></span>    | <span data-ttu-id="4da7c-118">Der Name der Shaderfunktion, gefolgt von Klammern.</span><span class="sxs-lookup"><span data-stu-id="4da7c-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="4da7c-119">Freigegebene Fragmentparameter werden durch Hinzufügen eines Präfixes \_ "r" zu ihrer Semantik markiert.</span><span class="sxs-lookup"><span data-stu-id="4da7c-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="4da7c-120">In diesem Beispiel identifizieren die Semantik von r PosWorld und r NormalWorld, dass diese beiden Parameter gemeinsame Parameter \_ \_ für andere Fragmente sind.</span><span class="sxs-lookup"><span data-stu-id="4da7c-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="4da7c-121">Fragmentlinker war eine Microsoft Direct3D 9-Technologie in D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="4da7c-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="4da7c-122">Der Fragmentlinker war ein Tool (Flink.exe), eine D3DX 9-API und eine HLSL-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4da7c-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="4da7c-123">Der Fragmentlinker wurde ab dem DirectX SDK-Release vom August 2009 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4da7c-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="4da7c-124">Fragmentlinker wird nie auf Microsoft Direct3D 10, Microsoft Direct3D 10.1 oder Microsoft Direct3D 11 angewendet.</span><span class="sxs-lookup"><span data-stu-id="4da7c-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4da7c-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4da7c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da7c-126">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4da7c-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
