---
title: ID3DX12PipelineParserCallbacks ibstripcutvaluecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Rückruf Wert des Index Puffers eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Ibstripcutvaluecb-Methode
- Ibstripcutvaluecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, ibstripcutvaluecb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350704"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a><span data-ttu-id="fd7db-106">ID3DX12PipelineParserCallbacks:: ibstripcutvaluecb-Methode</span><span class="sxs-lookup"><span data-stu-id="fd7db-106">ID3DX12PipelineParserCallbacks::IBStripCutValueCb method</span></span>

<span data-ttu-id="fd7db-107">Ruft den untergeordneten Rückruf Wert des Index Puffers eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="fd7db-107">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7db-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd7db-108">Syntax</span></span>


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a><span data-ttu-id="fd7db-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd7db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd7db-110">*Ibstripcutvalue*</span><span class="sxs-lookup"><span data-stu-id="fd7db-110">*IBStripCutValue*</span></span> 
</dt> <dd>

<span data-ttu-id="fd7db-111">Type: **[ **D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span><span class="sxs-lookup"><span data-stu-id="fd7db-111">Type: **[**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span></span>

<span data-ttu-id="fd7db-112">Details des von einem Pipeline Status-Stream analysierten Bereichs Ausschneide Werts für den Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fd7db-112">Details of the index buffer strip-cut value subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd7db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd7db-113">Return value</span></span>

<span data-ttu-id="fd7db-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="fd7db-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7db-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd7db-115">Requirements</span></span>



| <span data-ttu-id="fd7db-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd7db-116">Requirement</span></span> | <span data-ttu-id="fd7db-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fd7db-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7db-118">Header</span><span class="sxs-lookup"><span data-stu-id="fd7db-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fd7db-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd7db-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fd7db-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd7db-120">Library</span></span><br/> | <dl> <span data-ttu-id="fd7db-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd7db-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd7db-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7db-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd7db-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd7db-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd7db-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd7db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7db-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fd7db-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="fd7db-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="fd7db-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="fd7db-127">**D3D12 \_ Index-Puffer leisten- \_ \_ \_ Ausschneide \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="fd7db-127">**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





