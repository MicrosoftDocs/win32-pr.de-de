---
title: CD3DX12_DEFAULT-Struktur (D3dx12. h)
description: Übergibt D3D12 \_ default an einen Konstruktor für jede hilfsstruktur. Diese Struktur wird einfach als Mechanismus verwendet, um Standardparameter für die anderen Hilfsstrukturen festzulegen.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354352"
---
# <a name="cd3dx12_default-structure"></a><span data-ttu-id="7281b-105">CD3DX12- \_ Standardstruktur</span><span class="sxs-lookup"><span data-stu-id="7281b-105">CD3DX12\_DEFAULT structure</span></span>

<span data-ttu-id="7281b-106">Übergibt D3D12 \_ default an einen Konstruktor für jede hilfsstruktur.</span><span class="sxs-lookup"><span data-stu-id="7281b-106">Passes D3D12\_DEFAULT into a constructor for each helper structure.</span></span> <span data-ttu-id="7281b-107">Diese Struktur wird einfach als Mechanismus verwendet, um Standardparameter für die anderen Hilfsstrukturen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7281b-107">This structure is simply used as a mechanism to set default parameters on the other helper structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="7281b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7281b-108">Remarks</span></span>

<span data-ttu-id="7281b-109">Diese Struktur wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="7281b-109">This struct is declared as follows:</span></span>

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

<span data-ttu-id="7281b-110">Übergibt D3D12 \_ default an einen Konstruktor für jede hilfsstruktur.</span><span class="sxs-lookup"><span data-stu-id="7281b-110">Passes D3D12\_DEFAULT into a constructor for each helper struct.</span></span> <span data-ttu-id="7281b-111">Der folgende Konstruktor wird z. b. in d3dx12. h deklariert:</span><span class="sxs-lookup"><span data-stu-id="7281b-111">For example, the following constructor is declared in d3dx12.h:</span></span>

<span data-ttu-id="7281b-112">CD3DX12- \_ CPU- \_ \_ Deskriptorhandle (CD3DX12 \_ Standard) {PTR = 0;}</span><span class="sxs-lookup"><span data-stu-id="7281b-112">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT) { ptr = 0; }</span></span>

## <a name="requirements"></a><span data-ttu-id="7281b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7281b-113">Requirements</span></span>



| <span data-ttu-id="7281b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7281b-114">Requirement</span></span> | <span data-ttu-id="7281b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7281b-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7281b-116">Header</span><span class="sxs-lookup"><span data-stu-id="7281b-116">Header</span></span><br/> | <dl> <span data-ttu-id="7281b-117"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7281b-117"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7281b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7281b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7281b-119">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="7281b-119">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





