---
title: ID3DX12PipelineParserCallbacks nodemaskcb-Methode (D3DX12. h)
description: Ruft den nodemask-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Nodemaskcb-Methode
- Nodemaskcb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, nodemaskcb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353338"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a><span data-ttu-id="8b92c-106">ID3DX12PipelineParserCallbacks:: nodemaskcb-Methode</span><span class="sxs-lookup"><span data-stu-id="8b92c-106">ID3DX12PipelineParserCallbacks::NodemaskCb method</span></span>

<span data-ttu-id="8b92c-107">Ruft den nodemask-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="8b92c-107">Calls the nodemask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b92c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b92c-108">Syntax</span></span>


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a><span data-ttu-id="8b92c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b92c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b92c-110">*Nodemask*</span><span class="sxs-lookup"><span data-stu-id="8b92c-110">*Nodemask*</span></span> 
</dt> <dd>

<span data-ttu-id="8b92c-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8b92c-111">Type: **UINT**</span></span>

<span data-ttu-id="8b92c-112">Details zum nodemask-unter Objekt, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8b92c-112">Details of the nodemask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b92c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b92c-113">Return value</span></span>

<span data-ttu-id="8b92c-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="8b92c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b92c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b92c-115">Requirements</span></span>



| <span data-ttu-id="8b92c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b92c-116">Requirement</span></span> | <span data-ttu-id="8b92c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8b92c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b92c-118">Header</span><span class="sxs-lookup"><span data-stu-id="8b92c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8b92c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b92c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8b92c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b92c-120">Library</span></span><br/> | <dl> <span data-ttu-id="8b92c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b92c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b92c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8b92c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8b92c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b92c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b92c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b92c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b92c-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8b92c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8b92c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8b92c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





