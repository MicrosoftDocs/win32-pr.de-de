---
title: Von Shader angegebener Schablone-Verweis Wert (Direct3D 11 Grafiken)
description: Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a089ec8ab56a1cf00021f97bb40cf86fe42f04
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340007"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="7d4cf-103">Von Shader angegebener Schablone-Verweis Wert (Direct3D 11 Grafiken)</span><span class="sxs-lookup"><span data-stu-id="7d4cf-103">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="7d4cf-104">Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.</span><span class="sxs-lookup"><span data-stu-id="7d4cf-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="7d4cf-105">Der angegebene Shader-Wert ersetzt den von der API angegebenen *Schablone-Verweis Wert* für diesen Aufruf, d. h. die Änderung wirkt sich auf den Schablonen Test aus, und wenn der "Schablone op D3D11 \_ Schablone op \_ Replace" \_ (ein Member von [**D3D11 \_ Schablone \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) zum Schreiben des Verweis Werts in den Schablonen Puffer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d4cf-105">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="7d4cf-106">In früheren Versionen von D3D11 kann der Schablonen Verweis Wert nur von der [**Verknüpfung id3d11devicecontext aus:: omsetdepthstencilstate**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d4cf-106">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="7d4cf-107">Dies bedeutet, dass dieser Wert nur für die Granularität pro zeichnen definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7d4cf-107">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="7d4cf-108">Dieses D3D 11.3-Feature ermöglicht Entwicklern das Lesen und Verwenden des Schablonen Verweis Werts ( `SV_StencilRef` ), der von einem Pixelshader ausgegeben wird. Dies bedeutet, dass er in einer Granularität pro Pixel oder pro Stichprobe angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="7d4cf-108">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="7d4cf-109">Diese Funktion ist in D3D 11.3 optional.</span><span class="sxs-lookup"><span data-stu-id="7d4cf-109">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="7d4cf-110">Um die Unterstützung zu testen, überprüfen Sie das `PSSpecifiedStencilRefSupported` boolesche Feld [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="7d4cf-110">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="7d4cf-111">Im folgenden finden Sie ein Beispiel für die Verwendung von `SV_StencilRef` in einem Pixelshader:</span><span class="sxs-lookup"><span data-stu-id="7d4cf-111">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="7d4cf-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d4cf-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d4cf-113">Direct3D 11,3-Features</span><span class="sxs-lookup"><span data-stu-id="7d4cf-113">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="7d4cf-114">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="7d4cf-114">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
