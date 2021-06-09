---
title: SV_InnerCoverage
description: SV InputCoverage stellt verdeckte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig \_ abgedeckt ist).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 168f90c17c9e6837d696ebb6dac8f39dc6dfb366
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826624"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="ace52-104">SV \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="ace52-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="ace52-105">SV InputCoverage stellt verdeckte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig \_ abgedeckt ist).</span><span class="sxs-lookup"><span data-stu-id="ace52-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="ace52-106">Typ</span><span class="sxs-lookup"><span data-stu-id="ace52-106">Type</span></span>



| <span data-ttu-id="ace52-107">Typ</span><span class="sxs-lookup"><span data-stu-id="ace52-107">Type</span></span>     |
|------|
| <span data-ttu-id="ace52-108">uint</span><span class="sxs-lookup"><span data-stu-id="ace52-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ace52-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ace52-109">Remarks</span></span>

<span data-ttu-id="ace52-110">Dieser vom System generierte Wert ist für die Unterstützung der Ebene 3 erforderlich und nur in dieser Ebene verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ace52-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="ace52-111">Diese Eingabe schließen sich mit SV \_ Coverage gegenseitig aus. Beides kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ace52-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="ace52-112">Für den Zugriff auf SV InnerCoverage muss es als einzelne Komponente aus einem der \_ Pixel-Shader-Eingaberegister deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="ace52-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="ace52-113">Der Interpolationsmodus für die Deklaration muss konstant sein (interpolation does not apply).</span><span class="sxs-lookup"><span data-stu-id="ace52-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="ace52-114">Die konservative Rasterung ist sowohl in D3D11.3 als auch in D3D12 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ace52-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="ace52-115">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ace52-115">Refer to:</span></span>

-   [<span data-ttu-id="ace52-116">D3D11.3 Konservative Rasterung</span><span class="sxs-lookup"><span data-stu-id="ace52-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="ace52-117">D3D12 Konservative Rasterung</span><span class="sxs-lookup"><span data-stu-id="ace52-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="ace52-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ace52-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace52-119">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="ace52-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="ace52-120">Shadermodell 5.1 Systemwerte</span><span class="sxs-lookup"><span data-stu-id="ace52-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
