---
title: Deducingvaluegetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen getget-Rückruf Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf.
ms.assetid: E2E5CCC3-B112-4D3C-8840-121A55C4F1A2
keywords:
- Deducingvaluegetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd6eac823457882513f97557939db884efcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356368"
---
# <a name="deducingvaluegetter"></a><span data-ttu-id="46475-104">Deducingvaluegetter</span><span class="sxs-lookup"><span data-stu-id="46475-104">DeducingValueGetter</span></span>

<span data-ttu-id="46475-105">Leitet die-Klasse und die-Argumente ab und ruft dann einen getget-Rückruf Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="46475-105">Deduces the class and arguments and then calls a member-function property getter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="46475-106">Deducingvaluegetter sollte nicht direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="46475-106">DeducingValueGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueGetter(
    _In_ P (C::*callback)() const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="46475-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46475-107">Requirements</span></span>



| <span data-ttu-id="46475-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46475-108">Requirement</span></span> | <span data-ttu-id="46475-109">Wert</span><span class="sxs-lookup"><span data-stu-id="46475-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46475-110">Header</span><span class="sxs-lookup"><span data-stu-id="46475-110">Header</span></span><br/> | <dl> <span data-ttu-id="46475-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="46475-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46475-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46475-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46475-113">**Direct2D::D educingvaluesetter**</span><span class="sxs-lookup"><span data-stu-id="46475-113">**Direct2D::DeducingValueSetter**</span></span>](deducingvaluesetter.md)
</dt> </dl>

 

 





