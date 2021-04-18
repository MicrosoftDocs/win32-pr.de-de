---
title: ID3DX12PipelineParserCallbacks errorduplitoresubobject-Methode (D3DX12. h)
description: Ruft den doppelten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Errorduplitoresubobject-Methode
- Errorduplitoresubobject-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, errorduplitoresubobject-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361226"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a><span data-ttu-id="d8f91-106">ID3DX12PipelineParserCallbacks:: errorduplitoresubobject-Methode</span><span class="sxs-lookup"><span data-stu-id="d8f91-106">ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject method</span></span>

<span data-ttu-id="d8f91-107">Ruft den doppelten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8f91-107">Calls the duplicate subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f91-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8f91-108">Syntax</span></span>


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a><span data-ttu-id="d8f91-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8f91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f91-110">*Duplialisietype*</span><span class="sxs-lookup"><span data-stu-id="d8f91-110">*DuplicateType*</span></span> 
</dt> <dd>

<span data-ttu-id="d8f91-111">Type: **[ **D3D12 \_ Pipeline \_ State \_ SubObject \_ Type**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span><span class="sxs-lookup"><span data-stu-id="d8f91-111">Type: **[**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span></span>

<span data-ttu-id="d8f91-112">Der Typ des untergeordneten Objekts, das dupliziert wurde.</span><span class="sxs-lookup"><span data-stu-id="d8f91-112">The subobject type that was duplicated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8f91-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8f91-113">Return value</span></span>

<span data-ttu-id="d8f91-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="d8f91-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8f91-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8f91-115">Requirements</span></span>



| <span data-ttu-id="d8f91-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8f91-116">Requirement</span></span> | <span data-ttu-id="d8f91-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d8f91-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f91-118">Header</span><span class="sxs-lookup"><span data-stu-id="d8f91-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d8f91-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8f91-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d8f91-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8f91-120">Library</span></span><br/> | <dl> <span data-ttu-id="d8f91-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8f91-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8f91-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d8f91-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8f91-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8f91-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8f91-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8f91-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f91-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d8f91-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d8f91-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d8f91-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d8f91-127">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="d8f91-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

