---
title: ID3DX12PipelineParserCallbacks dscb-Methode (D3DX12. h)
description: Ruft den Domänen-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- Dscb-Methode
- Dscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, dscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf5f68ca6e6e4891fa391a142d45a1496a42ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355819"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a><span data-ttu-id="9c2ac-106">ID3DX12PipelineParserCallbacks::D SCB-Methode</span><span class="sxs-lookup"><span data-stu-id="9c2ac-106">ID3DX12PipelineParserCallbacks::DSCb method</span></span>

<span data-ttu-id="9c2ac-107">Ruft den Domänen-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="9c2ac-107">Calls the domain shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c2ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c2ac-108">Syntax</span></span>


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a><span data-ttu-id="9c2ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c2ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c2ac-110">*DS* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="9c2ac-110">*DS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2ac-111">Typ: **Konstanten [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="9c2ac-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="9c2ac-112">Details des Domänen-Shader-unter Objekts, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9c2ac-112">Details of the domain shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c2ac-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c2ac-113">Return value</span></span>

<span data-ttu-id="9c2ac-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="9c2ac-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c2ac-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c2ac-115">Requirements</span></span>



| <span data-ttu-id="9c2ac-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c2ac-116">Requirement</span></span> | <span data-ttu-id="9c2ac-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9c2ac-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2ac-118">Header</span><span class="sxs-lookup"><span data-stu-id="9c2ac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9c2ac-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c2ac-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="9c2ac-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9c2ac-120">Library</span></span><br/> | <dl> <span data-ttu-id="9c2ac-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c2ac-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c2ac-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9c2ac-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9c2ac-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c2ac-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c2ac-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c2ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2ac-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9c2ac-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9c2ac-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="9c2ac-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="9c2ac-127">**D3D12- \_ Shader- \_ Bytecode**</span><span class="sxs-lookup"><span data-stu-id="9c2ac-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





