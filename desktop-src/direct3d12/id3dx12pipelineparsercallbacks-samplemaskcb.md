---
title: ID3DX12PipelineParserCallbacks samplemaskcb-Methode (D3DX12. h)
description: Ruft den Sample Mask-Unterordner Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Samplemaskcb-Methode
- Samplemaskcb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, samplemaskcb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371880"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a><span data-ttu-id="91c7a-106">ID3DX12PipelineParserCallbacks:: samplemaskcb-Methode</span><span class="sxs-lookup"><span data-stu-id="91c7a-106">ID3DX12PipelineParserCallbacks::SampleMaskCb method</span></span>

<span data-ttu-id="91c7a-107">Ruft den Sample Mask-Unterordner Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="91c7a-107">Calls the sample mask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c7a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="91c7a-108">Syntax</span></span>


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a><span data-ttu-id="91c7a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="91c7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c7a-110">*Samplemask*</span><span class="sxs-lookup"><span data-stu-id="91c7a-110">*SampleMask*</span></span> 
</dt> <dd>

<span data-ttu-id="91c7a-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="91c7a-111">Type: **UINT**</span></span>

<span data-ttu-id="91c7a-112">Details zum in einem Pipeline Status-Stream analysierten Sample Mask-unter Objekt.</span><span class="sxs-lookup"><span data-stu-id="91c7a-112">Details of the sample mask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c7a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91c7a-113">Return value</span></span>

<span data-ttu-id="91c7a-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="91c7a-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c7a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91c7a-115">Requirements</span></span>



| <span data-ttu-id="91c7a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91c7a-116">Requirement</span></span> | <span data-ttu-id="91c7a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="91c7a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="91c7a-118">Header</span><span class="sxs-lookup"><span data-stu-id="91c7a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="91c7a-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c7a-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="91c7a-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91c7a-120">Library</span></span><br/> | <dl> <span data-ttu-id="91c7a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91c7a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="91c7a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="91c7a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="91c7a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c7a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c7a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91c7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c7a-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="91c7a-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="91c7a-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="91c7a-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





