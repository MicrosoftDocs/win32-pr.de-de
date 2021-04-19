---
title: ID3DX12PipelineParserCallbacks errorunknownsubobject-Methode (D3DX12. h)
description: Ruft den unbekannten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Errorunknownsubobject-Methode
- Errorunknownsubobject-Methode, ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks Interface, errorunknownsubobject-Methode
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355213"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a><span data-ttu-id="84f21-106">ID3DX12PipelineParserCallbacks:: errorunknownsubobject-Methode</span><span class="sxs-lookup"><span data-stu-id="84f21-106">ID3DX12PipelineParserCallbacks::ErrorUnknownSubobject method</span></span>

<span data-ttu-id="84f21-107">Ruft den unbekannten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="84f21-107">Calls the unknown subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f21-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="84f21-108">Syntax</span></span>


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a><span data-ttu-id="84f21-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="84f21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f21-110">*Unknowntypevalue*</span><span class="sxs-lookup"><span data-stu-id="84f21-110">*UnknownTypeValue*</span></span> 
</dt> <dd>

<span data-ttu-id="84f21-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="84f21-111">Type: **UINT**</span></span>

<span data-ttu-id="84f21-112">Der unbekannte untergeordnete Typ des versuchten untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="84f21-112">The unrecognized subobject type of the attempted subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f21-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84f21-113">Return value</span></span>

<span data-ttu-id="84f21-114">Gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="84f21-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f21-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84f21-115">Requirements</span></span>



| <span data-ttu-id="84f21-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84f21-116">Requirement</span></span> | <span data-ttu-id="84f21-117">Wert</span><span class="sxs-lookup"><span data-stu-id="84f21-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="84f21-118">Header</span><span class="sxs-lookup"><span data-stu-id="84f21-118">Header</span></span><br/>  | <dl> <span data-ttu-id="84f21-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f21-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="84f21-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="84f21-120">Library</span></span><br/> | <dl> <span data-ttu-id="84f21-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84f21-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="84f21-122">DLL</span><span class="sxs-lookup"><span data-stu-id="84f21-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="84f21-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f21-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f21-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84f21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f21-125">Hilfsschnittstellen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="84f21-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="84f21-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="84f21-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





