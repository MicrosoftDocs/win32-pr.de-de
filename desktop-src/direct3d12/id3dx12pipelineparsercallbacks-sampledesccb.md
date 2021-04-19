---
title: ID3DX12PipelineParserCallbacks sampledesccb-Methode (D3DX12. h)
description: Ruft den Beispiel Beschreibungs-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Sampledesccb-Methode
- Sampledesccb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, sampledesccb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361181"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a><span data-ttu-id="739bc-106">ID3DX12PipelineParserCallbacks:: sampledesccb-Methode</span><span class="sxs-lookup"><span data-stu-id="739bc-106">ID3DX12PipelineParserCallbacks::SampleDescCb method</span></span>

<span data-ttu-id="739bc-107">Ruft den Beispiel Beschreibungs-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="739bc-107">Calls the sample description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="739bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="739bc-108">Syntax</span></span>


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a><span data-ttu-id="739bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="739bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="739bc-110">*Sampledäsc* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="739bc-110">*SampleDesc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="739bc-111">Type: Konstante **[**DXGI \_ Sample \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span><span class="sxs-lookup"><span data-stu-id="739bc-111">Type: **const [**DXGI\_SAMPLE\_DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span></span>

<span data-ttu-id="739bc-112">Details der Beispiel Beschreibung, die aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="739bc-112">Details of the sample description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="739bc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="739bc-113">Return value</span></span>

<span data-ttu-id="739bc-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="739bc-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="739bc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="739bc-115">Requirements</span></span>



| <span data-ttu-id="739bc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="739bc-116">Requirement</span></span> | <span data-ttu-id="739bc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="739bc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="739bc-118">Header</span><span class="sxs-lookup"><span data-stu-id="739bc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="739bc-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="739bc-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="739bc-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="739bc-120">Library</span></span><br/> | <dl> <span data-ttu-id="739bc-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="739bc-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="739bc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="739bc-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="739bc-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="739bc-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="739bc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="739bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="739bc-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="739bc-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="739bc-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="739bc-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="739bc-127">**DXGI-Beispiel (Debug) \_ \_**</span><span class="sxs-lookup"><span data-stu-id="739bc-127">**DXGI\_SAMPLE\_DESC**</span></span>](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

