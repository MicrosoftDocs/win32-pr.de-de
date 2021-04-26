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
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996967"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="ec7e5-104">SV \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="ec7e5-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="ec7e5-105">SV InputCoverage stellt verdeckte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig \_ abgedeckt ist).</span><span class="sxs-lookup"><span data-stu-id="ec7e5-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="ec7e5-106">Typ</span><span class="sxs-lookup"><span data-stu-id="ec7e5-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="ec7e5-107">Typ</span><span class="sxs-lookup"><span data-stu-id="ec7e5-107">Type</span></span> |
| <span data-ttu-id="ec7e5-108">uint</span><span class="sxs-lookup"><span data-stu-id="ec7e5-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ec7e5-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec7e5-109">Remarks</span></span>

<span data-ttu-id="ec7e5-110">Dieser vom System generierte Wert ist für die Unterstützung der Ebene 3 erforderlich und nur in dieser Ebene verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec7e5-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="ec7e5-111">Diese Eingabe schließen sich mit SV \_ Coverage gegenseitig aus. Beides kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec7e5-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="ec7e5-112">Für den Zugriff auf SV InnerCoverage muss es als einzelne Komponente aus einem der \_ Pixel-Shader-Eingaberegister deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="ec7e5-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="ec7e5-113">Der Interpolationsmodus für die Deklaration muss konstant sein (interpolation does not apply).</span><span class="sxs-lookup"><span data-stu-id="ec7e5-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="ec7e5-114">Die konservative Rasterung ist sowohl in D3D11.3 als auch in D3D12 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec7e5-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="ec7e5-115">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ec7e5-115">Refer to:</span></span>

-   [<span data-ttu-id="ec7e5-116">D3D11.3 Konservative Rasterung</span><span class="sxs-lookup"><span data-stu-id="ec7e5-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="ec7e5-117">D3D12 Konservative Rasterung</span><span class="sxs-lookup"><span data-stu-id="ec7e5-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="ec7e5-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec7e5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7e5-119">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="ec7e5-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="ec7e5-120">Shadermodell 5.1 Systemwerte</span><span class="sxs-lookup"><span data-stu-id="ec7e5-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
