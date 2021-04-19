---
title: ID3DX12PipelineParserCallbacks rtvformatscb-Methode (D3DX12. h)
description: Ruft den untergeordneten Rückruf des renderzielformatarrays eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Rtvformatscb-Methode
- Rtvformatscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, rtvformatscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353381"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a><span data-ttu-id="85ffc-106">ID3DX12PipelineParserCallbacks:: rtvformatscb-Methode</span><span class="sxs-lookup"><span data-stu-id="85ffc-106">ID3DX12PipelineParserCallbacks::RTVFormatsCb method</span></span>

<span data-ttu-id="85ffc-107">Ruft den untergeordneten Rückruf des renderzielformatarrays eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="85ffc-107">Calls the render target format array subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ffc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="85ffc-108">Syntax</span></span>


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a><span data-ttu-id="85ffc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="85ffc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ffc-110">*RTV-Formate* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="85ffc-110">*RTVFormats* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="85ffc-111">Type: **Konstanten [**D3D12 \_ RT- \_ Format \_ Array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span><span class="sxs-lookup"><span data-stu-id="85ffc-111">Type: **const [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span></span>

<span data-ttu-id="85ffc-112">Details zum Array des renderzielformatarrays, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="85ffc-112">Details of the render target format array subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ffc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85ffc-113">Return value</span></span>

<span data-ttu-id="85ffc-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="85ffc-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ffc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85ffc-115">Requirements</span></span>



| <span data-ttu-id="85ffc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85ffc-116">Requirement</span></span> | <span data-ttu-id="85ffc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="85ffc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="85ffc-118">Header</span><span class="sxs-lookup"><span data-stu-id="85ffc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="85ffc-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ffc-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="85ffc-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85ffc-120">Library</span></span><br/> | <dl> <span data-ttu-id="85ffc-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85ffc-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="85ffc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="85ffc-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="85ffc-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85ffc-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ffc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85ffc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ffc-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="85ffc-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="85ffc-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="85ffc-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="85ffc-127">**D3D12 \_ RT- \_ Format \_ Array**</span><span class="sxs-lookup"><span data-stu-id="85ffc-127">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





