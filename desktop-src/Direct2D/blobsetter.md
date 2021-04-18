---
title: Blobsetter (D2d1effecthelpers. h)
description: Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.
ms.assetid: 29411D53-1D27-4040-A3C0-B1511E627A32
keywords:
- Blobsetter Direct2D
topic_type:
- apiref
api_name:
- BlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a073db2fb53fa86414ed6081ede0e24c2eb7dcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357543"
---
# <a name="blobsetter"></a><span data-ttu-id="dfc5a-104">Blobsetter</span><span class="sxs-lookup"><span data-stu-id="dfc5a-104">BlobSetter</span></span>

<span data-ttu-id="dfc5a-105">Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="dfc5a-105">Calls a member-function property setter callback for a blob-type property.</span></span>

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobSetter(
    _In_ IUnknown *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="dfc5a-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfc5a-106">Requirements</span></span>



| <span data-ttu-id="dfc5a-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfc5a-107">Requirement</span></span> | <span data-ttu-id="dfc5a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="dfc5a-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc5a-109">Header</span><span class="sxs-lookup"><span data-stu-id="dfc5a-109">Header</span></span><br/> | <dl> <span data-ttu-id="dfc5a-110"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfc5a-110"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfc5a-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfc5a-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc5a-112">**Direct2D:: blobgetter**</span><span class="sxs-lookup"><span data-stu-id="dfc5a-112">**Direct2D::BlobGetter**</span></span>](blobgetter.md)
</dt> </dl>

 

 





