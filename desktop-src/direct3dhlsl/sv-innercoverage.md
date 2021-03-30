---
title: SV_InnerCoverage
description: SV \_ inputcoverage stellt unterschätzte konservative rasterisierungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist).
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
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993550"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="49198-104">SV \_ innercoverage</span><span class="sxs-lookup"><span data-stu-id="49198-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="49198-105">SV \_ inputcoverage stellt unterschätzte konservative rasterisierungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist).</span><span class="sxs-lookup"><span data-stu-id="49198-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="49198-106">Typ</span><span class="sxs-lookup"><span data-stu-id="49198-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="49198-107">Typ</span><span class="sxs-lookup"><span data-stu-id="49198-107">Type</span></span> |
| <span data-ttu-id="49198-108">uint</span><span class="sxs-lookup"><span data-stu-id="49198-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="49198-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49198-109">Remarks</span></span>

<span data-ttu-id="49198-110">Dieser vom systemgenerierte Wert ist für die Unterstützung der Ebene 3 erforderlich und nur in dieser Ebene verfügbar.</span><span class="sxs-lookup"><span data-stu-id="49198-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="49198-111">Diese Eingabe schließt sich mit der SV \_ -Abdeckung gegenseitig aus. beide können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49198-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="49198-112">Für den Zugriff auf die SV \_ innercoverage muss Sie als einzelne Komponente aus einem der Pixel-Shader-Eingabe Register deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="49198-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="49198-113">Der Interpolations Modus für die Deklaration muss konstant sein (Interpolation ist nicht anwendbar).</span><span class="sxs-lookup"><span data-stu-id="49198-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="49198-114">Die konservative rasterisierung ist in D3D 11.3 und D3D12 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="49198-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="49198-115">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="49198-115">Refer to:</span></span>

-   [<span data-ttu-id="49198-116">D3D 11.3 konservative rasterisierung</span><span class="sxs-lookup"><span data-stu-id="49198-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="49198-117">D3D12 konservative rasterisierung</span><span class="sxs-lookup"><span data-stu-id="49198-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="49198-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49198-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49198-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="49198-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="49198-120">Shader-Modell 5,1 System Werte</span><span class="sxs-lookup"><span data-stu-id="49198-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 