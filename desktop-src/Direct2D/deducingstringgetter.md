---
title: Deducingstringgetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann für eine Eigenschaft vom Typ "String" einen Eigenschaften-Getter-Rückruf für eine Element Funktion auf.
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- Deducingstringgetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac65b9e5d7e37e2db83f06f80172e90f9f27f80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351351"
---
# <a name="deducingstringgetter"></a><span data-ttu-id="93ce2-104">Deducingstringgetter</span><span class="sxs-lookup"><span data-stu-id="93ce2-104">DeducingStringGetter</span></span>

<span data-ttu-id="93ce2-105">Leitet die-Klasse und die-Argumente ab und ruft dann für eine Eigenschaft vom Typ "String" einen Eigenschaften-Getter-Rückruf für eine Element Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="93ce2-105">Deduces the class and arguments and then calls a member-function property getter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="93ce2-106">Deducingstringgetter sollte nicht direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="93ce2-106">DeducingStringGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringGetter(
    _In_ HRESULT (C::*callback)(PWSTR, UINT32, UINT32*) const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize 
    ) 
```

## <a name="requirements"></a><span data-ttu-id="93ce2-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93ce2-107">Requirements</span></span>



| <span data-ttu-id="93ce2-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93ce2-108">Requirement</span></span> | <span data-ttu-id="93ce2-109">Wert</span><span class="sxs-lookup"><span data-stu-id="93ce2-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ce2-110">Header</span><span class="sxs-lookup"><span data-stu-id="93ce2-110">Header</span></span><br/> | <dl> <span data-ttu-id="93ce2-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="93ce2-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ce2-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93ce2-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ce2-113">**Direct2D::D educingstringsetter**</span><span class="sxs-lookup"><span data-stu-id="93ce2-113">**Direct2D::DeducingStringSetter**</span></span>](deducingstringsetter.md)
</dt> </dl>

 

 





