---
title: Shader-angegebener Schablone-Verweis Wert (Direct3D 12-Grafiken)
description: Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548699"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="38f3c-103">Shader-angegebener Schablone-Verweis Wert (Direct3D 12-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="38f3c-103">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="38f3c-104">Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.</span><span class="sxs-lookup"><span data-stu-id="38f3c-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="38f3c-105">Der Schablonen Verweis Wert wird normalerweise von der [**ID3D12GraphicsCommandList:: omsetstencilref**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) -Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="38f3c-105">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="38f3c-106">Diese Methode legt den Schablonen Verweis Wert auf eine Granularität pro zeichnen fest.</span><span class="sxs-lookup"><span data-stu-id="38f3c-106">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="38f3c-107">Dieser Wert kann jedoch durch den Pixelshader überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="38f3c-107">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="38f3c-108">Diese D3D12-Funktion (und D3D 11.3) ermöglicht Entwicklern das Lesen und Verwenden des Schablonen Verweis Werts (*SV \_ stencilref*), der von einem Pixelshader ausgegeben wird. Dadurch wird eine Granularität pro Pixel oder pro Stichprobe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="38f3c-108">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="38f3c-109">Der angegebene Shader-Wert ersetzt den von der API angegebenen Verweis Wert für diesen Aufruf, d. h. die Änderung wirkt sich auf den Schablonen Test aus, und wenn der Schablonen Vorgang D3D12 \_ Schablone \_ op \_ Replace (ein Member von [**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) zum Schreiben des Verweis Werts in den Schablonen Puffer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38f3c-109">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="38f3c-110">Diese Funktion ist sowohl in D3D12 als auch D3D 11.3 optional.</span><span class="sxs-lookup"><span data-stu-id="38f3c-110">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="38f3c-111">Um die Unterstützung zu testen, überprüfen Sie das boolesche Feld *psspecifiedstencilrefsupported* von [**D3D12 \_ Feature \_ Data \_ D3D12 \_ Optionen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) mithilfe von [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="38f3c-111">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="38f3c-112">Im folgenden finden Sie ein Beispiel für die Verwendung von *SV \_ stencilref* in einem Pixelshader:</span><span class="sxs-lookup"><span data-stu-id="38f3c-112">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="38f3c-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="38f3c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38f3c-114">Darstellung</span><span class="sxs-lookup"><span data-stu-id="38f3c-114">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="38f3c-115">Ressourcen Bindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="38f3c-115">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="38f3c-116">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="38f3c-116">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="38f3c-117">Angeben von Stamm Signaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="38f3c-117">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
