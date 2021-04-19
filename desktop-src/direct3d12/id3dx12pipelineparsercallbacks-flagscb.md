---
title: ID3DX12PipelineParserCallbacks flagscb-Methode (D3DX12. h)
description: Ruft den untergeordneten Flags-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Flagscb-Methode
- Flagscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, flagscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363991"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a><span data-ttu-id="8a9f0-106">ID3DX12PipelineParserCallbacks:: flagscb-Methode</span><span class="sxs-lookup"><span data-stu-id="8a9f0-106">ID3DX12PipelineParserCallbacks::FlagsCb method</span></span>

<span data-ttu-id="8a9f0-107">Ruft den untergeordneten Flags-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="8a9f0-107">Calls the flags subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a9f0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a9f0-108">Syntax</span></span>


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="8a9f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a9f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a9f0-110">*Flags*</span><span class="sxs-lookup"><span data-stu-id="8a9f0-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="8a9f0-111">Type: **[ **D3D12 \_ Pipeline \_ State \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span><span class="sxs-lookup"><span data-stu-id="8a9f0-111">Type: **[**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span></span>

<span data-ttu-id="8a9f0-112">Details der Flags, die aus einem Pipeline Status-Stream analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8a9f0-112">Details of the flags subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a9f0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a9f0-113">Return value</span></span>

<span data-ttu-id="8a9f0-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="8a9f0-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a9f0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a9f0-115">Requirements</span></span>



| <span data-ttu-id="8a9f0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a9f0-116">Requirement</span></span> | <span data-ttu-id="8a9f0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8a9f0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a9f0-118">Header</span><span class="sxs-lookup"><span data-stu-id="8a9f0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8a9f0-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a9f0-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8a9f0-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a9f0-120">Library</span></span><br/> | <dl> <span data-ttu-id="8a9f0-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a9f0-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a9f0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8a9f0-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a9f0-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a9f0-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a9f0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a9f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a9f0-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8a9f0-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8a9f0-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8a9f0-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="8a9f0-127">**D3D12 \_ Pipeline \_ - \_ Statusflags**</span><span class="sxs-lookup"><span data-stu-id="8a9f0-127">**D3D12\_PIPELINE\_STATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





