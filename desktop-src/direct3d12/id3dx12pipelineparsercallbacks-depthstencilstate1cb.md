---
title: ID3DX12PipelineParserCallbacks DepthStencilState1Cb-Methode (D3DX12. h)
description: Ruft den \_ unterbobject-Rückruf der tiefen Schablone (D3D12 tiefen \_ Schablone \_ DESC1) eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- DepthStencilState1Cb-Methode
- DepthStencilState1Cb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, DepthStencilState1Cb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365071"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a><span data-ttu-id="ff5d7-106">ID3DX12PipelineParserCallbacks::D epthstencilstate1cb-Methode</span><span class="sxs-lookup"><span data-stu-id="ff5d7-106">ID3DX12PipelineParserCallbacks::DepthStencilState1Cb method</span></span>

<span data-ttu-id="ff5d7-107">Ruft den unterbobject-Rückruf der tiefen Schablone ([**D3D12 \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff5d7-107">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5d7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff5d7-108">Syntax</span></span>


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="ff5d7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff5d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5d7-110">*Depthstencilstate* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="ff5d7-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5d7-111">Typ: **Konstanten [**D3D12 \_ Tiefe \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span><span class="sxs-lookup"><span data-stu-id="ff5d7-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span></span>

<span data-ttu-id="ff5d7-112">Details des von einem Pipeline Status-Stream analysierten tiefen Schablone-Zustands untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff5d7-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff5d7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff5d7-113">Return value</span></span>

<span data-ttu-id="ff5d7-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="ff5d7-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5d7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff5d7-115">Requirements</span></span>



| <span data-ttu-id="ff5d7-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff5d7-116">Requirement</span></span> | <span data-ttu-id="ff5d7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ff5d7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5d7-118">Header</span><span class="sxs-lookup"><span data-stu-id="ff5d7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ff5d7-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff5d7-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ff5d7-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff5d7-120">Library</span></span><br/> | <dl> <span data-ttu-id="ff5d7-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff5d7-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff5d7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ff5d7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ff5d7-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff5d7-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff5d7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff5d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5d7-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ff5d7-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ff5d7-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ff5d7-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="ff5d7-127">**D3D12 \_ Tiefe \_ Schablone \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="ff5d7-127">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





