---
title: ID3DX12PipelineParserCallbacks primitivetopologytypecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Topologietyp-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Primitivetopologytypecb-Methode
- Primitivetopologytypecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, primitivetopologytypecb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357253"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a><span data-ttu-id="2e57c-106">ID3DX12PipelineParserCallbacks::P rimitivetopologytypecb-Methode</span><span class="sxs-lookup"><span data-stu-id="2e57c-106">ID3DX12PipelineParserCallbacks::PrimitiveTopologyTypeCb method</span></span>

<span data-ttu-id="2e57c-107">Ruft den untergeordneten Topologietyp-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="2e57c-107">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e57c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e57c-108">Syntax</span></span>


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a><span data-ttu-id="2e57c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e57c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e57c-110">*Primitivetopologytype*</span><span class="sxs-lookup"><span data-stu-id="2e57c-110">*PrimitiveTopologyType*</span></span> 
</dt> <dd>

<span data-ttu-id="2e57c-111">Type: **[ **D3D12 \_ primitiver \_ \_ Topologietyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span><span class="sxs-lookup"><span data-stu-id="2e57c-111">Type: **[**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span></span>

<span data-ttu-id="2e57c-112">Details des primitiven topologietyps, der aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2e57c-112">Details of the primitive topology type subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e57c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e57c-113">Return value</span></span>

<span data-ttu-id="2e57c-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="2e57c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e57c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e57c-115">Requirements</span></span>



| <span data-ttu-id="2e57c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e57c-116">Requirement</span></span> | <span data-ttu-id="2e57c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2e57c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2e57c-118">Header</span><span class="sxs-lookup"><span data-stu-id="2e57c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2e57c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e57c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2e57c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e57c-120">Library</span></span><br/> | <dl> <span data-ttu-id="2e57c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e57c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2e57c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2e57c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e57c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e57c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e57c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e57c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e57c-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2e57c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2e57c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="2e57c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="2e57c-127">**D3D12 \_ primitiver \_ \_ Topologietyp**</span><span class="sxs-lookup"><span data-stu-id="2e57c-127">**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





