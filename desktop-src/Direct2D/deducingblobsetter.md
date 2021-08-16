---
title: DeducingBlobSetter (D2d1effecthelpers.h)
description: Deduces the class and arguments and then calls a member-function property setter callback for a blob-type property.
ms.assetid: 4B8B871D-FE5E-4EF3-AEED-A3D92C10E8C6
keywords:
- DeducingBlobSetter Direct2D
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
ms.openlocfilehash: 165f88f9ba9a7f0706726a13a1dfa3445d3b752719e71dc231a23cdd1583a4c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825974"
---
# <a name="deducingblobsetter"></a>DeducingBlobSetter

Deduces the class and arguments and then calls a member-function property setter callback for a blob-type property.

> [!Note]  
> DeducingBlobSetter sollte nicht direkt aufgerufen werden.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobSetter(  
    _In_ HRESULT (C::*callback)(const BYTE *, UINT32),  
    _In_ I *effect,  
    _In_reads_(dataSize) const BYTE *data,  
    UINT32 dataSize,  
    ) 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Direct2D::D educingBlobGetter**](deducingblobgetter.md)
</dt> </dl>

 

 





