---
title: ID3DX12PipelineParserCallbacks streamoutputcb-Methode (D3DX12. h)
description: Ruft den untergeordneten Datenstrom-Ausgabe Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Streamoutputcb-Methode
- Streamoutputcb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, streamoutputcb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361839"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a><span data-ttu-id="30f0c-106">ID3DX12PipelineParserCallbacks:: streamoutputcb-Methode</span><span class="sxs-lookup"><span data-stu-id="30f0c-106">ID3DX12PipelineParserCallbacks::StreamOutputCb method</span></span>

<span data-ttu-id="30f0c-107">Ruft den untergeordneten Datenstrom-Ausgabe Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="30f0c-107">Calls the stream output description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f0c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30f0c-108">Syntax</span></span>


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a><span data-ttu-id="30f0c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30f0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f0c-110">*Streamoutput* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="30f0c-110">*StreamOutput* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="30f0c-111">Typ: **Konstanten [**D3D12 \_ Stream- \_ Ausgabe \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span><span class="sxs-lookup"><span data-stu-id="30f0c-111">Type: **const [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span></span>

<span data-ttu-id="30f0c-112">Details der Datenstrom Ausgabe Beschreibung, die aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="30f0c-112">Details of the stream output description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f0c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30f0c-113">Return value</span></span>

<span data-ttu-id="30f0c-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="30f0c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f0c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30f0c-115">Requirements</span></span>



| <span data-ttu-id="30f0c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30f0c-116">Requirement</span></span> | <span data-ttu-id="30f0c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="30f0c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30f0c-118">Header</span><span class="sxs-lookup"><span data-stu-id="30f0c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="30f0c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f0c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="30f0c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30f0c-120">Library</span></span><br/> | <dl> <span data-ttu-id="30f0c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30f0c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="30f0c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="30f0c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="30f0c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30f0c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f0c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30f0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f0c-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="30f0c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="30f0c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="30f0c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="30f0c-127">**D3D12-Daten \_ Strom \_ Ausgabe \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="30f0c-127">**D3D12\_STREAM\_OUTPUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





