---
title: Vom Shader angegebener Schablonenverweiswert (Direct3D 11-Grafiken)
description: Erfahren Sie mehr über den Schablonenverweiswert in Direct3D 11-Grafiken. Das Aktivieren von Pixel-Shadern für die Verwendung des Schablonenverweiswerts ermöglicht eine fein kontrollierte Steuerung von Schablonenvorgängen.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e8a34d53bc7f30dc2a91fafabb561dff7a1e96
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408103"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="1f9e8-104">Vom Shader angegebener Schablonenverweiswert (Direct3D 11-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="1f9e8-104">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="1f9e8-105">Die Aktivierung von Pixel-Shadern zum Ausgeben des Schablonenverweiswerts anstelle des von der API angegebenen Werts ermöglicht eine sehr präzise Steuerung von Schablonenvorgängen.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="1f9e8-106">Der angegebene Shaderwert ersetzt den von der API angegebenen *Schablonenverweiswert* für diesen Aufruf. Dies bedeutet, dass sich die Änderung sowohl auf den Schablonentest auswirkt als auch wenn stencil op D3D11 \_ STENCIL \_ OP REPLACE \_ (ein Member von [**D3D11 \_ STENCIL \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) verwendet wird, um den Verweiswert in den Schablonenpuffer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-106">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="1f9e8-107">In früheren Versionen von D3D11 kann der Schablonenverweiswert nur von der [**ID3D11DeviceContext::OMSetDepthStencilState-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-107">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="1f9e8-108">Dies bedeutet, dass dieser Wert nur mit einer Granularität pro Zeichnen definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-108">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="1f9e8-109">Dieses D3D11.3-Feature ermöglicht Entwicklern das Lesen und Verwenden des Schablonenverweiswerts (), der `SV_StencilRef` von einem Pixel-Shader ausgegeben wird. Dies bedeutet, dass er für eine Pixel- oder Stichprobengranularität angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-109">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="1f9e8-110">Dieses Feature ist in D3D11.3 optional.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-110">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="1f9e8-111">Überprüfen Sie zum Testen der Unterstützung das `PSSpecifiedStencilRefSupported` boolesche Feld [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) mit [**ID3D11Device::CheckFeatureSupport.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="1f9e8-111">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="1f9e8-112">Hier sehen Sie ein Beispiel für die Verwendung von `SV_StencilRef` in einem Pixel-Shader:</span><span class="sxs-lookup"><span data-stu-id="1f9e8-112">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="1f9e8-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f9e8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f9e8-114">Direct3D 11.3-Features</span><span class="sxs-lookup"><span data-stu-id="1f9e8-114">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="1f9e8-115">Shadermodell 5.1</span><span class="sxs-lookup"><span data-stu-id="1f9e8-115">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
