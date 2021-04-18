---
title: ID3DX12PipelineParserCallbacks depthstencilstatuecb-Methode (D3DX12. h) (DSV)
description: Ruft den untergeordneten Rückruf eines Objekts, das diese Schnittstelle implementiert, mit dem tiefen Schablone-Wert Format auf.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
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
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372031"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a><span data-ttu-id="29723-106">ID3DX12PipelineParserCallbacks depthstencilstatuecb-Methode (D3DX12. h) für den tiefen Schablonen Wert</span><span class="sxs-lookup"><span data-stu-id="29723-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h) for depth stencil value</span></span>

<span data-ttu-id="29723-107">Ruft den untergeordneten Rückruf eines Objekts, das diese Schnittstelle implementiert, mit dem tiefen Schablone-Wert Format auf.</span><span class="sxs-lookup"><span data-stu-id="29723-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="29723-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="29723-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="29723-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29723-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29723-110">*Depthstencilstate*</span><span class="sxs-lookup"><span data-stu-id="29723-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="29723-111">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="29723-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="29723-112">Details zum Format des tiefen Schablone-Wert Formats, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="29723-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29723-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29723-113">Return value</span></span>

<span data-ttu-id="29723-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="29723-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="29723-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29723-115">Requirements</span></span>



| <span data-ttu-id="29723-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29723-116">Requirement</span></span> | <span data-ttu-id="29723-117">Wert</span><span class="sxs-lookup"><span data-stu-id="29723-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="29723-118">Header</span><span class="sxs-lookup"><span data-stu-id="29723-118">Header</span></span><br/>  | <dl> <span data-ttu-id="29723-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="29723-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="29723-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29723-120">Library</span></span><br/> | <dl> <span data-ttu-id="29723-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29723-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="29723-122">DLL</span><span class="sxs-lookup"><span data-stu-id="29723-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="29723-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29723-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29723-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29723-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29723-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="29723-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="29723-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="29723-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="29723-127">**DXGI- \_ Format**</span><span class="sxs-lookup"><span data-stu-id="29723-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

