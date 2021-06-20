---
title: Vom Shader angegebener Schablonenverweiswert (Direct3D 12-Grafiken)
description: Erfahren Sie mehr über den Schablonenverweiswert in Direct3D 12-Grafiken. Das Aktivieren von Pixel-Shadern für die Verwendung von Schablonenverweiswerten ermöglicht eine fein kontrollierte Steuerung von Schablonenvorgängen.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408313"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="4b9f5-104">Vom Shader angegebener Schablonenverweiswert (Direct3D 12-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="4b9f5-104">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="4b9f5-105">Das Aktivieren von Pixel-Shadern zum Ausgeben des Schablonenverweiswerts anstelle des von der API angegebenen Werts ermöglicht eine sehr präzise Steuerung von Schablonenvorgängen.</span><span class="sxs-lookup"><span data-stu-id="4b9f5-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="4b9f5-106">Der Schablonenverweiswert wird normalerweise von der [**ID3D12GraphicsCommandList::OMSetStencilRef-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b9f5-106">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="4b9f5-107">Diese Methode legt den Schablonenverweiswert auf eine Granularität pro Zeichnen fest.</span><span class="sxs-lookup"><span data-stu-id="4b9f5-107">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="4b9f5-108">Dieser Wert kann jedoch vom Pixelshader überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4b9f5-108">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="4b9f5-109">Dieses D3D12-Feature (und D3D11.3) ermöglicht Entwicklern das Lesen und Verwenden des Schablonenverweiswerts *(SV \_ StencilRef),* der von einem Pixel-Shader ausgegeben wird, und ermöglicht eine Granularität pro Pixel oder pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="4b9f5-109">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="4b9f5-110">Der angegebene Shaderwert ersetzt den von der API angegebenen Verweiswert für diesen Aufruf. Dies bedeutet, dass sich die Änderung auf den Schablonentest auswirkt und wenn der Schablonenvorgang D3D12 \_ STENCIL \_ OP \_ REPLACE (ein Member von [**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) verwendet wird, um den Verweiswert in den Schablonenpuffer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="4b9f5-110">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="4b9f5-111">Dieses Feature ist sowohl in D3D12 als auch in D3D11.3 optional.</span><span class="sxs-lookup"><span data-stu-id="4b9f5-111">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="4b9f5-112">Um die Unterstützung zu testen, überprüfen Sie das boolesche Feld *PSSpecifiedStencilRefSupported* von [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) mit [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="4b9f5-112">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="4b9f5-113">Hier sehen Sie ein Beispiel für die Verwendung von *SV \_ StencilRef* in einem Pixel-Shader:</span><span class="sxs-lookup"><span data-stu-id="4b9f5-113">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="4b9f5-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b9f5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b9f5-115">Darstellung</span><span class="sxs-lookup"><span data-stu-id="4b9f5-115">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="4b9f5-116">Ressourcenbindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="4b9f5-116">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="4b9f5-117">Shadermodell 5.1</span><span class="sxs-lookup"><span data-stu-id="4b9f5-117">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="4b9f5-118">Festlegen von Stammsignaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="4b9f5-118">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
