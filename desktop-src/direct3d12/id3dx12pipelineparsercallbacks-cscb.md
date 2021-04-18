---
title: ID3DX12PipelineParserCallbacks cscb-Methode (D3DX12. h)
description: Ruft den Compute-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Cscb-Methode
- Cscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, cscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361227"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a><span data-ttu-id="90d0e-106">ID3DX12PipelineParserCallbacks:: cscb-Methode</span><span class="sxs-lookup"><span data-stu-id="90d0e-106">ID3DX12PipelineParserCallbacks::CSCb method</span></span>

<span data-ttu-id="90d0e-107">Ruft den Compute-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="90d0e-107">Calls the compute shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d0e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="90d0e-108">Syntax</span></span>


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a><span data-ttu-id="90d0e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="90d0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90d0e-110">*CS* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="90d0e-110">*CS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="90d0e-111">Typ: **Konstanten [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="90d0e-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="90d0e-112">Details des von einem Pipeline Status-Stream analysierten Compute-Shader-untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="90d0e-112">Details of the compute shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90d0e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90d0e-113">Return value</span></span>

<span data-ttu-id="90d0e-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="90d0e-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="90d0e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90d0e-115">Requirements</span></span>



| <span data-ttu-id="90d0e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90d0e-116">Requirement</span></span> | <span data-ttu-id="90d0e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="90d0e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90d0e-118">Header</span><span class="sxs-lookup"><span data-stu-id="90d0e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="90d0e-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="90d0e-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="90d0e-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90d0e-120">Library</span></span><br/> | <dl> <span data-ttu-id="90d0e-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90d0e-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="90d0e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="90d0e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="90d0e-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90d0e-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90d0e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90d0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d0e-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="90d0e-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="90d0e-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="90d0e-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="90d0e-127">**D3D12- \_ Shader- \_ Bytecode**</span><span class="sxs-lookup"><span data-stu-id="90d0e-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





