---
title: ID3DX12PipelineParserCallbacks hscb-Methode (D3DX12. h)
description: Ruft den Hull-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: B2967E7F-391F-4A76-A087-E0B925018EE3
keywords:
- Hscb-Methode
- Hscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, hscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.HSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7d351e0b3827087cb51c38af173badd28d698c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370447"
---
# <a name="id3dx12pipelineparsercallbackshscb-method"></a><span data-ttu-id="6b618-106">ID3DX12PipelineParserCallbacks:: hscb-Methode</span><span class="sxs-lookup"><span data-stu-id="6b618-106">ID3DX12PipelineParserCallbacks::HSCb method</span></span>

<span data-ttu-id="6b618-107">Ruft den Hull-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b618-107">Calls the hull shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b618-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b618-108">Syntax</span></span>


```C++
void HSCb(
  [ref] const D3D12_SHADER_BYTECODE &HS
);
```



## <a name="parameters"></a><span data-ttu-id="6b618-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b618-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b618-110">*HS* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="6b618-110">*HS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6b618-111">Typ: **Konstanten [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="6b618-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="6b618-112">Details des Hull-Shader-unter Objekts, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6b618-112">Details of the hull shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b618-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b618-113">Return value</span></span>

<span data-ttu-id="6b618-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="6b618-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b618-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b618-115">Requirements</span></span>



| <span data-ttu-id="6b618-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b618-116">Requirement</span></span> | <span data-ttu-id="6b618-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6b618-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6b618-118">Header</span><span class="sxs-lookup"><span data-stu-id="6b618-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6b618-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b618-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6b618-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b618-120">Library</span></span><br/> | <dl> <span data-ttu-id="6b618-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b618-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b618-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6b618-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b618-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b618-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b618-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b618-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b618-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6b618-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6b618-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="6b618-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="6b618-127">**D3D12- \_ Shader- \_ Bytecode**</span><span class="sxs-lookup"><span data-stu-id="6b618-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





