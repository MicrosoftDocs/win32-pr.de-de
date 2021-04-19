---
title: Deducingstringsetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Eigenschaft vom Typ "String" auf.
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- Deducingstringsetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7860978fd271b2ff395caae068cd651d3057020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354210"
---
# <a name="deducingstringsetter"></a><span data-ttu-id="a49c8-104">Deducingstringsetter</span><span class="sxs-lookup"><span data-stu-id="a49c8-104">DeducingStringSetter</span></span>

<span data-ttu-id="a49c8-105">Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Eigenschaft vom Typ "String" auf.</span><span class="sxs-lookup"><span data-stu-id="a49c8-105">Deduces the class and arguments and then calls a member-function property setter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="a49c8-106">Deducingstringsetter sollte nicht direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a49c8-106">DeducingStringSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="a49c8-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a49c8-107">Requirements</span></span>



| <span data-ttu-id="a49c8-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a49c8-108">Requirement</span></span> | <span data-ttu-id="a49c8-109">Wert</span><span class="sxs-lookup"><span data-stu-id="a49c8-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49c8-110">Header</span><span class="sxs-lookup"><span data-stu-id="a49c8-110">Header</span></span><br/> | <dl> <span data-ttu-id="a49c8-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="a49c8-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a49c8-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a49c8-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49c8-113">**Direct2D::D educingstringgetter**</span><span class="sxs-lookup"><span data-stu-id="a49c8-113">**Direct2D::DeducingStringGetter**</span></span>](deducingstringgetter.md)
</dt> </dl>

 

 





