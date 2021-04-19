---
title: ID3DX12PipelineParserCallbacks depthstencilstatuecb-Methode (D3DX12. h)
description: Ruft den Unterbrechungs Status der tiefen Schablone eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Depthstencilstatuecb-Methode
- Depthstencilstatus ECB-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, depthstencilstatuecb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355782"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="2b398-106">ID3DX12PipelineParserCallbacks depthstencilstatuecb-Methode (D3DX12. h)</span><span class="sxs-lookup"><span data-stu-id="2b398-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="2b398-107">Ruft den Unterbrechungs Status der tiefen Schablone eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="2b398-107">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b398-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b398-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="2b398-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b398-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b398-110">*Depthstencilstate* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="2b398-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2b398-111">Typ: **Konstanten [**D3D12 \_ Tiefe \_ Schablone \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span><span class="sxs-lookup"><span data-stu-id="2b398-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span></span>

<span data-ttu-id="2b398-112">Details des von einem Pipeline Status-Stream analysierten tiefen Schablone-Zustands untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="2b398-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b398-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b398-113">Return value</span></span>

<span data-ttu-id="2b398-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="2b398-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b398-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b398-115">Requirements</span></span>



| <span data-ttu-id="2b398-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b398-116">Requirement</span></span> | <span data-ttu-id="2b398-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2b398-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b398-118">Header</span><span class="sxs-lookup"><span data-stu-id="2b398-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2b398-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b398-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2b398-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b398-120">Library</span></span><br/> | <dl> <span data-ttu-id="2b398-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b398-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b398-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2b398-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b398-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b398-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b398-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b398-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b398-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2b398-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2b398-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="2b398-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="2b398-127">**D3D12 \_ tiefen \_ Schablone-Schablone \_**</span><span class="sxs-lookup"><span data-stu-id="2b398-127">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





