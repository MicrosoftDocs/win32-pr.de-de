---
title: ID3DX12PipelineParserCallbacks inputlayoutcb-Methode (D3DX12. h)
description: Ruft das Eingabe Layout-untergeordnete Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Inputlayoutcb-Methode
- Inputlayoutcb-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, inputlayoutcb-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361879"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a><span data-ttu-id="95836-106">ID3DX12PipelineParserCallbacks:: inputlayoutcb-Methode</span><span class="sxs-lookup"><span data-stu-id="95836-106">ID3DX12PipelineParserCallbacks::InputLayoutCb method</span></span>

<span data-ttu-id="95836-107">Ruft das Eingabe Layout-untergeordnete Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="95836-107">Calls the input layout subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="95836-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95836-108">Syntax</span></span>


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a><span data-ttu-id="95836-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95836-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95836-110">*Input Layout* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="95836-110">*InputLayout* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="95836-111">Typ: **Konstanten [**D3D12 \_ Eingabe \_ Layout \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span><span class="sxs-lookup"><span data-stu-id="95836-111">Type: **const [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span></span>

<span data-ttu-id="95836-112">Details zum eingabelayoutobjekt, das aus einem Pipeline Status-Stream analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="95836-112">Details of the input layout subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95836-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95836-113">Return value</span></span>

<span data-ttu-id="95836-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="95836-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="95836-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95836-115">Requirements</span></span>



| <span data-ttu-id="95836-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95836-116">Requirement</span></span> | <span data-ttu-id="95836-117">Wert</span><span class="sxs-lookup"><span data-stu-id="95836-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95836-118">Header</span><span class="sxs-lookup"><span data-stu-id="95836-118">Header</span></span><br/>  | <dl> <span data-ttu-id="95836-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="95836-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="95836-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95836-120">Library</span></span><br/> | <dl> <span data-ttu-id="95836-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95836-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="95836-122">DLL</span><span class="sxs-lookup"><span data-stu-id="95836-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="95836-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95836-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95836-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95836-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95836-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95836-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="95836-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="95836-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="95836-127">**D3D12 \_ Eingabe \_ Layout-Debug \_**</span><span class="sxs-lookup"><span data-stu-id="95836-127">**D3D12\_INPUT\_LAYOUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





