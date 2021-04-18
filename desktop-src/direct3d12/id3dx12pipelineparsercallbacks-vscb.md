---
title: ID3DX12PipelineParserCallbacks vscb-Methode (D3DX12. h)
description: Ruft den Vertex-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- Vscb-Methode
- Vscb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, vscb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365324"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a><span data-ttu-id="012aa-106">ID3DX12PipelineParserCallbacks:: vscb-Methode</span><span class="sxs-lookup"><span data-stu-id="012aa-106">ID3DX12PipelineParserCallbacks::VSCb method</span></span>

<span data-ttu-id="012aa-107">Ruft den Vertex-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="012aa-107">Calls the vertex shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="012aa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="012aa-108">Syntax</span></span>


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a><span data-ttu-id="012aa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="012aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="012aa-110">*Vs* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="012aa-110">*VS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="012aa-111">Typ: **Konstanten [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="012aa-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="012aa-112">Details des Vertex-Shader-unter Objekts, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="012aa-112">Details of the vertex shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="012aa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="012aa-113">Return value</span></span>

<span data-ttu-id="012aa-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="012aa-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="012aa-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="012aa-115">Requirements</span></span>



| <span data-ttu-id="012aa-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="012aa-116">Requirement</span></span> | <span data-ttu-id="012aa-117">Wert</span><span class="sxs-lookup"><span data-stu-id="012aa-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="012aa-118">Header</span><span class="sxs-lookup"><span data-stu-id="012aa-118">Header</span></span><br/>  | <dl> <span data-ttu-id="012aa-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="012aa-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="012aa-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="012aa-120">Library</span></span><br/> | <dl> <span data-ttu-id="012aa-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="012aa-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="012aa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="012aa-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="012aa-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="012aa-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="012aa-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="012aa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="012aa-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="012aa-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="012aa-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="012aa-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="012aa-127">**D3D12- \_ Shader- \_ Bytecode**</span><span class="sxs-lookup"><span data-stu-id="012aa-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





