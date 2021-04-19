---
title: ID3DX12PipelineParserCallbacks rootsignaturecb-Methode (D3DX12. h)
description: Ruft den untergeordneten Signatur-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Rootsignaturecb-Methode
- Rootsignaturecb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, rootsignaturecb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373482"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a><span data-ttu-id="193f6-106">ID3DX12PipelineParserCallbacks:: rootsignaturecb-Methode</span><span class="sxs-lookup"><span data-stu-id="193f6-106">ID3DX12PipelineParserCallbacks::RootSignatureCb method</span></span>

<span data-ttu-id="193f6-107">Ruft den untergeordneten Signatur-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="193f6-107">Calls the root signature subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="193f6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="193f6-108">Syntax</span></span>


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a><span data-ttu-id="193f6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="193f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="193f6-110">*Rootsignature*</span><span class="sxs-lookup"><span data-stu-id="193f6-110">*RootSignature*</span></span> 
</dt> <dd>

<span data-ttu-id="193f6-111">Typ: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span><span class="sxs-lookup"><span data-stu-id="193f6-111">Type: **[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span></span>

<span data-ttu-id="193f6-112">Details des Stamm Signatur Objekts, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="193f6-112">Details of the root signature subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="193f6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="193f6-113">Return value</span></span>

<span data-ttu-id="193f6-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="193f6-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="193f6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="193f6-115">Requirements</span></span>



| <span data-ttu-id="193f6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="193f6-116">Requirement</span></span> | <span data-ttu-id="193f6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="193f6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="193f6-118">Header</span><span class="sxs-lookup"><span data-stu-id="193f6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="193f6-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="193f6-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="193f6-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="193f6-120">Library</span></span><br/> | <dl> <span data-ttu-id="193f6-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="193f6-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="193f6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="193f6-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="193f6-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="193f6-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="193f6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="193f6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="193f6-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="193f6-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="193f6-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="193f6-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="193f6-127">**ID3D12RootSignature**</span><span class="sxs-lookup"><span data-stu-id="193f6-127">**ID3D12RootSignature**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

