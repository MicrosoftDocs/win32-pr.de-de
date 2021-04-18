---
title: ID3DX12PipelineParserCallbacks rasterizerstatuecb-Methode (D3DX12. h)
description: Ruft den Zustands Beschreibungs Rückruf für den Raster eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Rasterizerstatuecb-Methode
- Rasterizerstatuecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, rasterizerstatuecb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361225"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a><span data-ttu-id="c3c3a-106">ID3DX12PipelineParserCallbacks:: rasterizerstatuecb-Methode</span><span class="sxs-lookup"><span data-stu-id="c3c3a-106">ID3DX12PipelineParserCallbacks::RasterizerStateCb method</span></span>

<span data-ttu-id="c3c3a-107">Ruft den Zustands Beschreibungs Rückruf für den Raster eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-107">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c3a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3c3a-108">Syntax</span></span>


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="c3c3a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3c3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c3a-110">*Rasterizerstate* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="c3c3a-110">*RasterizerState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c3c3a-111">Typ: **Konstanten [**D3D12 \_ Rasterizer \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span><span class="sxs-lookup"><span data-stu-id="c3c3a-111">Type: **const [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span></span>

<span data-ttu-id="c3c3a-112">Details zur Zustands Beschreibungs Beschreibung des Rasterizers, die aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-112">Details of the rasterizer state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3c3a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3c3a-113">Return value</span></span>

<span data-ttu-id="c3c3a-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c3a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3c3a-115">Requirements</span></span>



| <span data-ttu-id="c3c3a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3c3a-116">Requirement</span></span> | <span data-ttu-id="c3c3a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c3c3a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c3a-118">Header</span><span class="sxs-lookup"><span data-stu-id="c3c3a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c3c3a-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3c3a-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c3c3a-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3c3a-120">Library</span></span><br/> | <dl> <span data-ttu-id="c3c3a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3c3a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c3c3a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c3c3a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3c3a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3c3a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c3a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3c3a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c3a-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c3c3a-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c3c3a-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="c3c3a-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="c3c3a-127">**D3D12 \_ Rasterizer- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="c3c3a-127">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





