---
title: Deducingblobgetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen Get-Rückruf Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- Deducingblobgetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ca5cc37a9fbd79807e258a87a199be7319ce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352023"
---
# <a name="deducingblobgetter"></a><span data-ttu-id="aa4a9-104">Deducingblobgetter</span><span class="sxs-lookup"><span data-stu-id="aa4a9-104">DeducingBlobGetter</span></span>

<span data-ttu-id="aa4a9-105">Leitet die-Klasse und die-Argumente ab und ruft dann einen Get-Rückruf Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-105">Deduces the class and arguments and then calls a member-function property getter callback for a blob-type property.</span></span>

> [!Note]  
> <span data-ttu-id="aa4a9-106">Deducingblobgetter sollte nicht direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-106">DeducingBlobGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
    _In_ const I *effect,  
    _Out_writes_opt_(dataSize) BYTE *data,  
    UINT32 dataSize,  
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="aa4a9-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa4a9-107">Requirements</span></span>



| <span data-ttu-id="aa4a9-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa4a9-108">Requirement</span></span> | <span data-ttu-id="aa4a9-109">Wert</span><span class="sxs-lookup"><span data-stu-id="aa4a9-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4a9-110">Header</span><span class="sxs-lookup"><span data-stu-id="aa4a9-110">Header</span></span><br/> | <dl> <span data-ttu-id="aa4a9-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4a9-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4a9-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa4a9-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4a9-113">**Direct2D::D educingblobsetter**</span><span class="sxs-lookup"><span data-stu-id="aa4a9-113">**Direct2D::DeducingBlobSetter**</span></span>](deducingblobsetter.md)
</dt> </dl>

 

 





