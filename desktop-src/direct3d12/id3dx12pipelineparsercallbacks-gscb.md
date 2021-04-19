---
title: ID3DX12PipelineParserCallbacks gscb-Methode (D3DX12. h)
description: Ruft den Geometry-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 0D8846C5-15E4-43EB-AA82-163BB514C5B7
keywords:
- Gscb-Methode
- Gscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, gscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.GSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768e64ccdf06eccce731cafd0d40a9862b695e1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357254"
---
# <a name="id3dx12pipelineparsercallbacksgscb-method"></a><span data-ttu-id="cc058-106">ID3DX12PipelineParserCallbacks:: gscb-Methode</span><span class="sxs-lookup"><span data-stu-id="cc058-106">ID3DX12PipelineParserCallbacks::GSCb method</span></span>

<span data-ttu-id="cc058-107">Ruft den Geometry-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="cc058-107">Calls the geometry shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc058-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc058-108">Syntax</span></span>


```C++
void GSCb(
  [ref] const D3D12_SHADER_BYTECODE &GS
);
```



## <a name="parameters"></a><span data-ttu-id="cc058-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc058-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc058-110">*GS* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="cc058-110">*GS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cc058-111">Typ: **Konstanten [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="cc058-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="cc058-112">Details zum Geometry-Shader-unter Objekt, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cc058-112">Details of the geometry shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc058-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc058-113">Return value</span></span>

<span data-ttu-id="cc058-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="cc058-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc058-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc058-115">Requirements</span></span>



| <span data-ttu-id="cc058-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc058-116">Requirement</span></span> | <span data-ttu-id="cc058-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cc058-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc058-118">Header</span><span class="sxs-lookup"><span data-stu-id="cc058-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cc058-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc058-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="cc058-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc058-120">Library</span></span><br/> | <dl> <span data-ttu-id="cc058-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc058-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc058-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cc058-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cc058-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc058-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc058-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc058-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc058-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="cc058-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="cc058-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="cc058-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="cc058-127">**D3D12- \_ Shader- \_ Bytecode**</span><span class="sxs-lookup"><span data-stu-id="cc058-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





