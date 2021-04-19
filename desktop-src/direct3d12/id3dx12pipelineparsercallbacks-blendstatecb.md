---
title: ID3DX12PipelineParserCallbacks blendstatuecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Blend-Zustands Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Blendstatuecb-Methode
- Blendstatuecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, blendstatus ECB-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353382"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a><span data-ttu-id="17e0d-106">ID3DX12PipelineParserCallbacks:: blendstatuecb-Methode</span><span class="sxs-lookup"><span data-stu-id="17e0d-106">ID3DX12PipelineParserCallbacks::BlendStateCb method</span></span>

<span data-ttu-id="17e0d-107">Ruft den untergeordneten Blend-Zustands Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="17e0d-107">Calls the blend state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e0d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e0d-108">Syntax</span></span>


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a><span data-ttu-id="17e0d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="17e0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e0d-110">*Blendstate* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="17e0d-110">*BlendState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="17e0d-111">Typ: **Konstanten [**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span><span class="sxs-lookup"><span data-stu-id="17e0d-111">Type: **const [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span></span>

<span data-ttu-id="17e0d-112">Details der Blend-Statusbeschreibung, die aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="17e0d-112">Details of the blend state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e0d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17e0d-113">Return value</span></span>

<span data-ttu-id="17e0d-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="17e0d-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e0d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17e0d-115">Requirements</span></span>



| <span data-ttu-id="17e0d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17e0d-116">Requirement</span></span> | <span data-ttu-id="17e0d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="17e0d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17e0d-118">Header</span><span class="sxs-lookup"><span data-stu-id="17e0d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="17e0d-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e0d-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="17e0d-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17e0d-120">Library</span></span><br/> | <dl> <span data-ttu-id="17e0d-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17e0d-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="17e0d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="17e0d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="17e0d-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17e0d-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e0d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17e0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e0d-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="17e0d-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="17e0d-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="17e0d-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="17e0d-127">**D3D12 \_ Blend- \_ Entsc**</span><span class="sxs-lookup"><span data-stu-id="17e0d-127">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





