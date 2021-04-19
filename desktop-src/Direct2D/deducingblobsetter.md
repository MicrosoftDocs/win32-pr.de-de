---
title: Deducingblobsetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.
ms.assetid: 4B8B871D-FE5E-4EF3-AEED-A3D92C10E8C6
keywords:
- Deducingblobsetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d3bbfcc0a48d722bd98456821d7f7df5e8780a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367700"
---
# <a name="deducingblobsetter"></a><span data-ttu-id="4cac6-104">Deducingblobsetter</span><span class="sxs-lookup"><span data-stu-id="4cac6-104">DeducingBlobSetter</span></span>

<span data-ttu-id="4cac6-105">Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="4cac6-105">Deduces the class and arguments and then calls a member-function property setter callback for a blob-type property.</span></span>

> [!Note]  
> <span data-ttu-id="4cac6-106">Deducingblobsetter sollte nicht direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4cac6-106">DeducingBlobSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobSetter(  
    _In_ HRESULT (C::*callback)(const BYTE *, UINT32),  
    _In_ I *effect,  
    _In_reads_(dataSize) const BYTE *data,  
    UINT32 dataSize,  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="4cac6-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cac6-107">Requirements</span></span>



| <span data-ttu-id="4cac6-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cac6-108">Requirement</span></span> | <span data-ttu-id="4cac6-109">Wert</span><span class="sxs-lookup"><span data-stu-id="4cac6-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cac6-110">Header</span><span class="sxs-lookup"><span data-stu-id="4cac6-110">Header</span></span><br/> | <dl> <span data-ttu-id="4cac6-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cac6-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cac6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cac6-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cac6-113">**Direct2D::D educingblobgetter**</span><span class="sxs-lookup"><span data-stu-id="4cac6-113">**Direct2D::DeducingBlobGetter**</span></span>](deducingblobgetter.md)
</dt> </dl>

 

 





