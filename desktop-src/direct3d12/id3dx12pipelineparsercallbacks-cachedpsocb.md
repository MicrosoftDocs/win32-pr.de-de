---
title: ID3DX12PipelineParserCallbacks cachedpsocb-Methode (D3DX12. h)
description: Ruft den zwischengespeicherten PSO (Pipeline State Object)-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Cachedpsocb-Methode
- Cachedpsocb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, cachedpsocb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367465"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a><span data-ttu-id="81189-106">ID3DX12PipelineParserCallbacks:: cachedpsocb-Methode</span><span class="sxs-lookup"><span data-stu-id="81189-106">ID3DX12PipelineParserCallbacks::CachedPSOCb method</span></span>

<span data-ttu-id="81189-107">Ruft den zwischengespeicherten PSO (Pipeline State Object)-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="81189-107">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="81189-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="81189-108">Syntax</span></span>


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a><span data-ttu-id="81189-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="81189-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81189-110">*Cachedpso* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="81189-110">*CachedPSO* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="81189-111">Typ: **Konstanten [**D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span><span class="sxs-lookup"><span data-stu-id="81189-111">Type: **const [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span></span>

<span data-ttu-id="81189-112">Details des zwischengespeicherten PSO-Objekts (Pipeline Zustands Objekt), das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="81189-112">Details of the cached PSO (Pipeline State Object) subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81189-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81189-113">Return value</span></span>

<span data-ttu-id="81189-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="81189-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="81189-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81189-115">Requirements</span></span>



| <span data-ttu-id="81189-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81189-116">Requirement</span></span> | <span data-ttu-id="81189-117">Wert</span><span class="sxs-lookup"><span data-stu-id="81189-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81189-118">Header</span><span class="sxs-lookup"><span data-stu-id="81189-118">Header</span></span><br/>  | <dl> <span data-ttu-id="81189-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="81189-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="81189-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81189-120">Library</span></span><br/> | <dl> <span data-ttu-id="81189-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81189-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="81189-122">DLL</span><span class="sxs-lookup"><span data-stu-id="81189-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="81189-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81189-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81189-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81189-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81189-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="81189-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="81189-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="81189-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="81189-127">**D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status**</span><span class="sxs-lookup"><span data-stu-id="81189-127">**D3D12\_CACHED\_PIPELINE\_STATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





