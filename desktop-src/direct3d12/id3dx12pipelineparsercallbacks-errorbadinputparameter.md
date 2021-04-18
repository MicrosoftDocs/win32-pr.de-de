---
title: ID3DX12PipelineParserCallbacks errorbadinputparameter-Methode (D3DX12. h)
description: Ruft den ungültigen Eingabeparameter-Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Errorbadinputparameter-Methode
- Errorbadinputparameter-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, errorbadinputparameter-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355034"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a><span data-ttu-id="5dce8-106">ID3DX12PipelineParserCallbacks:: errorbadinputparameter-Methode</span><span class="sxs-lookup"><span data-stu-id="5dce8-106">ID3DX12PipelineParserCallbacks::ErrorBadInputParameter method</span></span>

<span data-ttu-id="5dce8-107">Ruft den ungültigen Eingabeparameter-Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5dce8-107">Calls the bad input parameter error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dce8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dce8-108">Syntax</span></span>


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a><span data-ttu-id="5dce8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dce8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dce8-110">*Parameter Index*</span><span class="sxs-lookup"><span data-stu-id="5dce8-110">*ParameterIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="5dce8-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="5dce8-111">Type: **UINT**</span></span>

<span data-ttu-id="5dce8-112">Die Position des Parameters, der eine ungültige Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="5dce8-112">The position of the parameter that contains bad input.</span></span> <span data-ttu-id="5dce8-113">Der linke Parameter befindet sich an Position 1 und nicht an Position 0.</span><span class="sxs-lookup"><span data-stu-id="5dce8-113">The left-most parameter is at position 1, not position 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dce8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5dce8-114">Return value</span></span>

<span data-ttu-id="5dce8-115">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="5dce8-115">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dce8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5dce8-116">Requirements</span></span>



| <span data-ttu-id="5dce8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5dce8-117">Requirement</span></span> | <span data-ttu-id="5dce8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5dce8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5dce8-119">Header</span><span class="sxs-lookup"><span data-stu-id="5dce8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5dce8-120"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dce8-120"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5dce8-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5dce8-121">Library</span></span><br/> | <dl> <span data-ttu-id="5dce8-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dce8-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5dce8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5dce8-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5dce8-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dce8-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dce8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dce8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dce8-126">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5dce8-126">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5dce8-127">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5dce8-127">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





